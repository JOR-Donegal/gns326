# Introduction

!!! abstract "GNS3"

I could teach networking at a postgraduate level and only cover theory. This would only have an actual benefit if somehow you were separately tutored in the practical and functional implementation of network equipment. I'm very critical of universities who teach networking in this way, and I would be unlikely to hire a graduate who only had theoretical skills.

To teach the practice of networking, I need to have an environment in which my students can work. If you're on campus, we have a considerable pool of network equipment with which we can do our laboratory work. But time on campus is precious, I need some sort of environment where you can learn how to configure network equipment, and how to test it.

In the past, we have used tools like Cisco's Packet Tracer, but this only serves one manufacturer's equipment. In recent versions, there are also license restrictions.

Most universities that I'm aware of who teach practical networking now use GNS3 or EVE-NG. If you are on campus, I will be getting you to install Ubuntu 24.04 and then GNS3. In a system like GNS3, we can run network devices as VM’s using conventional virtual machine managers like KVM and QEMU. There are also legacy modes we could use. Many managed switches and routers ran on specialist processors like MIPS. Some years ago (c. 2005) an emulator was developed called Dynamips, which allows MIPS-based images to run on a PC. The advantage of this is that you are running actual production images which run on real physical hardware. Functionality is a little bit flaky, and we will generally stay away from these images in this module.

If you are working remotely, we will provide you with a VM and remote tools to do the same thing. And you are of course free to do a considerable amount of this work entirely on your own laptop or PC.

There are many ways to install and use GNS3, I no longer cover these. Feel free to read about this independently. 
