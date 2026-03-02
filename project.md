${{ content_synopsis }} This image will run a container registry [rootless](https://github.com/11notes/RTFM/blob/main/linux/container/image/rootless.md) and [distroless](https://github.com/11notes/RTFM/blob/main/linux/container/image/distroless.md), for maximum security and performance. Can by used by default to act as a container image proxy to pull and cache container images for all your on-prem servers. Simply add ```"registry-mirrors": ["https://registry.domain.com"]``` to your ```/etc/docker/daemon.json```. For more information about the ```config.yml``` consult the [documentation](https://distribution.github.io/distribution/).

${{ content_uvp }} Good question! Because ...

${{ github:> [!IMPORTANT] }}
${{ github:> }}* ... this image runs [rootless](https://github.com/11notes/RTFM/blob/main/linux/container/image/rootless.md) as 1000:1000
${{ github:> }}* ... this image has no shell since it is [distroless](https://github.com/11notes/RTFM/blob/main/linux/container/image/distroless.md)
${{ github:> }}* ... this image is auto updated to the latest version via CI/CD
${{ github:> }}* ... this image has a health check
${{ github:> }}* ... this image runs read-only
${{ github:> }}* ... this image is automatically scanned for CVEs before and after publishing
${{ github:> }}* ... this image is created via a secure and pinned CI/CD process
${{ github:> }}* ... this image is very small

If you value security, simplicity and optimizations to the extreme, then this image might be for you.

${{ content_comparison }}

${{ title_config }}
```yaml
${{ include: ./rootfs/registry/etc/config.yml }}
```

${{ title_volumes }}
* **${{ json_root }}/etc** - Directory of the configuration file
* **${{ json_root }}/var** - Directory of all container data downloaded and cached

${{ content_compose }}

${{ content_defaults }}

${{ content_environment }}

${{ content_source }}

${{ content_parent }}

${{ content_built }}

${{ content_tips }}