#Dell 7060系列 Catalina 和 Big Sur 的OpenCore 0.6.0引导

2021年1月1日更新：OC0.6.4 目测可以休眠了

整体配置：Overall configuration:

Dell 7060MFF @ macOS 10.15.6 (Macmini8,1)

CPU 	Intel Core i3-8100T @ 3.10 GHz

MB	Dell OptiPlex Q370

MEM	Samsung 8 GB DDR4 2133MHz 

VGA	Intel UHD Grahpics 630 2048MB

LAN	BCM94360cs2 +Ngff Adapter

AUD	Realtek ALC255 ID=11

SSD	Samsung SM951 250G


安装之前请先在u盘ESP（大于200MB）区中复制1.efi文件夹，并更名为efi

进入grub并执行命令

setup_var 0x8DC 0x2  （修改dvmt 为64MB，只适合dell 7060TM/SSF/MFF,其他机器请自行查找） 

setup_var 0x5BE 0x0  （禁用CFG lock，重置bios需要重新执行两条命令）

之后，复制2.efi文件夹到esp分区（大于200MB），并更名为efi，开机选择安装盘即可

PS：经测试，可以支持10.15.6和升级big sur,声卡未测试内置喇叭，耳机孔和线路输出无问题，麦克没有去修复



Before installation, please copy the 1.efi folder in the ESP (larger than 200MB) area of the U disk, and rename EFI

Enter grub and execute the command

setup_ Var 0x8dc 0x2 (modify DVMT to 64MB, only suitable for Dell 7060tm / SSF / MFF, other machines please find it by yourself)

setup_ Var 0x5be 0x0 (disable CFG lock,Reset BIOS requires two more commands)

After that, copy the 2.efi folder to the ESP partition (larger than 200MB), and rename EFI ，boot and select the installation disk

PS: after testing, it can support Catalina 10.15.6 and upgrade Big Sur beta7，The sound card did not test the built-in speaker, 

the earphone hole and the line output were OK, and the microphone did not repair it

ENJOY！
