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
{% highlight solidity %}
""" SOLIDITY COMMENT """

{% endhighlight %}

- Data types: mapping, address.
  Each account has its own address(e.g., 0x0cE446255506E92DF41614C46F1d6df9Cc969183).
  An address is owned by a specific user (or a smart contract).

The daya type (mapping) is another way of storing organized data in Solidity.
A mapping is essentially a key-value store for storing and looking up data. In the first example, the key is an address and the value is a uint, and in the second example the key is a uint and the value is a string.
{% highlight solidity %}
""" Create a mapping called zombieToOwner. The key will be a uint (we'll store and look up the zombie based on its id) and the value an address. Let's make this mapping public. """
mapping (uint => address) public zombieToOwner;
""" Create a mapping called ownerZombieCount, where the key is an address and the value a uint. """
mapping (address => uint) ownerZombieCount;
{% endhighlight %}

- msg.sender

mapping (address => uint) favoriteNumber;

function setMyNumber(uint \_myNumber) public {
// Update our `favoriteNumber` mapping to store `_myNumber` under `msg.sender`
favoriteNumber[msg.sender] = \_myNumber;
// ^ The syntax for storing data in a mapping is just like with arrays
}

function whatIsMyNumber() public view returns (uint) {
// Retrieve the value stored in the sender's address
// Will be `0` if the sender hasn't called `setMyNumber` yet
return favoriteNumber[msg.sender];
}

<br>
<br>
<br>

[cryptozombie]: https://cryptozombies.io/
