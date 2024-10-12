## Deprecated

Ntfs3 is included in OpenWrt 23.05

# Ntfs3 driver backport to OpenWrt 22.03

## Description

This feed backports [Ntfs3 driver](https://www.kernel.org/doc/html/v5.15/filesystems/ntfs3.html) from Linux 5.15 to OpenWrt 22.03.

## Usage

Add the feed to the end of `feeds.conf`:

```
src-git ntfs3 https://github.com/xymopen/openwrt-ntfs3
```

If `feeds.conf` doesn't exist, copy `feeds.conf.default` and reanme it to `feeds.conf`.

Install package definitions:

```
./scripts/feeds update ntfs3
./scripts/feeds install -a -p ntfs3
```

Select `kmod-fs-ntfs3` at:

```
-> Kernel modules
  -> Filesystems
    -> kmod-fs-ntfs3
```

Optionally, if you plan to use `block-mount`, select `ntfs3-mount` at:

```
-> Utilities
  -> Filesystem
    -> ntfs3-mount
```

## Note

Default Linux codepage setting might be wrong for Windows. Add the mount option:

```
iocharset=utf8
```

Refer the [documentation](https://www.kernel.org/doc/html/v5.15/filesystems/ntfs3.html) for more mount options.

## Discussion

https://forum.openwrt.org/t/118626

## License

See [LICENSE](LICENSE) file.
