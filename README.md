# fty-template-rest

This is just a template for rest servelet repository 

## How to create your agent

To create your rest servelet, you have to specify this template when creating a repo on gitbub.

Then you have to update the project.xml file and run from the local clone of your repo the tools ProjectXML from the repo FTY.
You will need 2 terminal. 1. for launching the update, the other for running the script before to analyse the diff.

```bash
../FTY/ProjectXML -A --kill-cmake
```
Before to continue with the difftool, open an new terminal and run

```bash
./create_rest_package.sh
```
Then you can continue with the difftool. Be carrefull, lot of file need to be updated with the difftool. You will find a note on the top of each such as "# Note: this file is customized..."

Then you can add all the file needed: Example with generation of the template:

```bash
	doc/fty-template-rest.adoc
	include/fty-template-rest.h
	include/fty_template_rest_library.h
	packaging/debian/fty-template-rest.dsc.obs
	packaging/debian/libfty-template-rest1.install
	packaging/redhat/fty-template-rest.spec
	src/fty_template_rest_classes.h
	src/fty_template_rest_private_selftest.cc
	src/fty_template_rest_selftest.cc
	src/libfty_template_rest.pc.in
	src/rest_template_GET.ecpp
	src/rest_template_GET.h
```

Do not forget to rename src/40_template-rest.xml and update it.
Do not forget to update the file install.xml

Each time you run ../FTY/ProjectXML -A --kill-cmake do not forget to run also ./create_rest_package.sh