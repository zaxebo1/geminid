# geminid
A Gemini Server in C. Please note that this is not production-ready code.
The current state is a result of a few hours of hacking, barely able to even
serve content. But the goal is to have a compliant gemini server written in C.

## Configuring

There is no configuration file yet. Some tunable parameters are avaible in
gemini.h. For convenience you can use `make cert` to generate a self-signed
certificate.

## Building
Edit Makefile and gemini.h to your needs, do `make geminid`

## Running
Just run the produced executable geminid. Some options are now configurable via command line parameters:
- `-d <file>`: Filename of the default document, which is loaded when a directory is requested. Default: index.gmi
- `-p <port>`: Use different listen port than 1965.
- `-r <path>`: Path of the document root directory. Default is `docroot` (local to the process)

You can find a demonstration of it running at gemini://gemini.uxq.ch/
