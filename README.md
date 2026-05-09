# Martin Ebongue — Image CDN

Free global image hosting via GitHub + jsDelivr CDN.

## How to Use

Upload any image to a folder in this repo, then use this URL pattern:

```
https://cdn.jsdelivr.net/gh/mebongue9/martin-image-cdn@main/FOLDER/IMAGE.jpg
```

### Folder Index

| Folder | Purpose |
|---|---|
| substack-newsletter/ | Cover images and body images for Substack newsletters |
| launchpad-pro/ | Launchpad Pro assets |
| skills-black-magic/ | Skills Black Magic promo images (rotated in every Substack edition) |
| etsy-empire/ | Etsy Empire assets |
| adsense-empire/ | AdSense Empire assets |
| misc/ | Everything else |

### Example URL

If you upload `banner.jpg` to `substack-newsletter/`, the CDN URL is:

```
https://cdn.jsdelivr.net/gh/mebongue9/martin-image-cdn@main/substack-newsletter/banner.jpg
```

### Important Notes

- The repo must stay PUBLIC for jsDelivr to serve files
- jsDelivr caches files permanently — old URLs never break
- GitHub recommends keeping repos under 1GB for hosting use
- Supported formats: jpg, jpeg, png, gif, webp, svg

## Uploading via GitHub API (for n8n workflows)

```
PUT https://api.github.com/repos/mebongue9/martin-image-cdn/contents/FOLDER/IMAGE.jpg
```

Body requires:
- `message`: commit message
- `content`: base64-encoded image
- `branch`: main

A GitHub Personal Access Token with `repo` scope is needed.
