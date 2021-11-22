---
layout: post
title: Crypto Zombies Basic [3/6]
categories: cryptocurrency solidity ethereum Chainlink
author: Simon Lee
permalink: /:categories/:title
---

<strong>>> [Crypto Zombies Official Website][cryptozombie] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">Crypto Zombie Basic [3/6]</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Advanced Solidity Concepts</div>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>constructor:&nbsp;</strong>constructor() is an optional special function that has the same name as the contract. It will get executed only one time, when the contract is first created.</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>modifier:&nbsp;</strong>modifiers are kind of half-functions that are used to modify other functions, usually to check some requirements prior to execution.</p>

{% highlight solidity %}
""" Remember to have the last line of the modifier call the rest of the function with \_;. """
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Ownable contract&nbsp;</strong>bascially does the following:</p>
- When a contract is created, its constructor sets the owner to msg.sender.
- It adds an onlyOwner modifier, which can restrict access to certain functions to only the owner.
- It allows you to transfer the contract to a new owner.
<p style="font-family: 'Times New Roman', serif; font-size: 16px">Notice the <i>onlyOwner</i> modifier on the <i>renounceOwnership</i> function. When you call <i>renounceOwnership</i>, the code inside <i>onlyOwner</i> executes first. Then when it hits the <i>_;</i> statement in <i>onlyOwner</i>, it goes back and executes the code inside <i>renounceOwnership</i>.

So while there are other ways you can use modifiers, one of the most common use-cases is to add a quick require check before a function executes.

In the case of onlyOwner, adding this modifier to a function makes it so only the owner of the contract (you, if you deployed it) can call that function.</p>

{% highlight solidity %}
contract Ownable {
address private \_owner;

constructor() internal {
\_owner = msg.sender;
emit OwnershipTransferred(address(0), \_owner);
}

function owner() public view returns(address) {
return \_owner;
}

modifier onlyOwner() {
require(isOwner());
\_;
}

function isOwner() public view returns(bool) {
return msg.sender == \_owner;
}

function renounceOwnership() public onlyOwner {
emit OwnershipTransferred(\_owner, address(0));
\_owner = address(0);
}

{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>gas:&nbsp;</strong>In Solidity, your users have to pay every time they execute a function on your DApp using a currency called <i>gas</i>. The total <i>gas cost</i> of your function is the sum of the gas costs of all its individual operations.</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>More examples about function modifier:&nbsp;</strong></p>
{% highlight solidity %}
""" Create a function called changeName. It will take 2 arguments: _zombieId (a uint), and _newName (a string with the data location set to calldata ), and make it external. It should have the aboveLevel modifier, and should pass in 2 for the _level parameter. (Don't forget to also pass the _zombieId). """
""" In this function, first we need to verify that msg.sender is equal to zombieToOwner[_zombieId]. Use a require statement. Then the function should set zombies[_zombieId].name equal to _newName. """
  function changeName(uint _zombieId, string calldata _newName) external aboveLevel(2, _zombieId) {
      require(msg.sender == zombieToOwner[_zombieId]);
      zombies[_zombieId].name = _newName;
  }
""" Create another function named changeDna below changeName. Its definition and contents will be almost identical to changeName, except its second argument will be _newDna (a uint), and it should pass in 20 for the _level parameter on aboveLevel. And of course, it should set the zombie's dna to _newDna instead of setting the zombie's name. """
  function changeDna(uint _zombieId, uint _newDna) external aboveLevel(20, _zombieId) {
      require(msg.sender == zombieToOwner[_zombieId]);
      zombies[_zombieId].dna = _newDna;
  }
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong><i>view</i> functions don't cost <i>gas</i>:&nbsp;</strong> this is because the <i>view</i> functions don't actually change anything on the blockchain.</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong><i>storage</i> is expensive because every time you write or change a piece of data, it's written permanently to the blockchain. This means that thousands of nodes across the world need to store that dat on their hard drives.</p>

{% highlight solidity %}
""" Declare a uint[] memory variable called result and Set it equal to a new uint array. The length of the array should be however many zombies this \_owner owns, which we can look up from our mapping with: ownerZombieCount[_owner]. """
function getZombiesByOwner(address \_owner) external view returns(uint[] memory) {
uint[] memory result = new uint[](ownerZombieCount[_owner]);
return result;
}
{% endhighlight %}

<br>
<br>
<br>

[cryptozombie]: https://cryptozombies.io/
