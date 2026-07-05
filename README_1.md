# Viral Guard V4 Pro

Tamamen Kotlin, Jetpack Compose, Material Design 3 ile geliştirilmiş profesyonel Android video haber uygulaması.

## Özellikler
- Video seç / kamera ile çek
- ExoPlayer önizleme
- ElevenLabs ses klonlama ve TTS
- OpenAI ile metni TRT Ana Haber, Belgesel, Son Dakika, Sosyal Medya Spikeri stiline dönüştürme
- Whisper ile otomatik altyazı
- FFmpeg Kit ile ses, müzik, altyazı işleme, gürültü azaltma (afftdn)
- H.264 MP4 çıktı
- Koyu tema, Türkçe arayüz
- MVVM + Room + Retrofit + Coroutines

## Kurulum
1. Android Studio Hedgehog veya üstü
2. Projeyi aç: `ViralGuardV4Pro`
3. `local.properties` dosyasına ekle:
```
OPENAI_API_KEY=sk-...
ELEVENLABS_API_KEY=...
```
4. Gradle sync, Run

## İzinler
Kamera, mikrofon, medya (Android 10+ uyumlu)

## Mimari
- `ui.screens` : Compose ekranlar
- `viewmodel` : ProjectViewModel, VoiceViewModel
- `data.remote` : OpenAI, ElevenLabs
- `data.local` : Room
- `utils` : FFmpegProcessor, FileUtils

## Release APK
1. Build > Generate Signed Bundle / APK
2. Keystore oluştur
3. release build al
4. Çıktı: `app/release/app-release.apk`

## Notlar
- ElevenLabs ses klonlama için en az 60 saniye temiz ses kaydı önerilir
- FFmpeg ilk çalıştırmada ~40MB indirir
- API anahtarları BuildConfig ile güvenli tutulur
