---
title: 'The Plan - Devlog #1'
date: 2025-02-22 17:00:00
---
My favourite type of Roblox game is emergency roleplay. Only thing is, I've been struggling to find one that has a good balance of gameplay and roleplay. [Emergency Response: Liberty County](https://www.roblox.com/games/2534724415/Emergency-Response-Liberty-County) is what I've been playing for the past couple years because it had a good balance between those two things and was fun, but recently the updates have been slowing and getting smaller, and it's becoming less fun in general.

So I'm going to make my own emergency roleplay game, focusing on that balance between gameplay and roleplay. Right now I'm thinking of calling it Renoak County and having the main city be called Willowfield, and I might have one or two smaller towns to make the map a bit bigger. If you have any better ideas for the game/city name, please add them to the comments. I don't want it to be in a state or really anywhere in America, like how Springfield from The Simpsons isn't really set anywhere (unless you count [this film theory episode](https://www.youtube.com/watch?v=S3FtIuVNY8k)), but I do want to base them off of Coloradoan towns (is Coloradoan a word?). These are a couple of pictures showing kind of how I want it to look, quite sunny but also quite mountainous.

<img src="/blog/assets/colorado-springs.jpg" alt="Colorado Springs" height="300">
<img src="/blog/assets/greeley.jpg" alt="Greeley" height="300">
<img src="/blog/assets/golden.jpg" alt="Golden" height="300">

I don't have a full plan for what features I'll be adding to it, but I've got a few planned. I might change these, but it's what I have in my head right now.

## Planned features

### Crime planning

For major crimes like robbing/burglarising a store or house there'll be a planning system so you can decide how to commit those crimes and it doesn't get boring. This is how I want the 'flow' to go:

1. You buy blueprint paper from a store.
2. You choose the crime to commit, e.g. robbing a store or breaking into a house.
3. You choose how to commit the crime, with pros and cons for each way, for example:
    - When burglarising a house, you can choose to cut the power to the house which'll cost an extra thousand and add a star to your wanted level, but give you an extra minute or two to rob the house.
    - When robbing a store, you can choose whether you tell the clerk about the gun, point it at them, fire a warning shot, or shoot their foot. Each one will give you a higher wanted level and give you less time in the store (e.g. the warning shot will attract attention) but the clerk will be amore intimidated and give you more money.
    - When taking a hitman job, you can choose whether to use a knife, pistol, or sniper. A knife will cost less but you have less of a chance of succeeding. A pistol will cost more and have a higher chance of succeeding but you'll be spotted more easily. A sniper will cost the most but have a 100% chance of succeeding and give you more time to run away.
4. You spend the cost of the robbery on printing the plans.
5. You have to carry the plans around with you before committing the crime, so police can find it and arrest you for conspiracy. There'll also be an option to spend more money and memorise the plan so you don't need to carry it.
6. You commit the crime and run away, and the blueprint gets destroyed.

I think this'll be good as it'll make the game a bit calmer, make crimes feel bigger, and remove the repetition of other games.

### ATMs

There'll be ATMs where you can collect a daily reward, transfer money, buy money with Robux and *rob them.* In ER:LC, police will camp an ATM when they see somebody using it because there's no other use than just to rob it, so adding some uses will hopefully reduce that.

### Chaos lobbies

It'll be a bit like the Bad Sport feature on GTA Online, where if you randomly kill 5 people or shoot at 10 cars, you will be labelled a "Menace" for a day or two and will be forced into chaos lobbies with other menaces. I think I'll also make it where non-menaces will be able to join chaos lobbies if they want to, and maybe after being a menace 5 times in a month or 20 times in total you get banned. I think I'll change around the conditions for being a menace and might make it a temporary ban instead of permanent ban when you reach a certain amount, and I think I'll hide exactly how you get labelled a menace so people can't get around it but it'll be something like this.

## Finished features

OK, so I've actually been working on this for about a week or two before making this blog so I have a couple features done already.

### Phones

I think this'll be my alternative to menus: phones. You can practically put anything in a phone and it'll make sense. A map? GPS app. Settings? Settings app. A cash store? Robux to cash currency conversion on a bank app. It's perfect to keep people immersed, or as immersed as you can on a Roblox game. I shouldn't have put this in the finished features section because I haven't actually fully finished it, but I've made a start. There's a holding animation, a model, and a home screen with the real-world time and app icons. I've modelled it after the more recent Samsung Galaxy phones, one because it's easier to do (just a rectangle with some cameras as opposed to the round corners of an IPhone), and two because I use one myself and don't see much love for it on other games.

![The opening and closing animation of the phone](/blog/assets/phone-open-close-anim.gif)

I've also made a settings app where you can change between 12h and 24h time or change your background and ringtone. The ringtone doesn't really do anything yet since I haven't made the phone app yet, but it does save.

<img src="/blog/assets/phone-settings-app.png" alt="A settings page" height="350" style="display: inline;">
<img src="/blog/assets/phone-change-background.png" alt="A change background page" height="350" style="display: inline;">
<img src="/blog/assets/phone-change-ringtone.png" alt="A change ringtone page" height="350" style="display: inline;">

I'll also have a phone app where you can call people (over voice chat) or message them, a bank app where you can see your balance, transactions and transfer money, and a camera app where you can take photos using Roblox's [CaptureService](https://create.roblox.com/docs/reference/engine/classes/CaptureService) (which I don't see many other games using).

### Behind the scenes stuff

I have cash and the wanted system set up already, but haven't done the GUI so there isn't much to show. The cash system is pretty simple, just I have it so it saves the 10 most recent transactions kind of as a novelty feature so you can see how you've spent your money on a bank app. The wanted system is a bit more complicated:

- When you commit a crime, it adds to your stars up to 5 stars (like how it usually works) but also adds to your expiration time, so if you commit a new crime, your old crimes won't expire until your most recent one expires
- When your wanted level expires, instead of dissapearing completely, it converts to a warrant
- Warrants expire after a week and mean you can be arrested, but unlike wanted levels police have to specifically search your records to see if you have one. So, if you have a wanted level, police will know about it (it'll be pinned to their screen or something), but if you have a warrant, they'll only know if they search your record during a traffic stop or something.
- If you get a wanted level while having a warrant, your warrant gets converted to your wanted level (e.g. you have a 3 star warrant and commit a 1 star crime, so you get a 4 star wanted level)
- I haven't added this yet, but I might make a 6 star wanted level that only happens if you commit a large crime, like robbing a bank. I don't really have any plans for what would happen if you get a 6 star wanted level, so please put your ideas in the comments.

## Future devlogs and release

I'll be making devlogs fairly inconsistently but I'll try to post regularly. Also some of them might be huge like this one while some might be small and only showing off one feature. Also, I might end up completely changing the game since I'm still making it, so please don't get mad at me if I change it. I'm thinking of releasing the game in paid beta (probably only around 50-75 robux) once I have a working game ready hopefully by late Q3 to mid Q4 but it might be earlier/later, and I have no idea when the full release will be (most games have many years in beta before fully releasing). I might pay for some people's paid access if you're active on the blog.

## I need your help!

I don't really think anybody reads this blog, but if you do, please comment some ideas for what to add. You'll need to have a [Github](https://github.com/) account and sign in to comment since the comment software I use ([utterances](https://utteranc.es)) uses Github Issues to work. I haven't made much and I'm looking for ideas so I will consider *all* of them. I'll also give out some in-game rewards on release to anybody who suggests an idea that I end up adding.

Thanks for reading, please stay tuned for new blog posts and devlogs.