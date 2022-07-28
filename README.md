# Kredit_berishni_bashorat_qilish

1. Sarlavha: Bank marketingi (ijtimoiy/iqtisodiy)
 
2. Tegishli ma'lumotlar:

   Bu maʼlumotlar toʻplami “Bank Marketing” UCI maʼlumotlar toʻplamiga asoslangan (tavsifni http://archive.ics.uci.edu/ml/datasets/Bank+Marketing manzilida tekshiring).
   Ma'lumotlar Banco de Portugal tomonidan e'lon qilingan va https://www.bportugal.pt/estatisticasweb saytida ommaga ochiq bo'lgan beshta yangi ijtimoiy va iqtisodiy xususiyat/atributlar (~10 million aholiga ega mamlakat bo'yicha milliy ko'rsatkichlar) qo'shilishi bilan boyitilgan. .
   Bu maʼlumotlar toʻplami [Moro va boshq., 2014] da ishlatilgan maʼlumotlar toʻplami bilan deyarli bir xil (maxfiylik bilan bogʻliq muammolar tufayli u barcha atributlarni oʻz ichiga olmaydi). 
   Rminer to'plami va R vositasidan (http://cran.r-project.org/web/packages/rminer/) foydalanib, biz beshta yangi ijtimoiy va iqtisodiy atributlarning qo'shilishi (bu erda mavjud) sezilarli yaxshilanishga olib kelishini aniqladik. muvaffaqiyatni bashorat qilishda, hatto qo'ng'iroqning davomiyligi kiritilmagan bo'lsa ham. Eslatma: faylni R tilida o'qish mumkin: d=read.table("bank-additional-full.csv",header=TRUE,sep=";")
   
   Zip fayl ikkita ma'lumotlar to'plamini o'z ichiga oladi: 
      1) barcha misollar bilan bank-additional-full.csv, sana bo'yicha tartiblangan (2008 yil mayidan 2010 yil noyabrigacha).
      2) bank-additional.csv 10% misollar bilan (4119), bank-additional-full.csv dan tasodifiy tanlangan.
   Eng kichik ma'lumotlar to'plami ko'proq hisoblash talab qiladigan mashinani o'rganish algoritmlarini (masalan, SVM) sinab ko'rish uchun taqdim etiladi.

   Ikkilik tasniflash maqsadi mijozning bank muddatli depozitiga obuna bo'lishini bashorat qilishdir (y o'zgaruvchisi).

3. Namunalar soni: bank-additional-full.csv uchun 41188

4. Atributlar soni: 20 + chiqish atributi.

5. Atribut haqida ma'lumot:

   Qo'shimcha ma'lumot olish uchun [Moro va boshq., 2014] o'qing.

   Kirish o'zgaruvchilari:
   # bank mijozi maʼlumotlari:
   1 - yosh (raqamli)
   2 - ish : ish turi (toifali: "admin.", "ko'k yoqalar", "tadbirkor", "uy xizmatchisi", "boshqaruv", "nafaqadagi", "yakka tartibdagi tadbirkor", "xizmatlar", "talaba" ,"texnik","ishsiz","noma'lum")
   3 - oilaviy : oilaviy holat (kategorial: "ajrashgan", "turmush qurgan", "bo'ydoq", "noma'lum"; eslatma: "ajrashgan" ajrashgan yoki beva qolgan degan ma'noni anglatadi)
   4 - ta'lim (toifali: "asosiy.4y","asosiy.6y","asosiy.9y","o'rta.maktab","savodsiz","professional.kurs","universitet.darajali","noma'lum")
   5 - sukut bo'yicha: sukut bo'yicha kredit bormi? (kattegorik: "yo'q", "ha", "noma'lum")
   6 - uy-joy: uy-joy krediti bormi? (kattegorik: "yo'q", "ha", "noma'lum")
   7 - kredit: shaxsiy kredit bormi? (kattegorik: "yo'q", "ha", "noma'lum")
   # joriy kampaniyaning oxirgi kontakti bilan bog'liq:
   8 - aloqa: aloqa turi (toifali: "uyali", "telefon") 
   9 - oy: yilning oxirgi aloqa oyi (kategorik: "jan", "fevral", "mar", ..., "nov", "dec")
  10 - haftaning_kuni: haftaning oxirgi aloqa kuni (kategorial: "du", "shanba", "chors", "pays", "juma")
  11 - davomiylik: oxirgi aloqa davomiyligi, soniyalarda (raqamli). Muhim eslatma: bu atribut chiqish maqsadiga juda ta'sir qiladi (masalan, agar davomiyligi=0 bo'lsa, u holda y="yo'q"). Biroq, qo'ng'iroqni amalga oshirishdan oldin uning davomiyligi noma'lum. Bundan tashqari, qo'ng'iroq tugagandan keyin y aniq ma'lum. Shunday qilib, ushbu ma'lumot faqat benchmark maqsadlari uchun kiritilishi kerak va agar maqsad real bashoratli modelga ega bo'lish bo'lsa, o'chirilishi kerak.
   # boshqa atributlar:
  12 - kampaniya: ushbu kampaniya davomida va ushbu mijoz uchun amalga oshirilgan kontaktlar soni (raqamli, oxirgi kontaktni o'z ichiga oladi)
  13 - pdays: mijoz bilan oldingi kampaniyadan so‘nggi marta bog‘langanidan keyin o‘tgan kunlar soni (raqamli; 999 mijoz avval bog‘lanmaganligini bildiradi)
  14 - oldingi: ushbu kampaniyadan oldin va ushbu mijoz uchun qilingan kontaktlar soni (raqamli)
  15 - poutcome: oldingi marketing kampaniyasining natijasi (kattegorik: "muvaffaqiyatsizlik", "mavjud emas", "muvaffaqiyat")
   # ijtimoiy va iqtisodiy kontekst atributlari
  16 - emp.var.rate: bandlikning o'zgarishi darajasi - choraklik ko'rsatkich (raqamli)
  17 - cons.price.idx: iste'mol narxlari indeksi - oylik ko'rsatkich (raqamli)     
  18 - cons.conf.idx: iste'molchi ishonch indeksi - oylik ko'rsatkich (raqamli)     
  19 - euribor3m: euribor 3 oylik kurs - kunlik ko'rsatkich (raqamli)
  20 - band bo'lmaganlar: xodimlar soni - choraklik ko'rsatkich (raqamli)

  Chiqish o'zgaruvchisi (kerakli maqsad):
  21 - y - mijoz muddatli depozitga obuna bo'lganmi? (ikkilik: "ha", "yo'q")
