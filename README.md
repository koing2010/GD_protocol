# 1 USB_Printer
usb virtual printer <br>

## 1 MatchingIterm<br>

### 1.1建立匹配项 A1+A2+~  <br>
 {"现" + "金"}  <br>
 {"现" + "价"} 等等   <br>
		
### 1.2匹配规则  <br>
Iterm = { A + 数字字符开始 + 数字字符结尾}  <br>
	
	
## 2 Loading MatchingIterm  <br> <br>
 
###	 2.1 format: <br>
{{{现金}{现价}{总额}{合计}{总价}}}  <br> <br>
###	  以两个左大括号 '{{'开始，两个右 '}}'  结束      <br>
大括号字符不是常打印字符，容易检索  <br> <br>
###	  目前先固定两个汉字  <br>
###   设置完成验证 <br>
把设置的**Iterm**+**金额**分别按发送出去**蜻蜓**端出现收款提示为正确   <br>
如依次发送：  <br>
    **“现金 0.1 元”**   <br>
	**“现价 0.2 元”** 等等  <br>
	
## 设置功能只在上电前五分钟有效  <br> 
暂定五分钟 <br> <br>

##  清除设置 <br>
{{{XXXX}{XXXX}{XXXX}{现在}{总额}}}   <br>
    想删除所有设置用大写 XXXX代替  <br>
##  略过设置   <br>
   如果不设置的话，用四个英文空格(hex = 0x20)代替  <br>
##  一个Pakage总共34个字节   <br>
   一个中文字符占两个英文字符空间   <br>
#  2 升级工具UpDateTool 的使用   <br>
[PC端软件工具件下载](https://raw.githubusercontent.com/koing2010/GD_protocol/master/UpDateTool/BootToolrelease20191119-0.zip) <br>
##  软件使用  <br>
解压上面的软件工具,打开 GWUpdateToo.exe <br>
### 1.选择升级文件 如 XXXX.bin  <br>
### 2.选择升级串口，evb板子得按 **硬件连接**中的说明连接好 <br>
### 3.点升级按键，升级提完成即可  <br>
### 4.从PC拔下evb usb的连接线，然后拔下跳线冒（断开 2-3脚的连接）  <br>
### 5.重新将EVB插回PCB就识别为打印机了 <br>
### 6. 以后每次升级重复此过程就行  <br>
![](/UpDateTool/UpDateToolUI.jpg) <br>
##  硬件连接  <br>
下图评估板上标红框的位置， 跳线冒把 2脚和3脚短接起来，然后 用usb线将evb板子到PC  <br>
### PC端会识别出一个串口 <br>
### 升级完成后将跳线冒拔下来 重新将板子连接PC 就升级完成 <br>
![](/UpDateTool/EVB.jpg) <br>


	
