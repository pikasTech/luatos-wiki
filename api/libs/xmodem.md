# xmodem - xmodem 驱动

> 本页文档由[这个文件](https://gitee.com/openLuat/LuatOS/tree/master/luat/../script/libs/xmodem/xmodem.lua)自动生成。如有错误，请提交issue或帮忙修改后pr，谢谢！


**示例**

```lua
--注意:因使用了sys.wait()所有api需要在协程中使用
-- 用法实例
local xmodem = require "xmodem"
sys.taskInit(function()
    xmodem.send(2,115200,"/luadb/test.bin")
    while 1 do
        sys.wait(1000)
    end
end)

```

## xmodem.send(uart_id, uart_br, file_path,type)

xmodem 发送文件

**参数**

|传入值类型|解释|
|-|-|
|number|uart_id uart端口号|
|number|uart_br uart波特率|
|string|file_path 文件路径|
|bool|type 1k/128 默认1k|

**返回值**

|返回值类型|解释|
|-|-|
|bool|发送结果|

**例子**

```lua
xmodem.send(2,115200,"/luadb/test.bin")

```

---

