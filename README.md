# CLIP1:คำสั่ง Add, Jump
## สิ่งที่ควรรู้
- ใน CPU MIPS คำสั่งมีขนาด 32-bit เเบ่งเป็น 3 แบบ คือ
  <br>1.R-type ส่วนประกอบคือ
  ![i](https://drive.google.com/file/d/1fWAumswl5BsaHHyyDIJdfVm_kp-du-Hd/view?usp=sharing)
  
  |op(6-bit)|rs(5-bit)|rt(5-bit)|rd(5-bit)|shamt(5-bit)|func(6-bit)|
  |-|-|-|-|-|-|
  
  
  ![p](rt1.jpg)
  
  <br>ตัวอย่างคำสั่ง add $rd,$rs,$rt
  
  <br>2.I-type ส่วนประกอบคือ
  
  
  |op(6-bit)|rs(5-bit)|rt(5-bit)|   value or offset(16-bit)   |
  |-|-|-|-|
  
  
  <br>ตัวอย่างคำสั่ง lw $rt,offset($rs)

  <br>3.J-type ส่วนประกอบคือ
  
  
  |op(6-bit)|    absolute address(26-bit)    |
  |-|-|
  
  
  <br>ตัวอย่างคำสั่ง j address
  
- คำสั่ง Add เป็นคำสั่งแบบ R-type มีรูปแบบคือ add $rd,$rs,$rt การทำงานมีขั้นตอนดังนี้
  <br>1.แปลงค่าregisterเเต่ละตัวเป็นเลขฐาน2ขนาด5บิท ใช้เลขจากregisterเเต่ละตัว
  <br>2.ดูว่าคำสั่งaddมีobcodeเเละfuncเท่าไรซึ่งในที่นี่เท่ากับ 000000 เเละ 100000 ตามลำดับ
  <br>3.ส่วนของshamtมีค่าเป็น00000เพราะไม่มีการชิฟใดๆ
  <br>4.นำเลขที่ได้มาต่อกันตามลำดับr-typeให้ครบ32บิท
  <br>5.จากนั้นนำเลข32บิทเปลี่ยนเป็นเลขฐาน16จะได้คำสั่งในรูปแบบท่คอมพิวเตอร์เข้าใจ

- คำสั่ง Jump เป็นคำสั่งแบบ J-type มีรูปแบบคือ j address การทำงานมีขั้นตอนดังนี้
  <br>1.นำตำเเหน่งที่อยู่ที่จะกระโดดไป เป็นเลขฐาน16ขนาด8ตัวมาเเปลงเป็นเลขฐาน2ขนาด32บิท
  <br>2.ทำการชิฟไปทางขวา2ตำเเหน่งคือการตัดเลขทางขวาสุด2ตำเเหน่งเเล้วตัด4บิทเเรกทิ้งไป
  <br>3.เติมobcodeขนาด6บิทของคำสั่งjumpซึ่งมีค่า 001000 ไปข้างหน้า
  <br>4.จะได้คำสั่งขนาด32บิทจากนั้นแปลงเป็นเลขฐาน16จะได้คำสั่งที่คอมพิวเตอร์เข้าใจ
  
- ลิ้งค์คลิป [CLIP1(คำสั่งAdd)](https://youtu.be/U5B8R18Q3nM)


# CLIP2:การทำงานเเต่ละคำสั่งของคอมพิวเตอร์
- โดยทั่วไปแล้วคอมพิวเตอร์ไมได้เข้าใจภาษาที่มนุษย์พูดเลยคอมพิวเตอร์เข้าใจเพียงเเต่ตัวเลขที่ต่อๆกันมาในรูปเเบบฐาน2,8,16
  เเต่กลับกันคนเราก็ไม่เข้าใจภาษาเครื่องคอมพิวเตอร์เช่นกันดังนั้นเราจึงต้องแปลคำสั่งที่เราเข้าใจให้เป็นตัวเลขเพื่อให้เครื่องสามารถ
  ทำงานตามที่เราบอกได้โดยขั้นตอนเเละวิธีการอธิบายไว้อยู่ในคลิปหมดเเล้ว
- ลิ้งค์คลิป [CLIP2(การทำงานเเต่ละคำสั่งของคอมพิวเตอร์)](https://www.youtube.com/watch?v=kX9hZPzyaBc&t=19s)


# CLIP3:Singlecycle and Multicycle

- แบบ singlecycle 

![p1](https://lings2mi.files.wordpress.com/2012/12/figure4-11-mipsdatapathr-lod-beq.gif?w=702&zoom=2)

  <br> **ข้อสังเกตุ**
  <br>1.คำสั่งจบใน 1 cycle
  <br>2.มี memory 2 ตัว
  <br>3.มี ALU 3 ตัว
  <br>4.การทำงานของเเต่ละคำสั่งใช้เวลาเท่ากัน(เป็นเวลาของคำสั่งที่นานที่สุด)
  
- แบบ multicycle
 
![p2](https://camo.githubusercontent.com/3a759f503101d7359e3b9e88a79a64b022814d5a/68747470733a2f2f692e696d6775722e636f6d2f6d5758485770542e706e67)

  <br>**ข้อสังเกตุ**
  <br>1.คำสั่งเเต่ละคำสั่งไม่จบใน 1 cycle
  <br>2.มี memory 1 ตัว
  <br>3.มี ALU 1 ตัว
  <br>4.การทำงานของเเต่ละคำสั่งไม่เท่ากัน
  <br>5.มีการเก็บข้อมูลไว้ที่เเต่ละจุด
  
- ลิ้งค์คลิป [CLIP3(Singlecycle and Multicycle)](https://www.youtube.com/watch?v=ns2NKb_gKvM)
  
# CLIP4:การทำงานของคำสั่ง lw(load word) แบบ Multicycle

- คำสั่ง lw นั้นมีขั้นตอนทั้งหมด 5 step(T1-T5)
  <br>T1 : IR = Memory[PC] ,pc + 4 
  <br>T2 : A=Reg[IR[25-21]] ,B=Reg[IR[20-16]] ,ALUout = PC+(sign-extend(IR[15-0])<<2)
  <br>T3 : ALUout = A + (sign-extend(IR[15-0])
  <br>T4 : Memory data register = Memmory(AlUout)
  <br>T5 : B = Memory data register
- รายละเอียดเพื่มเติมในคลิป [CLIP4(lw in muticycle)](https://www.youtube.com/watch?v=Z5NQPWH3Bhk&t=4s)
  
# CLIP5:การทำงานของคำสั่ง beq(branch on equal) แบบ Multicycle

- คำสั่ง beq นั้นมีขั้นตอนทั้งหมด 3 step(T1-T3)
  <br>T1 : IR = Memory[PC] ,pc + 4 
  <br>T2 : A=Reg[IR[25-21]] ,B=Reg[IR[20-16]] ,ALUout = PC+(sign-extend(IR[15-0])<<2)
  <br>T3 : If(A==B) PC = ALUout 
- รายละเอียดเพื่มเติมในคลิป [CLIP5(beq in muticycle)](https://www.youtube.com/watch?v=bck_AWRrWS4)

# CLIP6:คำสั่ง R-Type ใน state machine แบบ multicycle

- 
