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
<<<<<<< HEAD
Нажмите клавишу **Esc.**<br>
Наберите последовательность символов **:qa!**.<br>
Нажмите **Enter**.<br>

**nano** <br>
После нажатия **Ctrl+X** nano предложит сохранить файл, для этого нужно нажать **Y** (от англ. yes).<br>
=======
Нажмите клавишу Esc.<br>
Наберите последовательность символов :qa!.<br>
Нажмите Enter.<br>

**nano** <br>
После нажатия Ctrl+X nano предложит сохранить файл, для этого нужно нажать Y (от англ. yes).<br>
>>>>>>> 3c1df06980b163a333f579c99a388ba719837a80
