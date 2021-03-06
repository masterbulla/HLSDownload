# HLSDownload [![Travis Status for Ejz/HLSDownload](https://travis-ci.org/Ejz/HLSDownload.svg?branch=master)](https://travis-ci.org/Ejz/HLSDownload)

Recursive HTTP Live Streaming Downloader!

### Install

Download and install the latest `hlsdownload.phar` (see [releases page](https://github.com/Ejz/HLSDownload/releases) for details):

```bash
$ wget "https://github.com/Ejz/HLSDownload/releases/download/v1.4.3/hlsdownload.phar"
$ chmod +x hlsdownload.phar
$ sudo mv hlsdownload.phar /usr/local/bin/hlsdownload
```

Test it:

```bash
$ hlsdownload "http://content.jwplatform.com/manifests/nJEIV3eJ.m3u8"
```

### Requirements

PHP 5.6 or above (with cURL library installed).

### Usage

* The `-d` option sets target directory
* The `-F` option allows you to select streams from master manifest
* The `--limit-rate` limits download speed
* The `--no-decrypt` turns off decryption (is turned on by default)

### Examples

Download stream with highest bitrate:

```bash
$ hlsdownload -F Bandwidth=MAX "http://content.jwplatform.com/manifests/nJEIV3eJ.m3u8"
```

Save to `/tmp` and limit connection speed:

```bash
$ hlsdownload -d /tmp --limit-rate 100k "http://content.jwplatform.com/manifests/nJEIV3eJ.m3u8"
```

### Demo

![HLSDownload Demo](demo.gif "HLSDownload Demo")

### Authors

- [Evgeny Cernisev](https://ejz.ru) | [GitHub](https://github.com/Ejz) | <ejz@ya.ru>

### License

[HLSDownload](https://github.com/Ejz/HLSDownload) is licensed under the [WTFPL License](https://en.wikipedia.org/wiki/WTFPL) (see [LICENSE](LICENSE)).
