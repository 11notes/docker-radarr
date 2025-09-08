${{ content_synopsis }} This image will give you a rootless and lightweight Radarr installation directly compiled from source.

${{ content_uvp }} Good question! Because ...

${{ github:> [!IMPORTANT] }}
${{ github:> }}* ... this image runs [rootless](https://github.com/11notes/RTFM/blob/main/linux/container/image/rootless.md) as 1000:1000
${{ github:> }}* ... this image is auto updated to the latest version via CI/CD
${{ github:> }}* ... this image is built and compiled from source
${{ github:> }}* ... this image supports 32bit architecture
${{ github:> }}* ... this image has a health check
${{ github:> }}* ... this image runs read-only
${{ github:> }}* ... this image is automatically scanned for CVEs before and after publishing
${{ github:> }}* ... this image is created via a secure and pinned CI/CD process
${{ github:> }}* ... this image is very small

If you value security, simplicity and optimizations to the extreme, then this image might be for you.

${{ content_comparison }}

**Why is this image not distroless?** I would have loved to create a distroless, single binary image, sadly the way that Radarr is setup makes it really difficult to compile a static binary from source. Enabling AOT breaks almost 30% of used libraries because they are not setup to be statically linked (like Assembly.GetExecutingAssembly().Location). It’s also not fixable with a single PR. This is something the Radarr team would need to do.

${{ title_volumes }}
* **${{ json_root }}/etc** - Directory of all your settings and database

${{ content_compose }}

${{ content_defaults }}

${{ content_environment }}

${{ content_source }}

${{ content_parent }}

${{ content_built }}

${{ content_tips }}