
Encoded sound was first patented in 1857 by Édouard-Léon Scott de Martinville, where a recording could be etched into parchment paper. However, Thomas Edison built one that could *play back* 20 years later in 1877. Eventually, the technology adapted to cylinders, then to vinyl records, then to cassette tapes. Circular storage was re-implemented with the compact disc, and the information was then completely digitized from there, most notably with the MP3 audio [standard](/protocols/).

While cassette tapes are most recognized for audio playback, many of the first [computer memory](/memory/) implementations used cassette tape, with the memory reference specifying how far to rewind or fast forward on the track. The concept is *mostly* the same with audio CDs, though there are two moving parts instead of one.

Portable radios became popular since 1955. To sell them, Sony [marketed](https://notageni.us/marketing/) the product as small enough to fit in your pocket, but the radios were *not* small enough. Their solution was to alter the sales staff shirt pockets to fit the radio, and it worked.

## What sound is

Strictly speaking, sound is the vibrations of air molecules, which are interpreted when they make an eardrum vibrate. Different combinations of simultaneous vibrations can create harmonic sounds, which are known as chords. The speed the waves hit the eardrum is the frequency, which we then process as the pitch ([this tone generator](https://www.szynalski.com/tone-generator/) gives a visual depiction).

To understand sound measurements, there are several important components:

- The volume of the sound, measured in decibels (dB)
- The pitch of the sound, measured in hertz (Hz)

Most healthy adults can hear between 20 Hz up to 20 kHz. Anything below that is infrasound, and anything above that is ultrasound. We're most sensitive to sounds between 2-5 kHz.

People typically lose the top range of their hearing over their lifetime. While infants can hear 20 kHz, young adults often can only hear 17 kHz, 50-year-olds often at 12 kHz, and people with hearing impairments only at 8 kHz. Some teenagers have [exploited this fact](/hacking/) to make extremely high-pitched text message notifications to not get in trouble in class.

## Encoding

To record sound, the device captures the vibrations, at the speed they're traveling, and records them onto something. A microphone is a "transducer" that converts sound waves into electromagnetic waves, and a speaker is simply a transducer in the opposite direction. In fact, speakers and microphones are so similarly designed that speakers can be [hacked](/hacking/) as low-quality microphones simply by plugging it into a microphone jack.

Depending on [the standards used](/protocols/), the electromagnetic waves can come from analog electrical pulses or digital electrical signals.

The oldest sound capture devices directly encoded the waveform, but computers will now [calculate](/math/) a [Fourier transform](https://en.wikipedia.org/wiki/Fourier_transform) to encode the data. Once it's encoded, it can then be saved to [memory](/memory/) or transmitted [over a network](/networks/). This can either be by measuring the relative density of sound waves compared to before and after it (pulse-density modulation, or "PDM") or the absolute measurement of sound waves relative to a fixed point (pulse-code modulation, or "PCM").

Speakers are either passive (without internal amplification abilities) or amplified (and often with their own volume control).

Most speakers are designed as an electromagnetic coil attached to a magnetic cone, with an acoustic medium such as cardboard or plastic. As the pulses engage the coil, the cone contracts and expands, and the vibration creates sound through the medium.

## Sampling frequency

For the sake of phone conversations, very high-quality audio isn't that important, and this was especially true when phone calls were made across upgraded telegraph lines. When converting analog signals to digital, phone calls are only "sampled" between the normal human speaking pitch, which is 0.3 to 3.4 kHz. The Nyquist sampling rate, an analog-to-digital calculation, effectively doubles that max number, and it becomes 8 kHz, meaning phone calls are recording pitch and volume information 8,000 times a second. Any lower, and certain phonemes (like "sh", "s", and "f") are too hard to distinguish.

Often, any sounds that go *above* the sampling frequency (like a high-pitched tone) will bounce back and create "aliasing" that will distort the sound. To fight this, most audio systems will use a "low-pass filter" beforehand to only permit frequencies through the Nyquist sampling below the measured frequency.

On the other hand, music itself higher standards around 44.1 kHz, which allow up to 22.05 kHz to be recorded. The extra 2.05+ kHz range beyond our hearing allows for filters to prevent aliasing without any issues in sound quality.

Anti-aliasing filters used to be expensive, so aliasing issues used to require more elaborate standards. High-end audio production (e.g., recording studios, movies) are at 48 kHz. Some sound engineers, for specific reasons, will work with multiples of 44.1 (88.2 and 176.4 kHz) or 48 (96 and 192 kHz). This *will* take up more memory, and may be potentially convenient, but for all practical purposes will probably get "downsampled" to 44.1 or 48 kHz anyway.

One creative use of extremely high sampling is to record at a comparatively higher pitch, then drop it down to 44.1 or 48 without any loss in quality.

## Sampling depth

"Sample depth" is the amount of data that each sample gathers, which determines the audio sample's quality. [8 bits gives 256](/memory/) possible representations on a spectrum, 16 gives 65,536. Standard "telephony" audio is usually 16 or 32 bit sampling depth.

This sampling is necessary for the computer to rebuild the sound wave when it reconstructs it. But, the computer is only using an *approximate* estimation of the waveform (which is perfect-enough for our ears). The last 0 or 1 on the bits will be random with a process known as "quantization". Since computers don't know how to fill it in, it creates quantization error throughout the audio.

We hear quantization error as "white noise", a low-level static throughout the recording as the "noise floor". The quantization can mix with the other sounds to create harmonic relationships throughout the song and magnify the noise in a recorded signal. You can most easily see the comparison by listening to the same song on an old vinyl record, then on a modern remastered version of the exact same song. This is actually a *preferable* experience to vinyl enthusiasts, but can also be useful for audio effects.

To avoid quantization patterns, that last bit can be "dithered", which means it's intentionally randomized.

## Bitrate

Combined together, the sampling rate and sampling depth create a "bitrate", measured as a flow of bits per second. Phone calls translate anywhere between 24 and 88 [kilobits per second](/memory/), depending on how it's getting [packaged and sent](/protocols/).

Music in MP3 or AAC format often come as low as 128 kbps or as high as 320 kbps. The way they keep the memory low while providing a high-quality music experience is by [mathematically](/algorithms/) stripping away components of the audio that our ears won't hear due to biological limitations.

Calculating memory or bandwidth use from this point is as simple as using a calculator, bearing in mind that kilobytes are 8 times more than kilobits.

## Channels

It's worth noting how many independently captured information streams, or "channels" that audio is encoded to use. Stereophonic sound gives a channel for each speaker, while surround sound can have upwards of 5 or 7 speakers.

Speakers are also configured for various audio ranges. Woofers are on the low end of the audio spectrum (with subwoofers at the lowest) and tweeters are on the high end.

A subwoofer is an affordable way to add higher-quality sound to the audio. By adding a low-bass loudspeaker, the audio feels louder and more impactful.

In typical home stereo systems, the number of channels is represented as [speakers].[subwoofers]. So, two speakers and a subwoofer is a 2.1 speaker system. It becomes "surround sound" when it comes from in front and behind.

While most people will do fine with a 2.1 speaker system, the audio quality can be enhanced upward:

- 3.1 - left, center, right, subwoofer
- 5.1 - left, center, right, left rear, right rear
- 7.1 - left, center, right, left rear, right rear, left mid, right mid
- 7.1.2 - 7.1, but with two aimed at the ceiling
- It can go as far as 9.1, 10.2, 13.1, and more

The quality of the played sound, however, is almost hard-limited by the quality of the original recording. While some [algorithms](/algorithms/) *can* improve the sound experience, true audiophiles are divided between the highest-possible-quality recording (e.g., remastered songs) or most accurate recording (e.g., vinyl records) for the most complete listening experience.

For a legitimately advanced experience, the audio must reflect the precise *location* of where the sound should be. Most [modern games](/game-dev/) and [VR experiences](/vr/) use "binaural processing" to reproduce the relative location of a sound source, which updates as the user changes their direction or distance from the object.

## File format

An audio clip in its purest form is a stream of raw data. Compressor/decompressors ("codecs") permit storing that ifnormation without as much memory.

There are a variety of encoding formats. The format is the abstraction (and is an [open standard](/protocols/), while the specification is an implementation (which is often [proprietary](/floss/)).

Audio recordings have different use cases, and the "lossiness" of the information determines how compressed (and therefore how small) an audio [file](/files/) can be:

- Non-compressed: this takes up a *lot* of space, but is the best quality and doesn't need a sampling rate
  - Mostly stored as FFmpeg, but is usually stored in container formats like WAV, FLAC, AIFF, and AU
- Lossless: using encryption, but only in a way that it fully restores back to its original
  - FLAC, ALAC, APE, and a variety of other proprietary encoding formats
- Lossy: Uses a discrete cosine transform
  - Many to choose from, with MP3 as the most popular format

This isn't exclusive to audio, and many audio formats also combine [video](/screen/) information as well, and often in parallel.

The [drivers](/os/) for managing audio are very difficult to work with. The only people qualified to even *explore* the concept need a healthy intermediate-level working knowledge of [C++](/langs/) alongside quite a bit of [networking](/networks/) experience.

Another unique standard allows musicians to directly input information via musical instrument digital interface (MIDI), which sends the inputs from a musical instrument (e.g., synthesizer keyboard) to a very time-sensitive mapping. This allows the information to send various outputs, including [storage for later](/memory/). By using "MIDI voices", the audio can output as whatever the [creator](https://gainedin.site/creativity/) wants.

## Cabling

Most speaker cables are color-coded and single-channel, *especially* for high-end audio production. However, most modern computer cables designed for everyday consumer use (like the ubiquitous 3.5 mm cable) have more than one channel built into them. In the case of the 3.5 mm cable specifically, the number of channels is represented by the number of colored bands on the plug itself.

It's worth noting electrical signals from wires traveling across a distance *can* create signal disruptions with neighboring wires. This won't matter for any consumer-grade needs, but merging channels with a cable splitter can create issues for a high-end audio output (e.g., a concert).

## Post-production

Most audio software includes filters that add or remove elements.

The most common filter is an equalizer, which boosts or diminishes specified ranges:

- 20-60 Hz - sub-bass and kick drums
- 60-200 Hz - bass and lower drums
- 200-600 Hz - lower-range standard instruments (e.g., low range of guitars, left side of piano)
- 600-3k Hz - mid-range frequencies, which include most instruments and vocals
- 3-8 kHz - upper mid-range frequencies (e.g., high range of guitars, violins), can be annoying if not performed or mixed well
- >8 kHz - most trebles, not popular to maximize because many people (especially the elderly) can't hear at that sound

It's worth noting that the protocols for modifying [video](/graphics/) are effectively working alongside sound. Or, to put another way, a sound file is simply a video file minus the streaming video data. This simplicity streamlines a media player's ability to process it.

One of the most powerful software programs for converting *both* audio and video is FFmpeg, which stands for Fast-Forward-Moving-Picture-Experts-Group. It has the power to trim, cut, convert, adapt color, overlay an image, crop it, add more audio tracks, change the volume, add audio effects, and export to a wide variety of *both* audio and video file formats. It has been a corporate standard for a long time, is continuously updated, and is [open-source](/floss/), so it may live forever.

Most equalizers include presets for specific frequencies, though they can be manually configured:

- Acoustic - boost lower (drums and bass) and mid/mid-high (vocals, instruments)
- Electronic - boost lower (drums and bass) mid (synthesizer) and high (digital arpeggios)
- Latin American - boost lower (drums) and high (Latin American instruments)
- Piano and classical - lower high-range (to emphasize the mid-range instruments)
- Pop - boost mid-range (vocals)
- Rock - boost low-range (drums and bass) and high-range (guitar arpeggios)

One of the most frequent tools to work with (and create) recorded sound is a "Digital Audio Workstation" (DAW). It borrows heavily from [IDEs](/ide/), with an extensible "Virtual Studio Technology" (VST) plugin standard that works somewhat independently of the workstation software itself. To that end, there are *thousands* of VSTs available, for a wide variety of purposes, and any new DAW can use most of them.

* * * * *

## Additional reading

[Learn Modern C++ by Building an Audio Plugin (w/ JUCE Framework)](https://www.youtube.com/watch?v=i_Iq4_Kd7Rc)

[FFmpeg - Ultimate Guide](https://img.ly/blog/ultimate-guide-to-ffmpeg/)
