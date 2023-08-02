---
title: Hidden Mineral World
tags: music
---

_written in the middle of making this_

<a class="external-link" href="https://open.spotify.com/album/33RZuDk2Ov47TVWEGgEGQ2?si=KvgLf1gxSLekgBTlrmf-2w">Spotify Link</a>

### Intro

Hidden Mineral World EP (or HMW for short) started out as a challenge from my friend. He generated this:
<img src="/assets/hmw.png"/>
using StableDiffusion and  I jokingly said I will do a dark techno/glitch EP for that.

==and the game was on==

### First try

I started dabbling in Ableton Live but with no real progress. After some short loops I kinda forgot about this.

### Second try

As I saw the cover again, I decided to give it another go. This time I used ChatGPT4 to write the song structure, bpm and track titles. It came up with
1. Subterranean Frequency
2. Crystal Resonance
3. Geode Rift
4. Iron Vein

I also got BPMs and tracks structures, but, having more draw into Ambient stuff it, again, got forgotten

### Third try

Third's time the charm, right?

I may have neglected this, but this EP kept coming back to my mind, so I decided to give it a final try, this time with extra challenge - I will work on it for 15min daily. No more, no less. I open up Ableton Live, start the timer and save&quit when timer gets off.

And, surprisingly, this works. Works so well, that I have force myself to stop.

As of the time of writing this I have a premix versions of tracks 1 & 2 and track 3 is in progress.

#### Subterranean Frequency

This is what I got from ChatGPT4

```
BPM: 125

- 0:00-1:15: Opening with a pulsating sub-bass drone, the sound of distant drilling emerges to introduce the thematic elements of the track.
- 1:15-2:30: The sub-bass transforms into a steady, dark techno beat as the percussion intensifies. Metallic glitches layer over the rhythm.
- 2:30-4:00: A breakdown in the middle introduces distorted synth elements, building tension.
- 4:00-5:00: The track closes by revisiting the initial rhythm, while the drilling and glitches fade, leaving only the deep echoes of the bass.
```

I started with marking the timestamps (which I had to move a bit to align with bars) and named locators after the defined structure. This helped me a lot, as I exactly saw how long each section is, what it is and what comes after another. I also added "end" locator to have a clear indication where the track ends.

It was a nice challenge, I used some CC0 industrial samples (drills, pickaxes, stones etc), learned a lot about wavetable. Used some more samples for glitchy beats above kicks, needed to use parallel compression to make it work properly.

This was the first one, I think the quickest one.
Going on for 15 minutes and with set structure was a bit of a challenge, but did help greatly move forward. If you have only 15 min to do work, you make every second count.


#### Crystal Resonance

This is what I got from ChatGPT4

```
BPM: 132

- 0:00-1:00: Introduction with ethereal pads, a soft, minimalistic drum beat enters to set the tempo.
- 1:00-2:15: Glitchy beats are layered over the pads, the tempo increases. Synths mimic the sound of crystals resonating.
- 2:15-3:30: The final section features a crescendo of resonant sounds, ending with a series of glitchy echoes that fade out to silence.
```

Again, I started with location markers, and, again, I had to adjust them to align with the beat. Here I added extra one for "echoes" before "end" - to show the time of the echoes to decay.

Another dive into wavetable. A lot of youtube diving into understanding this tool more definitely helped. 

I tried to make "glass needles" sound for `crystal resonance` here and I actually decided to use a MIDI drum clips from Ableton's packs. I did eventually change them a bit, partially to maintain `techno` feel.
Here I had a huge clash of frequencies and had to use a lot of parallel compression to make it sound good. It's actually even better than I've wanted and had an extreme case study of clashing instruments.


#### Geode Rift

This is what I got from ChatGPT4
```
BPM: 128

- 0:00-1:00: A heavy bassline starts the track, suggesting the outer shell of the geode.
- 1:00-2:15: The track 'cracks open' with sparkling arpeggios and expansive synths, replicating the awe of discovering the geode's interior.
- 2:15-3:45: Techno beats enter, increasing in intensity to represent the geode's harsh formation environment.
- 3:45-4:30: The music reduces to a soft, twinkling outro, mirroring the closing of the geode and leaving the listener with a sense of intrigue.
```

