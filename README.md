# Perfect-mariadbclient [简体中文](README.zh_CN.md)

<p align="center">
    <a href="http://perfect.org/get-involved.html" target="_blank">
        <img src="http://perfect.org/assets/github/perfect_github_2_0_0.jpg" alt="Get Involed with Perfect!" width="854" />
    </a>
</p>

<p align="center">
    <a href="https://github.com/PerfectlySoft/Perfect" target="_blank">
        <img src="http://www.perfect.org/github/Perfect_GH_button_1_Star.jpg" alt="Star Perfect On Github" />
    </a>  
    <a href="https://gitter.im/PerfectlySoft/Perfect" target="_blank">
        <img src="http://www.perfect.org/github/Perfect_GH_button_2_Git.jpg" alt="Chat on Gitter" />
    </a>  
    <a href="https://twitter.com/perfectlysoft" target="_blank">
        <img src="http://www.perfect.org/github/Perfect_GH_button_3_twit.jpg" alt="Follow Perfect on Twitter" />
    </a>  
    <a href="http://perfect.ly" target="_blank">
        <img src="http://www.perfect.org/github/Perfect_GH_button_4_slack.jpg" alt="Join the Perfect Slack" />
    </a>
</p>

<p align="center">
    <a href="https://developer.apple.com/swift/" target="_blank">
        <img src="https://img.shields.io/badge/Swift-3.0-orange.svg?style=flat" alt="Swift 3.0">
    </a>
    <a href="https://developer.apple.com/swift/" target="_blank">
        <img src="https://img.shields.io/badge/Platforms-OS%20X%20%7C%20Linux%20-lightgray.svg?style=flat" alt="Platforms OS X | Linux">
    </a>
    <a href="http://perfect.org/licensing.html" target="_blank">
        <img src="https://img.shields.io/badge/License-Apache-lightgrey.svg?style=flat" alt="License Apache">
    </a>
    <a href="http://twitter.com/PerfectlySoft" target="_blank">
        <img src="https://img.shields.io/badge/Twitter-@PerfectlySoft-blue.svg?style=flat" alt="PerfectlySoft Twitter">
    </a>
    <a href="https://gitter.im/PerfectlySoft/Perfect?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge" target="_blank">
        <img src="https://img.shields.io/badge/Gitter-Join%20Chat-brightgreen.svg" alt="Join the chat at https://gitter.im/PerfectlySoft/Perfect">
    </a>
    <a href="http://perfect.ly" target="_blank">
        <img src="http://perfect.ly/badge.svg" alt="Slack Status">
    </a>
</p>

C module import for MariaDB client Mac OS X

This files in this repository are part of the requirements for Swift Package Manager support and should not need to be manually cloned.

[Perfect-MariaDB](https://github.com/PerfectlySoft/Perfect-MariaDB)


Reference and documentation for the Perfect library.

Tests performed on MacOS X EI Captain / Sierra. Prior to build this library, please ensure:

```
brew install mariadb-connector-c
```

Please also make sure that there is a .pc file is the key to build this project.
If not found, please manually add the following content to /usr/local/lib/pkgconfig/mariadb.pc

```bash
prefix=/usr/local
exec_prefix=${prefix}/bin
libdir=${prefix}/lib/mariadb
includedir=${prefix}/include/mariadb

Name: mariadb
Description: MariaDB Connector/C
Version: 5.5.1
Requires:
Libs: -L${libdir} -lmariadb  -ldl -lm -lpthread
Cflags: -I${includedir}
Libs_r: -L${libdir} -lmariadb -ldl -lm -lpthread
```

Please replace the above path if need.

Then please also edit your ~/.bash_profile with the following line:

```
export PKG_CONFIG_PATH="/usr/local/lib/pkgconfig"
```

once done, reload this profile as

```
source ~/.bash_profile
```

The idea of the above commands is to config clang + pkg-config properly. For more information, please check the man page of pkg-config:

```
man pkg-config
```

## Further Information
For more information on the Perfect project, please visit [perfect.org](http://perfect.org).
