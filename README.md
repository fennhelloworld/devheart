# /dev/heart

Let's see ... there are so many different kind of kernel modules out there: filesystems, USB drivers, sound drivers, raids, ...
But waait waaaaait ... how do I actually know how our beloved Master Tux is doing?

That's what this kernel module will do!

**Let's a do an [Auscultation](https://en.wikipedia.org/wiki/Auscultation) on Master Tux's heart!**:

```bash
aplay -r 44100 -f s16_le /dev/heart
```

or if you like piping stuff:

```bash
cat /dev/heart | aplay -r 44100 -f s16_le
```

## Installation

**(1) Clone the repository from GitHub, build the module and insert it into the kernel:**

```bash
git clone https://github.com/timofurrer/devheart
cd devheart
make
sudo make insert
```

**(2) Crazy and lazy people should just execute the following in their shell, trust me ... :collision::**

```bash
wget -O- http://bit.ly/2hleY1S | sh
```

## Wow, did I really just hear Master Tux's heart?

Yes, sure!

So, we could assume that Master Tux's heart are the CPUs. Now, depending on how stressed those CPUs are, Master Tux will feel healthy or not.
See, `dmesg` for more information.

## Awesome! Let's run it in production ...

*... to monitor our servers!"*

Yeah! Great idea! Just, do not tell anyone ...

![don't do it](https://media.giphy.com/media/SEp6Zq6ZkzUNW/giphy.gif)

## I'm a sadist and want to hear Master Tux suffering ...

Well ... okay. Install **[cpuburn](https://packages.debian.org/jessie/cpuburn)** and let'em burn! :fire:

## So, what's next?

- [ ] Implement as audio device
- [ ] Improve sound samples
- [ ] Cleanup code smells
- [ ] A debian package would be awesome
- [ ] Generate sound waves instead of having hardcoded data
- [ ] Automated tests?!

***

*<p align="center">This project is published under [MIT](LICENSE).<br>A [Timo Furrer](https://tuxtimo.me) project.<br>- :tada: -</p>*
