Title: The Two Auths
Date: 2017-02-24
Authors: Bryce McNab
Tags: Alice and Bob, Security

Like in my [last article](http://blog.imnotat.work/security-vs-anonymity.html), authentication and authorization are often used interchangeably and when we are talking about security it can be very crucial for you to know the difference.

## Authentication

Authentication is not a question of what someone can do (that's authorization), but a question of who someone is. More accurately it is checking with a trusted source who someone is. Let's check in with our beloved supervisor, Charlie.

>Charlie wants to buy some alcohol. Despite what Alice and Bob are saying, Charlie knows how to party. Charlie is a young looking man and when he goes to the corner store to pick up some gin, he is carded. So he pulls out his trusty <insert state here> drivers license. 

Now the cashier is putting his trust in the state government that the card is saying accurately who this is. Dave (the cashier) is using the state as an _identity authority_.

>Dave, trusting the <insert state here> DMV, trusts that Charlie is who Charlie says he is.

This is important as the next step is to make sure Charlie has permission to purchase the gin he set out to get.

## Authorization

>Dave, trusting Charlie is who he says he is, now looks at the drivers license to confirm if Charlie has the proper _permission_ to buy alcohol. Looking at the date of birth, it's quite plain to see that Charlie is only 20 years old.

Charlie isn't at the minimum age of 21 in order to buy alcoholic beverages. So when Dave asks this trusted source if Charlie is allowed, it says no.

Sorry Charlie, you don't have permission to buy that gin. Maybe ask Bob to help you out?


>DISCLAIMER: I do not pretend to be a security analyst or researcher in trade or through education. I am a hobbyist, with an interest in security. I do practice what I preach here, but cannot be blamed for your computer eating your dog.

>If you do find I am inaccurate, feel free to contact me with the corrections! I love learning new things.
