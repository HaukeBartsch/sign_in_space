# sign_in_space

Sign in space decoding challenge

[A sign in space](https://asignin.space/decode-the-message/)


### A signal from the stars

The signal was created on earth (you know that means dirt yes?) and bounced back from a satellite. Received on Earth the first part of decoding the message produced a square binary image.

There is a header and a footer that are ignored here. There is also some binary coding at each 'pixel' that is ignored here. The resulting picture shows some clusters of dots. Some of the dots appear to be bigger (4x4) and show some pattern. The included notebook tries to analysis some of these pattern.

### Motiv analysis

The idea is to look at repeating arrangements of the 4x4 dots. Say that we find 2 dots that are relative to each other in some arrangement, for example, they are on-top of each other and 4 pixels appart. If this arrangement of 2 dots repeats in the image 5 times we might assume that is more than chance, that it is part of the message. Such an analysis for repeating arrangements with the largest number of points is done in the attached notebook [analysis.ipynb](https://github.com/HaukeBartsch/sign_in_space/blob/main/analysis.ipynb).

TODO: There are many overlapping (sharing points) pattern especially for low (2, 3, 4, ...) number of points.

We can filter out points using a random pattern normalization. For example, just by randomly placing dots into a square grid we might end up with some repeats given specific number of points. Calculating some statistics from random placements (monte carlo sampling) we can create a baseline frequency for motivs. If an arragement sticks out, if we see it more frequently than what would be expected from random placements we would highlight the finding.

TODO: The motivs with many points found multiple times are easy to visualize. But these motivs 'contain' smaller arragements of points that already repeat. How can we visualize these hierarchical repeats? How can we appreciate the totality of all repeats in the input space?
