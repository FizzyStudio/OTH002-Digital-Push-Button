# OTH002 数字按钮模块

###### 翻译

> `英文`请参考 [`这里`](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/README.md).

> `中文`请参考 [`这里`](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/README_cn.md).

![](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/OTH002.JPG "OTH002") 

### 产品介绍

> 按压式的开关数字输入模块,与Arduino专用传感器扩展板结合使用,能够实现非常有趣的互动作品,按钮模块使用大按钮加优质按键帽手感一流,使用方便可以做到“即插即用”。 
 
### 技术规格

* 电源要求：+3.3-5V 
* 输出类型：数字信号 
* 接口模式：pH2.0-3 
* 引脚定义：1--输出 2--电源 3---地。 
* 重量：15g 
* 外形尺寸：30mm×20mm

#### 接线图

![](https://github.com/FizzyStudio/OTH002-Digital-Push-Button/blob/master/OTH002_Diagram.png "Connection") 

#### 样例代码

    /*
      描述：
      这是一段简单的测试代码，当你按下按键时，板子上的13号引脚的LED将会被点亮，松开后，灯熄灭。
    */
    
    int ledPin = 13;                // 选择灯的引脚
    int inputPin = 2;               // 传感器连接引脚2
    
    void setup() {
      pinMode(ledPin, OUTPUT);      // 定义灯的引脚为输出引脚
      pinMode(inputPin, INPUT);     // 定义按键引脚为输入引脚
    }
    
    void loop(){
      int val = digitalRead(inputPin);  //读取输入值
      if (val == HIGH) {            // 检查输入是否为高，这里高为按下
         digitalWrite(ledPin, HIGH); // 灯亮起状态
      } else {
         digitalWrite(ledPin, LOW);  // 灯关闭状态
      }
    }

### 更多
