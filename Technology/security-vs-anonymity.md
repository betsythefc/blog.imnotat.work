Title: Security vs. Anonymity
Date: 2017-02-22 15:31
Author: Bryce McNab
Tags: Encryption, Alice and Bob, Privacy, Security 

With all this hoopla about digital security and privacy circulating recently I thought it might be a good idea to compare and contrast the difference between being _secure_ online and being _anonymous_.

Now both of these concepts mesh much like a Venn diagram does. Interestingly enough being secure can sometimes be anti-anonymous and being anonymous can be anti-secure. 

## Security

Security online usually refers to encryption. When you connect to a website there are 2 ways to do it. You can connect by going to http://www.domain.com or http**s**://www.domain.com. The big difference is that **s**. That **s** means "secure", which in this situation means all the traffic between your browser and the websites server is encrypted.

This encryption (TLS) hides _exactly_ what you are doing on that website, but it does not hide that _you_ are indeed on that website. Sneaky network snoopers will only see that your IP address connected to this specific website, and they will have no idea what you are doing on said website. This is one of that main things people confuse between security and anonymity. There is no anonymity here. The Sneaky network snooper knows that you connected to http**s**://www.domain.com. They also know that you connected to http**s**://another.domain.com and any other website you connect to. But Sneaky network snooper doesn't know exactly what you are doing. They can't look on your network and see the password you just sent to your banks website to log in, because it is _secure_.

Security in and of itself can be anti-anonymity. For example, a popular (amongst us tin-foil hat wearing folks) communications encryption scheme is GNU Privacy Guard (GPG). GPG let's users encrypt emails asymmetrically. Asymmetrical encryption means there is a public and a private key to your encrypted data. Here is a quick catch-me-up:

>Alice wants to send an email to Bob. But Charlie is listening in and reading all emails between Alice and Bob. How can Alice and Bob gossip about Charlie? Well one method is for Alice and Bob, who cannot meet in person, to agree on a password together and encrypt the messages with that password. But this means that if they ever send the password through email (the only conceivable way for them to communicate in this scenario) then Charlie will know the password. This is called symmetrical encryption. Meaning the encryption and decryption methods are symmetrical, requiring the same key. 

>Instead Alice and Bob both generate what is called a key pair. This key pair consists of a public key, and a private key. Bob can send his public key to Alice, and Alice sends hers to Bob. It doesn't matter if Charlie has these public keys, for Charlie doesn't have either of our protagonists private keys. When Bob wants to say something mean about Charlie to Alice, he can encrypt his message to her, using her public key. Now even Bob cannot decrypt the message. Only Alice can with her private key.

>With this setup, Bob and Alice rejoice and send as many insults about poor Charlie to each other as they want. and all Charlie can see is a load of gobbledygook.

Now we can get the philosophy of it all.

In order for Alice to send Bob an encrypted message, as in the above scenario, she _needs_ to know something about Bob. First she must have Bob's public key, and second she must trust that Bob is indeed Bob and not Charlie pretending to be Bob (It was his Halloween costume last year after all).

This is not a solution to anonymity. Sneaky network snooper (remember him?) can see that Alice and Bob are exchanging emails and other messages, but cannot see the contents. 

## Anonymity

Anonymity is a different beast altogether. To be anonymous, you must be hidden, and to be hidden is to blend in. This can be anti-security, thought it doesn't have to be. Let's go back to Alice and Bob's malicious attempt to insult Charlie:

>Charlie has known for some time now that Alice and Bob have been talking about him behind his back. He can see the emails going back and forth but he doesn't know what they say. Well lucky for him, he is their supervisor at work and has the power to put a stop to it!

>Alice and Bob are on the rocks now; they have been indirectly caught, with no evidence, but still, this is an at-will employment state, so they better watch their step. 

>But of course, like all good employees, Alice and Bob don't want to stop their bitching and moaning about the oppressive Charlie. So they devise another plan: to trade insults anonymously. In such a way that Charlie doesn't even know it is them insulting him. This can be done in a number of ways. In our scenario, Alice and Bob install tor.

A quick break here about what tor is. Tor is an acronym meaning "The Onion Router" which is an anonymous and secure routing protocol for connecting to the "dark web" (ooooo). The basics of tor are simple. 

>Alice want's to connect to a server to send messages to Bob. Bob can then connect over tor to the same server and read these messages. 

Tor will encrypt the communications (much like that very important **s** above) and route it with many layers of encryption to many randomly chosen hosts, each removing a layer of encryption revealing the next direction for this message to go to.

>Depending on the service Alice and Bob want to connect to, it may be inside the tor network or outside. In this example, it doesn't matter. 

At the last stage of encryption, the last node decrypts the last layer, sees what server they are trying to connect to and send the packet on it's way. When Charlie looks at his network, he only sees normal encrypted traffic going to normal websites (this is very over-simplified).

Now, back to the scheduled programming: Charlie is none the wiser and thinks that Alice and Bob have cleaned up their act.

Being that you have to blend in to be anonymous, it can be hard to run encrypted communications, especially if not everyone around you is doing it as well. You may have to not encrypt a message, or otherwise hide the message in some other way to get it sent without suspicion.

This is not to say of course that you can't have both. As I mentioned above security and anonymity are not mutually exclusive, they are a Venn diagram. They overlap in many ways and in fact most anonymizing methods use forms of encryption for that added security.


>DISCLAIMER: I do not pretend to be a security analyst or researcher in trade or through education. I am a hobbyist, with an interest in security. I do practice what I preach here, but cannot be blamed for your computer eating your dog.

>If you do find I am inaccurate, feel free to contact me with the corrections! I love learning new things.
