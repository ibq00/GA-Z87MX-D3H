# 免责声明

您不能按原样使用此EFI。

至少你必须改变你的序列号，它位于 [`EFI/OC/config.plist`](https://github.com/walteweiss/Hackintosh-GA-Z87MX-D3H/blob/master/EFI/OC/config.plist), 搜索 `PlatformInfo`, 查找: `MLB`, `ROM`, `SystemSerialNumber`, `SystemUUID`. 超级容易, 关于更多 [Dortania‘s guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html).

如果您使用其他硬件（例如，iGPU而不是dGPU），则可能需要检查其他事项。




# 当前版本

- Open Core: 0.6.5
- macOS Mojave, v.10.14.6
- SMBIOS: iMac14,2

# Hardware

- MB [GA-Z87MX-D3H](Extra/Specification-GA-Z87MX-D3H.md) @ BIOS [F6 (of F7)](https://www.gigabyte.com/Motherboard/GA-Z87MX-D3H-rev-1x/support#support-dl-bios)
- CPU [Intel Core i7-4770](https://ark.intel.com/content/www/us/en/ark/products/75122/intel-core-i7-4770-processor-8m-cache-up-to-3-90-ghz.html) 4C/8T @ 3.4 GHz
- GPU 建议使用免驱显卡！无任何调整！直接插上即可使用
- RAM 8 GB 1600 MHz DDR3 自己加
- Audio Codec Realtek **ALC892**
- Ethernet `00:00:00:00:00:00` **I217-V** from Intel 
推荐淘宝直接 FV-T919 bcm94360cd
- Wi-Fi + Bluetooth `00:00:00:00:00:00`  **BCM43602** 802.11ac

# 刷BIOS，支持M.2 NVME 协议SSD，走pcie x16 满速:3000/s

技嘉z87mx d3h 刷第三方bios 完美支持nvme协议！
/BIOS/Z87MXD3H.F7

自己刷！u盘f32格式！进BIOS f8 升级

##
OC修改好的！U盘写入黑苹果后，直接去EFI中删除CLOVER引导，替换成这个！

目前，网上还没有10.14.6现成的oc!

## SMBIOS Info

```
         Model: iMac14,2
      Board ID: Mac-2700000000000000
    FW Version: 141.0.0.0.0
 Hardware UUID: 00000000-0000-0000-0000-000000000000
 Serial Number: 000000000000
       Country:  D25 - Unknown
          Year:    N - 2014
          Week:    V - 50 (10.12.2014-16.12.2014)
          Line:  000 - 000 (copy 1)
         Model: 0000 - iMac14,2
   SystemModel: iMac (27-inch, Late 2013)
         Valid: Possibly
     System ID: 00000000-0000-0000-0000-000000000000
           ROM: 000000000000
           MLB: 00000000000000000
```

---

# BIOS Settings

## Home

- Home/Performance: Defaults
- Performance/Frequency: Defaults
- Performance/Memory: System Memory Multiplier is 18.66
- System: Defaults

## BIOS Features

All defaults

- OS Type: Windows 8 

**Disable:**

- Fast Boot


**Enable:**


## Peripherals

### Device Config

- Internal Graphics Memory Size: 64M
- DVMT Pre-Allocated (iGPU Memory): MAX
- EHCI Hand-off Enabled


# Recommended

**Disable:**

- Fast Boot
- VT-d (can be enabled if you set DisableIoMapper to YES)
- CSM
- Intel SGX
- Intel Platform Trust

**Enable:**

- VT-x
- Above 4G decoding
- Hyper-Threading
- Execute Disable Bit
- EHCI/XHCI Hand-off
- OS type: Windows 8.1/10 UEFI Mode
- DVMT Pre-Allocated (iGPU Memory): 64MB


## Not present in my BIOS

**Disable**

- Thunderbolt
- CFG Lock

**Enable**

- VT-x
- Above 4G decoding
- Hyper Threading
- Execute Disable Bit
