# LFS with FTP V1

This action allows you to download your LFS files from a FTP server.   
It is using [lfs-folderstore](https://github.com/sinbad/lfs-folderstore) binary.

## Setup LFS with FTP on your local machine

Please read this [documentation](./README.local.md).

## Usage

```yaml
- uses: actions/checkout@v4
  with:
    lfs: false

- uses: crosscode-game-studio/lfs-with-ftp@latest
  with:
    ftp-host : ${{ secrets.FTP_HOST }}
    ftp-user: ${{ secrets.FTP_USER }}
    ftp-password: ${{ secrets.FTP_PASS }}
```
<!-- end usage -->

## Disable cache

LFS caching is enabled by default. To disable it you can do:

```yaml
- uses: actions/checkout@v4
  with:
    lfs: false

- uses: crosscode-game-studio/lfs-with-ftp@latest
  with:
    ftp-host : ${{ secrets.FTP_HOST }}
    ftp-user: ${{ secrets.FTP_USER }}
    ftp-password: ${{ secrets.FTP_PASS }}
    cache: false
```

## License

The scripts and documentation in this project are released under the [MIT License](LICENSE)
