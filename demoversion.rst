=======
Demo version
=======

Setting CPU limits
=======

MapTiler is a multi-threaded program. By default it will use all the CPUs you have and print the information about the cores. You can also set limit on defined number of cores yourself with the -P option. ::

 ￼maptiler -P 4 ...

This is especially practical to evaluate the demo application before purchasing a license for particular number of cores.

The modern CPUs has multiple cores and support of Hyperthreading - which provides multiple logical CPUs per core. This way MapTiler can provide higher performance with -P 4 even on a dual-core computer.

Demo trial extension and software activation online
=======

The demo version of MapTiler is fully usable for 30 days after first start. In case this trial period for testing the software before purchase expires and you would like to continue to test the demo, it is necessary to contact Klokan Technologies and request a trial extension key.

Such key can be then used with the parameter:

`-extend_trial KEY`

And the demo can be then used during and extended time period.

After purchase of the software, when you receive your license key, it is necessary to activate MapTiler. After activation the demo version no longer enforce the “MapTiler DEMO” overlays.

To do the online activation, use the following command:

`-activate YOUR-OWN-LICENSE-KEY`

Example: ::

 ￼maptiler -activate YOUR-OWN-LICENSE-KEY
 
**In case you require to reinstall the computer, use** -deactivate **command to be able to re-activate the license later on.** 


Software activation in a virtual machine
--------

The activation process for MapTiler running in a virtual machine requires online activation only via environment variable `MAPTILER_LICENSE`.
The software will be automatically deactivated in the end.

Example on Windows OS ::

 set MAPTILER_LICENSE=YOUR-OWN-LICENSE-KEY
 maptiler ...


Example on Linux / maxOS ::

 export MAPTILER_LICENSE=YOUR-OWN-LICENSE-KEY
 maptiler ...

**Notice:** This activation process via environment variable requires **not-activated MapTiler Pro** instance on that computer! Starting MapTiler application without setting this environment variable `MAPTILER_LICENSE`, you should see either **MapTiler Pro Demo**, or **Your trial period has expired** error message.


Software activation offline
========
For computers which are not directly connected to the Internet or which are in security restricted installations, we have support for offline activation as well.

To use the offline activation with the key we supply you after purchase you need to call: ::

 ￼maptiler -activate_request YOUR-OWN-LICENSE-KEY request.xml

This will generate a "request.xml" file, which you must send to us by email, and we will provide you with a "response.xml" file back. This can be used to activate the MapTiler by running: ::

 ￼maptiler -activate_response response.xml
 
If at any time you will want to deactivate MapTiler, eg. to move it to another machine, run the following command and you have to send us again the newly generated "request.xml" file. ::

 ￼maptiler -deactivate_request request.xml

