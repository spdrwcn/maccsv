![image](https://github.com/spdrwcn/maccsv/assets/157886909/4153122c-93ff-48c2-956e-bcd324f721b1)## macjson

 - 从`redis`获取所有键值对并写入`csv`文件内
 - windows环境(I5 13450HX)下100万个键值对(159B)用时`6s`
 - `./maccsv -h `查看用法

### value格式必须为`json`格式，如下：

```
{
    "bluetooth_mac": "60:A5:E2:43:BE:48",
    "wired_mac": "04:BF:1B:65:ED:9A",
    "wireless_mac": "60:A5:E2:43:BE:44"
}
```

### 例如`key`为`BPB4BX3`，`value`为以上，则写入后的文件为以下：

```
|  SN   | wired_mac  | wireless_mac  | bluetooth_mac  |
|  ----  | ----  | ----  | ----  |
| BPB4BX3  | 04:BF:1B:65:ED:9A | 60:A5:E2:43:BE:44 | 60:A5:E2:43:BE:48 |

```


