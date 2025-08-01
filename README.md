# 🧠 CNN для классификации MNIST с интерактивным рисованием

Этот проект реализует сверточную нейронную сеть (CNN) для классификации рукописных цифр из набора данных MNIST. Проект оптимизирован для работы на GPU в Google Colab и включает интерактивные функции, такие как настройка гиперпараметров, визуализация карт активаций, матрицы ошибок и возможность рисовать цифры мышью для предсказания.

---

## 📦 Возможности

- ✅ **Обучение модели**: Интерактивный выбор количества эпох и размера батча с помощью `ipywidgets`.
- ✅ **Визуализация**: Отображение фильтров CNN, карт активаций, графиков точности/потерь и интерактивной матрицы ошибок с использованием `plotly`.
- ✅ **Анализ ошибок**: Визуализация неверно классифицированных изображений.
- ✅ **Интерактивное предсказание**: Выбор тестового изображения для предсказания.
- ✅ **Рисование цифр**: Пользователь может рисовать цифры на канвасе, а модель предсказывает класс с отображением уверенности и топ-3 вероятностей.

---

## 🚀 Установка и запуск

### Требования

- Google Colab с GPU (например, NVIDIA T4)
- Python 3.8+
- Зависимости (см. `requirements.txt`):
  - `tensorflow>=2.10`
  - `numpy`
  - `matplotlib`
  - `seaborn`
  - `plotly`
  - `ipywidgets`
  - `pillow`

### Установка

1. Откройте [Google Colab](https://colab.research.google.com).
2. Перейдите в `Runtime > Change runtime type` и выберите **GPU**.
3. Загрузите файл `cnn_mnist_gpu_drawing.ipynb` через `File > Upload Notebook`.
4. Установите зависимости:

```bash
!pip install -r requirements.txt
```

Или напрямую:

```bash
!pip install tensorflow numpy matplotlib seaborn plotly ipywidgets pillow
```

---

## 🛠 Использование

1. Выполните ячейки ноутбука по порядку (`Shift + Enter`).
2. В секции 3 настройте количество эпох и размер батча для обучения модели.
3. В секции 10 нарисуйте цифру на канвасе (размер 280x280), нажмите **Предсказать** для получения результата.
4. Используйте кнопку **Очистить** для стирания и повторного рисования.

> 💡 **Совет**: Для лучших результатов рисуйте чёткие белые цифры на чёрном фоне, как в MNIST.

---

## 📂 Структура проекта

```
cnn-mnist/
├── cnn_mnist_gpu_drawing.ipynb  # Основной ноутбук
├── README.md                    # Документация
├── requirements.txt             # Зависимости
```

---

## 🛑 Устранение неполадок

- **Ошибка: "Модель не обучена"**  
  Убедитесь, что вы выполнили ячейку с обучением (секция 3) перед использованием секций 9 или 10.

- **Проблемы с отображением канваса**  
  Проверьте, что вы используете Google Colab и JavaScript включен в браузере.

- **Низкая точность предсказаний для нарисованных цифр**  
  Рисуйте цифры в стиле MNIST (белые линии на черном фоне). Нечёткие или тонкие линии могут снизить точность.

- **Проблемы с зависимостями**  
  Убедитесь, что все библиотеки установлены. Если возникают конфликты версий — обновите среду.

---

## 📝 Примечания

- Для точного распознавания рисуйте цифры в стиле MNIST (белые линии на чёрном фоне).
- Проект оптимизирован для **GPU**, но также работает на **CPU** (медленнее).

---

## 📜 Лицензия

MIT License. См. файл `LICENSE` для деталей (если применимо).
