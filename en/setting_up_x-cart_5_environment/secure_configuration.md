---
lang: en
layout: article_with_sidebar
updated_at: '2016-09-27 23:37 +0400'
identifier: ref_secureconfig
title: Secure configuration of the server
published: true
order: 150
---

This guide offers some tips on how to configure your X-Cart server to be more secure. 

In general, you should limit the access to the server as much as possible. Use restrictive permissions, set up the right owner for the site files. 

{% note warning %}
The default UNIX 666/777 permissions, which X-Cart asks to set, don't take security requirements into consideration. They are provided to achieve a seamless procedure of the installation and upgrade, and cannot be tailored for your specific server configuration. Once the process of the installation is complete, you should set at least 644 permissions for the files and 755 permissions for the folders.
{% endnote %}

## Apache-specific settings

If you are using Apache2 server, most of the security settings are already set by .htaccess files inside folders. 

## Nginx-specific settings

You should lock some directories from web-access using these directives in the [server {} section](http://nginx.org/en/docs/http/ngx_http_core_module.html#server):

```
location ^~ /classes {
    return 403;
}

location ^~ /etc {
    return 403;
}

location ^~ /files {
    return 403;
}

location ^~ /files/attachments {
    try_files $uri =404;
}

location ^~ /images {
    location ~* \.(jpg|jpeg|gif|png|bmp|ico|tiff|flv|swf|svg|pdf) {
        try_files $uri =404;
    }
    return 403;
}

location ^~ /Includes {
    return 403;
}

location ^~ /lib {
    return 403;
}

location ^~ /skins {
    location ~* \.(tpl|twig|php|pl|conf) {
        return 403;
    }
    try_files $uri =404;
}

location ^~ /sql {
    return 403;
}

location ^~ /var {
    location ~* \.(gif|jpe?g|png|bmp|css|js) {
        try_files $uri =404;
    }
    return 403;
}

location ^~ /var/export {
    return 403;
}

location ^~ /var/import {
    return 403;
}
```

{% note warning %}
If your site is placed in subdirectory of your web-root, you should provide path, relative to web-root for each folder in `location ^~ ` lines like this: `location ^~ /xcart/classes`.
{% endnote %}
