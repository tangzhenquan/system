## 采集linux指标, 可用于监控

包括:
* cpu
* 内存
* io状态
* 磁盘占用
* 负载
* 内、外网卡的流入、流出流量等

## 使用
go get github.com/lycclsltt/system

```go
package main

import(
	"github.com/lycclsltt/system"
)

func main() {
    mem := &system.Mem{}
    mem.Collect()
    println("used:", mem.MemUsedFunc(""), "kb")
    println("free:", mem.MemFreeFunc(""), "kb")
}
```
