---
title: "Demonstrating How Shor’s Algorithm Cracks the RSA Encryption Standard (POC — 4-bit Version)"
seoTitle: "Source Code to Crack Shor's Algorithm"
seoDescription: "Smaranjit Ghose did a wonderful job of cracking a 4-bit version of the RSA cipher using a quantum algorithm. I wrapped it in a Flutter UI, find it here."
datePublished: Fri Feb 25 2022 19:37:28 GMT+0000 (Coordinated Universal Time)
cuid: cl9y3962u00289fnvexymdr8a
slug: demonstrating-how-shors-algorithm-cracks-the-rsa-encryption-standard-poc-4-bit-version-b8cc9a62c06a
canonical: https://thomascherickal.medium.com/demonstrating-how-shors-algorithm-cracks-the-rsa-encryption-standard-poc-4-bit-version-b8cc9a62c06a
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1667299800590/Gr-DK8aQ-.jpeg
tags: encryption, quantum-computing, poc, shors-algorithm

---

#### We do not use the current industry standard RSA implementation but a version implemented by a fellow coder. A similar procedure will be used once million-qubit Quantum Computers become reality.


First of all — he is not cracking industry-standard RSA. He implemented a 4-bit version of RSA using Python code. I refer to Mr. Smaranjit Ghose, an extremely cool character, whom I have never met but whose work speaks for itself.

This guy actually implemented RSA for 4-bits and a demonstration of Shor’s Algorithm that cracks RSA. This is a tiny example, but the devil is in the details. And he has done a wonderful job.

You can find the full implementation [here as a Jupyter Notebook](https://github.com/smaranjitghose/quantum_burglary/blob/master/quantum_burglary.ipynb).



I refactored the code into a project, ran unit tests, added console capabilities and a UI in Flutter.

Enough of the chat — this is our combined code:

%[https://gist.github.com/thomascherickal/864ae038a20dfdb4596357477582edc6]

That’s the source code and I’m aware that to most of us it has the meaning of ancient Greek. 

I’ve tried to explain it as much as I can in the comments.

Here’s the Wiki page on RSA:
[https://en.wikipedia.org/wiki/RSA_(cryptosystem)](Link)

Welcome to IBM’s quantum computing library

https://qiskit.org/

And here’s the book on quantum computing by IBM (free):
[https://qiskit.org/textbook/content/ch-ex/](Link)

Now comes the coolest part:

I refactored the entire project into a monolithic project coupled with the Python code already available and added a UI in Flutter. This was the result.

This was my first serious Flutter project, and I really enjoyed the process of creating it. This was the output in Linux:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299797220/oqLsreR7u.png)

Linux Ubuntu Output

In Chrome:

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1667299798905/4J0A19BF0h.png)

Google Chrome

My system takes too long for the Android emulator to run, so I decided not to demo that. 

*But it will look the same. This is one of Flutter’s biggest advantages — uniform output across platforms.*

Sample output:

Plain Text: Thomas

Cipher Text: 56467465150941795

Cracked Text: Thomas

Hope you enjoyed this article. Quantum computing has a large number of applications. We just need to be clever as to how to useit in its current NISQ formulation.



*God bless.* 


*Love you all!*