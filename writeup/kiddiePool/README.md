# Warm-Up
# Kiddie Pool Challenge

Tool using: imagemagick

In this challenge, we have to use one of the tool from imagemagick which is 'convert' with the -swirl flag for swirl style

Downloading a file named 'kiddie_pool.png' from the bsidesbos CTF website. After opening it, we see a picture of the flag but it's really hard to see when it is all stick together

So we use 'convert' command to make it back to the original state (if don't have 'convert' command in the system, install 'imagemagick' package)

The command that we use:

convert kiddie_pool.png -swirl -900 kiddie_pool_swirl.png

![image](https://user-images.githubusercontent.com/71739262/94349418-43b0be80-0012-11eb-873f-9f009fe34d34.png)

And then a 'kiddie_pool_swirl.png' should be created in the same folder with the original image

Open it and get the flag!
![image](https://user-images.githubusercontent.com/71739262/94349438-5fb46000-0012-11eb-90b4-29cee9f4baab.png)
