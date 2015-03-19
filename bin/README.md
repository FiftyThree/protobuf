Building Protobuf compiler and setting up source for building with xcode.

* Source is located here:https://github.com/google/protobuf 
They include tags for releases, see clone do ```git tag -l```
Setup Autotools:

* Install macports (yes this is annoying, you need some gnu commandline tools not in homebrew or OSX). https://www.macports.org/install.php

* Install gnu versions of auto tools ```sudo /opt/local/bin/port install autoconf automake libtool```

* Add ports to your path ```export PATH=$PATH:/opt/local/bin/```

Build protobuf compiler (protoc) OSX binary static binary

* ```./autogen.sh```

* ``./configure --disable-shared --enable-static  --prefix=$PWD```

* ```make; make check; make install;```

* Copy ```bin/protoc``` to bin/
