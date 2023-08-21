# dell-qt-speaker-simulator
Small QT Speaker Test simulation web app for Maia's live hands-on 


## ffmpeg Commands for Audio Editing
Documentation: https://ffmpeg.org/ffmpeg.html

### Cut audio file to a specific duration
**-ss** : Start point\
**-to**: End point

*Template*\
`
$ ffmpeg -i input.extension -ss 00:00:xx -to 00:00:yy -c copy output.extension 
`

*Example*: cut file to keep between seconds 2 and 3 only\
`
$ ffmpeg -i one.wav -ss 00:00:02 -to 00:00:03 -c copy one_cut.wav 
`

### Volume control 
(https://trac.ffmpeg.org/wiki/AudioVolume)

**volume** : Accepts decimal; It's the multiplication factor that will be applied to current volume
- ex: 1.5 = 150%, 0.5 = 50%, 40 = 40x

*Template*/
`
$ ffmpeg -i input.extension -filter:a "volume=20" output.extension
`

*Exemplo*: Raise the volume by 10 times\
` 
$ ffmpeg -i um_cut.wav -filter:a "volume=10" um_cut_vol.wav
`