# Media Elements

width------Sets the element's width in pixels.
height-----Sets the element's height in pixels.
<source>------ Deﬁnes resources of the audio or video ﬁles
track -------Deﬁnes the text track for media elements
controls-------- Displays controls
autoplay------ Automatically start playing the media
loop -----------Plays the media in a repeated cycle
muted --------Plays the media without sound
poster --------Assigns an image to display until a video is loaded

## Audio

HTML5 provides a new standard for embedding an audio ﬁle on a web page.
You can embed an audio ﬁle to a page using the <audio> element:

![image-20210630111829230](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630111829230.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <audio controls>
            <source src="file.mp3" type="audio/mpeg">
            Your browser does not support the audio element.
        </audio>
    </body>
</html>
```

## Video

You can embed also a video to a webpage using the <video> element:

![image-20210630112153504](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630112153504.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <video width="500" height="700" controls>
            <source src="video.mp4" type="video/mp4">
            Your browser does not support the video tag.
        </video>
    </body>
</html>
```

## Using `<video>` and `<audio>` element to display audio/video content

Use the HTML or <audio> element to embed video/audio content in a document. The video/audio element contains
one or more video/audio sources. To specify a source, use either the src attribute or the <source> element; the
browser will choose the most suitable one.
Audio tag example:

![image-20210630113344594](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630113344594.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <!-- Simple video example -->
        <video src="videoile.webm" autoplay poster="fav-icon.jpg">
            Sorry, your browser doesn't support embedded videos, but don't worry, you can 
            <a href="videofile.webm">fownload it</a> and watch it with your favorite video player!
        </video>

        <!-- Video with subtitles -->
        <video src="foo.webm">
            <track kind="subtitles" src="foo.en.vtt" srclang="en" label="English">
            <track kind="subtitles" src="foo.sv.vtt" srclang="sv" label="Svenska">
        </video>

        <!-- Simple video example -->
        <video width="480" controls poster="https://archive.org/download/WebmVp8Vorbis/webmvp8.gif">
            <source src="https://archive.org/download/WebmVp8Vorbis/webmvp8.webm" type="video/webm">
            <source src="https://archive.org/download/WebmVp8Vorbis/webmvp8_512kb.mp4" type="video/mp4">
            <source src="https://archive.org/download/WebmVp8Vorbis/webmvp8.ogv" type="video/ogg">
            Your browser doesn't support HTML5 video tag.
        </video>

    </body>
</html>
```

Audio tag example:

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
        </style>
    </head>
    <body>
        <!-- Simple audio playback -->
        <audio src="http://developer.mozilla.org/@api/deki/files/2926/=AudioTest_(1).ogg" autoplay>
            Your browser does not support the <code>audio<code> element.
        </audio>

        <!-- Audio playback with captions -->
        <audio src="foo.ogg">
            <track kind="captions" src="foo.en.vtt" srclang="en" label="English">
            <track kind="caption" src="foo.sv.vtt" srclang="sv" label="Svenska">
        </audio>
    </body>
</html>
```

## Video header or background

Adding a video that will autoplay on a loop and has no controls or sound. Perfect for a video header or background.

![image-20210630114916704](/home/aidyn/snap/typora/39/.config/Typora/typora-user-images/image-20210630114916704.png)

```html
<!DOCTYPE html>
<html lang = "en">
    <head>
        <meta charset="UTF-8">
        <title>HTML</title>
        <style>
            #videobg{
                background:url(shortcut.jpg);
                background-size: cover;
            }
        </style>
    </head>
    <body>
        <video width="1280" height="720" autoplay muted loop poster="video.jpg" id="videobg">
            <source src="video.mp4" type="video/mp4">
            <source src="video.webm" type="video/webm">
            <source src="video.ogg" type="video/ogg">
        </video>
    </body>
</html>
```

