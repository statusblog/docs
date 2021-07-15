---
sidebar_position: 3
---

# Add a custom domain

Statusblog provides a subdomain of `statusblog.io` out of the box for your status blog. However, you may want to add a custom domain and use that instead. Statusblog not only allows this, but is the only status communication tool that includes this functionality in the free tier so that _anyone_ can do it.

Whatever custom domain you use, we will additionally provision a SSL certificate on your behalf via [Let's Encrypt](https://www.letsencrypt.org).

## Picking a custom domain

We recommend choosing the `status` subdomain for your custom domain. For example, if your service is hosted at `www.myservice.com`, we recommend using the `status.myservice.com` domain for your status blog.

Some like to have an entirely different top level domain for their status blog. For example, `wwww.myservicestatus.com`. 

## Updating DNS records

Once you have picked your custom domain, you will need to configure the relevant DNS records. To do that, create a `CNAME` record pointing your domain at your status blog's subdomain.

```
status.myservice.com     CNAME    myservice.statusblog.io
```

### Cloudflare DNS example

Many use Cloudflare as their DNS for their subdomains. To add it there, you simply go to your DNS configuration dashboard and create a new CNAME record like so:

![cloudflare DNS example](/img/cloudflare-dns-example.png)

We do not recommend enabling the Cloudflare proxy ("orange cloud"), as that may cause issues with serving your status blog. We do not support external proxying in any form.

## Updating blog setting with your custom domain

Once your custom domain `CNAME` record is configured correctly, you will need to update your blog settings with that record, so we know that is the custom domain you want to use.

![custom-domain-setting](/img/custom-domain-setting.png)

Once your custom domain is set, you will not longer be able to configure your subdomain. This is to ensure that your CNAME record is always pointing to the correct subdomain.
