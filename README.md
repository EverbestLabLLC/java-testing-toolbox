# Java Testing Toolbox [Tarjima]
[Java Testing Toolbox](https://leanpub.com/java-testing-toolbox/) by Philip Riecks

## Kirish

Java test ekotizimi juda keng. Yillar davomida ko'plab kutubxonalar paydo bo'ldi. Ularning orasida eng mashhurlari: JUnit va Mockito. Java ilovasi uchun birinchi marta testlar yozganingizda, odatda dastlab kurashadigan kutubxonalar shulardir. Omadingiz kelsa, siz allaqachon martaba boshida ushbu kutubxonalarga duch kelasiz. Kamida men uchun shunday bo'lgan. Universitetda biz test mavzusiga chuqur kirib chiqmagan birgina darsimiz bo'lgan. Afsuski, bu dars "Java Ilovalarini Test Qilish 101" deb nomlanuvchi qulay va yangi boshlanuvchilar uchun mo'ljallangan ma'ruza emas edi. Bu ancha qattiqqo'l edi. 

Bizning test yozish motivatsiyamiz mutlaqo boshqacha edi. Sinfdan o'tish uchun taqdim etilgan dasturiy ta'minotda testlar bo'lishi kerak edi. Aks holda, biz topshiriqdan qolardik. Ushbu testlarning sifati muhim emas edi...

Sizning Java ilovalarini test qilishga birinchi tanishingiz butunlay boshqacha bo'lishi mumkin. Ko'plab dasturchilar birinchi marta testlarni faqat birinchi pull so'rovini rad etilgandan keyin yozishadi, chunki ular yo'q. Baribir, Java test safari qanday boshlangan bo'lsa, men ishonamanki, dastlab uchratgan kutubxonalar JUnit va Mockito bo'lgan. Ushbu vositalar sizning butun safaringiz davomida siz bilan birga bo'ladi.

Lekin Java test ekotizimida JUnit va Mockito'dan boshqa ko'p narsalar bor! Java'nin log tizimiga qaraganda, Java test manzarasi aniq tashkil etilgan. Ko'pchilik kutubxonalar aniq maqsadni bajaradi va g'ildirakni qayta ixtiro qilmaydi. Albatta, bir-birining o'rnini bosuvchi kutubxonalar mavjud. Turli xil vositalar (log qilishdan farqli o'laroq) turli test uslublari va texnikalarini mumkin qiladi.

Bundan tashqari, Java test ekotizimi yetukdir. Har kuni yangi kutubxonalar paydo bo'ladigan qiziqarli va rivojlanayotgan ekotizimni topa olmaysiz. Ammo, ko'plab Java test kutubxonalari va vositalari yetarlicha e'tiborga sazovor emas va har bir dasturchining radari doirasida emas.

Bu vaqt tugadi!

Ushbu kitob bilan siz Java test ekotizimining batafsil ko'rinishini olasiz va quyidagi kategoriyalardagi zaruriy vositalar va kutubxonalar haqida bilib olasiz:
- Test freymvorklari
- Tasdiqlash kutubxonalari
- Mocking kutubxonalari
- Test infratuzilma kutubxonalari
- Ishlashni test qilish uchun kutubxonalar va vositalar
- Foydali kutubxonalar va vositalar

Iltimos, bilish kerak va ishlatish kerak orasidagi nozik, lekin muhim farqni unutmang. Men har bir loyiha uchun barcha kutubxonalarni qo'shishni tavsiya qilmayapman. Bu juda ko'p bo'lardi. Aksincha, maqsad turli xil vositalar va kutubxonalar haqida xabardorlikni oshirishdir. Keyingi safar siz X muammosiga duch kelganingizda, Y va Z kutubxonalari mavjudligini bilasiz.

## Muqaddima

### Bu kitobni kimlar o'qishi kerak?
Bunga javob berish oson: Testga e'tibor beradigan va ish uchun to'g'ri vositalarni ishlatishni xohlaydigan har bir Java dasturchisi. Umid qilamanki, bu ko'pchilik dasturchilarni o'z ichiga oladi.

Yoqqaniga yoki yoqmaganiga qaramay, dasturiy ta'minot ishlab chiqish hunarmandchilik bilan taqqoslanadi. Hunarmandlar qanday qilib to'g'ri vositalarni ishlatayotganliklarini bilishadi? Agar ularning hammasi faqat bolg'a bo'lsa, hamma narsa mix kabi ko'rinadi. 

Hunarmandlar avvalo o'z asboblar qutisida nima borligini bilishlari, bu vositalarni o‘tkirlashtirishlari kerak, shundan keyingina ular mavjud muammoni samarali hal qilishlari mumkin.

Ushbu kitobning mavzusiga qaytsak, Java dasturchilari sifatida biz o‘z testlarimizni samarali yozishimizdan oldin, Java test ekotizimi nimalarni taqdim etishini bilishimiz kerak. Aks holda, biz noto‘g‘ri vositalar bilan ko‘p vaqtimizni behuda sarflaymiz va faqat bolg‘a bilan ishlaymiz.

Xususan, noaniq test mavzulari uchun (masalan, asinxron kod) sizning o'zingiz yaratgan test freymvorkingiz g'ildirakni qayta ixtiro qilishi ehtimoli yuqori. Bunday holda, tayyor yechim bilan ishlash yaxshiroq (va tezroq) bo'lishi mumkin. Siz omadlisiz, chunki endi ushbu kitobni qo'lingizga oldingiz.

Ushbu kitobning o'quvchisi sifatida siz faqat ikkita talablarga javob berishingiz kerak:
- Siz Java kodini o'qish va tushunish qobiliyatiga egasiz
- Siz test asboblar qutingizni yaxshilashga qiziqasiz.

Agar siz Kotlin yoki Scala kabi boshqa JVM tillarida ishlayotgan bo'lsangiz, bu kitob hali ham foydali bo'ladi. Ko'pchilik vositalar va kutubxonalar boshqa JVM tillari bilan tayyor ishlaydi yoki integratsiya uchun qo'shimcha modullarni taqdim etadi.

Ba'zi test kutubxonalari uchun biz ishlaydigan ilova kerak (masalan, REST API-ni test qilishda). Shuning uchun kitobda Spring Boot namunaviy ilovasi bilan ishlaymiz. Biroq, barcha kod misollari ilova freymvorkiga bog'liq bo'lmagan holda berilgan.

Shuningdek, ushbu kitob nimani qamrab olmasligini tushuntirish muhim. Biz TDD (Test-drevan-Development) yoki test qilish bo'yicha maxsus maslahatlar va usullar kabi mavzularni qamrab olmaymiz. Bu mavzular allaqachon quyidagi ajoyib kitoblarda yoritilgan:
- *Growing Object-Oriented Software, Guided by Tests* — Steve Freeman va Nat Pryce tomonidan
- *Unit Testing: Principles, Practices, and Patterns* — Vladimir Khorikov tomonidan
- ... yoki Kent Beck tomonidan yozilgan *Test Driven Development: By Example* nomli kitob.

### Ushbu kitobning tuzilishi
Ushbu kitob har bir testing vositasi va kutubxonasini bir xil "retseptlar kitobi" uslubida taqdim etadi:
- Kirish va ma'lumotlar varag'i
- Maven va Gradle uchun sozlash
- Eng ko'p qo'llaniladigan foydalanish usullari (Pareto printsipiga ko'ra, 20% xususiyatlar 80% vaqt davomida ishlatiladi).

Bundan tashqari, har bir bo'lim quyidagi savollarga javob beradi:
- Kutubxonaning asosiy API'si nima?
- Ushbu vosita yoki kutubxona menga qanday yordam beradi?
- U bilan ishlashda qanday muammolar bor?

Kitobning asosiy maqsadi sizning test qutingizni yangi vositalar va kutubxonalar bilan boyitishdir, balki hali ular haqida eshitmagan bo'lishingiz ham mumkin. Shuningdek, siz allaqachon ishlatayotgan test vositalarining yangi xususiyatlarini ham bilib olasiz.

Ushbu kitob sizga kutubxonani birinchi marta ko'rish imkoniyatini beradi. Bir nechta joylarda sizni texnologiyani batafsil tushuntiruvchi qo'shimcha resurslarga (kitoblar, videolar, maqolalar) havolalar topasiz.

Kitobda namoyish etilgan kutubxonalar va vositalarning soni yakuniy emas. Bu raqam kitobning har bir nashri bilan oshib boradi.

Men o'zimning test ko'nikmalarimni rivojlantirganimda va yangi test vositalari va kutubxonalari haqida bilganimda, “X Java Dasturchisi Bilishi Kerak bo'lgan Test Vositalari va Kutubxonalari”dagi X soni oraliq va oshib borayotgan ko'rsatkichdir.

### Ushbu kitobda ishlatiladigan konventsiyalar
Ko'pgina kod misollari uchun men statik bo'lmagan importlarni afzal ko'raman:
```java
Assertions.assertThat("duke").contains("d");
```
Bu misollarga qo'shimcha qiyinchilik qo'shsa-da, ularni aniq qiladi.

Xususan, Java'da yangi bo'lganlar importlarni osonlikcha chalkashtirib yuborishlari mumkin. Ushbu konventsiya noto'g'ri Java sinflarini ishlatishdan kelib chiqadigan bosh og'rig'idan qochishga yordam beradi (barchamiz bu holatga tushganmiz).

Misollarni loyihalaringiz uchun kiritganingizda, ba'zi bir klavishlarni saqlash uchun statik importlardan foydalanishni tavsiya qilaman:
```java
import static org.assertj.core.api.Assertions.*;
assertThat("duke").contains("d");
```
Bundan tashqari, kitobda *cut* (Class Under Test) qisqartmasi bir necha bor uchraydi. Ushbu o'zgaruvchi biz sinov qilayotgan ma'lum sinfga ishora qiladi. Test sinflarimiz odatda bir nechta maydon va mahalliy o'zgaruvchilarni o'z ichiga oladi, shuning uchun biz haqiqiy test subyekti haqida osonlikcha chalkashib ketishimiz mumkin. Ushbu konventsiya yordamida hamma narsa aniq bo'ladi. Boshqa mualliflar ba'zida *sut* (Subject Under Test) atamasini ham ishlatadilar.

Test misollari *given/when/then* (yoki *arrange/act/assert*) o'rnatilishiga amal qiladi. Har bir qism yangi qator bilan ajratiladi:
```java
@Test
void shouldPropagateException() {
  // given
  Mockito.when(userRepository.findByUsername("devil"))
    .thenThrow(new RuntimeException("DEVIL'S SQL EXCEPTION"));
  // when
  assertThrows(RuntimeException.class, () -> cut.registerUser("devil"));
  // then
  Mockito.verify(userRepository, never()).save(ArgumentMatchers.any(User.class));
  Mockito.verify(userRepository, times(1)).findByUsername("devil");
}
```
Barcha kod misollari GitHub'da mavjud. Biz turli xil vositalar va kutubxonalarni namoyish qilish uchun Spring Boot va Jakarta EE ilovasidan foydalanamiz. Kod misollari `src/test/java` ichidagi vosita nomidagi ajratilgan paketda joylashgan (Spring Boot va Jakarta EE). Agar boshqacha ko'rsatilmagan bo'lsa, testlar odatiy bo'lib `spring-boot-example` ilovasining bir qismi hisoblanadi.

### E'tiroflar
Men Java ilovalarini sinovdan o'tkazishni yanada yoqimli qilish uchun o'z vaqtini bag'ishlaydigan ko'plab ochiq manba dasturchilardan chin dildan minnatdorman. Juda ko'p yillar davomida ko'pchilik test kutubxonalari faol qo'llab-quvvatlanayotgani juda yaxshi.

Java dasturchisi bo'lish uchun ajoyib vaqt!

Maxsus rahmat Wim Deblauwe va Lorenzo Bettini'ga, ular texnik sharhlovchilar sifatida ko'ngilli bo'lib ishladilar. Ularning fikr-mulohazalari ushbu kitobning bir nechta boblarini qayta ko'rib chiqishda muhim rol o'ynadi.

Maxsus rahmat mening qiz do'stim Jessiga. U menga yozish uslubini yaxshilashga yordam berdi va ushbu kitob ustida ishlagan tonggi vaqtlarda mazali ovqat (porridge) bilan qo'llab-quvvatladi

.

### Hissa qo'shganlar
**Pradeep Murugesan** 
Pradeep Murugesan — Wise'da dasturiy ta'minot muhandisi, 2 yoshli bolaning otasi va London, Buyuk Britaniyada yashovchi kriket ishqibozi. U har kuni Java'da ishlaydi va bo'sh vaqtlarida ochiq manbali loyihalarga hissa qo'shadi. Endi texnik yozuvlar va bloglarga qo'l urmoqda.

**Texnik sharhlovchilar haqida**
**Wim Deblauwe** — 20 yildan ortiq tajribaga ega bo‘lgan frilanser Java dasturchisi. U *Testcontainers-Cypress* kutubxonasining muallifi bo'lib, Spring Boot va Thymeleaf bo'yicha kitob yozgan.

**Lorenzo Bettini** — Florensiya universitetida kompyuter fanlari bo'yicha dotsent. U 90 dan ortiq ilmiy ishlar muallifi va ko'plab kitoblar yozgan, shu jumladan *Test-Driven Development*.

### Muallif haqida
Filipp Berlin shahrida yashovchi IT-konsultant. U 2015 yildan beri Java bilan ishlaydi va ko'plab sohalarda bir nechta ilovalarda foydalanib kelmoqda. Sinov uning kundalik ishining muhim qismidir, chunki u puxta hunarmand.

Siz Filipp bilan turli platformalarda bog'lanishingiz mumkin:
- Twitter
- LinkedIn
- GitHub

Yetarli muqaddima qildik, boshlaymiz!
