Title: The 4 stages of data protection: In Transit
Author: Bryce McNab
Category: Security
Tags: Encryption
Status: draft
Date: 3/21/17

Your computers physical security has been assured, your local digital security is hardened open source encryption. That's all well and good, but how can you be sure the data you are sending to web services isn't hijacked before it gets there by one of those sneaky network snoopers?

# TLS

Have you ever seen that green padlock icon in the top left corner of your Firefox or Chrome window? That icon indicates that the communication between you and that website is encrypted. Let's get a little into the weeds of TLS, and with that, asynchronous encryption.

## Asynchronous

Asynchronous encryption is a method of encryption that uses two keys to secure the communication: A public key, and a private key. A public key is exactly what it sounds like: a file that is given out publicly so other entities can use it to send encryted communications or traffic to the holder of the private key. Let's analogize this:

>A public key is like a padlock. A private key is the physical key that opens this lock. If you want your friend to send you a letter, but you don't want anyone to read it, you can give them a lock. Your friend would put the letter in a metal box, put the lock you gave to them on it, and would send it to you.

>Notice that your friend only has the lock, and once it's locked, has no way to unlock what they just put in the box. So your friend send you this box, and you, with your private key, can unlock it and read the secret note inside.

## In practice

TLS is a form of asynchronous encryption where the web server that is using TLS has a publically available key that your browser uses to send encrypted traffic, using the public key, to the web server. Generally speaking, if you see that green icon in the top left of your browser, your communication with the website you are connected to is encrypted, and no prying eyes can see what you are doing on this site. One thing to note is that TLS does not stop sneaky network snoopers from seeing what websites you are visiting, this is unencrypted, but they cannot see what you are doing on that site.

TLS is the most common form of in-transit encryption in use today, because it is a very transparent encryption scheme that most people don't know it's happening in the background. This is one of the most successful role outs of encryption because of it's ease and transparency. There is no complicated setup for the user, much like GPG.

If you don't see the padlock on a particular website, try entering "https://" in the beginning of the url, replacing "http://" if it's there.

Now your traffic is encrypted between you and the web service you want to use. Next, and last, in this small series will most likely be the longest article of the 4, as it will go over lot's of privacy and security minded policies and how to choose the right web services for you.
