# Kredit_berishni_bashorat_qilish

1. Sarlavha: Bank marketingi (ijtimoiy/iqtisodiy)
   


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
