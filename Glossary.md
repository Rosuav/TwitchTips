# Glossary

* TOC
{:toc}

## General tips

Most streaming terminology is heavily derived from somewhere else. The Almighty
Google knows all, and sees all, and is a wizard, and is probably not even evil.

## Words, words, words

... is that all you blighters can do?

### Bandwidth

The amount of stuff you're sending or receiving. For a broadcaster, this is
generally limited by the quality of your internet connection; try to keep
your streaming software limited to no more than about 80% of what your actual
internet connection can handle (so if you can handle 5000Kbps, stream at no
more than 4000Kbps).

### FPS / Frame Rate

Frames Per Second. For gamers, it's usually important to have as many as you
can get (up to a point), but for streamers, every frame costs you bandwidth
(see above). Streaming at 30FPS is usually fine; if your connection struggles
to handle your output bandwidth, it may be better to stream a stable and high
quality 20FPS than a glitchy 30. Increasing to 60FPS should only be done if
you know you can handle it.

### Latency

The time delay between something happening and it being seen. For streamers,
this usually means the time from when you say something to when the viewers
see it (or, conversely, the time from when a viewer types something in chat
to when the streamer reacts to it).

### Operating System (OS)

The thing that runs your computer. It's your OS's job to run the things that
you actually care about. Popular operating systems include Mac OS (aka OSX
aka macOS), Microsoft Windows, Linux (usually seen in some form of distro
eg Debian, Ubuntu, Red Hat, Kali), FreeBSD, iOS, etc, etc, etc.

Your choice of operating system dictates some of the software you can use,
but other software ("cross-platform") can be run on many OSes.

### Noise

In statistics, "noise" is any variation that has no real meaning. For instance,
you might ask OBS to broadcast at approximately 4000Kbps, but your actual
bitrate varies from 3915Kbps to 4113Kbps; this is still basically 4000, and
the difference is "just noise". Viewer figures changing from 25 to 30 to 22 to
27 is also a whole lot of noise; the figure is basically stable.

### Resolution

The number of pixels in the image you're sending. Most viewers aren't going
to see anything more than 1080p or even 720p (an HD screen with some room
taken away for chat is generally going to leave about 800p at best), and
as with FPS, the higher your resolution, the more you have to output. It's
better to stream a high quality stable 480p than a glitchy 1080p.

### Recursion

See: [recursion](#recursion)

### Transcoding

In a Twitch context, "transcoding" is a feature offered by the Twitch servers
to adjust your bandwidth in real-time. It's also sometimes called "quality
options" because that's exactly what it gives to your viewers: they can all
choose from the available qualities, giving a tradeoff between bandwidth and
graphical quality. You, the broadcaster, still need to manage your output
bandwidth, but if you stream at 1080p 6000Kbps and have transcoding available,
any viewer can choose to view the stream at anything down to even 160p, to
relieve the load on their own connections.

If you don't have transcoding available, everyone has to download at the same
bandwidth that you are uploading.

### Uninterruptible Power Supply (UPS)

If a surge protector is a seatbelt, a UPS is a full-on ejector seat. When your
power goes out, your UPS will switch to battery power and keep everything going
for a while - long enough to cover for a short outage, or to let you cleanly
shut down before a longer one. Even without an actual outage, a good UPS will
clean your incoming power - industrial loads near you won't be able to hurt
your computing equipment. A UPS can significantly extend the life of your PC.

### VOD

Short for "Video On Demand", this refers to all forms of pre-published videos.
Most commonly, a VOD is a past broadcast, retained for some time automatically
and able to be preserved indefinitely as a Highlight. If you missed a glorious
moment from your favourite streamer, just nip over and check the VOD! You can
even VOD-clip (take clips directly from the VOD), giving extra flexibility.
