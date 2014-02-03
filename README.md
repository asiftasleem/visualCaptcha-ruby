visualCaptcha-ruby [![Build Status](https://travis-ci.org/emotionLoop/visualCaptcha-ruby.png?branch=master)](https://travis-ci.org/emotionLoop/visualCaptcha-ruby)
==================

Ruby sample for visualCaptcha. [You can also see it live](http://ruby.demo.visualcaptcha.net).

A demo/sample Ruby app that uses the [visualcaptcha rubygem](https://github.com/emotionLoop/visualCaptcha-rubyGem) and the [visualcaptcha Angular.js bower package](https://github.com/emotionLoop/visualCaptcha-frontend-angular), as a proof-of-concept for how to integrate it with your Ruby project.


## Installation 

You need Ruby 1.9.3+ installed with Bundler.
```
bundle install
```


## Run server

Run next command to start Rack server on port 8282
```
rackup -p 8282
```


## API

### GET `/start/:how_many`

This route is for generation common data (image field name, image name, image values and audio field name) for visual captcha front-end.

Parameters:

- `how_many` is required, the number of images to generate.

### GET `/image/:index`

This route is for getting generated image file by index. 

Parameters:

- `index` is required, the index of the image you wish to get.

### GET `/audio/:type`

This route is for getting generated audio file.

Parameters:

- `type` is optional, the audio file format and defaults to `mp3`, but can also be `ogg`.

### POST `/try` 

It is a demo example of validating the visual captcha.


## License

The MIT License (MIT)

Copyright (c) 2014 emotionLoop

Permission is hereby granted, free of charge, to any person obtaining a copy of
this software and associated documentation files (the "Software"), to deal in
the Software without restriction, including without limitation the rights to
use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of
the Software, and to permit persons to whom the Software is furnished to do so,
subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS
FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR
COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER
IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN
CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
