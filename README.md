debian-package-builder
======================

debian-package-builder is Jenkins plugin for building debian (.deb) packages.
It rocks. really.

To build debian-package-builder:

	mvn -Dmaven.test.skip=true

To install the module from commandline 

	jenkins-cli -s http://JENKINS-HOST:PORT install-plugin target/debian-package-builder.hpi


On your Jenkins host you will need to enable sudo without password for a few commands. Put the following in your sudoers (or /etc/sudoers.d/jenkins if directory exists)

	jenkins ALL=(ALL) NOPASSWD: /usr/bin/apt-get
	jenkins ALL=(ALL) NOPASSWD: /usr/lib/pbuilder/pbuilder-satisfydepends


