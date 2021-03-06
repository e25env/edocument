# ระบบงานสารบรรณอีเล็คทรอนิคส์ (E-Document)
ระบบงานสารบรรณอีเล็คทรอนิคส์ หรือ E-Document สร้างจากคชสารเว็บเฟรมเวิร์คโดยใช้โปรเจ็ค Personnel มาพัฒนาต่อ

จุดประสงค์หลักของโปรเจ็คนี้เพื่อทดสอบการพัฒนาโปรเจ็คในรูปแบบโมดูล ซึ่งตัวโปรเจ็คหลักจริงๆจะประกอบด้วยหลายๆโมดูล
นำมาใช้งานร่วมกันในระบบ ยกตัวอย่างเช่นโปรเจ็ค Repair ก็สามารถนำมาติดตั้งใช้งานร่วมกันกับโปรเจ็คนี้ได้

## การติดตั้ง
### 1. สร้างฐานข้อมูล ```edocument``` และ นำเข้าข้อมูลจากไฟล์ ```edocument.sql```
### 2. แก้ไขค่าติดตั้งของฐานข้อมูลให้ถูกต้อง ไฟล์ settings/database.php

```
<?php
/* settings/database.php */
return array(
  'mysql' => array(
    'dbdriver' => 'mysql',
    'username' => 'root',
    'password' => '',
    'dbname' => 'edocument',
    'prefix' => 'rp',
  ),
  'tables' => array(
    'user' => 'user',
    'edocument' => 'edocument',
    'edocument_download' => 'edocument_download',
  )
);
```

### 3. สร้างไดเร็คทอรี่ ```datas/``` ถ้ายังไม่มีและปรับ chmod ให้สามารถเขียนได้หรือปรับ chmod ให้เป็น 777

## การใช้งาน
* เข้าระบบเป็นผู้ดูแลระบบ : ```admin@localhost``` และ Password : ```admin```
* เข้าระบบเป็นเจ้าหน้าที่ : ```demo@localhost``` และ Password : ```demo```

## ข้อตกลงการนำไปใช้งาน
เป็นระบบที่พัฒนาขึ้นเพื่อทดสอบการทำงาน และการเรียนรู้การใช้งาน Kotchasan PHP Framework
โดยมีจุดประสงค์หลักเพื่อให้ตื่นตัวในการใช้งานคชสาร และ สามารถพัฒนาต่อยอดได้ ```ห้ามมิให้นำระบบที่แจกไปขาย```
แต่หากมีการพัฒนาต่อเติมแล้วให้สิทธิต่างๆในซอร์สโค้ดเป็นไปตามที่ผู้พัฒนากำหนด