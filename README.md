#### SUMMARY

A simple module to extend islandora solution pack install processes by adding
technical metadata extraction via the File Information Tool Set (FITS).

#### REQUIREMENTS

The File Information Tool Set (http://code.google.com/p/fits/).

#### INSTALLATION

Download and unzip the fits tool which can be found at
http://code.google.com/p/fits/.  Make sure to unzip it into a location where
the apache user can get access.  Navigate to the unpacked fits folder and add
executable permissions to fits.sh so the apache user can run the script.

#### CONFIGURATION

Navigate to http://yourhostname/#overlay=admin/islandora/fits.  Here you can
specify the location of the fits script (on the file system) and the dsid you
want to use for the technical metadata datastream.

The System path to fits processor must include "fits.sh", so it would look like:
"/usr/share/fits-0.6.1/fits.sh" instead of "/usr/share/fits-0.6.1/".

#### TROUBLESHOOTING

If you run an ingest and you don't get any technical metadata, check to make
sure the permissions on the fits folder and the fits.sh script are correct and
the apache user can run the script.

Some images and audio files will cause problems during metadata extraction.
These are not fatal errors, but appear to be formats the fits script can't
understand.  In these cases, you will get some error reporting in the technical
metadata datastream that may help determine what happened.

#### FAQ

 Q: I ingested an object but I didn't get any technical metadata, what happened?

 A: Its most likely you forgot to update the permissions on the fits.sh script.
    If that is not the case, make sure your configuration points to the correct
    file.

#### CONTACT
