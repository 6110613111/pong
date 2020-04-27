# CLIP1:คำสั่ง Add, Jump
## สิ่งที่ควรรู้
- ใน CPU MIPS คำสั่งมีขนาด 32-bit เเบ่งเป็น 3 แบบ คือ
  <br>1.R-type ส่วนประกอบคือ
  <br>![r](https://lh3.googleusercontent.com/O-jKbPnwE1kc319eqSgEFoVvowAM75rzraNyQaQ7EaIifmswtU0miSSe_YQANMKfA5ZifO8e88lj70E_4219Yh8ccGaURF-8zeZlnRlghcCge-9ggKCAaZ1cyCib8kGbBfDCk8eBKJMHDpQunScyiZrxDtICPeP-64NIsLFAlLjJ3cuHBcYlX4-1zqajmuxns6iQSEWgZwdMPEJuV6YhMVdNu9lEQ6bfQUxmX0d4HNkWTrULOGzKxQucL8dxY6qRxOCuJfRKD-OdpARO_V07fZ0u8bKZYW-jux_7DADeKCj7--EFGNthopxSXXtRlbYZktAldO5cyv--15fm0uGYnXdRUFtH2DawpmwExQO7jzNru3XY8NGbcw6Bobs1EnnlWNZfWZLycmqm515MNaCa3LPttWgb4I9pEwypt96rQCpbm38M6Y4diRrO_UMACCnvUtQQxsjDaUdHHEA0cfFFFrSA9yVqSDkPytNSLz0W1X4NLsizerZ_TEkESngz8pLS1gdk-IgwIynlVmjMXK-wqBKegGJ4qaI-ZmqRnpz9ENL7qHCqnRMHrpfE3i9B1AdxmksT5ULYvUNu7pLdnVW_DlTCd20twUwGdIoNg5oLD03_FFu9C--4v4-NpK6gVG9KJEPJTmVT0eOeO66Nr881XYwGRWt6RrIciX2X0U76ROwcPt1vRy6uMZvJFMD7PhPiwJM-dK6LmY4jB1lGy2gdmUxE3bcPwuLiwbu8uaVfihWe_IJl5jfw=w648-h45-no)

  <br>ตัวอย่างคำสั่ง add $rd,$rs,$rt
  
  <br>2.I-type ส่วนประกอบคือ
  <br>![i](https://lh3.googleusercontent.com/3H09GYJkou7DGHQI7WuSab9RXA0nuBXqplHOdPr2xbc537DkWzCn9zHFFk2HTo7yUSmTAR9TBfk9MKf-4b3F6pW352eCf2I_45bnwktTYPc1RJbqRP8RdzMMz4ge1nfoN1bZeyd89RBMOWlmYkHEFz4VKLk6XxXAfmhjahHX6X41ogjNg6r5S16ofHvkwq8Gvz2OYZ6mbnqZCGLhHs2iKrt4A9eM73IsokpaZvkQLUg3GLg5Q4CW2M9Qu5cehbrculDtzwJUoUSauFpEtpWwOXI0v7Yhxwsb1HYc9BwGakKycVjLlGvgolLMd0enQhNjf-lXyVpoFAMwVNCVKEikKrvpjhFewi3BrSecPSzARUt58Voj5pZo1LclEecUIfwdjcGqyrOc17Kd_HliLwn_tF-jsRmaYFktYNe4mb188gRdJZd8kxWzFsB_zb4r-yQcarkeWqUhAxpAms3K1Pm2AknczTSlSXzICMO8jV8k2Wi3_lH1JGaSo8ped1qyMkN3kZijHnbOkXSQ8cco-gtG9rFo8HhHj1JEaKnAYX3P8cBxh424Rsa1v0TEF_ksR0dSp48ZeD0RoXqUcwIGf0yuimCT8DHnkGC91HhWva_hoGZkaQxWHjmVQUN49pg6yxHbshDQhth_Qtmr2aZNhDJbNwpB3h6S2OgfGLp1_-V15PfrIgg_gS6opAlWv9E=w506-h44-no)
  
  <br>ตัวอย่างคำสั่ง lw $rt,offset($rs)

  <br>3.J-type ส่วนประกอบคือ
  
  <br>![j](https://lh3.googleusercontent.com/GN7ANMHQvPJk5b4cRRTvHSsL8xf1xyQRTkuvBLMXv7ldU0BN-EZ5Ezbvx3IF7EFlOWFxT-0RxEhvbICn2f_p4IcmtStmoZ_UGQ9pSa4OAQAvNQCynVGIOBDLVMwxn__VV8mUUb7fg8hCQvMJUiNTOmYk3ndnRZ9kQGT14P7lJVUaHutvI8uChnxrJksNEeQhXkjrK7DIA6_tRI9IBx8TT2KbMDO5jtb9FA2hrwuD4NO4Rh5Tzs0g0llI8booUfl_nk1SCiKNCGh9llmaVdINLsgGRtB-dqG3s0BgDerYLodx6bOUcL8l2GXwvIXfjEbZcpIdavUO4hQsijS0ozwxSs1bsrOqYcAYTop2jv6KNqcVN1AimI1EEodqU1HFT6ceKlUvfoL3Bftu_IUTQs9ftviQyHNBPIR-ggPQgyiUvWwKrHtWUjYoK77AOArPSiWfsTC_w7KA12veLP3Ww6cb4BqU6S6no86kmNa6-fo3OREyJxs7yrTkxhTWfXI6byJluFmb030-8YWIoPBVu0FkaJpLKoiPlzf_Eqqzov-11BW-HBDrLA-q0s13CDCpkpOn2dgbN-np4h_ryACOGsMbM1YKKQ5BjIb_aqTgs3vNcpayeEENwJSffJ-eP7RN8rEWtTQHmbkyZET_hVb69WbCYqilF-qfgZxXXUVok1wJGJT3BzUX8St1KVyyo-o=w336-h42-no)
  
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
