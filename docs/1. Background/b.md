# Legacy Images

I am going to demonstrate how to install commercial images in to GNS3.

You do not have free access to commercial images! These are licensed and have all the expected encumbrances. For me to access these images, I need an account with the vendor.

In the case of Cisco images, another way to get the images is to buy a subscription to Cisco’s network training tool, Cisco Modelling Labs (CML). This tool is over-engineered and overpriced, and we will not use it on the course. However, it does give me access to images. You can use these images while on the course, but you have no rights to use or distribute them in any way afterwards!

## 7200 Router

In this demonstration, I am going to create a Cisco 7200 router. This technology is deprecated as it uses the old MIPS emulation. However, its still worth taking a look at. I updated these notes in September 2024 due to permissions problems.

First, go to the module pages on Blackboard and download the image for the 7200 router. If you are using GNS3 in a VM, you need to use WinSCP or similar to copy the image up to your download folder in Ubuntu.

Open GNS3 and create a new project called __CiscoIOS__

<figure>
<img src = "https://jor-donegal.github.io/PowerShell7/images/fig1.png">
<figcaption>Fig 1. New Project.</figcaption>
</figure>

Select __Routers__ and then __New Template__.

<figure>
<img src = "https://jor-donegal.github.io/PowerShell7/images/fig2.avif">
<figcaption>Fig 2. New Template.</figcaption>
</figure>

Select to __Install from the GNS3 server__, click __Next__.

<figure>
<img src = "https://jor-donegal.github.io/PowerShell7/images/fig3.avif">
<figcaption>Fig 3. Install from GNS3 server.</figcaption>
</figure>

Select __Routers__ and then __Cisco 7200__. If the option is not there, then click __Update from online registry__. Then click __Install__.

<figure>
<img src = "https://jor-donegal.github.io/PowerShell7/images/fig4.avif">
<figcaption>Fig 4. Select appliance.</figcaption>
</figure>
