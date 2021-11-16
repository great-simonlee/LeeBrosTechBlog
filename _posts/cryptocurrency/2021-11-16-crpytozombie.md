---
layout: post
title: Crypto Zombies Basic [1/6]
categories: cryptocurrency solidity ethereum Chainlink
author: Simon Lee
permalink: /:categories/:title
---

<strong>>> [Crypto Zombies Official Website][cryptozombie] <<</strong>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 32px; font-weight: bold; margin-bottom: 18px; padding-top: 32px; border-top: black solid 1px;">Crypto Zombie Basic [1/6]</div>

<div style="text-align: center; font-family: 'Times New Roman', serif; font-size: 24px; font-weight: bold; margin-bottom: 12px;">Making the Zombie Factory</div>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>contract:&nbsp;</strong>Solidity's code is encapsulated in contracts. A contract is the fundamental building block of Ethereum applications — all variables and functions belong to a contract, and this will be the starting point of all your projects.</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>pragma:&nbsp;</strong> All solidity source code should start with a "version pragma" — a declaration of the version of the Solidity compiler this code should use.</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>struct:&nbsp;</strong>A customed set of data types.</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Data type: uint&nbsp;</strong>- non-negative integer</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Data type: int&nbsp;</strong>- integer</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Fixed array (e.g., uint[2], string[5])&nbsp;</strong>- array with a fixed length</p>
<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Dynamic array (e.g., uint[])&nbsp;</strong>- array without a specific length</p>

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Public array (e.g., Person[] public people;)&nbsp;</strong>- Solidity automatically creates a <i>getter</i> method for it.</p>
{% highlight solidity %}
""" Create a public array of Zombie structs, and name it zombies. """
Zombie[] public zombies;
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Public function declaration:&nbsp;</strong></p>
{% highlight solidity %}
""" Create a public function named createZombie. It should take two parameters: _name (a string), and _dna (a uint). Don't forget to pass the first argument by value by using the memory keyword """
function createZombie (string memory _name, uint _dna) public {}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Private function declaration:&nbsp;</strong></p>
{% highlight solidity %}
""" Modify createZombie so it's a private function. """
function _createZombie (string memory _name, uint _dna) private {}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Return values:&nbsp;</strong></p>
{% highlight solidity %}
""" Returning values """
string greeting = "Hello world";
function sayHello () public returns (string memory) {
    return greeting;
}
""" Only for viewing the returned value """
function sayHello() public view returns (string memory) {
    return greeting;
}
""" Cannot even access the state values """
function _multiply(uint a, uint b) public pure returns (uint) {
    return a * b;
}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Keccak256:&nbsp;</strong>is a version of SHA3 which can take a single parameter of type bytes.</p>
{% highlight solidity %}
""" The first line of code should take the keccak256 hash of abi.encodePacked(_str) to generate a pseudo-random hexadecimal, typecast it as a uint, and finally store the result in a uint called rand. """
""" We want our DNA to only be 16 digits long (remember our dnaModulus?). So the second line of code should return the above value modulus (%) dnaModulus. """
function _generateRandomDna(string memory _str) private view returns (uint) {
    uint rand = uint(keccak256(abi.encodePacked(_str)));
    return rand % dnaModulus;
}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Random Zombie Function</strong></p>
{% highlight solidity %}
""" Create a public function named createRandomZombie. It will take one parameter named _name (a string with the data location set to memory). (Note: Declare this function public just as you declared previous functions private) """
""" The first line of the function should run the _generateRandomDna function on _name, and store it in a uint named randDna. """
""" The second line should run the _createZombie function and pass it _name and randDna. """
    function createRandomZombie(string memory _name) public {
        uint randDna = _generateRandomDna(_name);
        _createZombie(_name, randDna);
    }
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 16px"><strong>Events:&nbsp;</strong>are a way for your contract to communicate that something happened on the blockchain to your app front-end, which can be 'listening' for certain events and take action when they happen.</p>
{% highlight solidity %}
""" The first line of code should take the keccak256 hash of abi.encodePacked(_str) to generate a pseudo-random hexadecimal, typecast it as a uint, and finally store the result in a uint called rand. """
""" We want our DNA to only be 16 digits long (remember our dnaModulus?). So the second line of code should return the above value modulus (%) dnaModulus. """
function _generateRandomDna(string memory _str) private view returns (uint) {
    uint rand = uint(keccak256(abi.encodePacked(_str)));
    return rand % dnaModulus;
}
{% endhighlight %}

<p style="font-family: 'Times New Roman', serif; font-size: 20px; margin-left: 35px;"></p>

<br>
<br>
<br>

[cryptozombie]: https://cryptozombies.io/
