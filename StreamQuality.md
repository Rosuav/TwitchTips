# Stream video quality

As you broadcast, you want to have the best possible visual display, within the
constraints of your available hardware and software. What are the tradeoffs?
What's the best way to improve the stream? How would you analyze your stream to
find out where the bottlenecks are?

## Internet connection

Live broadcasts require constant transmission via the internet. How fast can
your connection send stuff out? Find out your upload speed by doing a speed
test, but NOT while you are live - don't fall into the trap of thinking "I'll
just see what my speed is right now", because you won't get a reliable answer
AND you'll destroy your stream quality!

The quality of your connection can be described by a few useful numbers:

* Bandwidth - the total amount of stuff you can send each second
* Latency - how long it takes to send stuff out and get a response back
* Stability - how consistent the above two numbers are

In general, a wired internet connection (cable, ADSL, etc) should have good
stability and reasonably low latency, and the bandwidth will be something
your ISP advertises (but never guarantees). Having wifi doesn't generally
change your bandwidth, though it can affect your stability. Mobile internet
connections tend to have far worse bandwidth, latency, and stability, but
you can sometimes combine multiple connections to multiple providers and use
the total bandwidth for your stream. (This is outside the scope of this
document though.)

### Bandwidth

Be careful - sometimes bandwidth is measured in megabits per second, other
times in megabytes per second. (Or kilobits/kilobytes, for slower services.)
These can be spelled Mbps and MBps, so the difference can be subtle! Divide
the megabit rating by eight (or ten for simplicity) to get megabytes.

Streaming software such as OBS Studio will allow you to choose the maximum
bitrate to be used. Set the video bandwidth no higher than roughly 80% of
your network speed if you have good stability; lower if your connection is
unstable. Audio bandwidth isn't usually a problem.

NOTE: If you have [transcoding](Glossary#transcoding) available, you can set
your streaming quality as high as your own connection can manage; but if you
don't, it may be worth considering your viewers' needs, and streaming at no
more than 2500Kbps, or some other compromise figure.

### Latency

Normally not a problem for good quality home-grade wired internet connections,
but critically important when using a mobile phone connection (4G etc). When
latency is poor, it may be worth adjusting your settings to ensure that your
video remains stable. TODO: Figure out what you'd adjust.

### Stability

When your internet connection isn't stable, your video will be choppy. Aim for
the worst speed you can reliably manage, or alternatively, aim a bit higher and
then accept that you might sometimes have buffering.

## Computer processing power

In order to generate the images for your stream, some program has to do a lot of
work. That requires a lot of "grunt" from your computer.

### CPU speed and core count

Lots of what you do will require your CPU. If you use software encoding (x264),
that's part of your CPU load; if you have a lot of stream toys (Kappamon, bit
boss, alerts, animations, etc), they also cost CPU. Are you streaming a game?
That costs too. For the most part, extra cores can help with this, but some
jobs have to be done on a single core, so the speed of one core is important.

### Memory / RAM

Again, everything you do requires RAM. Stream toys require RAM. Your game or
art software etc will require RAM. If you don't have a lot of physical memory,
your computer will start thrashing as it goes into the swap/page file, and that
can kill performance.

### Video card / GPU

Hardware encoding (NVENC) takes load off your CPU and puts it onto your GPU
instead. If you're streaming a graphical game, this could impact your game's
performance; but if you're streaming something that doesn't use the graphics
card (such as digital art creation, or anything in the physical world), this
is a great way to improve performance.

## Finding the bottlenecks

How do you know what the limiting factors are? How do you know if you're
running into problems? This depends a bit on your [operating system](Glossary#operating-system-os)
and streaming software, but you should always be able to find a simple graph
that shows your CPU usage over time, and often your RAM and GPU usage as well.
Inside OBS Studio, choose View|Stats to see OBS's own summary; having this
open on a spare monitor can reveal a lot of possible problems.

### CPU saturation

You'll spot a CPU load issue by seeing that your CPU usage graph stays at the
top all the time. (Noticing a single-core problem is harder, but that's also
rarer.) In the OBS Stats window, "frames missed due to rendering lag" usually
indicates a CPU load problem. "Skipped frames due to encoding lag" can also
mean this, if you use software encoding.

### RAM saturation

If your RAM is full, any graph should show this - you'll be using a lot of
swap space or page file. You may also notice this if your hard disk is busy.

### GPU saturation

When you use NVENC, OBS's "skipped frames due to encoding lag" figure will
usually indicate that your GPU is overloaded. You may also observe this if your
game (if you're playing one) is unable to render frames at the usual rate.

### Bandwidth saturation

OBS Stats will show "Dropped Frames (Network)" if you are unable to push enough
data down the wire each second. If this number goes up rapidly for a while and
then stays the same, this may indicate a stability problem; if the number is
constantly rising and the percentage is consistent, this probably means a limit
on your total bandwidth.

OBS will also show a color marker on the main status bar if frames are being
dropped. This applies _only_ to bandwidth problems - CPU/GPU limits won't show
a yellow or red marker here.

### Stream bandwidth

If OBS is set to limit to a bandwidth that your network can handle, but it's
too low for your other settings, you won't see anything in your stream software
at all, but your viewers will see a lot of 'artifacting' and/or blurring. Ask
your faithful viewers (maybe your mods) to tell you when things look bad, or
watch your VOD afterwards, to see how good or bad it looks.

## Available tradeoffs

So you've determined that you have a problem, and want to reduce one particular
load. Or you've determined that you DON'T have a problem, and want to increase
stream quality by spending more of a resource. What can you do?

* Resolution and bandwidth - increasing resolution requires more bandwidth
* Bandwidth and artifacting - increasing bandwidth reduces artifacting
* Artifacting and CPU usage - higher quality settings reduce artifacting but
  cost more CPU
* Frame rate and bandwidth and CPU - 60 FPS costs a lot more CPU and bw than
  30 FPS does
* CPU and GPU - switching between NVENC and x264 chooses where that load goes
* Fanciness and CPU/RAM - stream toys cost CPU and memory to render, more at
  higher frame rates

## So how do you choose?

Start by picking your output bandwidth. Limit this at about 80% of your most
stable internet connection speed, and if you don't have transcoding, cap it at
what your viewers will be able to handle (maybe 2500 or 3000 - maybe lower).

Having chosen your bandwidth, check [Twitch's recommendations](https://stream.twitch.tv/encoding/)
for what sort of resolution and frame rate would be appropriate. As of 2019,
they no longer have recommendations below 3000Kbps, so here are mine:

* 2000Kbps: 720p 30fps if you can handle the CPU load and/or use NVENC,
  otherwise 720p25 or 720p20, or 540p30, depending on whether frame rate or
  resolution is more important to you.
* 1500Kbps: 540p20 for a first guess, and then you may be able to raise that
* 1000Kbps: 480p20, but at this kind of bandwidth you may have other considerations
  such as stability. Experiment on your own setup.

With your bandwidth locked in, how can you best spend your other resources so
you get the best possible video image? The easiest way to find out is to try.
Twitch has an extremely useful [Inspector](https://inspector.twitch.tv/) which
can help you here; run a bandwidth test by adjusting your stream key (their
instructions are on the Help Guide on that page, once you log in), and keep
adjusting and running another test stream. You won't actually be broadcasting
(as long as you set the bandwidthtest flag), so you can safely test at leisure.
Increase something until you start to see problems, then back off a bit.

Once you have a stream setup that works for you, keep an eye on things periodically,
making sure your stream isn't deteriorating - or to see if you can crank
something up!
