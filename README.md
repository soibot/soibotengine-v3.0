soibotengine-v3.0
=================

**[@soibot][1]** was a Twitter chat bot by unk... \*cough\* \*cough\*. Born 12 Dec 2010. Initially, it is his secondary account uses to convince fellow his followings/followers to:

- unnecessary buying expensive items/games/etc
- annoy his friends
- make fun of his friends

Very pointless. I still don't get why it became so popular... Under 4 years. He now has **4,000** followers.

**v1.0** uses free Twittbot service by some Japanese dude. Upgrade to Pro version is neccessary if I want extra features. So I moved to similar free service for version **v2.0** which runs on Google AppEngine.
Bot service went dead because Japanese bot host ran out of API for some reason and shut the site. That was the reason why the bot stopped tweeting since then. I was lucky enough to backup all the script before hand.

I know he was dead for a couple of years. Why not resurrects him?

**soibotengine-v3.0** is born.

## About

**soibotengine-v3.0** is a Twitter bot engine based on Regex snippet from [soibotengine v2.0][2] by unk... \*cough\* \*cough\*

**Yes.** version 3.0 is coded by the same dude. Spent full week rewriting the v2.0 code from scratch. Most of the scripts are based on v2.0. (Regular Reply and Timeline Reply) Same old dialog, but with new features. It's awesome! (Owner, 2014)

By the way, this github is just a documentation. So please don't expect any source code for the time being.

## Purpose

* To have fun

Yes. One purpose!

## Amendment of these Terms

The owner reserves the right, at its sole discretion, to modify, add, or delete portions of or otherwise change these Terms at any time without notice to you. Please check these Terms periodically for changes. Your continued use of the Services after the posting of changes constitutes your binding acceptance of such changes.

##Disclaimer

None of the epigrams are own by the bot owner. With the exception of 'soi' or 'สอย' in it. Please understand that most of the phrase are over 3 years old and never changes. However:

1. If plagiarism issue arise between the bot and Twitter celebrities for ludicrous reason.

2. If owner finds any user attempting to engage in unacceptable use of the services which includes, without limitation, use of the Services or the Site to: (i) disseminate or transmit material that, to a reasonable person, may be abusive, obscene, pornographic, defamatory, harassing, grossly offensive, vulgar, threatening, or malicious (ii) conduct any action that may violate Thailand law and its agencies or authorities. (iii) and any of [these rules][6]

3. If owner find any user spamming the bot that greatly affect its API usage.

If any of the above case happens, the owner reserve the right to immediately terminate future interaction of that user and the bot without further notice.

## Changes from soibotengine-v2.0
Acutally it's too many to write, let's list few of the key changes.

**New features**

- Running on *Linux Paid VPS*
- Better at natural language processing (Thai only)
- Smart quota system to limits Twitter [API usages][4].
- Web search
- Image upload
- Fetching useful information
- Error reporting (at [@soibotstatus][3])
- Updated script to match today's situation.
- and much more 

**Removed features**

- Auto follow-back

Actually, I want to name this version **1.0** while two versions before are **0.1** and **0.2** respectively.

## Usage

Same as v2.0. Mention tweet or reply to [@soibot][1]. Or simply tweet normally if the bot is following you. ([@soibot][1] is in your follower list)

Notable Examples for v3.0:

