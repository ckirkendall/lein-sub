# lein-sub

Leiningen plugin to execute tasks on sub-projects


## Installation

### Lein 2 users

Either install as a plugin:

    $ lein2 plugin install lein-sub "0.2.0"

Or, specify as a plugin in `project.clj`:

    :plugins [[lein-sub "0.2.0"]]

### Leiningen 1.x users

Either install as a plugin:

    $ lein plugin install lein-sub "0.1.2"

Or, include as a dev-dependency in `project.clj`:

    :dev-dependencies [[lein-sub "0.1.2"]]


## Usage

Your project may have sub-projects (each having its own project.clj file) - you can specify them as follows:

    :sub ["module/foo-common" "module/dep-vendor-xyz"]

Execute the plugin as follows:

    $ lein sub deps   # runs "lein deps" on each of 'foo-common' and 'dep-vendor-xyz'

    $ lein sub jar      # runs "lein jar" on both
    $ lein sub install  # install both sub-project artifacts to local Maven repo
    $ lein clean; rm -rf lib  # clean current dependency JARs
    $ lein deps && lein test  # get deps from remote and local Maven repos and run tests


## Getting in touch

On Twitter: [@kumarshantanu](http://twitter.com/kumarshantanu)

On Leiningen mailing list: [http://groups.google.com/group/leiningen](http://groups.google.com/group/leiningen)


## License

Copyright (C) 2011-2012 Shantanu Kumar, Phil Hagelberg

Adapted from Phil Hagelberg's example: http://j.mp/oC9TTo

Distributed under the Eclipse Public License, the same as Clojure.