This one is still in progress, so this entry may actually start being interesting.

As usual, I started with location markers. 

Then I used operator -> noise with some processing (EQ, filters, erosions etc) to create cracking noise to simulate "cracking open". LFO helped give it some rhythm.

Quick heavy bassline in wavetable, quick synth arpeggios and some beats.

Challenge here was that it was the most melodic track yet. I started with some scale to help me - continued to use that for other stuff, but I knew it was not working.

Actually after initial bass I went into designing fading outro, with automated autofilter and freeze from reverb.

I actually broke from the scale suggestions and went with what sounds cool to me (and arpeggiated). Grouping wavetable with second, more plucky one, did help to get more pleasing sound as well.

I changed previous midi clips to new melody and added new synth for a bass line for the "cracking open" part, that will stay with the song till the end.
Initial bass is automated to get to `-inf dB` slowly over the course of the second part.

I though that I need some pads, so I whipped out wavetable to create something lush. I duplicated the track, froze two chords (first one from pattern and very last one), reversed audio clips and used them as smooth transition. It works especially well if you have reverse audio going into the synth when there's a transition between parts. It makes it all glue together, and sounds really well.

After rendering and listening to it, I may go back to it and add something in first part, as, right now, it's a bit boring.

#### Iron Vein

This is what I got from ChatGPT4
```
BPM: 130

- 0:00-0:45: A steady, driving beat starts, metallic synths layer over to build tension.
- 0:45-2:00: The intensity increases, bringing the raw energy of iron extraction to life.
- 2:00-3:30: The track breaks down into a quieter passage, with softer sounds representing the depleting vein.
- 3:30-4:15: A somber, atmospheric outro, symbolizing the aftermath of extraction.
```

I spent first session, trying to make synths that are `metallic enough`. I decided to switch things a bit, and went with Ashlight from NI for some dark pad paired with quiet `metallic` operator with some echo.
Turns out that first part is divisible by 6, not 4 (given the length of patterns I created), so this makes things a bit more interesting.
Afterwards I added a standard 808 kick that slowly appears. Synth has parallel compression to make that kick stand out, but this time I did 50% wet (instead of 100%), and, I must say, it sounds great.

I managed to create simple hihat pattern and got `time outed` when trying to find next percussive sounds.

While playing around with `bongo` sound I managed to create great accents using sparse two hits at a same time (with some reverb on some of the hits) and found great rhythmic pattern with second preset. I actually made it quicker to test some effects and realised that it sounds great as a background sound, so I kept it there.

I stole the idea of "arpeggiating" 5 notes to create rhythmic variety - put a long 5 note MIDI with arpeggio on operator bell sounds. To enforce the melody, in third section of a song I used the same notes, just slower, going up with first note as a pedal note. I just found a nice Vital preset that fit the mood. Moving it around a bit made "progression" that was supported with sustained bass. 

As LLM suggested track slowly fading away I started getting more sparse with bongos (to the point it was removed), slowly removing layers. Track ends with reverb tail from bass and Vital.

#### Final touches

I went around the tracks and did some small fixes here and there. Also I mixed it quickly (limiter on master maybe is not advanced technique but did the job) and added a little, barely audible, heavy processed sample in Geode Rift. Afterwards I uploaded it to streaming services. And now only thing left is to wait for it to be processed.

### Random thoughts 

- As said many times, both image and text generative AIs give "raw material" rather than finished product. Cover was worked on in PhotoShop after it was generated. I did interpret the song structure in my own way.
- OTOH, not having a blank page to start with is a great help. While here it's way more constraining that I would use for something else, LLMs can be great for ideation and getting some concrete starting points.
- I still deviated from some of the suggestions after banging my head against the wall, but, many of those were helpful, or made me try out and learn new things
