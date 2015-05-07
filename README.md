[![Build Status](https://travis-ci.org/jknack/antlr4ide.png?branch=master)](https://travis-ci.org/jknack/antlr4ide)
[ ![Download](https://api.bintray.com/packages/jknack/antlr4ide/antlr4ide/images/download.png) ](https://bintray.com/jknack/antlr4ide/antlr4ide/_latestVersion)

ANTLR 4 IDE
=========

![ANTLR 4 IDE](https://raw.github.com/jknack/antlr4ide/master/updates/screenshots/full.png)


Features
=========

* ANTLR 4.x
* Advanced Syntax Highlighting ([even for target language](https://raw.github.com/jknack/antlr4ide/master/updates/screenshots/target-language-highlighting.png))
* Automatic Code Generation (on save)
* Manual Code Generation (through External Tools menu)
* Code Formatter (Ctrl+Shift+F)
* [Syntax Diagrams as HTML](http://jknack.github.io/antlr4ide/Java/Javav4.g4.html)
* Live Parse Tree evaluation
* Advanced Rule Navigation between files (F3 or Ctrl+Click over a rule)
* Quick fixes


Welcome
=========

This is brand new version of the **old** [ANTLR IDE](http://antlrv3ide.sourceforge.net/). The new IDE supports ANTLR 4.x and it was created to run on Eclipse 4.x

The **old** [ANTLR IDE](http://antlrv3ide.sourceforge.net/) isn't supported anymore. When I wrote it, I was young and didn't know what was doing ;)

Don't get me wrong, the old version did a very good work from  user point of view, it just I'm not proud of the code base because is kind of complex and had a poor quality.

The main reason of complexity of the old IDE was in Dynamic Language ToolKit (DLTK) dependency. The DLTK project didn't evolve so much over the last few years and doing something in DLTK is very very complex and require a lot of work.

Now, the **new** IDE was built on [XText](http://www.eclipse.org/Xtext). [XText](http://www.eclipse.org/Xtext) is great for building DSL with Eclipse IDE support, so if you are not familiar with [XText](http://www.eclipse.org/Xtext) go and see it.

Requirements
=========
* Eclipse 4.4 (Luna)
* XText 2.7.3

Installation
=========
1. Install XText 2.7.3
  1. Go to ```Help > Install New Software...```
  2. Enter "http://download.eclipse.org/modeling/tmf/xtext/updates/composite/releases/" in the ```Work With``` textbox
  3. Hit Enter and wait for the list to load (this will take a few moments)
  4. Expand the Xtext and check "Xtext Complete SDK" version "2.7.3v*" (Xtext 2.8.* may cause errors)
  5. Click ```Next``` and follow the steps
2. Install ANTLR 4 IDE
  1. Go to: ```Help > Eclipse Marketplace...```
  2. Search for ```antlr```
  3. Choose ```ANTLR 4 IDE```
  4. Click ```Install```

Manual Installation
=========
You can [download the plugin](https://bintray.com/jknack/antlr4ide/antlr4ide/) and the save it in the ```dropins``` directory of your Eclipse installation.


Usage
=========
The new IDE is very simple to use all the files with a ```*.g4``` extension will be opened by the ANTLR 4 Editor. So, just open a ```*.g4``` file and play with it

Code Generation
=========
Code is automatically generated on save if the grammar is valid. You can turn off this feature by going to: ```Window > Preferences > ANTLR 4 > Tool``` and uncheck the "Tool is activated" option. From there you can configure a couple more of options.

You can find the generated code in the ```target/generated-sources/antlr4``` (same directory as antlr4-maven-plugin)

Manual Code Generation
=========
You can fire a code generation action by selecting a ```*.g4``` file from the Package Explorer, right click: ```Run As > ANTLR 4```.

A default ANTLR 4 launch configuration will be created. You can modify the generated launch configuration by going to: ```Run > External Tools > External Tools Configurations...``` from there you will see the launch configuration and how to set or override code generation options

Syntax Diagrams
=========
To open the Syntax Diagram view go to: ```Window > Show View > Other``` search and select: **Syntax Diagram**

Build with Maven 3.x
=========
1. Fork and clone the repository from github
2. Download and install [Maven 3.x](http://maven.apache.org/)
3. Open a shell console and type: ```cd antlr4ide```
4. Build the project with: ```mvn clean package```
5. It takes a while to download and configure Eclipse dependencies, so be patient
6. Wait for a: ```BUILD SUCCESS``` message

Eclipse setup
=========
1. Make sure you built the project first.
2. Open Eclipse Luna (4.4)
3. Install Xtext 2.7.3
4. Copy and paste this url: http://download.eclipse.org/modeling/tmf/xtext/updates/composite/releases/ in the **Work with** text field
5. Hit Enter
6. Choose **XText 2.7.3**. NOTE: DON'T confuse with Xtend, you must choose Xtext
7. Restart Eclipse after installing Xtext
8. Import the project into Eclipse
9. Go to: ```File > Import...``` then ```General > Existing Projects into Workspace```
10. Choose project root ```antlr4ide```
11. Enabled: ```Search for nested projects```
12. Finish

You don't need any extra Eclipse plugin (like m2e or similar). Project metadata is on git so all you need to do is: ```mvn clean package``` and then import the projects into Eclipse.


Want to contribute?
=========
* Fork the project on Github.
* Wandering what to work on? See task/bug list and pick up something you would like to work on.
* Create an issue or fix one from [issues list](https://github.com/jknack/antlr4ide/issues).
* If you know the answer to a question posted to our [mailing list](https://groups.google.com/forum/#!forum/antlr4ide) - don't hesitate to write a reply.
* Share your ideas or ask questions on [mailing list](https://groups.google.com/forum/#!forum/antlr4ide) - don't hesitate to write a reply - that helps us improve javadocs/FAQ.
* If you miss a particular feature - browse or ask on the [mailing list](https://groups.google.com/forum/#!forum/antlr4ide) - don't hesitate to write a reply, show us a sample code and describe the problem.
* Write a blog post about how you use or extend ANTLR 4 IDE.
* Please suggest changes to javadoc/exception messages when you find something unclear.
* If you have problems with documentation, find it non intuitive or hard to follow - let us know about it, we'll try to make it better according to your suggestions. Any constructive critique is greatly appreciated. Don't forget that this is an open source project developed and documented in spare time.

Help and Support
=========
  [Help and discussion](https://groups.google.com/forum/#!forum/antlr4ide)

  [Bugs, Issues and Features](https://github.com/jknack/antlr4ide/issues)

Author
=========
 [Edgar Espina] (https://twitter.com/edgarespina)

License
=========
[EPL](http://www.eclipse.org/legal/epl-v10.html)
