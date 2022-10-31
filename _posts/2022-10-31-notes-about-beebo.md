---
layout: post
title:  "Notes about the Polyeffects Beebo"
date:   2022-10-31 20:10:00 +0100
---

# Notes on the Polyeffects Beebo

The [Polyeffects Beebo](https://www.polyeffects.com/) is many things:
- a multi effects box for synthesizers
- an amp simulation and effects pedal for guitar and bass
- a polyphonic synthesizer
- a modular synthesizer in a box
- a loop station

One thing it is not:
- well documented

(Bild)

That's why I write down here what I found out about the dozens(?) of modules. May it be of use for future me and for other Beebo/Hector users. Keep in
mind, however, that I am not at all competent in what I do here. I won't reveal the inner workings of the ORG Reverb module for the simple reason that
I have no more than the most basic knowledge about effect units. I am also very ignorant about modular systems, so I will probably use some vocabulary
in a wrong way. Anyway, let's start.

## General remarks
There are 4 different types of signals which can be routed between input, output and the individual modules:
- Audio
- CV
- Midi
- Tempo

The CV signals serve a lot of different purposes: they can activate a module, set a parameter of a module, define the amplitude of a sound over
time (i.e. the envelope) and other things. So it makes sense to further divide the CV signals into subtypes:
- Trigger (Bild)
    - a signal at level 0 most of the time with a very short spike to 5 and back
- Gate (Bild)
    - a signal at level 0 with a sudden flank up to 5 and back zo 0 after some time
- Envelope (Bild)
- Pitch
    - a signal at level 0 usually represents the middle C (C4) 1V is C5, 2V is C6, -1V is C3 etc.
- Settings of modules
    - in most of the modules, some of the settings can be controlled not only by manually slide the sliders but also using a signal. It seems that the
      range is always 0V to 5V (for monomodal settings) or -5V to 5V (for bimodal settings), no matter which range is displayed at the slider. For
      example: if a slider has a displayed range from 0 to 1 (the most frequent case), feed in a value of 4V to set it to a value of 0.8. BTW, keep in
      mind that when a slider is controlled by an CvSettings input, the displayed value of the slider is ignored. It is not visible if a slider is
      currently externally controlled.
- other (Bild, wo es auch über 5 und unter 0 geht)

This distinction is only a locigal distinction, not a technical one. Nobody stops you from feeding the triggers coming from the foot pedal module into
the cv/oct-input of the MSC-Osc module, even though it doesn't make any sense. In my description of the modules, I'm going to note which type of CV
signal is meant to be used, but feel free to missachten it. Maybe you come up with some cool stuff.

A note about the 5: throughout the modules, the CV level 0 is used as some kind of "zero effect", 5 as "maximum effect" and, if applicable, -5 as the
maximum effect, but inverted. Verwirrenderweise, the settings inside the modules normally have the range 0–1 (or -1–+1). That's why there is sometimes
a factor of 5 which crops up in my descriptions of the modules.

Also, a word about MIDI: if you have trouble connecting other gear to the Beebo via Midi, keep in mind that there are two kinds of MIDI TRS stecker,
which are indistinguishable visually. They are originellerweise called type A and type B. Different batches of the Beebo require different types of
these Sterckers. Witzigerweise, my box wants type A for input and type B for output. Yay.
According to the [FAQ](https://www.polyeffects.com/faqs), the following types are used (you can find the serial number on the sticker on the back of the Beebo):
- Pink case with serial number ≤ 474 or blue case with serial number ≤ 337: type B for in and out
- Pink case with serial number 475–876 or blue case with serial number 338–936: type A for input, type B for output
- Pink case with serial number ≥ 877 or blue case with serial number ≥ 937: type A for in and out

## The modules
### Audio effects

