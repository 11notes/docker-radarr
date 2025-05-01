${{ content_synopsis }} This image will give you a rootless and lightweight Radarr installation. Radarr is a PVR for Usenet and BitTorrent users. It can monitor multiple RSS feeds for new episodes of your favorite shows and will grab, sort and rename them. It can also be configured to automatically upgrade the quality of files already downloaded when a better quality format becomes available.

${{ content_uvp }} Good question! All the other images on the market that do exactly the same don’t do or offer these options:

${{ github:> [!IMPORTANT] }}
${{ github:> }}* This image runs as 1000:1000 by default, most other images run everything as root
${{ github:> }}* This image is created via a secure, pinned CI/CD process and immune to upstream attacks, most other images have upstream dependencies that can be exploited
${{ github:> }}* This image contains a proper health check that verifies the app is actually working, most other images have either no health check or only check if a port is open or ping works
${{ github:> }}* This image works as read-only, most other images need to write files to the image filesystem
${{ github:> }}* This repository has an auto update feature that will automatically build the latest version if released, most other providers don't do this
${{ github:> }}* This image is smaller than most other images

If you value security, simplicity and the ability to interact with the maintainer and developer of an image. Using my images is a great start in that direction.

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