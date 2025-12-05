# Пример: Сложная задача

## Задача
"Создай сервис аутентификации с OAuth2, JWT токенами и refresh токенами"

## Workflow

### Шаг 1: Task Router
```
task-router анализирует задачу:
- Размер: Полный сервис
- Технологии: 3+ (Backend, Database, Security)
- Неопределенности: Много (провайдеры OAuth, сроки токенов)
- Тип: New Service

Complexity: Complex
Score: 7

Routing Decision:
- Workflow: full
- Orchestrator: workflow-orchestrator
- Estimated Tokens: 300K
- Estimated Time: 90 minutes
```

### Шаг 2: Workflow Orchestrator - Planning Phase

#### Task Analyzer
```
Анализ задачи:
- Функциональные требования: OAuth2, JWT, refresh tokens
- Нефункциональные: Безопасность, производительность
- Неопределенности: Провайдеры OAuth, сроки токенов, хранилище токенов
```

#### Requirements Clarifier
```
Вопросы пользователю:
1. Какие OAuth провайдеры нужны? (Google, GitHub, etc.)
2. Срок действия access token? (15 минут)
3. Срок действия refresh token? (7 дней)
4. Где хранить refresh tokens? (Database)

Ответы получены → Требования уточнены
```

#### Tech Stack Detector
```
Обнаружен стек:
- Backend: Node.js + Express
- Database: PostgreSQL
- Auth: passport.js, jsonwebtoken

Рекомендации:
- OAuth: passport-google-oauth20, passport-github2
- JWT: jsonwebtoken
- Refresh tokens: Хранить в БД с хешированием
```

#### Plan Generator
```
Создан детальный план:
- Epic 1: OAuth2 интеграция
- Epic 2: JWT токены
- Epic 3: Refresh tokens
- Epic 4: API endpoints
- Epic 5: Тестирование

Зависимости определены
Параллельные задачи идентифицированы
```

#### Quality Gate 1
```
Planning Phase Validation:
- Requirements completeness: 96% ✅
- Architecture feasibility: Validated ✅
- Task breakdown: Adequate ✅
- Risk assessment: Complete ✅

Status: PASSED (Score: 96/100)
→ Переход к Development Phase
```

### Шаг 3: Workflow Orchestrator - Development Phase

#### Backend Architect
```
Создает архитектуру:
- Структура сервиса
- API endpoints
- Database schema
- Security patterns
```

#### Backend Developer
```
Реализует:
- OAuth2 стратегии (Google, GitHub)
- JWT генерация и валидация
- Refresh token система
- API endpoints
- Database migrations
```

#### Test Automator
```
Создает тесты:
- Unit тесты (покрытие 85%)
- Integration тесты
- Security тесты
```

#### Code Reviewer
```
Проводит code review:
- Quality Score: 88/100 ✅
- Security: No critical issues ✅
- Best practices: Followed ✅
```

#### Quality Gate 2
```
Development Phase Validation:
- Code quality: 88% ✅ (>85%)
- Test coverage: 85% ✅ (>80%)
- Performance: Benchmarks met ✅
- Security: No critical vulnerabilities ✅

Status: PASSED (Score: 88/100)
→ Переход к Validation Phase
```

### Шаг 4: Workflow Orchestrator - Validation Phase

#### Result Validator
```
Валидация результатов:
- Все требования выполнены ✅
- API работает корректно ✅
- Тесты проходят ✅
- Документация полная ✅
```

#### Security Auditor
```
Security audit:
- OAuth2 implementation: Secure ✅
- JWT handling: Secure ✅
- Token storage: Secure ✅
- No vulnerabilities found ✅
```

#### Quality Gate 3
```
Validation Phase Validation:
- Code review: Approved ✅
- All tests: Passing ✅
- Documentation: Complete ✅
- Deployment: Ready ✅

Status: PASSED (Score: 94/100)
→ Задача завершена
```

### Результат
```
✅ Задача выполнена
- Сервис аутентификации создан
- OAuth2, JWT, refresh tokens реализованы
- Тесты написаны (85% покрытие)
- Документация полная
- Production ready

Время: 95 минут
Токены: 312K
```

## Метрики
- **Время**: 95 минут
- **Токены**: 312K (экономия 7% от оценки благодаря оптимизации)
- **Агентов**: 7
- **Quality Gates**: Все пройдены
- **Итераций**: 0 (все gates прошли с первого раза)

## Deliverables
- `auth-service/` - Код сервиса
- `tests/` - Тесты (85% покрытие)
- `docs/` - Документация
- `migrations/` - Database migrations
- `README.md` - Инструкции по развертыванию
