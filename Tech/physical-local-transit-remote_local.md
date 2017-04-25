Title: The 4 stages of data protection: Local
Author: Bryce McNab
Tags: Alice and Bob, Encryption, Security
Status: published
Date: 3/9/17

>Alice is getting ready to leave the office. She grabs her keys and wallet, and reaches for her phone. _But her phone isn't there_.

We've all had the panic that Alice is feeling now when we don't see our phone where we think it was last. Maybe you couldn't feel it in your pocket?

>The worst runs through her head. Charlie _must_ have been the one who stole it, and surely it was to get at those secret messages badmouthing him.

Maybe the phone wasn't stolen?

>Alice relaxes; there it is. The phone was a foot to the right on her desk.

But what if the phone was stolen? There is very sensitive information on her phone. And what of her laptop for that matter? Or the desktop at home?

That's what I'm here to talk about: How to keep the information on your computer secure even if the system was stolen.

Local data is defined as any and all information stored on any disk on the computer. This can include a hard drive, an SSD, SD card, or CD/DVD in the optical drive.

Concept of the day: encryption.

The general idea of encryption is to turn some data into an unintelligible mess, but allow a way for that unintelligible mess to be reversed into the same data. Let's look at an example:

Here is some data:

    Charlie has weird ears.

Now, Alice doesn't want this data to be seen by Charlie. So she uses the venerable encryption method called "AES256". Her password is the strongest password possible: password.

Here is the encrypted text:

    il7 >.mw} êÚ./t.
    ..ÕQbÀ.Zªa.â÷¡õ.

See, now nobody can see what the original string said. Now Alice is the only person who has the super secret password to this file. 

> When Alice wants to read this data, she can decrypt it using her super secret password and read back:

    Charlie has weird ears.

What's great about this encryption method is not only can it be applied to words and sentences, but files, and even entire hard drives. All of the major operating systems today (Windows, MacOS, Linux, BSD) and mobile operating systems (iOS, Android, etc) include ways to encrypt the entire drive of the system. These generally use very secure encryption schemes (algorithms). Apple has been setting iOS devices (iPhone/iTouch/iPad) to be encrypted by default. Most android devices are not and need to be enabled in the settings.

MacOS and Windows need to be enabled as well, and most are very simple. There are guides all over the place (not the purpose of this article).

> If Alice wants her data to be safe so only she can get to it, even if it has been stolen, encryption is the only way. 

Encrypting a drive takes time and the first time you enable encryption, you will need to leave your system (phone, laptop or otherwise) plugged in, until the process is complete. Even if your computer or phone is stolen, nobody will be able to read what is stored on the device locally without your password. Remember to pick a good password.

>DISCLAIMER: I do not pretend to be a security analyst or researcher in trade or through education. I am a hobbyist, with an interest in security. I do practice what I preach here, but cannot be blamed for your computer eating your dog.

>If you do find I am inaccurate, feel free to contact me with the corrections! I love learning new things.
