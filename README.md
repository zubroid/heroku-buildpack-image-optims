# heroku-buildpack-image-optims
Heroku buildpack for installing Image manipulating libraries such as [Jpegoptim](https://github.com/tjko/jpeginfo) v1.4.4 and [OptiPNG](http://optipng.sourceforge.net/) v0.7.6.

## Main feature

The main feature of the buildpack is posibility to change binaries' versions. For that you need to only change version in `image-optimizer-buildpack.config` file (with `BUILD_IT=true` flag).

## Getting Started

### Heroku settings

Copy link https://github.com/zubroid/heroku-buildpack-image-optims.git and put it to Settings/Buildpack in Heroku dashboard.

<img width="1300" alt="screen shot 2017-03-14 at 17 01 47" src="https://cloud.githubusercontent.com/assets/2873835/23908508/ea003896-08dc-11e7-80bc-c91799abdae0.png">

### Config file

Create a config file with `image-optimizer-buildpack.config` name and following content: 

```sh
OPTIPNG_VER="0.7.6"
JPEGOPTIM_VER="1.4.4"
BUILD_IT=true
```

and put it in the root of your project.

## BUILDPACK CONFIGS

After every push to heroku it builds Jpegoptim and OptiPNG binaries.
To avoid it in image-optimizer-buildpack.config file in your project change.

```sh
  BUILD_IT=true
```
to 
```sh
  BUILD_IT=false
```

P.S. Change it olny after first push.
