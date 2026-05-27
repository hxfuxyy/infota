[← На главную страницу](/guide/Russian/README-ru.md)

# Руководство по получению root-прав

## Метод 1: KernelSU-Next (Рекомендуется)

Это самый простой метод. ПК не нужен.

1. Скачайте последний APK **KernelSU-Next Manager** [отсюда](https://github.com/KernelSU-Next/KernelSU-Next/releases).
2. Установите и откройте приложение.
3. Следуйте инструкциям на экране.

> [!NOTE]
> InfinityX поставляется с ядром, совместимым с KernelSU-Next. Если менеджер показывает ваше устройство как поддерживаемое, вы готовы к работе.

## Готово! ✅

---

## Метод 2: Magisk

### Необходимое

- [Recovery Image (TWRP для nabu)](https://github.com/ArKT-7/twrp_device_xiaomi_nabu/releases/tag/mod-win)
- [Android Platform Tools](https://developer.android.com/studio/releases/platform-tools)
- [Magisk APK](https://github.com/topjohnwu/Magisk/releases/latest)

---

### Шаг 1: Загрузитесь в fastboot

Выключите устройство и удерживайте **Уменьшение громкости + Питание**, или выполните:
```bash
adb -d reboot bootloader
```

Подключите устройство к ПК через USB.

---

### Шаг 2: Загрузите образ рекавери

Замените плейсхолдер на фактический путь к скачанному образу рекавери:

```bash
# Windows:
fastboot boot path\to\recovery.img

# Linux / macOS:
fastboot boot path/to/recovery.img
```

---

### Шаг 3: Прошейте Magisk через рекавери

Скачайте `magisk.apk` на ПК и выполните:

```bash
# Windows:
adb push path\to\magisk.apk /tmp/magisk.zip && adb shell twrp install /tmp/magisk.zip

# Linux / macOS:
adb push path/to/magisk.apk /tmp/magisk.zip && adb shell twrp install /tmp/magisk.zip
```

---

### Шаг 4: Перезагрузитесь в Android

```bash
adb reboot
```

> [!NOTE]
> Если устройство не загружается автоматически, удерживайте кнопку питания для ручной перезагрузки.

---

### Шаг 5: Завершите настройку Magisk

1. Установите [Magisk APK](https://github.com/topjohnwu/Magisk/releases/latest) на устройство, если он ещё не установлен.
2. Откройте приложение **Magisk** и следуйте инструкциям на экране.
3. Устройство перезагрузится для завершения патчинга.

## Готово! ✅
