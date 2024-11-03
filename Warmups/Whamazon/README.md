# Whamazon
## Challenge Statement:
Author: @JohnHammond

Wham! Bam! Amazon is entering the hacking business! Can you buy a flag?

**Note**: This challenge was accompanied with a per-user instance

## Solution:
Starting the instance, I was provisioned a URL to an page. It was a [GoTTY](https://github.com/yudai/gotty) application. I was greeted with a menu to begin with.

![Greeting](assets/1.png)

Examining the inventory, it tells that we have to buy something.

![examining inventory](assets/2.png)

So, I decided to look at what was for sale.

![sale menu](assets/3.png)

It appears we have 50 dollars in my account and among many items the flag was also listed. So I went ahead and tried to buy it.

![attempt to buy flag](assets/4.png)

So we need quite the sum of money to buy the flag. At this point I thought there would be some session variable or token that contains the available balance on my account. I even went to inspect the web socket traffic and decode it in attempts to find it. 

And then it hit me. I tried to buy -1 quantity of Apples. And it worked. 

![the trick](assets/5.png)

So it is one of the oldest tricks in the book, insufficient input validation. So we should be able to use this to add money to our account and buy the flag. And that's exactly what I did.

![exploiting](assets/6.png)

So now that I have the balance I went ahead and bought the flag. But that's not it. I was invited to a Rock, Paper, Scissors and the program said it won't choose scissors. So I chose rock. It was a tie.

![buying flag and game](assets/7.png)

It played rock everytime, so when I chose paper I won and it said the flag was added to my inventory.

![winning game](assets/8.png)

Then I quit the game and the buy menu and opened my inventory. The flag was right there.

![inventory and flag](assets/9.png)


