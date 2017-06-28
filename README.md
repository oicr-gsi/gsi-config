# gsi-config
Config files for setting up new developers in GSI

## Settings.xml

We use Maven repositories at https://artifacts.oicr.on.ca and
https://seqwaremaven.oicr.on.ca to host our releases, so we need to configure
these in our Maven `settings.xml` file.

### While compiling/installing

To use this settings file while compiling workflows or deciders, use the
`--settings` flag.

    workflow-dir $ mvn --settings "${gsi-config-dir}/settings" clean install


### Replace user settings.xml

To install permanently in your local Maven install, replace the user settings
with the one in this directory. **WARNING:** this will remove any other
configurations you have in your `settings.xml`.

    mv ~/.m2/settings.xml ~/.m2/settings.xml.bak
    cp settings.xml ~/.m2/settings.xml

Alternatively, you can merge your `settings.xml` with the one in this directory.

## Contact

To get in touch with us, submit an issue on the Github repository:
https://github.com/oicr-gsi/gsi-config

