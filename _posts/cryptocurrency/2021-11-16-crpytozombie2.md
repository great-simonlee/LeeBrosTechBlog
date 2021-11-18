---
layout: post
title: Crypto Zombies Basic [2/6]
categories: cryptocurrency solidity ethereum Chainlink
author: Simon Lee
permalink: /:categories/:title
---

<strong>>> [Crypto Zombies Official Website][cryptozombie] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">Crypto Zombie Basic [2/6]</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Zombies Attack Their Victims</div>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Data type - mapping:&nbsp;</strong>mapping is another way of storing organized data in key-value.</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Data type - address:&nbsp;</strong>An address is owned by a specific user (or a smart contract). Each account has its own address (e.g. 0x0cE446255506E92DF41614C46F1d6df9Cc969183). </p>

{% highlight solidity %}
""" Create a mapping called zombieToOwner. The key will be a uint (we'll store and look up the zombie based on its id) and the value an address. Let's make this mapping public. """
mapping (uint => address) public zombieToOwner;
""" Create a mapping called ownerZombieCount, where the key is an address and the value a uint. """
mapping (address => uint) ownerZombieCount;
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>msg.sender:&nbsp;</strong>refers to the address of the person (or smart contract) who called the current function.</p>

{% highlight solidity %}
""" First, after we get back the new zombie's id, let's update our zombieToOwner mapping to store msg.sender under that id. """
zombieToOwner[id] = msg.sender;
""" Second, let's increase ownerZombieCount for this msg.sender. """
ownerZombieCount[msg.sender]++;
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>require&nbsp;</strong>makes the function be called if the require statement is true. It will throw an error and stop executing if some comdition is not true. So <i>require</i> is quite useful for verifying certain conditions that must be true before running a function.</p>

{% highlight solidity %}
""" Put a require statement at the beginning of createRandomZombie. The function should check to make sure ownerZombieCount[msg.sender] is equal to 0, and throw an error otherwise. """
function createRandomDna(string memory name) public {
require(ownerZombieCount[msg.sender] == 0);
}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>inheritance&nbsp;</strong></p>

{% highlight solidity %}
""" Make a contract called ZombieFeeding below ZombieFactory. This contract should inherit from our ZombieFactory contract. """
contract ZombieFactory {}
contract ZombieFeeding is ZombieFactory {}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>import&nbsp;</strong></p>

{% highlight solidity %}
""" Import zombiefactory.sol into our new file, zombiefeeding.sol. """
import './zombiefactory.sol';
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Storage:&nbsp;</strong><i>storage</i> refers to variables stored permanently on the blockchain. (like HDD)</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Memory:&nbsp;</strong><i>memory</i> variables are temporary, and are erased between external function calls to your contract. (like RAM)</p>

{% highlight solidity %}
""" Create a function called feedAndMultiply. It will take two parameters: \_zombieId (a uint) and \_targetDna (also a uint). This function should be public. """
""" We don't want to let someone else feed our zombie! So first, let's make sure we own this zombie. Add a require statement to verify that msg.sender is equal to this zombie's owner (similar to how we did in the createRandomZombie function). """
""" We're going to need to get this zombie's DNA. So the next thing our function should do is declare a local Zombie named myZombie (which will be a storage pointer). Set this variable to be equal to index \_zombieId in our zombies array. """
function feedAndMultiply(uint \_zombieId, uint \_targetDna) public {
require(msg.sender == zombieToOwner[_zombieId]);
Zombie storage myZombie = zombies[_zombieId];
}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>internal:&nbsp;</strong><i>internal</i> basically works in the same way as <i>private</i> works, except that it's also accessible to contracts that inherit from this contract.</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>external:&nbsp;</strong><i>external</i> is similar to <i>public</i> except that these functions can ONLY be called outside the contract - they can't be called by other functions inside that contract.</p>

{% highlight solidity %}
""" Create a function called feedAndMultiply. It will take two parameters: \_zombieId (a uint) and \_targetDna (also a uint). This function should be public. """
""" We don't want to let someone else feed our zombie! So first, let's make sure we own this zombie. Add a require statement to verify that msg.sender is equal to this zombie's owner (similar to how we did in the createRandomZombie function). """
""" We're going to need to get this zombie's DNA. So the next thing our function should do is declare a local Zombie named myZombie (which will be a storage pointer). Set this variable to be equal to index \_zombieId in our zombies array. """
function feedAndMultiply(uint \_zombieId, uint \_targetDna) public {
require(msg.sender == zombieToOwner[_zombieId]);
Zombie storage myZombie = zombies[_zombieId];
}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>interface:&nbsp;</strong>for our contract to talk to another contract on the blockchain that we don't own, first we need to define an interface.</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>external:&nbsp;</strong><i>external</i> is similar to <i>public</i> except that these functions can ONLY be called outside the contract - they can't be called by other functions inside that contract.</p>

{% highlight solidity %}
""" Create a function called feedAndMultiply. It will take two parameters: \_zombieId (a uint) and \_targetDna (also a uint). This function should be public. """
""" We don't want to let someone else feed our zombie! So first, let's make sure we own this zombie. Add a require statement to verify that msg.sender is equal to this zombie's owner (similar to how we did in the createRandomZombie function). """
""" We're going to need to get this zombie's DNA. So the next thing our function should do is declare a local Zombie named myZombie (which will be a storage pointer). Set this variable to be equal to index \_zombieId in our zombies array. """
function feedAndMultiply(uint \_zombieId, uint \_targetDna) public {
require(msg.sender == zombieToOwner[_zombieId]);
Zombie storage myZombie = zombies[_zombieId];
}
{% endhighlight %}

<br>
<br>
<br>

[cryptozombie]: https://cryptozombies.io/
