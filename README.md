# vCenterRest
Python REST API for managing VMWARE vCenter REST API.  Forked from PyU4V

Getting Started, just clone the git hub.

Edit the file PyVCR.conf to include your vCenter IP address and credentials

install requests library 

python -m pip install requests.

All functions should be located in the rest_functions class in PyVCR rest_vcenter.py file and imported into your scripts.

Follow the examples in PyU4V github to create your own functions.

WHAT'S SUPPORTED

This package will support any REST API with a few tweaks.  

For more information about what can be done with VMware vCenter REST API 6.5  see

https://code.vmware.com/apis/52/content

https://code.vmware.com/apis/62/vcenter-management

https://code.vmware.com/apis/60/vcenter-server-appliance-management

INSTALLATION

To give it a try, download the files and add your server and array details to the top of the PyU4V.conf configuration file, under the [setup] heading. Alternatively, you can pass some or all of these details on initialisation. Requires the 'requests' library (can be installed using pip). Password, username, server_ip, port, and array MUST be set (either in the config file or on initialisation). Cert and verify can be left as is, or you can enable SSL verification by following the directions below (see SSL CONFIGURATION).

SSL CONFIGURATION
Haven't tested this piece, SSL configuration should be similar to that in PyU4V.


PyVCR could also be used as the backend for a script, or a menu etc. Just move the PyU4V package into your working directory and import it into your script ('from PyVCR.rest_vcenter import rest_functions'), create an instance of rest_functions.
e.g.
vc=rest_functions()
vc.set_session()
You need to make a call to setup the sessions with vCenter before doing anything so be sure to do this.  


EXAMPLES

test.py has some very, and I do mean very basic examples, I was just exploring the API to see how I could leverage and if I could take it further, there is a lot of VM level functionality which is interesting but doesn't relate to my day job so I'm backing off here and leaving this as a launch pad until storage functions are a bit more robust.

FUTURE

This is still a work in progress. To be expected in the future:

Please feel free to contribute, the bones of what you need are here and you should be able to run with it.  Check out the examples of how we used this in PyU4V and you should be able to replicate similar functions based on the VMware API

CONTRIBUTION

Please do! Create a fork of the project into your own repository. Make all your necessary changes and create a pull request with a description on what was added or removed and details explaining the changes in lines of code. If it all looks good, I'll merge it.

SUPPORT

Please file bugs and issues on the Github issues page for this project. This is to help keep track and document everything related to this repo. 
