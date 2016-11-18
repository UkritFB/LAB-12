#ใบงานที่ 12
##การเขียนโปรแกรมกราฟฟิกส์ด้วย GDI+ (3)
##กล่าวนำ
ใบงานนี้ มีวัตถุประสงค์ เพื่อให้นักศึกษา ได้รู้จักกับ GDI+ ซึ่งจะช่วยให้นักษาสามารถ
* โหลดภาพชนิดต่างๆ เพื่อมาแสดงบนฟอร์มได้
* จัดการกับภาพโดยวิธีการง่ายๆ เช่น พลิกภาพ หมุนภาพ และเขียนข้อความลงบนภาพได้

###การโหลดภาพเพื่อแสดงบน Form
Project นี้จะโหลดภาพจากไฟล์ (ชนิดใดก็ได้) มาแสดงผลบน Form 
* สร้าง Project ใหม่เป็น Visual C#
* แก้ไข code เพื่อโหลดและแสดงภาพบน Form 
</p align = "center">
<img src="https://github.com/Desktop-Programming-Lab-2559/LAB-12/blob/master/imgs/lab12-1.png">
</p> 

**หมายเหตุ** ในบรรทัดที่ 23 หากนักศึกษาต้องการแสดงไฟล์อื่น ก็ให้ใส่ path พร้อมชื่อ แต่ต้องใส่ \\ แทน \ เนื่องจาก ในภาษา C# นั้น เครื่องหมาย \ จะเป็น escape character เช่นเดียวกับภาษา c และ c++

##การ Zoom ภาพ
การ Zoom ภาพ คือการกำหนดให้ขนาดของพื้นที่แสดงผลต่างไปจากขนาดที่แท้จริงของภาพ (Zoom in, Zoom out) นอกจากนี้เรายังสามารถเลือกส่วนของภาพที่จะแสดงได้อีกด้วย

### การ Zoom out  
คือการกำหนดให้ Rectangle ปลายทาง เล็กกว่าขนาดจริงของภาพ
 </p align = "center">
<img src="https://github.com/Desktop-Programming-Lab-2559/LAB-12/blob/master/imgs/lab12-2.png">
</p> 


### การ Zoom in  
คือการกำหนดให้ Rectangle ปลายทาง โตกว่า Rectangle ของภาพ ในที่นี้จะเลือกภาพมาแสดง
 
</p align = "center">
<img src="https://github.com/Desktop-Programming-Lab-2559/LAB-12/blob/master/imgs/lab12-3.png">
</p> 

### การพลิกและหมุนภาพ
 </p align = "center">
<img src="https://github.com/Desktop-Programming-Lab-2559/LAB-12/blob/master/imgs/lab12-4.png">
</p> 


## การเขียนข้อความลงในภาพ
 </p align = "center">
<img src="https://github.com/Desktop-Programming-Lab-2559/LAB-12/blob/master/imgs/lab12-5.png">
</p> 


##แบบฝึกหัด
ให้วาดตัวการ์ตูน Doraemon โดยใช้คำสั่งต่างๆ ทางด้านกราฟฟิกส์ พร้อมทั้งใส่ชื่อ นามสกุล และรหัสนักศึกษาของตนเองลงไปด้วย (ห้ามใช้วิธีการใส่รูปภาพ)

**[ตัวอย่างงานวาดภาพ Doraemon ของรุ่นพี่](https://github.com/Desktop-Programming-Lab-2559/LAB-12/blob/master/Doraemon.md)**
```c#

            Pen p1 = new Pen(Color.Black, 1);
            Pen p2 = new Pen(Color.Black, 2);
            Rectangle L1 = new Rectangle(50, 50, 200, 200);
            e.Graphics.FillEllipse(Brushes.Blue, L1);
            e.Graphics.DrawEllipse(p1, 50, 50, 200, 200);

            Rectangle L2 = new Rectangle(75, 100, 150, 150);
            e.Graphics.FillEllipse(Brushes.White, L2);
            e.Graphics.DrawEllipse(p1, 75, 100, 150, 150);

            Rectangle L3 = new Rectangle(88, 70, 63, 73);
            e.Graphics.FillEllipse(Brushes.White, L3);
            e.Graphics.DrawEllipse(p1, 88, 70, 63, 73);

            Rectangle L4 = new Rectangle(152, 70, 63, 73);
            e.Graphics.FillEllipse(Brushes.White, L4);
            e.Graphics.DrawEllipse(p1, 152, 70, 63, 73);

            Rectangle L5 = new Rectangle(85, 230, 130, 20);
            e.Graphics.FillRectangle(Brushes.Red, L5);
            e.Graphics.DrawRectangle(p1, 85, 230, 130, 20);

            Rectangle L8 = new Rectangle(135, 230, 30, 30);
            e.Graphics.FillEllipse(Brushes.Gold, L8);

            Rectangle L6 = new Rectangle(120, 100, 20, 25);
            e.Graphics.FillEllipse(Brushes.Black, L6);

            Rectangle L7 = new Rectangle(163, 100, 20, 25);
            e.Graphics.FillEllipse(Brushes.Black, L7);
            //////////////////เส้นกลาง  CEN
            Point P_l1 = new Point(152, 150);
            Point p_l2 = new Point(152, 200);
            ////////////////////หนวด 1  TL
            Point P_l3 = new Point(100, 150);
            Point p_l4 = new Point(140, 160);
            ////////////////////หนวด 2  TR
            Point P_l5 = new Point(162, 160);
            Point p_l6 = new Point(204, 150);
            ////////////////////หนวด 3  ML
            Point P_l7 = new Point(100, 160);
            Point p_l8 = new Point(140, 170);
            ////////////////////หนวด 4  LL
            Point P_l9 = new Point(100, 170);
            Point p_l10 = new Point(140, 180);
            ////////////////////หนวด 5  MR
            Point P_l11 = new Point(162, 170);
            Point p_l12 = new Point(204, 160);
            ////////////////////หนวด 6
            Point P_l13 = new Point(162, 180);
            Point p_l14 = new Point(204, 170);
            ///////////////////////mouth
            Point P_l15 = new Point(100, 180);
            Point p_l16 = new Point(152, 200);
            Point P_l17 = new Point(152, 200);
            Point p_l18 = new Point(204, 180);

            e.Graphics.DrawLine(p2, P_l1, p_l2);
            e.Graphics.DrawLine(p1, P_l3, p_l4);
            e.Graphics.DrawLine(p1, P_l5, p_l6);
            e.Graphics.DrawLine(p1, P_l7, p_l8);
            e.Graphics.DrawLine(p1, P_l9, p_l10);
            e.Graphics.DrawLine(p1, P_l11, p_l12);
            e.Graphics.DrawLine(p1, P_l13, p_l14);
            e.Graphics.DrawLine(p2, P_l15, p_l16);
            e.Graphics.DrawLine(p2, P_l17, p_l18);



            Rectangle L9 = new Rectangle(139, 120, 25, 25);
            e.Graphics.FillEllipse(Brushes.Red, L9);
            Brush mybrush = new SolidBrush(Color.LightSkyBlue);
            e.Graphics.DrawString("UkRiT FoNgSoMBooN 57030252", new Font("Verdana", 10, FontStyle.Bold) , mybrush, 0, 0);
```
![](https://github.com/UkritFB/LAB-12/blob/master/12.1.PNG?raw=true)
