# sign_in_space

Sign in space decoding challenge

[A sign in space](https://asignin.space/decode-the-message/]


### A signal from the stars

The signal was created on earth (you know that means dirt yes?) and bounced back from a satellite. Received on Earth the first part of decoding the message produced a square binary image.

There is a header and a footer that are ignored here. There is also some binary coding at each 'pixel' that is ignored here. The resulting picture shows some clusters of dots. Some of the dots appear to be bigger (4x4) and show some pattern. The included notebook tries to analysis some of these pattern.

### Motiv analysis

The idea is to look at repeating arrangements of the 4x4 dots. Say that we find 2 dots that are relative to each other in some arrangement, for example, they are on-top of each other and 4 pixels appart. If this arrangement of 2 dots repeats in the image 5 times we might assume that is more than chance, that its a message. Such an analysis for repeating arrangements with the largest number of points is done in the attached notebook [analysis.ipynb](https://github.com/HaukeBartsch/sign_in_space/blob/main/analysis.ipynb).

TODO: This motiv analysis needs to be callibrated. For example just by randomly placing dots into a square grid we might end up with some repeats given specific number of points. Calculating some statistics from random placements we can create a baseline frequency for motivs. Only if an arragement sticks out, observed more than would be expected we can highlight the finding.

