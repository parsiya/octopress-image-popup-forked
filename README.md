# Octopress Image Popup Plugin Forked

This is a fork of the the Octopress Image Popup Plugin at [https://github.com/ctdk/octopress-image-popup][original repo]. The original instructions did not work for me out of the box so I made some minor changes.

## Installation Instructions
For more information please refer to the [original repository][original repo]. My only modification in installation instructions is loading jQuery js files over HTTPS. The original instructions used HTTP.

Edit `octopress/Gemfile` and add the following gems:

    gem 'erubis'
    gem 'mini_magick'

Don't forget `bundle install`. You also need the `Image Magick` package.

Modify `sources/_includes/custom/head.html` and add the following lines"

    <script src="https://ajax.googleapis.com/ajax/libs/jquery/1.7.1/jquery.min.js" type="text/javascript"></script>
    <script src="https://ajax.googleapis.com/ajax/libs/jqueryui/1.8.16/jquery-ui.min.js" type="text/javascript"></script>

Copy `img_popup.html.erb` and `img_popup.rb` to `octopress/plugins`.

## How do I insert images?
To use an image use the following tag:

    {% imgpopup /images/pew.jpg 50% pew pew %}

I save all pictures in `octopress/images/`. Image path is relative to the original octopress installation folder.

## License (I am not good at this)  
The original code used a "[3 clause BSD license][bsd3license]" so I guess I am using the same thing.

[bsd3license]: http://opensource.org/licenses/BSD-3-Clause
[original Repo]: https://github.com/ctdk/octopress-image-popup