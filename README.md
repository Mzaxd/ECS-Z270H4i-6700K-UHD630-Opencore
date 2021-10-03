# Hackintosh i7-6700K&HD530

![](https://cdn.jsdelivr.net/gh/mzaxd/blog-img/20211003144927.png)
## Hardware
- CPU：I7-6700K    
- Motherboard：ECS Z270H4i (ITX Motherboard)
- GPU：Intel HD530  
- SSD：ZHITAI SC001 1T  
- Monitor：DELL 4K 
<br/>

## Issue
### USB
- 由于苹果在最近的MacOS中添加了USB端口数限制且不能通过Usbinjectall解除限制，新的限制为每个USB控制器下最多只能有15个接口（USB3.0向下兼容USB2.0 所以一个USB3.0接口占用2个接口数量），大部分高端主板可能有多个USB控制器甚至有雷电控制器，所以不用担心没有足够接口无法驱动的问题，而这张主板只有一个USB控制器，所以在定制USB时需要根据自己需要做取舍（建议在Windows下定制USB），如果使用镜像自带的EFI在进入系统后，由于USB接口识别不全（前面所说控制器的问题），你的免驱网卡（FV那几个）无法使用走USB2.0的蓝牙功能。

### IGPU
- 在我上一张主板 GA-Z170-HD3中所遇到的核显无法正常睿频问题，在这张主板中使用相同的机型ID（此EFI基于技嘉Z170的EFI）核显睿频正常，这点非常令我惊喜，这意味着可以在不使用独立显卡的情况下流畅使用，甚至是4K分辨率（系统动画有时会掉帧）
> 考虑到现在显卡的价格(mining)emmm...
<br/>

## By the way
- 由于我的硬件还没有到齐，所以暂时只做到这些，休眠可能有点问题，假如你跟我使用同一张主板，这套EFI已经能帮你解决大部分问题了
- 这套EFI使用的是免驱网卡，后面会再发一个用DW1820A的EFI
