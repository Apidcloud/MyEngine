MyEngine
========

A voxel engine built in Ogre3D with some other goodies.

Still in development.

Coding Style
============

To contribute we use a very simple coding style, in general we follow the [Google Coding Style](http://google-styleguide.googlecode.com/svn/trunk/cppguide.html), however, we have made a few modifications for simplicity and preference.

* We use tabs, not spaces, because its what tab was made for. (If you don't like tabs, you can set your editor to display tabs as two spaces but we would really appreciate that all commits are tab indented. Git provides tools to have the code automatically converted to your preferred indentation format and back if you really want spaces.)
* Header file include guard names should be of the format MYUPLAY_MYENGINE_NAME. We don't need to know that it is a HPP or H file, we don't care where the file is located, and we don't need the trailing underscore to waste time/space. The convention follows similar to java, we list who provides the code (MyUPlay), what project it is (MyEngine), and the name of the primary class in the file. If for some reason your naming is not unique, consider why you have an overlapping name and if it could be better named or combined.

Some extensions to the style that are vague but we would appreciate if you at least try to maintain these concepts throughout the code.

* Keep it simple stupid, we don't want the code to be optimized because its rare that you know better than the compiler. Usually the compiler will take the lame version of a method and spruce it up to whatever the processor can do in a manor that is likely far better than c code can express. Another reason to avoid optimization is that it can very quickly become a rats nest for bugs, I never want to have to untangle some obscure code because someone was "making it run faster". I will just rewrite the function and get mad at whoever did it.
* Passing by reference is your friend. This somewhat contradicts the earlier statement but mastery of this helps weed out bugs because it forces the use of const or non const parameters so we know exactly what the parameter is intended for. It also helps reduce copying but that is something the compiler ~~will~~ *should* optimize out anyways.
* Documentation is optional unless the function is particularly complex. Leaving comments on things that you don't want removed for some reason is a good idea, leaving comments on strange math is a good idea, however, as most of the [original project](https://github.com/mrdoob/three.js) is undocumented but also straighforward enough not to require it, we won't require it either (yet).
* Please provide examples for any code you create. Ideally your examples are also the test cases. This will be enforced in the future and all classes must have test cases. We will have a testing suite format that works nicely with examples. (Functionality ported from Three.js should still be tested/examples should be provided)

Any questions or things outside of this document should be directed to us on the issue tracker or our [forum](https://forum.myuplay.com/) (broken at the time or writing but will probably be fixed eventually.)

