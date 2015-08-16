# Building From Source Code #

Here are a few tips for building from source code v.0.6. I will probably prepare a video on that but right now some things you need to keep in mind until another version is available where build.xml is more flexible.

  * remove `<taskdef name="SSHExec" classname="org.apache.tools.ant.taskdefs.optional.ssh.SSHExec" classpath="${lib.dir.optional}/jsch-0.1.43.jar"/>` from the build script
  * use war-prod task (ant war-prod)
  * install all the software required as mentioned in the installation slideshow (don't install Subversion client, we are using Git and internal repository, all source code is uploaded in a zip file)
  * on Windows set FLEX\_HOME to the absolute path of your Flex SDK (currently 3.5). Use forward slash! Eg. FLEX\_HOME=D:/flexsdk35 Using back slash resulted in Ant's trying to find mxmlc.jar relative to the project. And hence some issues in the bug tracker.