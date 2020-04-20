# CLIP1:คำสั่ง Add, Jump
## สิ่งที่ควรรู้
- ใน CPU MIPS คำสั่งมีขนาด 32-bit เเบ่งเป็น 3 แบบ คือ
  <br> 1.R-type ส่วนประกอบคือ
  <br>|op(6-bit)|rs(5-bit)|rt(5-bit)|rd(5-bit)|shamt(5-bit)|func(6-bit)|
  |-|-|-|-|-|-| 
  
  <br> 2.I-type ส่วนประกอบคือ
  |op(6-bit)|rs(5-bit)|rt(5-bit)|   value or offset(16-bit)   |
  |-|-|-|-|


- ลิ้งค์คลิป [CLIP1(คำสั่งAdd)](https://youtu.be/U5B8R18Q3nM)

- คำสั่ง Add เป็นคำสั่งแบบ R-type |op|rs|rt|rd|shamt|func|
  มีรูปแแบบคือ Add $rd ,$rs , $rt การทำงานมีขั้นตอนดังนี้
  1.

- คำสั่ง Jump
