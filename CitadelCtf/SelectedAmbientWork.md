# Descripton

The symphonic adventure does not end here. On the next floor, a single song keeps echoing through the floor, repeating in a haunting loop. Amid the sound, you find a note left by a past candidate. It hints that the song holds a secret message, hidden in plain sight, much like how Aphex Twin concealed his face within his music with the help of spectrograms.

To move forward, you must find the message hidden in this sound.

Note: Separate the words in the flag with _ and make it UPPERCASE. Example: citadel{S3L3CT3D_AMB13NT_W0RK}

## My solve
I used the tool https://morsecode.world, because I noticed morse code started playing a few seconds into the given `.wav` file that was given, there I uploaded the audio file, n opening the audio and viewing its spectrogram the flag format citadel{ is visible at the 1:00 mark and the closing } at 1:12. This indicates the flag is the Morse code in between these timestamps.

The spectrogram gives a clear view of the flag now which is `.----   .-.. ----- ...- ...--   .---- -.. --`,

Then converted that to readable text using that tool only which came out to be `1 L0V3 1DM`, rest of the morse code wasn't really important.


## Flag 

`citadel{1_L0V3_1DM}`