| Command Type       | Tweet           | Reply  |
| ------------- |-------------| -----|
| Footfall matches today (EPL only) | @soibot บอลวันนี้มีอะไรบ้าง | @username Manchester City v Manchester United Aston Villa v Tottenham Hotspur |
| Horoscope      | @soibot ดูดวงให้หน่อย      |   @username อาจได้โชค มีลาภ อย่างไม่คาดฝันครัฟ |
| Lottery      | @soibot ขอหวยๆๆๆ      |   @username มั่วๆละกัน 806034 |
| Loveca draw (スクフェス) | @soibot เปิดซองๆๆ     |  @username ยินดีด้วยคุณได้ SR ( ꒪Д꒪)ノ |
| Buying suggeston | @soibot สอยอะไรดีอะครับ    |  @username สอยiPhoneสิ |
| Day in week | @soibot วันที่3 พย 57คือวันอะไรวะสอยบอท  |  @username วันที่3 พย 57เป็นวันจันทร์นะครัฟ |
| Taxi | @soibot เราติดธุระอะ เราต้องนั่งแท๊กซี่กลับบ้าน T^T    |  @username นั่งuberสิครัฟ สมัครเบย https://www.uber.com/invite/ubermy300 |
| Weather | @soibot อากาศที่เชียงรายเป็นไงมั่งอะ    |  @username ร้อนมากครัฟ 32 องศา มีเมฆบางส่วนที่Chiang Rai, Thailand http://t.co/ZIUfm3eAon |
| IP Tools | @soibot ip2dns 8.8.4.4    |  @username ตามนี้ครับ google-public-dns-b.google.com |
| Etc | @soibot เราเสี้ยนเกะอะสอยบอท    |  @username ลื้อห์ (´・ω・｀) |

And much more undocumented features

## Quota

He will tweet every **one** to **three** hrs for Timeline tweets and reply back in 2 minutes under normal circumstance.

Following is not required to interact with the bot (Following was necessary for v2.0). It's your own choice, but...

He **may** or **may not** reply back to you. This is one of new features in v3.0

Easy explanation in code snippet:

```python
if Tweet.type is 'Timeline':
    #replychance = '1%'
    if Tweet.phrase match phase in phraselist:
        replychance = phase.chance #Range - 1% to 100% (Could you find 100% phrase?)

if Tweet.type is 'RT': #Example - @Papa_soibot: RT @soibot สอยให้หมดตัวเลยสิครัฟ
    replychance = '10%'
    
if Tweet.type is 'Mention/Reply':
    if 'you are following bot':
        if 'bot is following you':
            replychance = '100%' 
        if 'bot is not following you':
            replychance = '75%'
    else 'you are not following bot':
        replychance = '25%'
```
So if the bot does not reply back to you, please kindly understand that it's solely to **limit its [API usage][4]**.

**The owner reserve rights to change all of its quota at anytime.**

*hint: 'bot' in this case might be its doppelganger*

If there is any error, it will be logged to [@soibotstatus][3].

## FAQs

#### Q: Why Soibot named สอยบอท anyway?
A: สอย means buy. บอท means bot. The bot that tells you to keep spending.

#### Q: How about cognitive feature?
A: No, and will never happen. It is too hard to control. (Example case: [Simsimi][5]

Every new script will be proof-read by the owner under his discretion.

This is to ensure that the bot will have the its personality. The personality that makes soibot unique.

#### Q: Will you open-source the code?
A: No. 

#### Q: I want to make a bot and will make it talk with soibot. Will that be ok?
A: Well, I want to reserve API for fellow Twitter user. I may block the bot if I find its content too repetitive.

#### Q: What should I do?
A: Have a great time. Please do not take it too seriously. 


For more question, please directly ask [@soibot][1] or http://ask.fm/soibot

If you want serious answer. Talk to its owner. Please do not ask about coding itself.

## Support, Discuss and Contribute

If you think you have found a bug/have a idea/suggestion, please tweet directly to the owner or DM to the bot itself. 

Or if you have github account. You can report an issue [here][7]

Thank you for reading and supporting.

## I want to help?

The owner currently not need any help, apart from designing new mascot that isn't own by any company or anime series.

Cute animal mascot is preferred.


[1]: https://twitter.com/soibot

[2]: https://sites.google.com/site/soibotengine/home

[3]: https://twitter.com/soibotstatus

[4]: https://dev.twitter.com/rest/public/rate-limiting

[5]: http://www.thairath.co.th/content/235632

[6]:https://support.twitter.com/articles/18311-the-twitter-rules#

[7]:https://github.com/soibot/soibotengine-v3.0/issues
