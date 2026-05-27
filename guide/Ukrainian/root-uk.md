[← На головну сторінку](/guide/Ukrainian/README-uk.md)

# Гайд з отримання root-прав

## Метод 1: KernelSU-Next (Рекомендовано)

Це найпростіший метод. ПК не потрібен.

1. Завантажте останній APK **KernelSU-Next Manager** [звідси](https://github.com/KernelSU-Next/KernelSU-Next/releases).
2. Встановіть та відкрийте додаток.
3. Дотримуйтесь інструкцій на екрані.

> [!NOTE]
> InfinityX постачається з ядром, сумісним із KernelSU-Next. Якщо менеджер показує ваш пристрій як підтримуваний, ви готові до роботи.

## Готово! ✅

---

## Метод 2: Magisk

### Необхідне

- [Recovery Image (TWRP для nabu)](https://github.com/ArKT-7/twrp_device_xiaomi_nabu/releases/tag/mod-win)
- [Android Platform Tools](https://developer.android.com/studio/releases/platform-tools)
- [Magisk APK](https://github.com/topjohnwu/Magisk/releases/latest)

---

### Крок 1: Завантажтесь у fastboot

Вимкніть пристрій і утримуйте **Зменшення гучності + Живлення**, або виконайте:
```bash
adb -d reboot bootloader
```

Підключіть пристрій до ПК через USB.

---

### Крок 2: Завантажте образ рекавері

Замініть плейсхолдер на фактичний шлях до завантаженого образу рекавері:

```bash
# Windows:
fastboot boot path\to\recovery.img

# Linux / macOS:
fastboot boot path/to/recovery.img
```

---

### Крок 3: Прошийте Magisk через рекавері

Завантажте `magisk.apk` на ПК і виконайте:

```bash
# Windows:
adb push path\to\magisk.apk /tmp/magisk.zip && adb shell twrp install /tmp/magisk.zip

# Linux / macOS:
adb push path/to/magisk.apk /tmp/magisk.zip && adb shell twrp install /tmp/magisk.zip
```

---

### Крок 4: Перезавантажтесь в Android

```bash
adb reboot
```

> [!NOTE]
> Якщо пристрій не завантажується автоматично, утримуйте кнопку живлення для ручного перезавантаження.

---

### Крок 5: Завершіть налаштування Magisk

1. Встановіть [Magisk APK](https://github.com/topjohnwu/Magisk/releases/latest) на пристрій, якщо він ще не встановлений.
2. Відкрийте додаток **Magisk** і дотримуйтесь інструкцій на екрані.
3. Пристрій перезавантажиться для завершення патчингу.

## Готово! ✅
