# CLIP1:คำสั่ง Add, Jump
## สิ่งที่ควรรู้
- ใน CPU MIPS คำสั่งมีขนาด 32-bit เเบ่งเป็น 3 แบบ คือ
  <br>1.R-type ส่วนประกอบคือ
  <br>![r](https://lh3.googleusercontent.com/O-jKbPnwE1kc319eqSgEFoVvowAM75rzraNyQaQ7EaIifmswtU0miSSe_YQANMKfA5ZifO8e88lj70E_4219Yh8ccGaURF-8zeZlnRlghcCge-9ggKCAaZ1cyCib8kGbBfDCk8eBKJMHDpQunScyiZrxDtICPeP-64NIsLFAlLjJ3cuHBcYlX4-1zqajmuxns6iQSEWgZwdMPEJuV6YhMVdNu9lEQ6bfQUxmX0d4HNkWTrULOGzKxQucL8dxY6qRxOCuJfRKD-OdpARO_V07fZ0u8bKZYW-jux_7DADeKCj7--EFGNthopxSXXtRlbYZktAldO5cyv--15fm0uGYnXdRUFtH2DawpmwExQO7jzNru3XY8NGbcw6Bobs1EnnlWNZfWZLycmqm515MNaCa3LPttWgb4I9pEwypt96rQCpbm38M6Y4diRrO_UMACCnvUtQQxsjDaUdHHEA0cfFFFrSA9yVqSDkPytNSLz0W1X4NLsizerZ_TEkESngz8pLS1gdk-IgwIynlVmjMXK-wqBKegGJ4qaI-ZmqRnpz9ENL7qHCqnRMHrpfE3i9B1AdxmksT5ULYvUNu7pLdnVW_DlTCd20twUwGdIoNg5oLD03_FFu9C--4v4-NpK6gVG9KJEPJTmVT0eOeO66Nr881XYwGRWt6RrIciX2X0U76ROwcPt1vRy6uMZvJFMD7PhPiwJM-dK6LmY4jB1lGy2gdmUxE3bcPwuLiwbu8uaVfihWe_IJl5jfw=w648-h45-no)
  <br>ตัวอย่างคำสั่ง add $rd,$rs,$rt
  
  <br>2.I-type ส่วนประกอบคือ
  <br>![i](https://lh3.googleusercontent.com/VT9A3AAMsq3w8DXFw9cvQto-FkjkCkByaMYusK3HLjk6KHRs9hPBXyT3GQqRJNJYg34mEkUz_FXS2BuuD5eJIIwzW354_jgF8tvR2fGdfE2L4RwxOZVUrPX5RvFA2OYy_xl55S1yPB-pBPicK2MxJ9sNb2acsEX8MmMr_3QKNoBcYrmkQ2e-5q5l0MfSEo1TptKUWbBKe3vigML-_aICTTBRhfMF-R1TMsKIW7VDzVaUiatF_9ttxuRvL6cp4JXKkrTk0GCKvu49XVhs_r0JSnuVozHFlSC4LyvPEswd2uUoJsPbPiA8-baxma5VqI1SFffioqFG1NBqghSdX5BfPgCyeo1QNcUAgcNRWBbgZiCTwblaYvAYmh6TcebqfSBArH0WPJM6jAKB2VwR8v7DA_E4AfpEenR43JDprCy-5kLj0artT_hjRZqUoZVUoMe9x8KqyNX6SoBUr4V7_THw8Wo2vbWQ0VZvhLJU5WHD00-ulSDz_Xa8O_PvF5_thEKZoyGf5f0FHRcCrdbj_t6CY9-AI_AfvOGA7IHgx0OvfF7MLlQp2yfBrk1NzanvTu9pz4s6MNIeyXj9w2g7y_5bYDvLqn4QG5hF36oeApoVhGpfynBLoZKm-EhBxTJBWMfL-GODKk_V2s83gkkyKWI59-jGPGnZqYoz2VJhYy7TVa-K_2VPwhoGnUXYVhlZ7Uyi8UE7oDMhGwRYMA4tUB7pdI_AitOEY9uk_YYOlHDkGwry7ctHsJBV=w506-h44-no)
  <br>ตัวอย่างคำสั่ง lw $rt,offset($rs)

  <br>3.J-type ส่วนประกอบคือ
  <br>![j](https://lh3.googleusercontent.com/kwa3QMC7w8bMvTl4nfnmgbl4pQDYHOdJp1zpslfg1tHNGW4QTk4VKPTRMKLX2c_qnI1oR9XUCOFxlrSK2bot9384Hbuy230Zn-oLU-LcLIB1lbYDOlitMqe1-s6MzO8yhwVymjfbK_0dLaKIGPy_GFHZ-gtf0hZFrhTvSh8VAlQcp0nUN7aLZEHPIQehszscbTh8W_XuQSm7dyq2Ep1Nny0DI6iVyP4m_DLKoe4VEjdbp82Fbmb9DWPrmAT1Ta12VnIP6dE7nljFWK8UX38N5a_wPlr7nm3qlXEKNbW74pgRBnOgssRTca4qIdAjKtnnsxQwWuWXElVVJisAdhis9bbWilPw5KQmxZwhUfGdtLZ5MV04zS58JSQfg5LLxcw8Byjcvf80ACI46ezGjhQ3fZrl0CeLhAW9V_qDxAUY0RNgIJluzChz-jnq5ftZwcDMeaCJm5UQhTPK7BtZdD8YAwTKGS-xcDVDdVz8C8SWinzyn-AZtSwCyzaxFHK8dyeeCCZxLDwn5c9PuMWMwcHfSjau_pzYzA3Hwax02XbnpD09hcz0hv6O3Wm5i66SBjVy_L9SYFAFHVPdf4Ff8OggnkR1oNZtId9tjlmg5ArhVsL5zWkx8W6YjEQyDOIeeeBzFI1gpRP4pWvf7AB1PoedhK43potmiTsKQV-11Zbmjz9ksCyK8_AMEskzLkg=w336-h42-no) 
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

- คำสั่ง R-Type ใน state machine แบบ multicycle มี ทั้งหมด 4 step

## Step 1 (Instruction Fetch)

  <br>![t1](https://lh3.googleusercontent.com/8tdB0rREkOOyEEcEGQn7PNAvX8erVN9G1uOiKIrkDGgRPWKfXEVuyJVjwn_8nAMaBq0iiqtoB3ax2kuHJdAM60qBK7KPt5843zDPH0MR9OR8j-27nqz2oE0SnyCeynHa8_czT_p2CgV3Dk5w6BkZlV8INuiNxqw98udcQkyZGgJRt8KlcH9L1TSrX7fJxRh7g4BSH9HOLXHlHsNj5M5S-uBI6o8qEwGmETF90uKf1u2sja4Qq80jXHWctQlGZT2E86SCe5uByWigp_KA7Ki9kOScyrdKczy1z4IXOA-ZGsEzD75Z97jX_FrgOKuGeGxTBqfEh2-3NZ19A1WJpPca5CDYgzQfkN7O_KQozogd7-lGtRIKSMSJzFAcwTucD8UtmsTmnCwKiDGePg3Y2JsOaI62dA9OBV8L4lQcpyI8ghW2x4y2UteZdn5XFec0YHt5ZAKZqkK6jHO_2ID-YfrcBKO-56vmVVLweavlPGLWUCMLXJpTuC6jYo48SuQ_I6deKcuX_PV-GeJc-FmjtLvMYH7ibbP_zhSlIQXgT45D7mM6xZoZIJuWxxJG9JKDvrOemYj1caC3Qbo4PoagqkQ15M3lntpDf2bMaBwTq5Ow9-YOpXmxhbWv7sGkguh_mNA_WkdHUeoQNcp7_PGeLUgJnz9F35qYPPIdzj8uzKsenBuR2IRRWP2eofT4VZDa7r1WSH6GPaoW6GyCqiTednnVzzXbKMb7qlcuMoFe7L2sLTgPaesMBI_z=w954-h675-no)
  
## Step 2 (Register Fetch - Decode)

  <br>![t2](https://lh3.googleusercontent.com/DwmWnajmWdzc3Fia_hxYjUIAd9AyQKCjIXoK1qw0C1SH_DrN1M5Aa00LE2N71wETTewAjegwakkAypGE89G8HtGdBGqXDHfytfVot7L29Y3iUdQr8wzd5qeObPnGjDi8Wyf64cu_7Jq3LbwHwSj-WCVE4CyV5QODQOx0t2G7VM_cRkrO7BbE1W477f-OHK8vRkNClpeB8FfGy6TZjWHJvkcU5wOuAsp4lr328gzbWzLDmWZ4Z3OHcNsKtJGJyrKvKu-7857o7s_VI7if5j8VGgfz-5xjh-SkYj7-rmQHodGRFX7TElb60egaAl6TVPNNEHKwH3DH4elLoNqqinCH5Ns0Dg8ZEmJ9pRNrht5W3wn2IesxWXVlZS3y6I-SyHkOCNj3EEymOR_K5GIb5LrhSawOy2frhXjU4iPudN8-nHeq39Dg9B0EScWRZDrNu7W0yeoQRBr6c1ftfK0EWgWFJ0OfBNj7JQMtEpGrddQjuRTjEPh_lx4iMmxLRylud5GClh-f2OLDsDknN4a5t-gtZudkxU1_V0xS2GMwU-MUOrdiMWRi-pYszEOSAUadh0oUULInlZ_utg_tJl9FUH3-ORR9tyJOjajgTc8LpAN4-E3NoPTKVnuti_M_67WXYN9P31KrEzjy1Z0-8la7R1BQ1aFp5f2gb_rr5pZ-tubQVTSyipW6lRSCqvM9VKYRNVVlo7rb_JH5pUiz6wkAn4yDxW7h_gcUVzYvHyntvht8G-ZjMQF-mHht=w771-h578-no)
  
## Step 3 (Execution)

  <br>![t3](https://lh3.googleusercontent.com/qMS0auswq1YYhOSlPAfJnbrgp1RyCRuhs_PTcfFnXGlEANmliM3k6il9xE7yuOJTzUNS_FcLqfLdaCmFsIHmFTb0b9cjojqUpn02P9X8yWIEmXgkixC6o0GjO38t9dZ-zH7YKKvlVcE7bp1cWQWX7BBAWfyTU4DNBh8-PerquiHvoTmSZqJuuMykeIv8-6gyzeJbOy9JOQTxpbOtB_SgHSkEczvXOJJlBU8GyL9w0d7GOEMtPkFRmaxAXGykQblOhnhknlOZeaJbQLhf_d1js82fLSjfL6JA1lRonOJAif1umHOTi_gVyODEliMxR3lqDJnwy3J2Ieb0ZfdXvbphLb_6cr30ycTMBmmXkHDYt-qBgzKfxE0Q1blVAnstT5wPYm1BO9ImTmiz0OGBhbBFYLeg08VXbb8KcJbz5w4Nuv9ePGxNV9-O46HLwO7HErLVH-EiIEH43d3tUoICEJwfI-eItzoIqpL4do-pY2PKIlm2L7gOczwp8YcrPc3p_ssl_WHS8DOFSQdK4VV7Ufvpi7RfNIV82hq8a1TorKOlBjH66315KJ6CGGqU6YFLUxT1vDix__5-C-EolPQkFJWlREYWrIcLtF5Jr_HFnS_YT98M8UopDpF26u3vrTqspeEzxSnWJ9kC_qRaCxeWRr8_pfJAKr3pK6edZxubYg7RI-4AUnPnTdK_FYBcETk=w942-h665-no)
  
## Step 4 (Write Register)

  <br>![t4](https://lh3.googleusercontent.com/MsGCNeBmATQpM0CdvzNShlgpUbsQILblSVyiALrhNKXJUqQysxFacK_JeDRQyaH-31MAQYFxq_3mPPEZ_5Ycd_XyZiyIBYZU_OnRealZ9R813ahvj3Uo6ep-3-_MzXf2k7jdPe1Lvj9fdJF7C-1vPPR2TPP6gIZe6d11H2r1quQUk3BkcobE9pMghqEtUI3J9tIc6GEIG2SiOCFt9gDi6T_XUJWalBbj4ypY0js58jF4xU40N-dMNEh5wuob9FtWPoLWlPLKxu5T_8SjDLdK3sXdTGnZ8fsFKqnVIponme1bMrxG4v7OsU31CuueMmW7ZJw_IDGoeb5PgSxfqjLVRlWDEJivUPnB28SFijFVB6oR8wUBmfUSMzeTzvPb04Sw86SiHhKn-7K4VBd8J6nlzCYQvDCqRaiUWtFbmt_EFlVT0Q2VVbmliFJaStOJC4Pr0T-usgpJ5pXK_t9Qb1oGFxbMEvzBOjs2Ybw4Pl93ZXCg8zteOctEiCjH3CzIj7t6ZdPt3Vclob8XLFxbdDsVTgsreZjvwMClpHt_CVQbocZheOx5E7kvQS6Zqnit6HEGr_YFsN88qXb9pjkxqgcJK5UF5TALeam03LZzzhxw8J9245nnDEWg11vVxrvHQr0WYCcDnvChEOLQrdizuSDwYeD-Jr6Pd_mP51gIONl13ePsdY_B1F5pd_c7ggnRL52pl6-VAevmpzfN55zmL-bD_cMSe55Ctff5WH_q23Lcw0HYJ99rreuq=w783-h578-no)
  
  <br>รายละเอียดเพิ่มเติม [CLIP6(state machine)](https://www.youtube.com/watch?v=FtLYTSzzU7I)
  
# CLIP7:หลักการ Pipelining
- Pipeline คือการทำงานแบบคาบเกี่ยวกัน (overlap) โดยการแบ่งซีพียูออกเป็นส่วนย่อย ๆ แล้วแบ่งงานกันรับผิดชอบ
- งาน[CLIP7(pipelining)](https://youtu.be/Xa014l4KN6k)
