Minimalistic program to set a video as wallpaper. 🦥

## Dependencies
- [hsetroot >= 1.02](https://github.com/himdel/hsetroot)
- [ffmpeg >= 4.2.3](https://ffmpeg.org/)

Ubuntu/Debian based:
```
sudo apt install ffmpeg hsetroot
```

## Install
```
mkdir -p "$HOME/.local/bin/" && rm -f "$HOME/.local/bin/videowall" && wget 'https://raw.githubusercontent.com/pablos123/videowall/main/videowall' -P "$HOME/.local/bin/" && chmod +x "$HOME/.local/bin/videowall"
```

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

## Demo
https://user-images.githubusercontent.com/52180403/231311767-bf23cd94-8715-43f9-8336-6b4fbc6b5614.mp4

## Troubleshooting

If `videowall` is not available after you run the install command you don't have `$HOME/.local/bin/` in your `$PATH`.

Maybe that's because you didn't have the directory before running the command.
In general `~/.profile` will load that directory if exists as part of your `$PATH`, so the next time you login or `source` `~/.profile` you'll have `videowall` available.

Others:

- The supported video formats depends on the version of `ffmpeg` that you have.

- Things can break depending on the version of `bash` and related programs used.

- Longer the video longer will take the program to prepare it.

- This program supports one video wallpaper at a time.

## More info

**Uninstall**: `rm -f "$HOME/.local/bin/videowall"`


The idea comes from https://github.com/terroo/wallset but:
- I wanted a less bloated program without the extra functionalities.
- I didn't like the 10 second limit.
- I use hsetroot for setting my wallpapers so I wanted to use it here too.

Thank you for the inspiration!

Tested on Linux Mint 21.1
