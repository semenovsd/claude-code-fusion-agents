# Пример: Простая задача

## Задача
"Исправь опечатку в UserService.java на строке 42: 'recieve' должно быть 'receive'"

## Workflow

### Шаг 1: Task Router
```
task-router анализирует задачу:
- Размер: 1 файл, 1 строка
- Технологии: 1 (Java)
- Неопределенности: Нет
- Тип: Bug fix

Complexity: Simple
Score: 1

Routing Decision:
- Workflow: direct
- Orchestrator: none
- Estimated Tokens: 15K
- Estimated Time: 2 minutes
```

### Шаг 2: Прямое выполнение
```
Прямое выполнение соответствующим агентом (java-expert или backend-developer):
- Читает файл UserService.java
- Находит строку 42
- Исправляет опечатку
- Сохраняет файл
```

### Результат
```
✅ Задача выполнена
- Файл: UserService.java
- Изменение: Строка 42, 'recieve' → 'receive'
- Время: 1.5 минуты
- Токены: 12K
```

## Метрики
- **Время**: 1.5 минуты
- **Токены**: 12K (экономия 60% по сравнению с полным workflow)
- **Агентов**: 1
- **Quality Gates**: Нет (не требуется для простых задач)
