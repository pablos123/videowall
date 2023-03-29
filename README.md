Minimalistic program to set a video as wallpaper.

This program supports one video wallpaper at a time.

The supported videos depends on the version of ffmpeg that you have.

## Dependencies
```terminal
sudo apt install ffmpeg hsetroot
```

Tested on linux Mint 21

## Install
```terminal
mkdir -p "$HOME/.local/bin/" && rm -f "$HOME/.local/bin/videowall" && wget 'https://raw.githubusercontent.com/pablos123/videowall/main/videowall' -P "$HOME/.local/bin/" && chmod +x "$HOME/.local/bin/videowall"
```
This will create a file in `$HOME/.local/bin/` named `videowall`

If `videowall` is not available after you run the command above you don't have `$HOME/.local/bin/` in your `$PATH`.

Maybe that's because you didn't have the directory before running the command.
In general `.profile` will load that directory if exists as part of your `$PATH`, so the next time you login or `source` `.profile` you'll have `videowall` available.

## Run
Prepare a video, this will set the video as wallpaper too. (You can specified a time limit)
```
videowall -p <video> [ -l <time_in_seconds> ]
```

Quit videowall.
```
videowall -q
```

Set the prepared video, you don't need to prepare the video again!
```
videowall
```
