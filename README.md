# mini_ctf

All tasks have level structure. You can not begin solving task3 if you haven't yet solved task2 from the same type of tasks.

*(mini ctf ITMO university just for 3 hours)*
STEGANO task1:

First of all, it was necessary to run binwalk:
binwalk 'task1.jpg' -e

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.01
41561         0xA259          Zip archive data, encrypted at least v1.0 to extract, compressed size: 32, uncompressed size: 20, name: first_flag.txt
41765         0xA325          End of Zip archive
41787         0xA33B          PNG image, 759 x 141, 8-bit/color RGB, non-interlaced

Binwalk could only pull out the zip archive, which turned out to be password-protected
But we see PNG signature there, try to extract by hands, and find image with password for archive, open archive.
![secreeeeeeeeyt](https://user-images.githubusercontent.com/35141662/48094539-7c2f2f80-e223-11e8-82d5-6fbdb4bacdc6.png)

FLAG: 1t_w4s_r34ll9_34zy!

