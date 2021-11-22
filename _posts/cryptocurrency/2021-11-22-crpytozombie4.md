---
layout: post
title: Crypto Zombies Basic [4/6]
categories: cryptocurrency solidity ethereum Chainlink
author: Simon Lee
permalink: /:categories/:title
---

<strong>>> [Crypto Zombies Official Website][cryptozombie] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">Crypto Zombie Basic [4/6]</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Zombie Battle System</div>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>payable modifier:&nbsp;</strong>Explanation</p>
{% highlight solidity %}
""" Define a uint named levelUpFee, and set it equal to 0.001 ether. """
uint levelUpFee = 0.001 ether;
""" Create a function named levelUp. It will take one parameter, _zombieId, a uint. It should be external and payable. The function should first require that msg.value is equal to levelUpFee. It should then increment this zombie's level: zombies[_zombieId].level++. """
function levelUp(uint _zombieId) external payable {
    require(msg.value == levelUpFee);
    zombies[_zombieId].level++;
}

{% endhighlight %}

<br>
<br>
<br>

[cryptozombie]: https://cryptozombies.io/
