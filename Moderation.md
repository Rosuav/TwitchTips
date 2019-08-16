# Moderation tools

Twitch offers a number of moderation tools and anti-spam/anti-troll guards. I
go into some detail during the second part of [Streamer Tips 2](StreamerAdvice_20190816)
which should be viewed as a companion to this. (TODO: Get a starting timestamp.)

## AutoMod

AutoMod is an AI that guards your chat. It is unique among moderation tools in
that it is a shield that prevents bad messages from being posted (as opposed to
a sword that removes them afterwards), but one whose blocks can be overridden
by a human mod.

To configure AutoMod, go to [https://www.twitch.tv/dashboard/settings/moderation/automod](your
Twitch Dashboard). Choose a protection level based on how you want to run your
channel - are you PG-13? G-rated? Swearing's okay but no targeted harassment?
Then make sure your (human) mods have the chat option "Show messages caught by
AutoMod" active (have them click the gear on their chat), and proceed to train
the AI.

When properly trained, AutoMod serves alongside your other moderation tools in
ways that nothing else can.

## Human mods

The absolute most important moderation tool is an actual person wielding a sword.
If your stream is small and quiet, you can do your own moderation, but as the
channel grows, you will want to appoint additional sword-bearers. New to Twitch
and don't know how things go? An experienced mod can help you out and make sure
you don't have to worry about anything.

Communicate well with your mods. Are they too aggressive? Too lenient? Don't
expect them to read your mind (though some are quite good at it), just let them
know what you want. A good mod will reflect your intentions as long as you're clear.

## Bot mods

Not to be confused with AutoMod which is a first-party Twitch tool, moderation
bots are simply chat bots that have been granted mod powers. You, the streamer,
choose which bots to empower, and you also choose how to configure them; all
the well-known moderation bots (Nightbot, DeepBot, StreamElements(?), StreamLabs(?))
have flexible configuration options to allow you to customize the moderation
they do. If you give a bot a sword, take responsibility for the way it behaves,
and teach it what you want it to do; communicate with your bots just as you do
with your humans.

## Chat restrictions

Twitch offers you a number of ways to restrict who's allowed to speak in chat.
These tools can be used to combat spam or trolls, but they can also block legit
people from chatting, so use them wisely (and sparingly).

### Follower-only mode

Anyone who's not following your channel, or who hasn't been following for long
enough, can't chat. This is an effective temporary measure for keeping out
newly-created accounts, but it's also a strong turn-off for new viewers. Your
channel will become more insular, less welcoming. I recommend not using this
permanently, except in special circumstances.

### Subscriber-only mode

Even stronger than follower-only mode, this is the veritable nuclear option for
keeping the unwashed millions out of your chat. This should basically be used
ONLY to tame a nightmare situation, and then disabled again afterwards. If you
are tempted to use sub-only mode permanently, consider instead creating a
sub-only *chat room*, as this offers similar benefits without the turn-off.

### Slow mode

Unlike the previous options, this does not block any users completely, but all
non-mods are restricted to one message every N seconds. For small values of N,
eg 1-second slow mode or 3-second slow mode, this can be a reasonable way to
keep your channel from getting too noisy (but usually that's not necessary);
for large values of N (eg 30-second or more), it can help to tame a bad
situation and let your mods catch up with what's going on.

### Chat delay

Generally, don't use this. AutoMod does a better job. If you really want it, be
aware that it has its own limitations (bots, even non-mod bots, can still see
chat without delays), and it can create weird situations.

### Link blocking

Twitch has a first-party option to block all links from non-mods, but if you
need more flexibility, it's best to leave that option off, and have a bot that
can choose who to permit and who to purge.

### Emote-only mode

Ahh... this one. It's not really a moderation tool, except that it is. It's
theoretically able to prevent certain forms of abusive messages... but more
commonly, it's treated as a toy. "Turn on emote-only chat for two minutes!"
is a fun reward for your community (maybe something people can spend their
channel currency on).

### R9K mode

This can be seen as a special form of slow mode. Unique messages are permitted;
duplicates are blocked. Be aware that this can make your channel unfriendly
towards incoming [raids](RaidingOnTwitch), as raids often involve all members
posting the same message.

## Mod icons

These are available in your own chat and in the chats of any channels you mod
for. You can, with a single click, ban someone or time them out; this is very
dangerous, and will often lead to banning the wrong person. Instead, use the
user's popup information (click on the name, or use the "/user" command) for
this purpose, unless you're dealing with a large number of trolls all at once.
The mod icons do have one unique feature, however: you can delete a single
message, something you can't easily do any other way. This message removal
does not remove a mod sword, does not excessively purge all text, and is a
great way to deal with an accidental slip-up by an otherwise-legit person.

----
