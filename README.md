# Bank – пример модульного тестирования на C# (MSTest)
[![MSTest](https://img.shields.io/badge/MSTest-4.0.1-green)](https://www.nuget.org/packages/MSTest/)

Данный проект демонстрирует создание и выполнение модульных тестов для класса банковского счёта с использованием фреймворка MSTest в Visual Studio. Проект создан в рамках практической работы по курсу тестирования ПО.

## 📋 Описание
Решение состоит из двух проектов:
- **Bank** – библиотека классов, содержащая основной класс `BankAccount`.
- **BankTests** – проект с модульными тестами для проверки логики работы `BankAccount`.

В ходе работы был реализован подход «красный-зелёный-рефакторинг» (TDD): первый тест выявил ошибку в коде, после исправления все тесты успешно проходят.

## 🚀 Технологии
- .NET 10.0
- MSTest 4.0.1 (мета-пакет)
- Visual Studio 2022 / .NET CLI

## 📁 Структура репозитория
├── Bank/ # Исходный код основного проекта
│ ├── BankAccount.cs # Класс банковского счёта
│ └── Bank.csproj
├── BankTests/ # Тестовый проект
│ ├── BankAccountTests.cs # Набор тестов
│ └── BankTests.csproj
├── .gitignore # Игнорируемые файлы Git
├── Bank.slnx # Файл решения Visual Studio
├── README.md # Этот файл
└── Report.md # Отчёт о выполненной работе (исходник Markdown)

## ✅ Запуск тестов

### В Visual Studio
1. Откройте файл решения `Bank.slnx`.
2. В меню выберите **Тест** → **Обозреватель тестов**.
3. Нажмите **Запустить всё**.

### Через .NET CLI
```bash
dotnet test BankTests/BankTests.csproj
```

## 📊 Результаты
Все три теста успешно проходят, подтверждая корректность метода Debit:

  `Debit_WithValidAmount_UpdatesBalance`

  `Debit_WhenAmountIsLessThanZero_ShouldThrowArgumentOutOfRange`

  `Debit_WhenAmountIsMoreThanBalance_ShouldThrowArgumentOutOfRange`

## 📄 Отчёт
Подробный отчёт о выполнении работы доступен в файле Report.md (исходный текст) и сконвертированной версии Report.pdf (если есть).

## 📌 Автор
[Бахматов Матвей / Linkimin]
GitHub: @Linkimin

