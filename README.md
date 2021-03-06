[![Build Status](https://travis-ci.org/stephenkopylov/SKAsyncGLViewController.svg)](https://travis-ci.org/stephenkopylov/SKAsyncGLViewController)
[![Version](https://img.shields.io/cocoapods/v/SKAsyncGLViewController.svg?style=flat)](http://cocoapods.org/pods/SKAsyncGLViewController)
[![License](https://img.shields.io/cocoapods/l/SKAsyncGLViewController.svg?style=flat)](http://cocoapods.org/pods/SKAsyncGLViewController)
[![Platform](https://img.shields.io/badge/platform-ios-brightgreen.svg?style=flat)](http://cocoapods.org/pods/SKAsyncGLViewController)

# SKAsyncGLViewController
SKAsyncGLViewController - replacement for classical GLKit stack (GLKView + GLKViewController). 

It renders all your stuff in background GCD-thread and shows result on main thread.

**Now it uses only OpenGLES2**

![Screenshot](misc/demo.gif)


### Install
#### CocoaPods
```ruby
pod "SKAsyncGLViewController"
```

#### Manual
Download this repo and drop this files into your project

![Screenshot](misc/screen1.png)

### Usage
After installation, inherit your viewController from SKAsyncGLViewController and implement these methods:

- **- (void)setupGL:(SKAsyncGLViewController *)viewController** 

:wrench: This one for setup your GL - create buffers/load shaders/etc here.
- **- (void)drawGL:(CGRect)rect**

:black_nib: :pencil2: Here you draws all your stuff!
- **- (void)clearGL:(SKAsyncGLViewController *)viewController**

:x: This method calls when your vc's view removes from superview. So here you have to clear all your gl stuff (delete buffers .etc)


You can access framebuffer, renderbuffer and background queue through view's properties.



### License
The MIT License (MIT)

Copyright (c) 2016 Stephen Kopylov, newonxp@gmail.com

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
