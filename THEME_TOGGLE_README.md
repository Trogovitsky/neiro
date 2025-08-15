# Переключатель темы для НейроКофейни

Красивый и функциональный переключатель темы с анимациями, похожий на пример из CodePen.

## 🎨 Особенности

- **Две темы**: Темная и светлая с плавными переходами
- **Адаптивный дизайн**: Автоматически адаптируется под размер экрана
- **Сохранение настроек**: Выбор темы сохраняется в localStorage
- **Автоопределение**: Учитывает системные настройки темы
- **Звуковые эффекты**: Приятные звуки при переключении
- **Тактильная обратная связь**: Вибрация на мобильных устройствах
- **Горячие клавиши**: Ctrl/Cmd + T для быстрого переключения
- **Ripple эффект**: Красивая анимация при клике

## 📁 Структура файлов

```
new/
├── css/
│   └── theme-toggle.css          # Стили переключателя темы
├── js/
│   └── theme-toggle.js           # JavaScript функциональность
├── index.html                    # Главная страница
├── menu.html                     # Страница меню
├── services.html                 # Страница услуг
├── contact.html                  # Страница контактов
├── theme-demo.html               # Демонстрационная страница
└── THEME_TOGGLE_README.md        # Этот файл
```

## 🚀 Установка

1. **Подключите CSS файл** в `<head>` вашего HTML:
```html
<link rel="stylesheet" href="css/theme-toggle.css">
```

2. **Подключите JavaScript файл** перед закрывающим тегом `</body>`:
```html
<script src="js/theme-toggle.js"></script>
```

3. **Готово!** Переключатель темы автоматически появится в правом верхнем углу.

## 🎯 Использование

### Автоматическое создание
Переключатель создается автоматически при загрузке страницы:

```javascript
// Переключатель создается автоматически
window.themeToggle = new EnhancedThemeToggle();
```

### Программное управление
```javascript
// Переключить тему
window.themeToggle.toggleTheme();

// Установить конкретную тему
window.themeToggle.setTheme('dark');  // или 'light'

// Получить текущую тему
const currentTheme = window.themeToggle.getCurrentTheme();
```

### Горячие клавиши
- **Ctrl/Cmd + T**: Переключить тему

## 🎨 Кастомизация

### Изменение позиции
Отредактируйте CSS в `theme-toggle.css`:

```css
.theme-toggle-container {
    position: fixed;
    top: 20px;          /* Измените позицию по вертикали */
    right: 20px;        /* Измените позицию по горизонтали */
    z-index: 1001;
}
```

### Изменение размеров
```css
.theme-toggle {
    width: 60px;        /* Ширина переключателя */
    height: 30px;       /* Высота переключателя */
}
```

### Изменение цветов
```css
.theme-toggle {
    background: linear-gradient(45deg, #667eea 0%, #764ba2 100%);
}

.theme-toggle.dark .toggle-bg {
    background: linear-gradient(45deg, #2c3e50 0%, #34495e 100%);
}
```

## 🌙 Темы

### Темная тема (dark-theme)
- Темный градиентный фон
- Светлый текст
- Полупрозрачные элементы
- Подходит для вечернего просмотра

### Светлая тема (light-theme)
- Светлый градиентный фон
- Темный текст
- Прозрачные элементы
- Подходит для дневного просмотра

## 📱 Адаптивность

Переключатель автоматически адаптируется под размер экрана:

- **Desktop**: Полный размер с текстом
- **Tablet**: Уменьшенный размер
- **Mobile**: Минимальный размер, текст скрыт

## 🔧 API

### Класс ThemeToggle

```javascript
class ThemeToggle {
    constructor()                    // Инициализация
    toggleTheme()                    // Переключить тему
    setTheme(theme)                  // Установить тему
    getCurrentTheme()                // Получить текущую тему
    saveTheme()                      // Сохранить тему
    loadSavedTheme()                 // Загрузить сохраненную тему
}
```

### Класс EnhancedThemeToggle

Расширенная версия с дополнительными функциями:

```javascript
class EnhancedThemeToggle extends ThemeToggle {
    addSystemThemeDetection()        // Автоопределение системной темы
    addThemeTransitionEffects()      // Добавить эффекты переходов
    playToggleSound()                // Воспроизвести звук
}
```

## 🎵 Звуковые эффекты

Переключатель использует Web Audio API для создания приятных звуковых эффектов:

- Частота: 800Hz → 600Hz
- Длительность: 0.1 секунды
- Громкость: 0.1 (10%)

## 📱 Мобильные устройства

### Тактильная обратная связь
```javascript
if ('vibrate' in navigator) {
    navigator.vibrate(50);  // Вибрация 50ms
}
```

### Адаптивный дизайн
- Уменьшенные размеры на маленьких экранах
- Скрытие текста для экономии места
- Оптимизированные touch-события

## 🔒 Безопасность

- Проверка поддержки localStorage
- Обработка ошибок при сохранении/загрузке
- Fallback на системные настройки

## 🐛 Отладка

### Проверка работы
```javascript
// В консоли браузера
console.log(window.themeToggle.getCurrentTheme());
console.log(localStorage.getItem('neuro-cafe-theme'));
```

### Включение отладки
```javascript
// Добавьте в theme-toggle.js
const DEBUG = true;
if (DEBUG) {
    console.log('Theme toggle initialized');
}
```

## 📋 Совместимость

- **Браузеры**: Chrome, Firefox, Safari, Edge
- **Версии**: ES6+ (современные браузеры)
- **Мобильные**: iOS Safari, Chrome Mobile
- **Полифиллы**: Не требуются

## 🎨 Демонстрация

Откройте `theme-demo.html` для интерактивной демонстрации всех возможностей переключателя темы.

## 📝 Лицензия

Разработано для проекта НейроКофейня.
Автор: Trogovitsky (https://t.me/Tisha_sir)

## 🤝 Поддержка

Если у вас есть вопросы или предложения:
- Telegram: https://t.me/Tisha_sir
- Email: TishUp@yandex.ru
- Сайт: https://ssir-team.ru/ 