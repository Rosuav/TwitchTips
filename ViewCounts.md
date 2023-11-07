# Counting viewers
# and when not to

As a streamer, it's really hard to get any sort of feedback on whether you're
doing a good job. Whether this is a hobby, a fledgling business, or your full
time job, you're probably tempted to look at your viewership to see whether
you're making good or bad decisions. Is that worth doing? Deceptive? What do
the different numbers even mean?

## What the figures mean

### Viewers

In general, a "viewer" is someone presently (or recently) consuming the video
stream. So long as the actual video is playing, that person should be counted.
Some browsers will unload tabs to conserve memory for tabs which are visible,
which would stop the video player. In Chrome, for example, you can turn off
this behaviour entirely in the Settings/Performance screen, or you can leave
it turned on and allow only certain sites to remain active.

An engineer who worked for Twitch confirmed that you can leave the video
player muted and you should still count as a viewer. In practise, however,
when the video buffers in a tab which isn't visible, the video player will
usually not resume playing until you switch back to that tab. If you're
going to switch between viewing a few different streamers, you may need to
switch to that tab every so often.

To minimize the bandwidth a background tab consumes, you can lower its video
quality, as long as the stream has [transcoding](Glossary#transcoding) active.

### Chatters

A "chatter" is someone connected to the text chat. Most people will be both
viewing and chatting, but it's possible to be either one without the other.
Many people will lurk in myriad channels' chats, and bots often connect to
chat without viewing the stream; these do not count as "viewers" but usually
do count as "chatters".

### Raiders

When you [raid another stream](RaidingOnTwitch), the number of raiders is
closely related to the number of chatters, but only those who actually "ride
the raid". Details on exactly how this works are scanty.

### Partnership Viewers

This is not an official term, but the viewer count has one special case: the
achievement required for a partnership application involves an average of 75
viewers, "excluding Hosts, Raids, and Embeds". All other definitions of view
count include those subcategories, but for this specific calculation, anyone
who has raided into your stream will not count; nor will people watching
your stream using some forms of multi-twitch (which count as "embeds"), or
those seeing your stream hosted elsewhere.

At some point it was thought that removing the ?referrer=raid parameter
from the URL or refreshing the stream or even clicking on the channel name
or a link to the channel would make you count for this calculation. Maybe
it did at some point, but the same engineer who confirmed that it is fine
to mute the video player also said that none of these things work.

For clarification, parameters in URLs may change what you see on a site,
like when you want to sort from lowest to highest, but they do not
actually change the data on the site. Whatever Twitch does to track who
raided in is data on their site which can't be manipulated.

However, the viewers who are part of a raid do still improve the chance
for the stream they raided to be discovered. Viewers who might never have
clicked on the stream before may see the stream recommended to them on
the front page of Twitch in one of the shelves, or in the category the
stream is in.

Instead of telling viewers to refresh the stream or click on a link, a
streamer should probably focus on being a welcoming host, and encourage
their viewers to make clips. The best clips are a great way of showcasing
the best parts of a streamer's channel, and can be made into Featured
clips which can be discovered on the front page of Twitch. This isn't a
guaranteed way of bringing in new viewers, but it's built-in and free, so
why not use it?

### Total Views

Honestly, I don't know what this figure actually means. It goes up whenever
people watch your stream but I have no idea what "one view" actually is.

### Followers

This one's pretty simple. Someone follows your channel, it goes up. Someone
unfollows, it goes down. Someone gets deleted who had followed your channel?
You guessed it, it's going down. So don't stress about losing a follower here
and there; people's accounts get cleaned out if they abandon them.

## When these figures are important

If you're trying to qualify for Twitch Affiliate status, you need to have an
average of three viewers for a month, and fifty followers. If you're trying for
partnership, you need seventy-five "right-here viewers" for a month.

As a measure of channel growth, all of these figures are very [noisy](Glossary#noise).
You can't look at today's stream and yesterday's and then [extrapolate](https://xkcd.com/605/)
from there. Even across a few weeks, there is considerable noise; and there are
busy and quiet times of year. Comparing your stats from the same time last year
is likely to give reasonably useful results, if you can be that patient.

## When these figures are NOT important

When you're deciding what to do. When you're deciding what time to stream. When
you're deciding pretty much anything about your stream! Stream what works for
you, don't try to "follow the numbers"; don't play the most popular games, or
the most popular days of week, just for the sake of "getting viewers". Be what
you can best be, even if it looks like you have zero viewers; stick with it
for at least a few weeks or a month before you decide that it's not working.

Especially, don't feel disheartened because nobody's in chat today, or the
viewer count is showing at zero. Stream anyway, and address the invisible
lurkers, because you never know who's watching the stream logged-out, or is
checking out the [VOD](Glossary#vod) afterwards!
