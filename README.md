Heroku buildpack for ffmpeg
=======================

This is a [Heroku buildpack](http://devcenter.heroku.com/articles/buildpacks) for using [ffmpeg](http://www.ffmpeg.org/) in your project.  

Currently, this will always install the latest version of ffmpeg.

Usage
-----
To use this buildpack, you should add this buildpack before your main one, then deploy your app!

```
$ heroku buildpacks:set heroku/ruby
$ heroku buildpacks:add --index 1 https://github.com/teepsllc/heroku-buildpack-ffmpeg.git
$ heroku buildpacks
  1. https://github.com/teepsllc/heroku-buildpack-ffmpeg.git
  2. heroku/ruby
```

You can verify the installation with
```
$ heroku run "ffmpeg -version"
```
