
# Specific config for htaccess files

## Make a folder publicly viewable

```htaccess
Options +Indexes
```

## Enable markdown files as viewable in browser

```htaccess
<FilesMatch "\.(md)$">
    Header set Content-Type: text/plain; charset=utf-8
</FilesMatch>
```
