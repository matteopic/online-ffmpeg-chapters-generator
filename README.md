FFmpeg Chapter Generator
========================

A lightweight, web-based utility designed to simplify the creation of metadata files for FFmpeg.
This tool converts a simple list of timestamps and titles into the structured FFMETADATA format required to add chapters to video and audio files.

[Use online for free](https://matteopic.github.io/online-ffmpeg-chapters-generator/)

## Features

* **Instant Conversion**: Automatically generates metadata as you type.
* **Timestamp Support**: Handles HH:MM:SS and MM:SS formats.
* **FFmpeg Ready**: Outputs standard-compliant [CHAPTER] blocks with nanosecond precision (Timebase 1/1000000000).
* **Flexible Endings**: Automatically calculates chapter duration based on the next entry, leaving the END tag empty for the final chapter to ensure compatibility.
* **Easy Export**: One-click "Copy to Clipboard" and "Download .txt" functionality.

## How to Use

* Paste your chapters in the input area using the format: 00:00:00 Title.
* Copy the generated output.
* Run the following command in your terminal/PowerShell to apply the metadata:
```
ffmpeg -i input.mp4 -i FFMETADATA.txt -map_metadata 1 -codec copy output.m4b
```
