# Zulu
## Challenge Statement:
Author: @JohnHammond

Did you know that zulu is part of the phonetic alphabet?

Attachment: [zulu](zulu)

## Solution:
Downloading the file and running file utility on it revealed that it is compressed data.

![file output](assets/1.png)

Now I didn't really look into the extact compression tool used because I use the [p7zip](https://github.com/p7zip-project/p7zip) utility. This can decompress any archive regardless of compression algorithm(generally used compression algorithms). So I decompressed the data with:

```bash
7z x zulu
```

![Uncompressing](assets/2.png)

![listing files](assets/3.png)

On opening the new uncompressed file, I found the flag.

![flag](assets/4.png)


