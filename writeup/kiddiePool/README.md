# Warm-Up
# Kiddie Pool Challenge

Tool using: imagemagick

In this challenge, we have to use one of the tool from imagemagick which is 'convert' with the -swirl flag for swirl style

Downloading a file named 'kiddie_pool.png' from the bsidesbos CTF website. After opening it, we see a picture of the flag but it's really hard to see when it is all stick together

So we use 'convert' command to make it back to the original state (if don't have 'convert' command in the system, install 'imagemagick' package)

The command that we use:

convert kiddie_pool.png -swirl -900 kiddie_pool_swirl.png

And then a 'kiddie_pool_swirl.png' should be created in the same folder with the original image

Open it and get the flag!
