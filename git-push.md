## Отправка изменений `git push`

Команда `git push` используется для отправки локальных коммитов в удалённый репозиторий. Это позволяет синхронизировать изменения, сделанные в вашем локальном репозитории, с сервером или другим удалённым хранилищем, например GitHub или GitLab.

### Синтаксис:
```bash
git push [options] [remote_repository] [branch]
```
- [remote_repository] — это имя удалённого репозитория, например, `origin`.
- [branch] — это имя ветки, на которую вы хотите отправить изменения (по умолчанию `main` или `master`).

### Примеры использования:
1. Отправка изменений на основную ветку:
```bash
git push origin main
```
Отправляет коммиты из локальной ветки `main` в удалённый репозиторий `origin`.

2. Отправка изменений на другую ветку:

```bash
git push origin feature-branch
```
Отправляет коммиты из локальной ветки `feature-branch` в удалённый репозиторий `origin`.

3. Отправка всех веток:

```bash
git push --all origin
```
Отправляет все локальные ветки в удалённый репозиторий.

4. Отправка тегов:

```bash
git push origin --tags
```
Отправляет все локальные теги в удалённый репозиторий.

### Полезные опции:
- `-u` или `--set-upstream` — устанавливает отслеживаемую ветку для локальной ветки. После этого можно просто использовать `git push` без указания удалённого репозитория и ветки.

```bash
git push -u origin main
```
- `--force` или `-f` — принудительная отправка изменений, даже если это перезапишет историю на удалённой ветке. Обычно используется в случае, когда вы переписали историю с помощью `git rebase`.

```bash
git push --force origin main
```
- `--dry-run` — показывает, что будет сделано при использовании команды, без реального выполнения.

```bash
git push --dry-run
```
- `--delete` — удаляет ветку на удалённом репозитории.

```bash
git push origin --delete feature-branch
```

### Когда использовать `git push`?
1. Когда вы хотите синхронизировать ваши локальные изменения с удалённым репозиторием.
2. После того как вы выполнили коммит (`git commit`) и хотите отправить изменения в общий репозиторий для других участников проекта.
3. Чтобы поделиться вашими изменениями с коллегами или сохранить копию работы в облаке.

### Подробнее:

- [Фиксация изменений (git commit)](git-commit.md)

[К содержанию](readme.md)