# Tebranma harakatlar — interaktiv fizika prezentatsiyasi (Android ilova)

20 slaydli interaktiv dars (simulyatsiyalar, virtual laboratoriya, viktorina) Android ilova ko‘rinishida.
Prezentatsiya oddiy HTML fayl: `app/src/main/assets/index.html` — ilova uni WebView orqali ochadi, internet kerak emas.

## APK olish (eng oson yo‘l — GitHub Actions)

1. GitHub da yangi repozitoriy oching va shu papkadagi hamma fayllarni yuklang (`git push`).
2. **Actions** bo‘limiga o‘ting → **Build APK** ishga tushadi (yoki *Run workflow* ni bosing).
3. Tugagach, ish sahifasi pastidagi **Artifacts** dan `Tebranma-harakatlar-apk` ni yuklab oling.
4. Telefonga o‘tkazib, o‘rnating (Sozlamalar → «Noma’lum manbalardan o‘rnatish»ga ruxsat bering).

`v1.0` kabi teg (`git tag v1.0 && git push --tags`) qo‘ysangiz, APK **Releases** bo‘limiga ham joylanadi.

## Kompyuterda yig‘ish

Android Studio (Hedgehog yoki yangiroq) da papkani oching → **Build → Build APK(s)**.
Yoki terminalda (JDK 17 + Android SDK + Gradle 8.7):

```
gradle assembleDebug
```

Natija: `app/build/outputs/apk/debug/app-debug.apk`

## Slaydni o‘zgartirish

`app/src/main/assets/index.html` ni tahrirlang, so‘ng qayta yig‘ing.

## Boshqaruv

- Ekranni surish yoki pastdagi panel — slaydlarni almashtirish
- «Orqaga» tugmasi — oldingi slayd (birinchi slaydda ilovadan chiqadi)
- Ilova gorizontal (landscape) rejimda, to‘liq ekranda ishlaydi

Paket nomi: `uz.fizika.tebranma` · minSdk 21 (Android 5.0+)
