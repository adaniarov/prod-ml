# prod-ml

Материалы курса и домашние задания.

- `papers/` — лекции.
- `homeworks/` — подмодуль с отдельным репозиторием GitLab для сдачи ДЗ.

## Работа на новом компьютере

Нужен SSH-доступ к GitHub и учебному GitLab.

```bash
git clone --recurse-submodules git@github.com:adaniarov/prod-ml.git
cd prod-ml/homeworks
git switch hw1
```

При клонировании подмодуль открывается на закреплённом коммите. Перед
редактированием переключитесь на ветку для сдачи (сейчас `hw1`).

Если проект уже клонирован без подмодулей:

```bash
git submodule update --init --recursive
```

## Сохранение и сдача ДЗ

Из `prod-ml/homeworks`, находясь в нужной ветке:

```bash
git add .
git commit -m "Update homework"
git push -u origin hw1
```

После успешной отправки в GitLab сохраните указатель в GitHub:

```bash
cd ..
git add homeworks
git commit -m "Update homework version"
git push
```

GitHub хранит адрес и коммит подмодуля, а файлы ДЗ загружаются из GitLab.
Неотправленные коммиты и локальные изменения не появятся на другом компьютере.
Настройка подмодуля не добавляет обратную ссылку на GitHub в GitLab.
