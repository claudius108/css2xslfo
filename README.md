# This is a port to github of the https://sourceforge.net/projects/css2xslfo/ project

Release Notes CSSToXSLFO 1.6.2
23 August 2010

1. Requirements

You need JRE 1.5 or a higher version to run the application.

If you run css2xep.jar you also have to specify another XSLT processor, because
XEP uses Saxon 6.5.x, with which it doesn't work. You can either prepend
another XSLT processor to the boot classpath or you can simply copy saxon8.jar
in the XEP lib directory.

2. Installation

You can place the jar file where you want and launch the application as
follows:

> java -jar css2xslfo.jar options

Consult the manual for details about running the application.

3. Known Problems

- The built-in XSLT-processors in JDK1.5.0 and JDK1.6.0 don't treat the
  "ancestor-or-self" axis as a reverse axis. This causes the "list-style-type"
  detection to fail for nested lists with different style types. As a
  workaround you should prepend Saxon or Xalan 2.7.0 to the boot classpath.

4. Contact Information

Comments and bug reports can be sent to support@pincette.biz. Information about
the application is available at http://www.re.be/css2xslfo/.
