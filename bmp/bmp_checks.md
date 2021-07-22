# Bitmap file checks(B-BMP)

## BMP Header(B-BMP-H)

### B-BMP-H-1
Check that file size is at minmum of 14 bytes.

### B-BMP-H-2
Check that magic number is one of the followings:
* BM
* BA
* CI
* CP
* IC
* PT

### B-BMP-H-3
Check that the size of the BMP file in bytes is the same as the files.

### B-BMP-H-4
Check that Reserved bytes in the headers equels 0.

_*TODO : Must check if it always right*_


### B-BMP-H-5
Check that the file is longer than a given offset.

## Dib header check (B-BMP-D)

### B-BMP-D-1
Check that there is at least enough length in file to have DIB header size.

### B-BMP-D-2
Check that DIB header size is one of the following:
* BITMAPCOREHEADER - 12 bytes
* BITMAPCOREHEADER2 - 64 bytes
* OS22XBITMAPHEADER - 16 bytes
* BITMAPINFOHEADER - 40 bytes
* BITMAPV2INFOHEADER - 52 bytes
* BITMAPV3INFOHEADER - 56 bytes
* BITMAPV4HEADER - 108 bytes
* BITMAPV5HEADER - 124 bytes

### B-BMP-D-3
Check that file has at least size of bitmap header and dib header size.

### B-BMP-D-4
Check that the given offset in bitmap header start after the dib header right by the given formula:
```
OFFSET_IN_HEADER = BITMAP_HEAEDER_SIZE(14) + DIB_HEADER_SIZE
```
_*TODO : Check if there is files with gap and color table*_

## BITMAPINFOHEADER header checks(B-BMP-I)

### B-BMP-I-1


