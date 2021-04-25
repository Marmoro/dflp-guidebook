**Full-Stack Developer Path | Virtual Lab Activity | Week 8 | HTTP Servers: Nginx & Apache | Apr 2021**

# Digital Future Leaders Program

In this week we will be taking a quick look at two of the most popular HTTP servers: Nginx & Apache.

### Learning Objectives

We will go through the steps to do the following:
1. Install Nginx on Ubuntu machine
2. Install Apache Server on Ubuntu machine
3. Configure Nginx for reverse proxy
4. Configure Apache to serve Virtual Hosts

### Tips

This list contains some of the most popular open-source HTTP servers:
- [Nginx](https://www.nginx.com/) (General HTTP Server focused on Load Balancer / Reverse Proxy features)
- [Apache Server](https://httpd.apache.org/) (General server, best used for PHP apps)
- [Caddy Server](https://caddyserver.com/) (General server)
- [HAProxy](http://www.haproxy.org/) (Load Balancer / Reverse Proxy focused server)
- [Jetty Server](https://www.eclipse.org/jetty/) (for Java apps)
- [IIS](https://www.iis.net/) (best used for .NET apps)

### Getting Started

#### Install Nginx on Ubuntu machine
```bash
$ sudo apt-get update
$ sudo apt-get install -y nginx
```

Once installation is complete, stop nginx
```bash
$ sudo service nginx stop
```

Because by default both nginx and apache uses the same ports (80, 443) which is for HTTP/HTTPS

#### Install Apache Server on Ubuntu machine
```bash
$ sudo apt-get install -y apache2
```

Once installation is complete, stop apache2
```bash
$ sudo service apache2 stop
```

#### Configure Apache to serve Virtual Hosts

Before creating virtual hosts, we need to change which port apache2 is listening to.

Let's edit this file (Ports Configuration) to match the exercise file here:
```bash
$ sudo nano /etc/apache2/ports.conf
```

Let's edit this file (Virtual Hosts Configuration) to match the exercise file here:
```bash
$ sudo nano /etc/apache2/sites-enabled/000-default.conf
```

Now we can start apache2
```bash
$ sudo service apache2 start
```

#### Configure Nginx for reverse proxy

Let's edit this file to match the exercise file here:
```bash
$ sudo nano /etc/nginx/sites-enabled/default
```

Now we can start nginx
```bash
$ sudo service nginx start
```