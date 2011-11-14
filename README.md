# qi4j-dev-scripts

Clone and add the bin folder to your $PATH.

Theses scripts are mostly tryouts written in shell script as I am comfortable with sh.
Some could be ported to the Qi4j build system once proven useful.

## qi4j-build

This command can be run from any directory containing a Qi4j build.gradle file.

    qi4j-build [-p group:project] command [flags]

      -p Select the target project
        group can be core, library, extension, tool, sample or tutorial
        project is the base name of the targeted submodule

    Available commands
        clean            Clean output
        test             Run tests
        install          Install only main artifacts
        devinstall       Install javadoc and sources artifacts
        distinstall      Install distributions archives

    Available flags
        skipTests        Skip tests

    Examples
        qi4j-build clean
        qi4j-build devinstall
        qi4j-build library:servlet test
        qi4j-build extension:entitystore-file test
        qi4j-build libraries install
        qi4j-build extensions install
        qi4j-build distinstall


