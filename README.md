# CookieCutter

___

### **Features**

CookieCutter is a program that takes comic/manga images and extracts one panel from that image, crops it, and then saves
as a new image.

* Access images from the /images/ directory
* Takes that image, converts it to grayscale, and then sends through threshold
* Take the threshold image and approximates a shape from the image's contours
* When the approximated shape is enough to crop a new image, it then saves a new cropped image to the /cropped/
  directory

### **Inspiration for this project**

I recently got into the raspberry pi and was **super** excited to see what I could do with the raspberry pi myself.
Well, one day I was on the [**raspberry pi website**](https://www.raspberrypi.com) and was looking at the products and I
stumbled upon the 'news' tab on the site and was just looking at the various projects that people have come up with. I
came across [**this**](https://www.raspberrypi.com/news/systemsix-a-love-letter-letter-to-old-macs-for-your-desk/)
amazing project that displays accurate weather updates and your own apple calendar. Such a cool project and such an
awesome idea that incorporates an E-reader display and discovering that made me want to make my own display that shows
the things that I want. I immediately came up with the idea of just shuffling through different cropped comic book
panels and displaying them on the E-ink reader and that's how I wound up researching the opencv library.

### **How to run**

Firstly, the global variables ```ASK_PANELS``` ```ASK_SAVE``` and ```SHOW_PANEL``` can be configured however you like.
If you want the program to index through the different contours to potentially grab other panels, then set it to
```ASK_PANELS = True```. Otherwise, it will just grab the largest contour area size if set to ```False```. If you would
like for the program to ask to save the current image, set it to ```ASK_SAVE = True```. Otherwise, it will just save
every new image that is created if set to ```False```. And lastly, if you would like the program to display the current
image then set it to ```SHOW_PANEL = True```. Otherwise, it will not show the current image if set to ```False```. I
recommend that if you are trying to look for more panels in the image, you should set all of the variables to ```True```
because you want to be able to see the different cropped images and be able to discard any panels that are not
accurately cropped, as it's not accurate yet... yet.

Secondly, you will need to install the other dependencies which is super simple and in the requirements.txt file.

Usually on the terminal you would just type in:

    pip install [dependency name]

I believe it's only with opencv where it's a command of:

    pip install opencv-python

Third and last thing (last major thing), are the photos. For right now I just have the program taking the images out of
the /images/ directory. Whatever photos you want to try, will be accessed from the /images/ directory so just place them
in there.

You can run this code on pycharm (that is what I used to develop this) and let it run. You will be able to see the
cropped photos in the cropped directory and booyah that's it.
