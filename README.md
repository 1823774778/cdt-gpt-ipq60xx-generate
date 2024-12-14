You will also like to see https://github.com/lgs2007m/uboot-ipq60xx-build

# CDT and GPT generate
CDT is Qualcomm Configuration Data Table.

GPT is GUID Partition Table.
## Linux
Install python2.7 and switch to python2.7.
```
git clone https://github.com/lgs2007m/cdt-gpt-ipq60xx-generate
cd cdt-gpt-ipq60xx-generate/meta-tools/
python2.7 prepareSingleImage.py --arch ipq6018 --fltype emmc --gencdt --genpart
```

## Windows
Install python2.7.
```
cd cdt-gpt-ipq60xx-generate/meta-tools/
prepareSingleImage.py --arch ipq6018 --fltype emmc --gencdt --genpart
```

The 1G SDRAM cdt binary will be: 

meta-tools/ipq6018/in/cdt-AP-CP03-C2_Arthur_512M16(1G)_DDR3.bin

The original FSEIASLD-64G-J02 eMMC gpt binary will be: 

meta-tools/ipq6018/in/gpt_main0.bin


uboot-ipq60xx-build
概述
本仓库提供了生成高通 IPQ6018 设备所需的 CDT（Configuration Data Table，配置数据表） 和 GPT（GUID Partition Table，全局唯一标识分区表） 工具。

核心概念
CDT：高通的配置数据表，用于描述硬件参数。
GPT：全局唯一标识分区表，用于定义存储设备的分区结构。
环境搭建
Linux 环境
安装 Python 2.7 并确保其为默认版本：

bash
复制代码
sudo apt-get install python2.7
sudo update-alternatives --install /usr/bin/python python /usr/bin/python2.7 1
sudo update-alternatives --config python
克隆本仓库：

bash
复制代码
git clone https://github.com/lgs2007m/cdt-gpt-ipq60xx-generate
cd cdt-gpt-ipq60xx-generate/meta-tools/
运行准备脚本：

bash
复制代码
python2.7 prepareSingleImage.py --arch ipq6018 --fltype emmc --gencdt --genpart
Windows 环境
安装 Python 2.7。

进入工具目录：

cmd
复制代码
cd cdt-gpt-ipq60xx-generate\meta-tools\
运行准备脚本：

cmd
复制代码
prepareSingleImage.py --arch ipq6018 --fltype emmc --gencdt --genpart
输出文件
CDT 文件
适用于 1G SDRAM 的 CDT 文件：

plaintext
复制代码
meta-tools/ipq6018/in/cdt-AP-CP03-C2_Arthur_512M16(1G)_DDR3.bin
GPT 文件
适用于 FSEIASLD-64G-J02 eMMC 的 GPT 文件：

plaintext
复制代码
meta-tools/ipq6018/in/gpt_main0.bin
相关项目
你可能也会感兴趣：

uboot-ipq60xx-build
