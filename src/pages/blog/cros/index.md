---
layout: ../../../layouts/BlogItem.astro
title: 'Developing on ChromeOS'
draft: true
---
## Developing on Chrome OS

I've had quite the on-off love-hate relationship with Linux, and for good reason, in my opinion.
For desktop system, its not hard to get a decently-stable linux up and running.
Many people go with Ubuntu, or some other debain based distro. Many go with and Arch or Manjaro based distro.
All of these work well, though my preference has always been Arch with its great AUR.
The biggest issue I've ever had with Linux is its stability, especially on laptops. Between touch-screen
support, suspend, trackpad + guestures, reliable battery life, and the occasional breaking update,
it always seemed that every time I left the house with my Arch laptop, something didn't work right
in the field.

When ChromeOS first came out, I was a bit intruiged. Its Chrome-Only on a Linux kernel. I got a cheap $300 to play with and
found that enabling the Dev Mode was neat. It let you break into the kernel a bit and run your own things, quite limited though.
Later on they added Crostini, which is quite a neat tool that most don't know about.

### Crostini
Crostini is a ChromeOS version of WSL2, if you're familiar. With a couple of button clicks, you can "Enable Linux" in the ChromeOS settings,
and it will download a VirtualMachine (dubbed `termina` under the hood), inside that virtual machine it installs `lxc`, which is similar to 
Docker, and launches a container called `penguin`. It installs `sommelier` as a service inside the container as well. Now you have a "Terminal" app
in Chrome os. Launching this and selecting your new `penguin` container will drop you into a shell! Inside this container you have full
`root` and `sudo` permissions!
