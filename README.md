# Cisco IOU License Generator

A small Python script that generates a Cisco IOU license entry based on the
local host id and hostname.

## Requirements

- Python 3
- Linux or any system with the `hostid` command (a fallback is used if missing)

## Usage

    chmod +x iou_keygen.py
    ./iou_keygen.py

The script prints the license line and writes it to `iourc.txt` in the
current directory.

Example output:

    [license]
    myhost = 1234567890abcdef;

## Installing the license

Copy the generated line into `~/.iourc`:

    cp iourc.txt ~/.iourc

Or append it manually:

    cat iourc.txt >> ~/.iourc


## Files

- `iou_keygen.py` - the generator script
- `iourc.txt` - generated license file (not tracked in git)

## License

Use at your own risk. This script is provided for educational purposes.
Ensure you have the right to use Cisco IOU software in your environment.
