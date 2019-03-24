# Video stabilization script

A simple python script to stabilize input video using FFmpeg and the vid.stab library.
The handling of the transform data is unnecessarily complicated on purpose - it's set so that it doesn't create additional files.
For this the output of the first pass-through is pushed to stdout, which is then piped into a variable. The variable is then written into a NamedTemporaryFile, which is destroyed on closing.

Video examples can be found [here.](https://www.youtube.com/watch?v=dWIE0YR4D2s&list=PL4QY2nHP-DXifsl_13CHqxgvCZFuUGKlt)
