
ffmpeg -i babies.mp4 -vf scale=-2:384 -crf 28 -y babies384.mp4
for i in *.mp4; do ffmpeg -i "$i" -vf scale=384:-2 -crf 28 -y `basename "$i" .mp4`384.mp4 ; done

scp -r ~/of/apps/Sites/moviePlayer/bin/data/videosSmall pi@pi3gl.local:~/of/apps/Sites/moviePlayer/bin/data

./gifenc.sh movie.mp4 output.gif
http://blog.pkh.me/p/21-high-quality-gif-with-ffmpeg.html

