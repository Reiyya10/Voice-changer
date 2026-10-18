# SuaraKu - AI Voice Changer (Vue 3 + Tailwind CSS)

Proyek tugas Desain Web. Vue 3 (Composition API), Vue Router (hash mode, 8 route), Tailwind CSS v4, Font Awesome.
Data, pemrosesan suara, dan pembayaran adalah simulasi (mode demo).

## Menjalankan
    npm install
    npm run dev        # buka http://localhost:5173
    npm run build      # hasil di folder dist/

## Route
/  /voice-changer  /karakter  /rekaman  /tentang  /masuk  /langganan  /akun (perlu login)

## Struktur
src/components : AppHeader, AppFooter, HeroSection, CharacterCard, CharacterModal, VoiceRecorder,
                 AudioPlayer, EffectSlider, PricingCard, ConfirmDialog, ToastNotification
src/views      : 8 halaman
src/store.js   : state (plan, credits, karakter terpilih)

## Upload ke GitHub
    git init && git add . && git commit -m "Initial commit: SuaraKu"
    git branch -M main
    git remote add origin https://github.com/USERNAME/suaraku.git
    git push -u origin main
