# vue-element-admin-backend

## Introduction

This is the backend project to support vue-element-admin. Wrote with node.js.

## Development Config

Config Nginx

#### edit /usr/local/etc/nginx/nginx.conf
##### set current user to owner
```sh
user yhe owner;
```
##### add upload conf
```sh
include /Users/yhe/upload/upload.conf;
```
#### add local upload conf
```
server
{ 
  charset utf-8;
  listen 8089;
  server_name http_host;
  root /Users/yhe/upload/;
  autoindex on;
  add_header Cache-Control "no-cache, must-revalidate";
  location / { 
    add_header Access-Control-Allow-Origin *;
  }
}
```

Run following command to start local development

###### npm install
###### node app.js

