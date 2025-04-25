
# بِسْمِ اللَّهِ الرَّحْمَٰنِ الرَّحِيمِ

# 📚 Q-uran-Data

![ChatGPT Image Apr 25, 2025, 06_09_36 PM](https://github.com/user-attachments/assets/b17c659d-e475-4d54-af24-e0b02986c7ad)

This repository contains well-structured datasets related to Islamic content, including:

- **azkar**  
  Contains daily supplications and remembrance (أذكار الصباح والمساء) categorized for easy access.

- **duaa**  
  Includes a wide variety of Islamic supplications (دعاء) from authentic sources.

- **hadith**  
  Contains CSV files for Hadith collections such as *Sahih Bukhari*, structured for analysis and display in applications.

- **names of allah**  
  A dataset of the 99 names of Allah (أسماء الله الحسنى) with meanings and descriptions.

- **tagweed**  
  Information and rules of Tajweed (تجويد), useful for learning Quranic recitation properly.

- **tasbeeh**  
  Structured dhikr and tasbeeh (تسبيح) data for use in digital rosary apps or spiritual reminder tools.

- **surahs.json**  
  JSON file containing metadata about Quranic surahs (chapter names, number of verses, etc.).

> ⚠️ **Note**: This repository provides **data files only**. It is not a standalone app or executable project.

---

## 🌐 Resources

### Quran APIs

To integrate dynamic Quran content into your apps or platforms, you can use the following APIs:

- [AlQuran Cloud API](https://alquran.cloud/api)  
- [Additional Quran API (Postman)](https://documenter.getpostman.com/view/7929737/TzkyMfPc)
  
### Quran Datasets

Useful open-source datasets for Quranic content:

- [Quran JSON Dataset by @semarketir](https://github.com/semarketir/quranjson)  
  A well-structured JSON format of the Quran with metadata, translations, and verse indexing.

- [Quran Data by @rn0x](https://github.com/rn0x/Quran-Data)  
  A collection of Quranic data including text, translations, and audio links in multiple formats.

### Prayer Times APIs

For accurate prayer timing data, consider using:

- [Muslim Salat API](https://lnkd.in/dnQWeB2K)  
- [Aladhan Prayer Times API](https://lnkd.in/diXsuM6U)

---

## 📦 Useful Flutter Packages

To build a complete Islamic app experience, the following Flutter packages are highly recommended:

- [`hijri`](https://pub.dev/packages/hijri)  
  Islamic Hijri calendar support for your Flutter app.

- [`adhan`](https://pub.dev/packages/adhan)  
  Advanced and reliable prayer time calculations.

- [`adhan_dart`](https://pub.dev/packages/adhan_dart)  
  Precise prayer time calculations in Dart (alternative to above).

- [`flutter_qiblah`](https://pub.dev/packages/flutter_qiblah)  
  A Flutter plugin to find Qiblah direction using device sensors.

- [`quran_library`](https://pub.dev/packages/quran_library)  
  Access to Quranic verses, Surahs, and metadata with search capabilities.
  
- [`location`](https://pub.dev/packages/location)  
  Get the user's real-time location — essential for calculating accurate prayer times and Qiblah direction.

- [`geolocator`](https://pub.dev/packages/geolocator)  
  Another reliable location plugin with geocoding and distance calculation features.

- [`just_audio`](https://pub.dev/packages/just_audio)  
  A powerful audio player to support Quran recitations, background dhikr, or app sound effects.

- [`assets_audio_player`](https://pub.dev/packages/assets_audio_player)  
  Play audio files from assets — useful for offline Quran and Azkar recitations.
---

## 📂 CSV Usage in Flutter

To use the provided CSV files (e.g., `Sahih Bukhari.csv`) in a **Flutter** project:

1. **Place the file** in your `assets/data/` directory.

2. **Declare the asset** in `pubspec.yaml`:

```yaml
flutter:
  assets:
    - assets/data/Sahih Bukhari.csv
```

3. **Load and parse the file** in your Dart code:

```dart
Future<String> loadAsset(String path) async {
  return await rootBundle.loadString(path);
}

void loadCSV() {
  loadAsset('assets/data/Sahih Bukhari.csv').then((String output) {
    setState(() {
      _data = output.split("\n");
    });
  });
}
```

---

## 📜 License

This repository is open for educational and non-commercial use.  
Please respect the authenticity and integrity of Islamic texts when using or modifying this data.

