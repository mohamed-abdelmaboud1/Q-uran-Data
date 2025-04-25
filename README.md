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
- [Quran API Documentation](https://quran.api-docs.io/)  
- [Additional Quran API](https://documenter.getpostman.com/view/7929737/TzkyMfPc)

### Prayer Times APIs

For accurate prayer timing data, consider using:

- [Muslim Salat API](https://lnkd.in/dnQWeB2K)  
- [Aladhan Prayer Times API](https://lnkd.in/diXsuM6U)

---

## 📂 CSV Usage in Flutter

To use the provided CSV files (e.g., `Sahih Bukhari.csv`) in a **Flutter** project, follow this approach:

1. **Place the file** in your `assets/data/` directory.

2. **Declare the asset** in `pubspec.yaml`:

```yaml
flutter:
  assets:
    - assets/data/Sahih Bukhari.csv
```

3. **Load and parse the file** in your code:

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

This will allow you to handle the CSV content line-by-line within your Flutter app.

---

## 📜 License

This repository is open for educational and non-commercial use. Please respect the integrity of the Islamic texts when using or modifying the data.
