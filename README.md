# The Crowd Computer

Go to the URL http://wwww.crowdcomputer.com and become a part of a global computer.
This is the target of this project.

## Implementation
Everything should work in the browser, so we use
* IndexedDB
* WebRTC
* JavaScript

So we can save things, can compute things and can talk to each other.

If you connect to the network the first time, you have to create a asymetric keypair,
so you can sign, what did you compute and nobody can manipulate it. And you upload you computations,
so that everybody can verify it.

So, a full dataset consists of:
* ID
* Type (data upload, has to be executed, was executed)
* entry state
* algorithm 
* output state
* timestamp
* signature
* public key

If you just want to upload data, the algorithm and output state is not needed,
if you want to execute something, the output state is empty.

## The immune system
Now, somebody could upload an endless computation or many data. To prevent this,
everybody shall log the actions of the others.
And if I compute x for you, than you compute y for me later.
This is like a credit, connected with you public key.
And even if someone wants to spam the network, he has to calculate usefull things.
And to save data, is another category than to calculate something. So there are 2 currencies.

## Todo
[ ] Generation of key pair in the browser<br>
[ ] Protocols for communication<br>
[ ] Behavior of a node<br>
[ ] Definition of "how much is a calculation-Cent?"<br>

## Usefull Links
Git Introduction: https://git-scm.com/book/en/v2/Getting-Started-Git-Basics <br>
JavaScript Succinctly: https://www.syncfusion.com/content/downloads/ebook/JavaScript_Succinctly.pdf <br>
For asymetric encryption and signing: pls google "introduction to modern cryptography" <br>
For using IndexedDB: http://pouchdb.com/ or https://github.com/aaronpowell/db.js <br>
&rarr; We have to ask the user for persistent storage: https://developer.chrome.com/apps/offline_storage <br>
For WebRTC: http://peerjs.com/ (more research needed)
