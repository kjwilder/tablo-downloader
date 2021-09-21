# tablo-downloader
Query a Tablo device to get and manage a list of recordings and then download
the recordings to local MPEG4 files using `ffmpeg`. This is being actively
developed. Feel free to create issues.

### Install
- `git clone https://github.com/kjwilder/tablo_downloader`
- `pip install ./tablo_downloader`

Running the install will create two programs, `tldl` (Tablo downloader) and
`tldlapis` (Tablo downloader APIs).

### Preliminaries.
- You can provide default values for any flags in `~/.tablodlr`. The format is
  json. If you have on Tablo device whose IP is `192.168.1.25`, a bare-bones config
  might look like the following:
  ```
  {
    "tablo_ips": "192.168.1.25"
  }
  ```
  If you do not specify an IP (or IPs), either via a flag or in your
  `~/.tablodlrc` file, the programs in this package will try to discover the
  IPs of your Tablo device(s) automatically.

### Usage
- `tldl --createdb` - Create a database of tablo recordings in `~/.tablodldb`.
  This can take several minutes to complete.
- `tldl --updatedb` - Update your database of tablo recordings. This can be
  run anytime and is quick.
- `tldl --dump` - Displays a summary of every recording.
- `tldlapis -h` - See a list of all the API calls you can make directly to
  your Tablo devices using this program.  

### Notes
- Local discovery may not work if connected to a VPN.

