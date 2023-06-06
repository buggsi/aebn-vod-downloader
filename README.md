# Download from AEBN for *FREE*

### This Python script allows you to download full movies from aebn.com without even having an account, all you need is a URL!
It works by parsing a preview playlist to get segment's urls, downloads them, and uses ffmpeg to mux video and audio.
Those preview playlist do not live for long, so if download fais, script will get a new one and try again.

It requires the following modules to be installed:

- lxml (https://pypi.org/project/lxml/)
- requests (https://pypi.org/project/requests/)
- ffmpeg-python (https://pypi.org/project/ffmpeg-python/)

## Usage

1. Install the required modules using pip:

```
pip install requests lxml ffmpeg-python
```
2. Run the script with the desired movie URL:
```
python aebn_dl.py --url https://*.aebn.com/*/movies/*
```

3. The script will download the movie and save it in the current working directory.

## Running the Script with Different Arguments

You can customize the behavior of the script by passing different arguments when running it. The available arguments are:

- `--url`: The URL of the movie to download (required)
- `--target-height`: The desired video resolution height (default: highest available)
- `--overwrite-existing-segments`: Set this flag to overwrite existing video segments if present (default: False)
- `--delete-segments-after-download`: Set this flag to delete segments after downloading (default: True)