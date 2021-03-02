程式碼:
```c++
int a[10][7] = {{1,1,1,1,1,1,0},
                {0,1,1,0,0,0,0},
                {1,1,0,1,1,0,1},
                {1,1,1,1,0,0,1},
                {0,1,1,0,0,1,1},
                {1,0,1,1,0,1,1},
                {0,0,1,1,1,1,1},
                {1,1,1,0,0,0,0},
                {1,1,1,1,1,1,1},
                {1,1,1,0,0,1,1}};
void setup() {
  // put your setup code here, to run once:
 int i;
 for (i=2;i<13;i++)
   pinMode(i,OUTPUT);
   
}

void loop() {
  // put your main code here, to run repeatedly:
  digitalWrite(9,HIGH);
  for (int j=0;j<10;j++)
  {for(int i=2;i<9;i++)
   digitalWrite(i,a[j][i-2]);
   delay(500);}
  
}
```
圖如下：![image](https://github.com/EN-PEN/7_led_1-9/blob/main/IMG20210302102104.jpg)
