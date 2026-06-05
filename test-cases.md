TC 1 (Positiv )
Title –  Ümumi sorğu
Description – Get sorğusu vasitəsilə bütün ölkələri tapmaq
Pre condition – Get sorğusu mövcüddur
Steps
1.	Swagger daxil ol
2.	Authorizasiyanı təsdiqlə
3.	Ölkələr hissəsini tap
4.	“Get” bütün ölkələri gətir seç
5.	Sağ küncdə try it out kliklə 
6.	Execute kliklə
Actual result – Bütün ölkələrə aid məlumatlar görsənir.
TC 2 (Neqativ )
Title – Ümumi sorğu
Description – Get sorğusu vasitəsilə bütün ölkələri tapmaq
Pre condition – Get sorğusu mövcüddur
Steps 
1.	Swagger daxil ol
2.	Ölkələr hissəsini tap
3.	“Get” bütün ölkələri gətir seç
4.	Sağ küncdə try it out kliklə 
5.	Execute kliklə
Actual result –  popupda Authorization header tələb olunur yazısı görsənir , Status code 400 dür 
Expected result - Bütün ölkələrə aid məlumatlar görsənir.
TC 3 (Positiv )
Title – Valid id ilə yoxlanış
Description – Get sorğusu vasitəsilə ID si 930 olan ölkəni  tapmaq
Pre condition – Get sorğusu mövcüddur , ID 930 ölkə mövcuddur.
Steps 
1.	Swagger daxil ol
2.	Authorizasiyanı təsdiqlə
3.	Ölkələr hissəsini tap
4.	“Get” ID ilə ölkə gətir seç
5.	ID hissəsinə 930 yaz
6.	Sağ küncdə try it out kliklə 
7.	Execute kliklə
Actual result –  ID 930 olan ölkə görsənir. Status code 200 dir
TC 4 (Positiv )
Title –  Delete vasitəsilə ölkəni silmək
Description –  ID -i 930 olan ölkəni silmək
Pre condition – Delete etmək mümkündür ,  ID 930 olan ölkə mövcuddur, Swagger aktivdir.
Steps 
1.	Swagger daxil ol
2.	Authorizasiyanı təsdiqlə
3.	Ölkələr hissəsini tap
4.	“Delete” ölkəni sil seç
5.	Sağ küncdə try it out kliklə 
6.	ID hissəsinə 930 yaz
7.	Execute kliklə
Actual result –  Status code 200 ,  [] görsənir.

TC 5 (Neqativ  )
Title –  Post vasitəsilə yeni məlumat əlavə etmək
Description –  ID 124 olan yeni ölkə yaratmaq
Pre condition – məlumat əlavə etmək mümkündür , Swagger aktivdir.
Steps 
1.	Swagger daxil ol
2.	Authorizasiyanı təsdiqlə
3.	Ölkələr hissəsini tap
4.	“Post” yeni ölkə əlavə et seç
5.	Sağ küncdə try it out kliklə 
6.	Body hissəsini zəruri məlumatlarla doldur
7.	Execute kliklə
Actual result –  Popuda “Error – response status – 409 “ görünür. ID 124 olan ölkə artıq mövcuddur . 
Expected result – Status code 200 olmalı və yeni ölkə yaranmalıdır.


TC 6 (Neqativ  )
Title –  Patch vasitəsilə məlumatı dəyişmək
Description –  ID 4238 olan ölkənin məlumatlarını qismən dəyişmək
Pre condition –Patch sorğusu mövcüddur, Swagger aktivdir.
Steps 
1.	Swagger daxil ol
2.	Authorizasiyanı təsdiqlə
3.	Ölkələr hissəsini tap
4.	“Patch” ölkəni qismən yenilə seç
5.	Sağ küncdə try it out kliklə 
6.	Body hissəsini zəruri məlumatlarla doldur
7.	 Bodydə ID hissəsini boş saxla
8.	Execute kliklə
Actual result –  Popupda “Parameter string value must be valid JSON “ görünür. 
Expected result – Status code 400 olmalı  və məlumatlar dəyişməz qalmalıdır.




