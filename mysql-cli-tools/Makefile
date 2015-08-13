# To run this you need to have the sdist of the python package in this folder.
# You can produce that by running
#
#   $ python setup.py sdist
#
# in the root of the python distributation.

package=mysql-cli-tools
vers=0.1

package:
	# Create the debian files.
	py2dsc -m 'Thomas Nyberg <tomnyberg@gmail.com>' $(package)-$(vers).tar.gz 
	# Copy in the custom files.
	cp -v debian/* deb_dist/$(package)-$(vers)/debian
	# Try to build the package to see if everything is working.
	cd deb_dist/$(package)-$(vers); debuild -uc -us

clean:
	rm -rf deb_dist
