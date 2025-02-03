--- >-
<!DOCTYPE html> <html lang="th"> <head> <meta charset="UTF-8"> <meta
name="viewport" content="width=device-width, initial-scale=1.0">
<title>ส่งรูปและข้อความ</title> </head> <body> <h1>ส่งรูปและข้อมูล</h1> <form
id="form1" action="page2.html" method="get" enctype="multipart/form-data">
<label for="image">เลือกรูปภาพ:</label> <input type="file" id="image"
name="image" accept="image/*" required><br><br>

<label for="tableNumber">เลขโต๊ะ:</label> <input type="text" id="tableNumber"
name="tableNumber" required><br><br>

<label for="contactInfo">ช่องทางติดต่อ:</label> <input type="text"
id="contactInfo" name="contactInfo" required><br><br>


<button type="submit">ส่ง</button> </form>

<script> // การจัดการเมื่อฟอร์มถูกส่ง document.getElementById('form1').onsubmit
= function(event) { const formData = new
FormData(document.getElementById('form1')); const imageFile =
formData.get('image'); const tableNumber = formData.get('tableNumber'); const
contactInfo = formData.get('contactInfo');

// ส่งข้อมูลไปยังหน้า 2 โดยใช้ URL query parameters window.location.href =
`page2.html?image=${encodeURIComponent(imageFile.name)}&tableNumber=${encodeURIComponent(tableNumber)}&contactInfo=${encodeURIComponent(contactInfo)}`;
event.preventDefault(); } </script> </body> </html>
