# 免责声明

您不能按原样使用此EFI。

至少你必须改变你的序列号，它位于 [`EFI/OC/config.plist`](https://github.com/walteweiss/Hackintosh-GA-Z87MX-D3H/blob/master/EFI/OC/config.plist), 搜索 `PlatformInfo`, 查找: `MLB`, `ROM`, `SystemSerialNumber`, `SystemUUID`. 超级容易, 关于更多 [Dortania‘s guide](https://dortania.github.io/OpenCore-Post-Install/universal/iservices.html).

如果您使用其他硬件（例如，iGPU而不是dGPU），则可能需要检查其他事项。



https://github.com/walteweiss/Hackintosh-GA-Z87MX-D3H
- OpenCore  0.6.9 也可以直接用这位大哥的
- OpenCore编辑器2.42.0.0，oc引导需要对应版本的编辑器，用错可能会导致无法启动，


- MB [GA-Z87MX-D3H]
- CPU [Intel Core i7-4770](https://ark.intel.com/content/www/us/en/ark/products/75122/intel-core-i7-4770-processor-8m-cache-up-to-3-90-ghz.html) 4C/8T @ 3.4 GHz
- GPU 建议使用免驱显卡！无任何调整！直接插上即可使用
- RAM 8 GB 1600 MHz DDR3 自己加
- 推荐淘宝直接 FV-T919 bcm94360cd

# 刷BIOS，支持M.2 NVME 协议SSD，走pcie x16 满速:3000/s

技嘉z87mx d3h 刷第三方bios 完美支持nvme协议！稳定使用两年，macos 10.14/macos 10.15 都ok
/BIOS/Z87MXD3H.F7

自己刷！u盘f32格式！进BIOS f8 升级



