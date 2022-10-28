# Как легко и просто редактировать сайт с помощью Chrome

## Важно

Редачить можно `ТОЛЬКО В ПРИВАТЕ` (если ее нет в привате, попросите Вову залить ее вам)

## Подготовка

> Скачать транзитку и приберечь, если что-то пойдет не так, чтобы восстановить

![Keitaro](./images/keitaro-export.jpg)

> Переход в редактор

Чтобы зайти в редактор открываем транзитку в режим просмотра. Как только она открылась, открываем инспектор кода нажатием F12 (либо ПКМ -> Просмотреть код/Inspect)

> Важные замечания

Во время редактирования **не перезагружать** эту вкладку, иначе прогресс не сохранится !

Сохранять прогресс можно только с помощью расширения

Не забывайте, что вы может откатывать любое действие как обычно `Ctrl + Z`

---

## Как редактировать текст

Открываем консоль и вводдим следующую команду

```
document.designMode="on"
```

![Rewrite](./images/rewrite-text.jpg)

Нажимаем ENTER

> Обязательно, если копируете текст вставлять его через `Ctrl + Shift + V`, чтобы стили текста не переносились

Теперь без проблем редактируем текст прям на сайте, все интуитивно понятно и просто

---

## Как заменить картинку

В первую очередь заливаем фото на наш хостинг через CRM и берем ссылку (`ИЗ ДРУГИХ ИСТОЧНИКОВ НЕЛЬЗЯ БРАТЬ ССЫЛКИ`)

Нажимаем следующие клавиши или верхний левый значок в панели инспектора

```
Ctrl + Shift + C
```

![Selector](./images/selector.jpg)

Нажимаем на это фото и в инспекторе видим строчку следующего типа

```
<img alt="" src="images/123-a36.arb.jpg" loading="lazy">
```

Здесь нас интересует только атрибут **src**. Все что нужно это вставить ссылку внутрь кавычек после знака равно получим что-то типа (два раза нажимаем по синему тексту внутри кавычек, чтобы менять)

```
<img alt="" src="https://cdn.d-vl.com/perm.jpeg" loading="lazy">
```

![Select Src](./images/select-image.jpg)

Картинка сразу должна измениться

---

## Как добавить блок (текст/картинку)

Нажимаем следующие клавиши или верхний левый значок в панели инспектора

```
Ctrl + Shift + C
```

![Selector](./images/selector.jpg)

Сначала находим тот блок по типу которого вы хотите получить новый

![Select-Text](./images/select-text.jpg)

Выбираем в инспекторе этот блок, нажимаем ПКМ + Copy/Копировать -> Copy Element/ Копировать элемент

Затем ищем блок ПОСЛЕ которого нужно вставить ваш блок (с текстом картинкой) выбираем блок и жмем `Ctrl + V`

---

## Добавляем отступы

Нажимаем следующие клавиши или верхний левый значок в панели инспектора

```
Ctrl + Shift + C
```

![Selector](./images/selector.jpg)

Находим необходимый блок (необходимо кликнуть)

Затем смотрим в инспектор и ищем это поле

![ElStyle](./images/element-style.jpg)

Для отсупа сверху

```
margin-top: 15px;
```

Для отсупа снизу

```
margin-bottom: 15px;
```

Значения можно менять

Выглядеть будет это следующим образом

![Margin](./images/margin.jpg)

---

## Как удалить блок

Нажимаем следующие клавиши или верхний левый значок в панели инспектора

```
Ctrl + Shift + C
```

![Selector](./images/selector.jpg)

Находим блок

![Select-Text](./images/select-text.jpg)

Выбираем в инспекторе этот блок, нажимаем ПКМ + Удалить элемент/Delete element

---

## Как сохранить измнения

1. Убедитесь, что вы сохранили копию транзитки на всякий случай

2. Открывем редактор кода

![Edit HTML](./images/save.jpg)

3. На сайте в инспекторе поднимаемся на самый верх и копируем тэг html

![Select HTML](./images/copy-html.jpg)

4. В редакторе кода необходимо удалить все кроме первой строчки такого типа `<!DOCTYPE html>`

5. А вместо этого вставить скопированный текст
