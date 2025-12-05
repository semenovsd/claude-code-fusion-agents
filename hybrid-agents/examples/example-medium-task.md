# Пример: Средняя задача

## Задача
"Добавь страницу профиля пользователя с возможностью загрузки аватара"

## Workflow

### Шаг 1: Task Router
```
task-router анализирует задачу:
- Размер: Компонент + API endpoint
- Технологии: 2 (Frontend + Backend)
- Неопределенности: Некоторые (формат изображения, размер)
- Тип: Feature

Complexity: Medium
Score: 4

Routing Decision:
- Workflow: light
- Orchestrator: simple-coordinator
- Estimated Tokens: 60K
- Estimated Time: 10 minutes
```

### Шаг 2: Simple Coordinator
```
simple-coordinator анализирует задачу и выбирает команду:

Selected Agents:
- frontend-developer: Создание компонента профиля
- backend-developer: Создание API endpoint для загрузки

Coordination Pattern: Sequential (backend first, then frontend)
```

### Шаг 3: Backend Developer
```
backend-developer создает:
- API endpoint: POST /api/users/profile/avatar
- Валидация файла (формат, размер)
- Сохранение файла
- Обновление профиля пользователя
- Unit тесты
```

### Шаг 4: Frontend Developer
```
frontend-developer создает:
- Компонент UserProfile
- Форма загрузки аватара
- Интеграция с API
- Обработка loading/error состояний
- Unit тесты компонента
```

### Результат
```
✅ Задача выполнена
- Backend: API endpoint создан и протестирован
- Frontend: Компонент профиля создан и интегрирован
- Время: 12 минут
- Токены: 58K
```

## Метрики
- **Время**: 12 минут
- **Токены**: 58K (экономия 40% по сравнению с полным workflow)
- **Агентов**: 2
- **Quality Gates**: Базовые проверки
