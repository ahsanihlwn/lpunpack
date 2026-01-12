This project is a fork of lpunpack by unix3dgforce.
Modified by ahsanihlwn.

Original project:
https://github.com/unix3dgforce/lpunpack

# lpunpack

##### lpunpack.py - command-line tool for extracting partition images from super images

    Usage:
    lpunpack.py [-h] [-p NAME] [-S NUM] [--type] [--unsparse] SUPER_IMAGE OUTPUT_DIR

##### Positional arguments:
    SUPER_IMAGE  
        Path to the super image file.

    OUTPUT_DIR  
        Output directory for extracted partitions.

##### Optional arguments:
    -h, --help  
        Show this help message and exit.

    -p NAME, --partition NAME  
        Extract the named partition. Can be specified multiple times or using delimiters ["," ":"].

    -S NUM, --slot NUM  
        Slot number (default is 0).  
        !!! No implementation yet !!!

    --info, --no-info  
        Display pretty-printed partition metadata (default: False).

    -f {text,json}, --format {text,json}  
        Choose output format for info display.

##### Notes:
- Extracting A/B slot index is not implemented yet.

---

## Tips

### Check super image type
    To quickly detect the super image type without extracting:
    lpunpack SUPER_IMAGE --type

### Convert super image to unsparse format
    To unsparse the super image before extraction:
    lpunpack SUPER_IMAGE OUT_DIR --unsparse

This is useful if the super image is sparse and you want a raw image layout before processing.

