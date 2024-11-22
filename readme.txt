How to download youtube video/playlist with subtitles via python(yt_dlp)

Requirements:
python3 (3.8.10 prefered)
yt_dlp
ffmpeg
chrome & gett coockies
================================================================
Installation Instructions:

1. check python
python3 --version

2. install yt_dlp on mac
sudo curl -L https://github.com/yt-dlp/yt-dlp/releases/latest/download/yt-dlp -o /usr/local/bin/yt-dlp
sudo chmod a+rx /usr/local/bin/yt-dlp

3. download ffmpeg (https://www.ffmpeg.org/download.html)

4. add get coockies extension to chrome browser (https://chromewebstore.google.com/detail/get-cookiestxt-locally/cclelndahbckbenkjhflpdbgdldlbecc?hl=en)
================================================================
Examples

1. Dowload video/playlist with subtitle
yt-dlp "https://www.youtube.com/playlist?list=PLZHQObOWTQDNU6R1_67000Dx_ZCJB-3pi"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies (2).txt"\
    -o "/Users/meysam/Downloads/youtube/%(title)s_%(ext)s.mp4"\
    --ffmpeg-location "/Users/meysam/Documents/binary"\
    --no-keep-fragments\
    --write-subs --embed-subs\
    -f 'bv*[ext=mp4][height>480]+ba' 


    --write-auto-subs --embed-subs\
yt-dlp "https://www.youtube.com/watch?v=L4qQdWrrUj8"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies (1).txt"\
    -o "/Users/meysam/Downloads/youtube/%(title)s_%(ext)s.mp4"\
    --ffmpeg-location "/Users/meysam/Documents/binary"\
    --no-keep-fragments\
    -f 'bv*[ext=mp4][height>720]+ba' 


yt-dlp "https://www.youtube.com/watch?v=MNw9x53Ybos&t=27s"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies (4).txt"\
    --list-subs    

2. Dowload the section of video
yt-dlp "https://www.youtube.com/watch?v=MNw9x53Ybos&t=27s"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies (10).txt"\
    -o "/Users/meysam/Downloads/youtube/%(title)s_%(ext)s.mp4"\
    --ffmpeg-location "/Users/meysam/Documents/binary"\
    --no-keep-fragments\
    --write-subs --embed-subs\
    --download-sections "*2:00-3:00" --force-keyframes-at-cuts\
    -f 'bv*[ext=mp4][height>480]+ba'


    yt-dlp "https://www.youtube.com/watch?v=MNw9x53Ybos&t=27s"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies (10).txt"\
    -o "/Users/meysam/Downloads/youtube/%(title)s_%(ext)s.mp4"\
    --ffmpeg-location "/Users/meysam/Documents/binary"\
    --no-keep-fragments\
    --download-sections "*2:00-3:00" --force-keyframes-at-cuts\
    -f 'bv*[ext=mp4][height>480]+ba'
    


2. Dowload music
yt-dlp "https://www.youtube.com/watch?v=5-J1t0rAlOU"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies.txt"\
    -o "/Users/meysam/Downloads/youtube/%(title)s_%(ext)s.mp3"\
    --no-keep-fragments\
    -f 'ba'

https://www.youtube.com/watch?v=d023ag6ELfc
www.youtube.com_cookies (1)

yt-dlp "https://www.youtube.com/watch?v=5S1z6NOe4Lk"\
    --cookies "/Users/meysam/Downloads/www.youtube.com_cookies (1).txt"\
    -o "/Users/meysam/Downloads/youtube/%(title)s_%(ext)s.srt"\
    --skip-download\
    --write-auto-subs



    
         



