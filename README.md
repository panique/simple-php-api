# simple-php-api (in under 40 lines of code)

An extremely simple API (with authentication) example, written in PHP
on top of the excellent Slim micro framework.
This repo shows the "server", meaning the part that offers the data.
There's another repo (https://github.com/panique/simple-php-api-client) 
showing a "client", meaning the part that GETS the data.

## What's inside ?

The entire API is inside index.php, but it's using the micro framework
Slim and an authentication module. The .htaccess creates these
 nice-looking URLs like /api/test, that's actually part of Slim.

## How to install

#### Manual installation:
 
Put index.php, composer.json and .htaccess from the *application* folder
inside your server. As this API uses "beautiful URLs" (like 
/api/stuff, not index.php?path=api&...), make sure you have mod_rewrite
activated (when using Apache) and set your virtualhost to 
"AllowOverride All". If you don't know what this means, better use the
automatic installation:

#### Automatic installation:

For simple setup, this project comes with a full installer which sets
up a Ubuntu 14.04 LTS Vagrant box and installs Apache, PHP5, Composer 
etc. and sets up the application. To do so, go to where the 
*Vagrantfile* is and do a "vagrant up" on the console. Your application
 is then reachable under 192.168.33.44
 
## How to use

After installing, check the API which a browser, when using the 
auto-installer you can do that under http://192.168.33.44/api/test,
you'll be asked to enter your login (username: demouser, password: 123)
and get back a JSON string. Nice!

## Real-world use

For real use, you or somebody else will probably access this API 
remotely with a client, plase have a look at my other repo
https://github.com/panique/simple-php-api-client which shows exactly
how to access this API from the outside, also in PHP.
 
## License
 
MIT, do whatever you want with it.

The MIT License (MIT)

Copyright (c) 2016 panique

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

## Like what you see ?

I'm also blogging at https://www.dev-metal.com, also find my others 
repos here: https://github.com/panique !