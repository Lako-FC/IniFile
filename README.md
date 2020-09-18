<p align="center"> 
  <img align="center" src="https://github.com/Lako-FC/IniFile/blob/master/logo.png?raw=true" width="150"/> 
</p>

<h1><div align="center">IniFile</h1>
<p align="center">
  <img src="https://img.shields.io/badge/PRICE-free-%231DC8EE"/>
  <img src="https://img.shields.io/badge/SUPPORT-yes-%231DC8EE"/>
</p>

<p align="center">
  <img src="https://img.shields.io/github/downloads/Lako-FC/IniFile/total?color=%231DC8EE&label=DOWNLOADS&logo=GitHub&logoColor=%231DC8EE&style=flat"/>
  <img src="https://img.shields.io/github/last-commit/Lako-FC/IniFile?color=%231DC8EE&label=LAST%20COMMIT&style=flat"/>
  <img src="https://img.shields.io/github/release-date/Lako-FC/IniFile?color=%231DC8EE&label=RELEASE%20DATE&style=flat"/>
</p>

<p align="center">
  Данный класс представляет возможность работы с <b>ini-файлами</b> на основе вызовов функций из <b>kernel32.dll</b>.
</p>

[releases]: https://github.com/Lako-FC/IniFile/releases/

## 🔧 Основной функционал
- <b>Write</b> устанавливает строковые значения в ini-файлах. 
- <b>ReadString</b> читает строковые значения из ini-файлов.
- <b>ReadInt</b> читает числовое значение заданного ключа из ini-файла.
- <b>ReadBool</b> читает логическое значение заданного ключа из ini-файла.
- <b>GetAllDataSection</b> извлекает все ключи и значения для указанной секции файла инициализации.
- <b>GetAllSections</b> извлекает имена всех секций в файле инициализации.
- <b>DeleteKey</b> удаляет значение заданного ключа в определенной секции.
- <b>DeleteSection</b> удаляет заданную секцию.
- <b>KeyExists</b> производит чтение ключа по определенной секции и проверяет наличие значения.

## 🚀 Как использовать

- ### Инициализация класса 
1. Скачайте последний **релиз** : **[Releases][releases]**.
2. Добавьте файл `IniFile.cs` в свой проект.
3. Инициализируйте класс: 
```csharp
IniFile iniFile = new IniFile("file_name.ini");
```

- ### Примеры использования
1. Запись строкового значения ключа:
```csharp
iniFile.Write("KEY", "value", "SECTION");
```
2. Чтение строкового значения ключа (<b>return: string</b>):
```csharp
iniFile.ReadString("KEY", "value", "SECTION");
```
3. Чтение числового значения ключа (<b>return: int</b>):
```csharp
iniFile.ReadInt("KEY", "SECTION");
```
4. Чтение логического значения ключа (<b>return: bool</b>):
```csharp
iniFile.ReadBool("KEY", "SECTION");
```
5. Получение всех ключей и их значений в определенной секции (<b>return: string[]</b>):
```csharp
iniFile.GetAllDataSection("SECTION");
```
6. Получение имен всех секций (<b>return: string[]</b>):
```csharp
iniFile.GetAllSections();
```
7. Удаление значения заданного ключа в определенной секции:
```csharp
iniFile.DeleteKey("KEY", "SECTION");
```
8. Удаление заданной секции:
```csharp
iniFile.DeleteSection("SECTION");
```
9. Чтение ключа по определенной секции и проверка наличия значения (<b>return: bool</b>):
```csharp
iniFile.KeyExists("KEY", "SECTION");
```
