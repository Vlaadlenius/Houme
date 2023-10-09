## Шпаргалка
---


### Оформление текста
---
```
Heading	# H1
        ## H2
        ### H3
Bold	**bold text**
Italic	*italicized text*
Blockquote	> blockquote
Ordered List	1. First item
                2. Second item
                3. Third item
Unordered List	- First item
                - Second item
                - Third item
Code	`code`
Horizontal Rule	---
Link	[title](https://www.example.com)
Image	![alt text](image.jpg)
```


### Исправление коммита с помощью *amend*
---
**--amend** рассчитан на работу с последним коммитом **(HEAD)**.<br>
Дополнить коммит новыми файлами можно с помощью **git commit --amend --no-edit**.<br>
Благодаря опции **--no-edit** сообщение к коммиту останется таким, каким и было. <br>
Изменить сообщение к коммиту позволяет команда **git commit --amend -m "Обновлённое сообщение коммита"**. <br>

**VIM** <br>
Нажмите клавишу **Esc.**<br>
Наберите последовательность символов **:qa!**.<br>
Нажмите **Enter**.<br>

**nano** <br>
После нажатия **Ctrl+X** nano предложит сохранить файл, для этого нужно нажать **Y** (от англ. yes).<br>


### Как сделать шаг назад, если что-то пошло не так
---
- Команда **git restore --staged `<file>`** переведёт файл из staged обратно в modified или untracked.
- Команда **git reset --hard `<commit hash>`** «откатит» историю до коммита с хешем <hash>. Более поздние коммиты потеряются!
- Команда **git restore `<file>`** «откатит» изменения в файле до последней сохранённой (в коммите или в staging) версии.


### Просматр изменений в файлах.
---
Команда **git diff** сравнит последнюю закоммиченную версию файла с той, что находится в состоянии **modified**. 
Команда **git diff --staged** покажет изменения в staged-файлах относительно последних закоммиченных версий. 

	
**Зачем вообще указывать, какие строки файла участвуют? Разве сравниваются не все строки?**
---
Указывается не то, какие строки сравнивались, а какие попали в вывод команды **git diff.** 
Это важно для больших файлов. Если, например, сравнить два файла по 
**1000** строк, в которых отличается только
**500-я** строка, то **git diff** выведет порядка 
**10** строк (что-нибудь вроде **@@ -495,10 +495,10 @@ — с 
495-й по 505-ю**). Иначе пришлось бы читать всю тысячу. 
**10** строк вместо одной нужно, чтобы было проще понять контекст изменения.