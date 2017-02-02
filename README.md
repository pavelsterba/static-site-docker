Goal of **static-site** image is to provide ready-to-go container to serve static websites. It runs on **nginx** and works well even when running inside Virtualbox (eg. on Mac), where problem with file updates can occur.

To make it work, just run container with this image and mount your website root to `/var/www/` like this:

```
docker run -p 80:80 -d -v /var/www/:/var/www/:ro pavelsterba/static-site
```
