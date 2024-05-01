# cellive-creator

Creating CentOS Stream 9 LiveOS Image.

## Examples

### Execution Environment

- CentOS Stream 9 (x86_64)
- podman installed

### Build cellive-creator

```
podman build -t cellive-creator:el9 docker/
```

### Build the CentOS Stream 9 LiveOS

```
mkdir release
podman run --privileged --rm -it \
-v /lib/modules:/lib/modules:ro \
-v /dev:/dev \
-v $PWD/release:/release \
-v $PWD/kickstart:/BUILDDIR/kickstart \
-t cellive-creator:el9 liveos-creator \
--distribution="CentOS Stream" \
--releasever="9" \
--config kickstart/centos-stream-9-live-gnome.cfg
```

## References

- lorax 28 : https://weldr.io/lorax/f28-branch/lorax.html
- Livemedia-creator- How to create and use a Live CD : https://fedoraproject.org/wiki/Livemedia-creator-_How_to_create_and_use_a_Live_CD
- centos-7-livemedia-japanese : https://github.com/lunatilia/centos-7-livemedia-japanese
