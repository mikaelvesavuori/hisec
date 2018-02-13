# Hisec

Hisec is a drop-in set of extremely intolerant server security configurations. They are meant to practically lock down your site with all of the means available through request/response headers and [Content Security Policy](https://content-security-policy.com). In short, what the files do is to let the server allow a lot less. Enjoy security!

Rather than starting small I believe it makes sense—in order to decrease the surface area of a potential hack—to selectively allow access to only that which is absolutely necessary for your site/app to function. This is of course easy if you're starting fresh. However, if you are running an existing, long-running site or web app, you should expect that you will need to be cautious and test quite a bit before going to production with Hisec.

In any regard, having a limited white-listing policy instead of an extensive black-listing policy will always be more strict, and thus from a security standpoint, better. It's also going to make you well-aware of what resources and domains are involved in serving your site – a bit of knowledge not to be scoffed at.

## Features

* Ready templates for Netlify, Apache and Nginx
* Based on an enforced version of the [H5BP Apache config](https://github.com/h5bp/server-configs-apache)

## Should I expect problems?

The most common "error" that may turn up is therefore simply that a script or some other resource is disallowed. Make sure to check the console for any errors.

## Strongly encouraged: Set up HTTPS redirections

Set up your server/host to redirect only to HTTPS. It's a quick fix with big security implications. Hisec can't help you with that.

## Optional: Use report-uri to get security logging

There's already a report-uri snippet for you ready to change for your own profile (at the very end of the Content-Security-Policy string). Get a free account at [Report URI](https://report-uri.com).

## Check your site

Use [Mozilla Observatory](https://observatory.mozilla.org) for a bigger check-up, which can also optionally include scores from "third-party" sites such as [Security Headers](https://www.securityheaders.io).

## IIS?

I don't use IIS, but you can get a pretty detailed guide to using Hisec in IIS if you [adapt what Scott Helme writes here](https://scotthelme.co.uk/hardening-your-http-response-headers/).