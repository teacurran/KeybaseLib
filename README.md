KeybaseLib
=========

General-purpose Java-language library for keybase.io clients

At the moment, this is set up as an Android shared library project with Android Studio apparatus, 
because it was motivated by adding Keybase search to OpenKeychain.  But it should work as a pure
vanilla Java library.


## Forked - teacurran ##

This is a forked version of the repo:  
https://github.com/timbray/KeybaseLib

I wanted to test out the complaints found in this blog post:  
https://www.tbray.org/ongoing/When/201x/2014/06/20/Hating-Java-in-2014

There seemed to be two complaints:  

__1. running command line programs in java is hard.__

For this, it is pretty easy. I am using Maven exec runner (I don't know gradle well enough).  
If you have maven installed this is easy.

to run simply do:
    ./run.sh teacurran

** Update I just re-read the post, it seems this isn't really a complaint at all. He is rightfully saying that if Java can't do #2 here then running it on the command line is a failure since all other languages can run command line apps that can do SSL properly. No arguement here, I'll leave this forked repo for anyone else who is curious. **

__2. https doesn't work with URLConnection:__

For this issue I know it has something to do with the default CA certs that come with java 7 and 8.  
I'm looking into it, but I totally agree with the blog post, it isn't clear why it doesn't work  
by default out of the box with the JDK Oracle is shipping. If it is an issue with their tight security  
then they should have some clear documentaiton for how to get it working.
    
