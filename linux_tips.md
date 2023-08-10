```
装载驱动程序：insmod ***.ko

卸载驱动程序：rmmod ***.ko

查看驱动结点：ls /dev/name -l

使用这个来打开驱动程序的调试信息：echo "7	4	1	7" > /proc/sys/kernel/printk
```

```
设备树：
编译：make dtbs V=1
在uboot下 print 查看 fdtfile 使用的文件；/sys/firmware/devicetree/base；/sys/firmware/fdt。此处为dtb文件
fdt 反汇编为 dts文件：
./scripts/dtc/dtc -I dts -O tmp.dtb arch/arm64/boot/dts/***.dts //汇编 dts 为 dtb
./scripts/dtc/dtc -I dtb -O tmp.dts arch/arm64/boot/dts/***.dtb  //反汇编 dtb 为 dts
/sys/devices/platform 下存放被内核解析的设备结点
```

```
linux 基础操作：
查看应用程序的进程号：ps -A | grep "app_name"
查看函数的头文件：man function
终端发送信号到对应的进程ID：kill -SIGIO ID

```

