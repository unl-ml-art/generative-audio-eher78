# Project 2 Generative Audio - The Musical Turing Test

Abraham Schaecher, aschaecher2@huskers.unl.edu

## Abstract

<!-- Include your abstract here. This should be one paragraph clearly describing your concept, method, and results. This should tell us what architecture/approach you used. Also describe your creative goals, and whether you were successful in achieving them. Also could describe future directions. -->

For this project, I was fascinated with the relationship between generated works from a computer and human interpretation of a result. In particular, I 
was interested on the Turing Test developed by Alan Turing to determine whether or not a generated piece of audio can be familiar or even be recognizeable 
as regular human made works. This project will involve the use of 3 generated audio samples in the style of Classical Music and one human made music 
sample for evaluation. All the samples will be in piano composition with Midi files as a control output. The process will be to take individuals and 
judge each work by itself and selecting the one piece of audio that is an original musical composition. The sample selected will be compared to the other 
samples and a result will be acheieved in how close the generated samples are to a "human musical composition".


## Model/Data

<!-- Briefly describe the files that are included with your repository:
- trained models
- training data (or link to training data) -->
This classical musical data was collected on the MIDI Dataset for classical piano music titled [Classical Piano MIDI](http://www.piano-midi.de/).

The main task is not to get an entire sequence of a MIDI composition but rather a few sequences of MIDI
notes to generate a larger component of MIDI music. For this, I could not just edit a MIDI file in Adobe or any other audio editing software. Rather, 
I had to rely on a free online software titled [Online Sequencer](https://onlinesequencer.net/import). From there, I was able to alter the original MIDI
file to just a few sequences of notes suitable for MuseNet, the main generative music composition for testing.

[MuseNet](https://openai.com/blog/musenet/) is a deep nerual network that is able to generate musical compositions from an original sample of music. This
generative model is the right fit for my research as it is perfect for generating generative audio on a few sample notes and was able to compose classical
music in the style of that time period. For this, the model requires a sample from a MIDI file and with the steps taken before, I was able to gather the
necessary sources and sample data for generation.

The steps taken to generate a sequence of music from a sample music MIDI file is:
- Select Advanced Settings in the "Try MuseNet"
- Style of Composer as either "Mozart" or "Beethoven"
- Intro as a "Custom MIDI Upload"
- Instruments as "Piano"
- Number of Tokens as "400"
- Repeat if necessary after each generation

These steps can repeated for as many music samples you would like to produce. I had 3 generated music files ready to be experimented.

## Experimentation 

After gathering the generated musical compositions, I did a variation of the [Turing Test](https://en.wikipedia.org/wiki/Turing_test). 
In this case, for each participant, the process works like this:
- Each participant is given instruction on selecting the human made piano composition or most "humaan-made" piano composition.
- The participants are then directed to a survey that has access to **3 generated musical compositions** and **1 human-made composition**.
- All four musical compositions are listened with no emphasis on order or repeated listening. 
- The survey then asks to rank the musical compositions from most human-like to generated by a computer.
- There is also an optional comment box indicating what made them chose their rankings and overall thoughts on the musical compositions.

The hypothesis was that there would be at least some variation in the "closeness" between the generated musical composition and the actual human-made
coposition in terms of aesthetics and notation. 

From there, the results have been recorded and examined.

Survey is also available [here](https://forms.gle/jrnX3B5C1om7nkBM9).

## Results

<!-- Documentation of your results in an appropriate format, both links to files and a brief description of their contents:
- `.wav` files or `.mp4`
- `.midi` files
- musical scores
- ... some other form -->
#### Generated Music Results
You can listen to the following generated musical compositions from MuseNet. Remember, one of the four is made by a human. I won't go too much in detail as
listening to the results are self-explanatory but I will provide links to the results and the original source materials. (Be sure to download the results to listen!)

Generated Music Results:
- [Result 1](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/generatedMusicResults/MuseNetSample1.mp3)
- [Result 2](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/generatedMusicResults/MuseNetSample2.mp3)
- [Result 3](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/generatedMusicResults/MuseNetSample3.mp3)
- [Result 4](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/generatedMusicResults/MuseNetSample4.mp3)

Original Musical Files:
- [Original Source 1](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/originalMusic/Chopin_Nocturne_No_13_In_C_Minor_Op_48_No_1.mp3)
- [Original Source 2](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/originalMusic/Granados_danza_espan%CC%83ola_n_2_Oriental.mp3)
- [Original Source 3](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/originalMusic/%20Takemitsu-Litany.mp3)
- [Original Source 4](https://github.com/unl-ml-art/generative-audio-eher78/blob/master/originalMusic/Liszt-HungarianRhapsodyNo2.mp3)

#### Survey Results (aka the Musical Turing Test)

<img width="753" alt="Screen Shot 2022-03-26 at 6 06 23 PM" src="https://user-images.githubusercontent.com/78128630/160260000-66c27070-e3e9-41fa-9ab9-ad126589cebf.png">

In the results from the survey, there is an indication that Sample 3 (the human generated music) was easily identified as the most or first human-based
musical composition from the other music files. There is some indication that Sample 4 also got into the most human-like but I'll address that topic in
the next section.

Resides that, there is clear indication that the is some variance in the generated samples between 2nd, 3rd, and 4th in terms of most felt like composed by a human. These generated samples (Sample 1, Sample 2, Sample 4) are not as easily identifiable in ranking after selecting the human sample first.

The average position for each sample is the following:
- Sample 1 = 2.33
- Sample 2 = 3.00
- Sample 3 = 2.00
- Sample 4 = 2.66


#### Observations, Caution, and Reflections from Results
As mentioned before, the results are self-explanatory as the participants were mostly able to identify the human-made musical composition from the given
samples. In fact, I would argue that the results were close in that the participants did comment on how the notes and feeling of the music was similar to
other classical piano music. The main thing that the participants identified was the volume. Both in general and in the music. 

One of the main things going back at the results was how I identified an error in the original sound sample in regards to the volume as it was very clear
that I used the wrong sound format for the sample. As such, the original error in that sound sample carried on to the MuseNet and hence there was a 
difference that was clear when comparing the other generated results. 

Also things to consider from the survey results:
- I was unable to gather a relevant sample size of participants to the survey so I mostly relied on close friends and family to help me out.
- The few participants and results also meant that I had to scale back on some of the statistics due to less data.
- A participant also mentioned that one of the instructions was unclear so the results may also impact on that as well.

Considering all of these things, it is important to take the overall results with a grain of salt. However, I do believe I accomplish the main tasks of
creating generative music and the creating an initial task of human-based survey on those results. I did provide links of the generative music from 
MuseNet and was also able to provide some proper feedback not just the results but also on the survey.

I could see this project being pushed further in a way to capture a certain style of music whether it would be classical, jazz, rock, abstract, or any 
other genre that could be listenable. As you listen to the results, the generative musical composition does provide a glimpse of how similar or the 
capture of the musical notes into a somewhat recognizable sequence. The conversion of initial music samples to generative audio tracks is a long process
that requires the use of different tools but I think with new technology and resoruces, the step-by-step process from audio track to audio track can be a
lot more managable. 

Finally, I had a lot of fun researching this topic despite all of the challenges and errors that were in my way whether it was from technical errors to 
just selecting the right music for conversion. As a person who has some musical background, I enjoy listening to both classical music and the generative results just from an aesthtic view because of the variety and the dynamics associated with the audio. Perhaps this could be a glimpse into the potential of "AI Musicians"...

Concluding Statement: Are the generative musical compositions so familar that it could be made by a human? No. Are we close? Yes. 

## Technical Notes

<!-- Any implementation details or notes we need to repeat your work. 
- Does this code require other pip packages, software, etc?
- Does it run on some other (non-datahub) platform? (CoLab, etc.) -->
- There is not really a lot of external resources or computation hardware for this project.
- [MuseNet](https://openai.com/blog/musenet/) by itself can produce generative musical compositions from a prompt but if you want to go the extra mile, find a MIDI music library such as [Classical Piano MIDI](http://www.piano-midi.de/) and it should be fine.

## Reference

<!-- References to any papers, techniques, repositories you used:
- Papers
- Repositories
- Blog posts -->
- [Classical Piano MIDI](http://www.piano-midi.de/)
- [MuseNet](https://openai.com/blog/musenet/)
- [Online Sequencer](https://onlinesequencer.net/import)
- [Turing Test](https://en.wikipedia.org/wiki/Turing_test)
