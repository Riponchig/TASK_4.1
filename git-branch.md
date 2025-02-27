## Работа с ветками `git branch`

Команда `git branch` используется для работы с ветками в Git. Она позволяет создавать, удалять, переименовывать ветки и показывать список существующих веток.

### Синтаксис:
```bash
git branch [опции] [ветка]
```
- ветка — имя ветки, с которой вы хотите работать (например, создавать или удалять).

### Примеры использования:
1. Просмотр списка всех веток:

```bash
git branch
```
Эта команда выводит список всех веток в вашем репозитории. Ветка, на которой вы находитесь, будет отмечена звездочкой.

**Пример вывода:**

```bash
* main
  feature-branch
```
2. Создание новой ветки:

```bash
git branch feature-branch
```
Эта команда создаёт новую ветку с именем `feature-branch` на основе текущей ветки, но не переключает вас на неё.

3. Переключение на другую ветку: Чтобы переключиться на другую ветку, используйте команду `git checkout`, но с Git 2.23 и выше можно использовать новый синтаксис:

```bash
git switch feature-branch
```
Это переключит вас на ветку `feature-branch`.

4. Создание новой ветки и переключение на неё:

```bash
git checkout -b feature-branch
```
Это создаст новую ветку `feature-branch` и сразу переключит вас на неё.

5. Удаление ветки: 

Чтобы удалить ветку, используйте команду `git branch -d` для безопасного удаления или `-D` для принудительного удаления (например, если ветка не была слита).

```bash
git branch -d feature-branch
```
Принудительное удаление:

```bash
git branch -D feature-branch
```
6. Переименование ветки: Для переименования текущей ветки:

```bash
git branch -m new-branch-name
```
Чтобы переименовать ветку, на которой вы не находитесь:

```bash
git branch -m old-branch-name new-branch-name
```

### Полезные опции:
- `-a` — показывает все ветки, включая локальные и удалённые.

```bash
git branch -a
```
- `-r` — показывает только удалённые ветки.

```bash
git branch -r
```
- `-v` — показывает последние коммиты для каждой ветки.

```bash
git branch -v
```
- `--merged`— отображает все ветки, которые были слиты с текущей веткой.

```bash
git branch --merged
```
- `--no-merged` — отображает ветки, которые ещё не были слиты с текущей веткой.

```bash
git branch --no-merged
```
### Подробнее:
- [Слияние веток (git merge)](git-merge.md)

[К содержанию](readme.md)