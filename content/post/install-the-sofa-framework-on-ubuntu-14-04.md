+++
title = "Install the Sofa Framework on Ubuntu 14.04"
id = 12
categories = ["Modeling"]
tags = ["Ubuntu", "Ubuntu 14.04"]
date = "2015-09-07 10:41:05"
url = "2015/09/07/install-the-sofa-framework-on-ubuntu-14-04"
banner = "/images/sofa.jpg"
+++

The instructions provided on the [Sofa website](https://www.sofa-framework.org/documentation/general-documentation/build-sofa/) are for Ubuntu 12.04. They mostly apply to Ubuntu 14.04 as well, except:

1.  You do not need cmake binaries from other repositories.
2.  libopencascade-dev no longer exists, it has been replaced by many packages. I am not sure which ones are necessary, so, in doubt, I just installed them all:

    *   liboce-caf-dev
    *   liboce-modeling-dev
    *   liboce-visualization-dev
    *   liboce-foundation-dev

3.  Before building, you might want to enable other features/plugins. From the build-release folder, run:
4.  <pre>cmake-gui ..</pre>
and pick what you need. If you happen to be installing Sofa to use in conjunction with OpenAlea/VirtualPlants through the sofameca module (developed by the VirtualPlants team, not open source yet), pick these:

    *   SOFA-LIB_GUI_QGLVIEWER
    *   SOFA-PLUGIN_FLEXIBLE
    *   SOFA-PLUGIN_IMAGE
    *   SOFA-PLUGIN_SOFAPYTHON
	
<small>Banner photo by [Scott Allen](https://flic.kr/p/bASEfK) [![](/images/cc.png#cc)](http://creativecommons.org/licenses/by-nd/2.0/ "Attribution-NoDerivs License")</small>