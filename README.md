# ZenPackBuilderDocker
Framework for using the CustomScriptBuilder[1] repo in a Docker container where a development lab may be unavailable

Installation:

From scratch:
```
# git clone https://github.com/linkslice/ZenPackBuilderDocker.git
# cd ZenPackBuilderDocker
# docker build -t customscriptbuilder .
# cd /tmp/
# mkdir libexec
# <move your scripts into libexec>
# docker run -v $(pwd):/mnt/pwd -it customscriptbuilder /bin/sh /CustomScriptBuilder/makepack.sh -a "Your Name" -n CompanyName -v <version>
```
You should end up with an egg in `/tmp/`

From Docker Hub:
```
# docker pull linkslice/customscriptbuilder:v1
# mkdir libexec
# <move your scripts into libexec>
# docker run -v $(pwd):/mnt/pwd -it linkslice/customscriptbuilder:v1 /bin/sh /CustomScriptBuilder/makepack.sh -a "Your Name" -n CompanyName -v <version>
```
** Add `-p` to install Nagios Plugins into your container and add to to egg automatically.

[1] https://github.com/linkslice/CustomScriptBuilder
