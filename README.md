# xv6-labs-2020-answer
Learning Record of MIT's 6.S081

这里是华南师范大学2023级本科生龙成飞（longjinx）的操作系统作业实操记录

旨在ubuntu22.04LTS下实现MIT（麻省理工大学）的6.S081 Fall2020课程

需要注意的是，原课程所提供的xv6-labs-2020已失效，可在https://github.com/longjinx/xv6-labs-2020-origin找到源代码，Fork自cccriscv

但是因为qemu-system-risc的升级导致make qemu会卡在编译环节，以下引用自MIT：

At this moment in time, it seems that the package qemu-system-misc has received an update that breaks its compatibility with our kernel. If you run make qemu and the script appears to hang after

qemu-system-riscv64 -machine virt -bios none -kernel kernel/kernel -m 128M -smp 3 -nographic -drive file=fs.img,if=none,format=raw,id=x0 -device virtio-blk-device,drive=x0,bus=virtio-mmio-bus.0

you'll need to uninstall that package and install an older version

然而MIT给出的方案也随库的升级而失效，故笔者自6.1810课程（MIT的2023年的操作系统课程）下载源文件,

可视为用新的riscv版qemu完成旧的课程实验

构建工具链的方法为

sudo apt-get install git build-essential gdb-multiarch qemu-system-misc gcc-riscv64-linux-gnu binutils-riscv64-linux-gnu

之后git clone https://github.com/longjinx/xv6-labs-2020.git即可

该方法截至2025.5.18仍然有效

学习过程中，学习了知乎up“易保山”的专栏，网址为https://zhuanlan.zhihu.com/p/1902514407541565063

笔者所作答案：git clone https://github.com/longjinx/xv6-labs-2020-answer

感谢刘老师的教诲，感谢MIT等的资源公开 2020版官网： https://pdos.csail.mit.edu/6.828/2020/xv6.html 2023版官网： https://pdos.csail.mit.edu/6.1810/2023/tools.html

邮箱：longjinx@qq.com 本项目已在github上开源，传播时需携带该README文件，网址为：https://github.com/longjinx/xv6-labs-2020-answer

Learning Record of MIT's 6.S081

This is the operating system homework practice record of Long Jinx, a 2023 undergraduate student at South China Normal University

Intended to implement MIT's 6.S081 Fall 2020 course on Ubuntu 22.04 LTS

It should be noted that the xv6-labs-2020 provided in the original course is no longer valid and can be used in https://github.com/longjinx/xv6-labs-2020-origin Find the source code, Fork from cccriscv

However, due to the upgrade of qemu system isc, make qemu may get stuck in the compilation process. The following quote is from MIT:

At this moment in time, it seems that the package qemu-system-misc has received an update that breaks its compatibility with our kernel. If you run make qemu and the script appears to hang after

qemu-system-riscv64 -machine virt -bios none -kernel kernel/kernel -m 128M -smp 3 -nographic -drive file=fs.img,if=none,format=raw,id=x0 -device virtio-blk-device,drive=x0,bus=virtio-mmio-bus.0

you'll need to uninstall that package and install an older version

However, the solution provided by MIT also failed with the upgrade of the library, so the author downloaded the source file from course 6.1810 (MIT's 2023 operating system course),

It can be regarded as using the new Riscv version of QEMU to complete the old course experiment

The method for building a toolchain is as follows:

sudo apt-get install git build-essential gdb-multiarch qemu-system-misc gcc-riscv64-linux-gnu binutils-riscv64-linux-gnu

Afterwards, git clone https://github.com/longjinx/xv6-labs-2020.git immediately

This method is still valid as of May 18, 2023

During the learning process, I learned about the column "Yibao Mountain" on Zhihu Up, which can be found at the website https://zhuanlan.zhihu.com/p/1902514407541565063

Author's answer: git clone https://github.com/longjinx/xv6-labs-2020-answer

Thank you to Teacher Liu for his teachings, and thank you to MIT and others for making their resources publicly available on the 2020 official website https://pdos.csail.mit.edu/6.828/2020/xv6.html 2023 official website: https://pdos.csail.mit.edu/6.1810/2023/tools.html

Email: longjinx@qq.com This project has been open sourced on GitHub, and when spreading it, you need to bring the README file at the following URL: https://github.com/longjinx/xv6-labs-2020-answer

