# Heroku NGINX with Apache PageSpeed Buildpack

This custom buildpack vendors NGINX inside a dyno and has been configured to include Apache PageSpeed. This buildpack is based off of multiple different forks of the [original Heroku NGINX buildpack](https://github.com/heroku/heroku-buildpack-nginx).

## Versions (as of June 4, 2019)

* Heroku Stack: 18
* NGINX Version: 1.16.0
* Apache PageSpeed Version: 1.13.35.2-stable

## Customizable NGINX Compile Options

To make changes to the NGINX and/or Apache PageSpeed compile options:
1. Make changes to `scripts/build_nginx`.
2. Run `make build` to recompile NGINX in a Docker container.

If everything compiles successfully, the `bin/nginx-heroku-18` executable will be updated. This file gets copied during the compile phase of the buildpack. There is an alternate version (`bin/nginx-heroku-18-with-debug`) that has been compiled with NGINX debug logging enabled. To use it, just rename it to `bin/nginx-heroku-18`.

## License
Copyright (c) 2013 Ryan R. Smith
Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:
The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.
THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
