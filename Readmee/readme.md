# Шпаргалка markdown

## Выделение текста

Вы можете выделять текст в markdown с помощью символов `_` или `*`. Например:

Пример _курсива_ и **жирного** текста.

## Заголовки

Заголовки можно создавать с помощью символа `#`. Чем больше `#`, тем меньше заголовок. Например:

# Заголовок первого уровня
## Заголовок второго уровня
### Заголовок третьего уровня

## Выделение кода

Чтобы выделить текст как код, поместите его в тройные кавычки `````. 

```
mkdir my_project
cd my_project
git init
```
Это лишь некоторые функции markdown. 

## Папка .git содержит много непонятных файлов — об одном из них мы рассказали в этом уроке. Подытожим:

В числе прочих файлов в папке .git есть служебный файл HEAD. Он указывает на самый свежий коммит.
Вместо хеша последнего коммита можно написать слово HEAD — Git вас поймёт.

## что такое хеш коммита и для чего он нужен. Подведём итоги:

Git преобразует информацию о коммитах с помощью алгоритма SHA-1 и для каждого из них рассчитывает уникальный идентификатор — хеш.
Хеш — основной идентификатор коммита и позволяет узнать его автора, дату и содержимое закоммиченных файлов.
Все хеши, а также таблицу соответствий хеш → информация о коммите Git хранит в папке .git.

## Cостояние и жизненный цикл файлов в Git чуть больше. Важное:

Статусом untracked помечается файл, о существовании которого Git знает, но не следит за изменениями в нём. Этот статус — противоположность tracked, в который попадают все файлы, отслеживаемые Git.
Файл переходит в статус staged после выполнения git add.
Статус modified означает, что файл был изменён.
Большинство файлов в проектах «шагает» по следующему циклу: «изменён» → «добавлен в список на коммит» → «закоммичен» → «изменён» → и так далее.

## Отлично! 
### Правильно описывать коммиты — искусство, к которому стоит приобщиться как можно раньше. Хорошо, когда:
1. сообщение коммита легко читается;
2. оно информативное;
3. все сообщения оформлены в одном стиле.  

## MERMAID

#### HEAD -- это голова.
#### Коммит -- это всему голова.

Статусы файлов:


```mermaid
%% коммментарий (описание схемы)
graph LR;
  untracked -- "git add" --> staged;
  staged    -- "commit"     --> tracked/comitted;

%% стрелка без текста для примера: 
  A --> B;
``` 
