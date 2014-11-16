# FocusPoint: Smarter Image Cropping for SilverStripe

## Overview

The goal of this module is to provide some control over automatic image cropping in SilverStripe.

**Problem:** SilverStripe crops all images from the centre. If the subject is off-centre, it may be cropped out.

**Solution:** FocusPoint allows you to tag the subject in an image and ensures it is not lost during cropping.

![Comparison of cropping with and without FocusPoint](screenshots/comparison.jpg?raw=true)

## Requirements

SilverStripe 3.1

## Installation

**Manually:** Download, place the folder in your project root and run a dev/build?flush=1.

**Composer/Packagist:** Add "jonom/focuspoint" to your requirements.

## Usage

**In the CMS:** When you edit an image in the CMS there should be an extra 'Focus Point' field. Click on the subject of the image to set the focus area and save the image.

**In templates and PHP:** Use just like CroppedImage, but use CroppedFocusedImage instead. Additionally you can specify that images should not be upscaled by passing a third argument: `$image->CroppedFocusedImage($w,$h,$upscale=false)`.

**Responsive cropping:** You can use this module in combination with [jQuery FocusPoint ](https://github.com/jonom/jquery-focuspoint)to accomplish 'responsive cropping' on your website. Check out a [demo here](http://jonom.github.io/jquery-focuspoint/demos/grid/lizard.html). There is an example .ss template included in the jquery-focuspoint folder to help you set this up.

## To Do

 * Override CroppedImage() instead of adding new method (Note: I've tried everything I could think of to do this. It may be impossible)
 * ImageMagick support (maybe already works - need to test)
 
## Maintainer contact

[jonathonmenz.com](http://jonathonmenz.com)
