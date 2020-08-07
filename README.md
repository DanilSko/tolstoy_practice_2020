## Инструкция по разметке семантических ролей в романе "Война и мир" для практикантов


### Основная задача 
#### легкая с т.з. интеллектуальных усилий, делается руками

[Вот тут]() лежат XML-документы с главами "Войны и мира". В этих текстах размечены:
1. Упоминания персонажей, в т.ч. анафорические. Тег [<rs>](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-rs.html) из стандарта TEI (```rs``` означает referring string, то есть любая строка, за которой стоит сущность-референт; т.е. семантика этого тега в TEI -- примерно "любая именованная сущность"). Всем персонажам романа, кроме эпизодических, присвоены уникальные ID ("Pierre_Bezukhov", "Natasha_Rostova", "Vasili_Kuragin" и т.п.), ссылка на которые хранится в атрибуте ```@ref```. Выглядит как-то так:

```<rs ref="Pierre_Bezukhov">Он</rs>, казалось, не мог переносить вида слез```

2. Прямая речь персонажа с указанием ID говорящего, адресата речи и самого текста реплики. Помечается тегом [```<said>```](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-said.html) В этом задании нам не очень важна. 

3. [Семантические роли](https://ru.wikipedia.org/wiki/%D0%A1%D0%B5%D0%BC%D0%B0%D0%BD%D1%82%D0%B8%D1%87%D0%B5%D1%81%D0%BA%D0%B0%D1%8F_%D1%80%D0%BE%D0%BB%D1%8C) (т.н. глубинные позиции), в которых оказываются упоминания персонажей. О семантических ролях в лингвистике см. также [этот хэндаут](http://www.philol.msu.ru/~otipl/new/main/courses/syntax/05_Semroli_i_interfejs.pdf). В нашей разметке используется упрощенная модель: основных ролей сейчас всего три.

  3.1. Агенс ("agent") — когда персонаж совершает любое активное действие, хоть как-то регистрируемое внешней средой: (говорить, жестикулировать, ехать)
  3.2. Пациенс/Объект ("undergoer") — когда персонаж претерпевает действие или является объектом разговора, восприятия и т.п.)
  3.3. Экспериенцер ("experiencer") — когда персонаж что-то думает, чувствует, видит. Т.е. перцепция или мыслительная активность, не имеющая выражения во внешней среде. 

Роль указывается в атрибуте ```@rolename``` уже знакомого вам тега ```rs```

 ```Так говорила в июле 1805 года известная <rs ref="Anna_Pavlovna_Scherer" *rolename="agent"* subrole="speaker">Анна Павловна Шерер</rs>, фрейлина и приближенная <rs ref="empress_Mariya">императрицы Марии Феодоровны</rs>, встречая важного и чиновного <rs ref="Vasili_Kuragin" *rolename="undergoer"*>князя Василия</rs>```

В разметке также встречаются иные роли, например, possessor (обладатель чего-то). Эту роль можно пока игнорировать. Сейчас она в первую очередь размечена в конструкциях вида "рука Пьера". Нас же будут интересовать лишь те случаи, когда упоминание персонажа напрямую зависит в предложении от какого-то предиката (глагола или отглагольного существительного).  

### Описание основной задачи:

Нужно 
1. выбрать себе сколько-то глав. Для начала можно, например, 5.
2. Записаться разметчиком этих глав [в этой таблице]()
3. Сохранить себе эти главы [отсюда]()
4. Открыть в любом удобном вам редакторе с подсветкой XML-синтаксиса (Notepad++ / Sublime / Atom / VS Code  ... — на ваш вкус. Знакомые с Oxygen XML editor могут пользоваться им). Если не знаете, что взять, и у вас Windows, берите Notepad++.
5. Пройти по всем местам, где у персонажа указан rolename "undergoer" или "agent" и заменить на experiencer там, где речь идет о том, что персонаж что-то думает, чувствует, видит. Сейчас из-за несовершенства инструмента разметки, который тут когда-то использовался, во многих случаях experiencer не разобрался. 

### Дополнительная задача (посложнее и требует автоматизации)

Разметить глаголы. Сгенерировать ID.


### Дополнительная задача 2 (посложнее и требует автоматизации)

Разметить глаголы. 



You can use the [editor on GitHub](https://github.com/DanilSko/tolstoy_practice_2020/edit/master/README.md) to maintain and preview the content for your website in Markdown files.

Whenever you commit to this repository, GitHub Pages will run [Jekyll](https://jekyllrb.com/) to rebuild the pages in your site, from the content in your Markdown files.

### Markdown

Markdown is a lightweight and easy-to-use syntax for styling your writing. It includes conventions for

```markdown
Syntax highlighted code block

# Header 1
## Header 2
### Header 3

- Bulleted
- List

1. Numbered
2. List

**Bold** and _Italic_ and `Code` text

[Link](url) and ![Image](src)
```

For more details see [GitHub Flavored Markdown](https://guides.github.com/features/mastering-markdown/).

### Jekyll Themes

Your Pages site will use the layout and styles from the Jekyll theme you have selected in your [repository settings](https://github.com/DanilSko/tolstoy_practice_2020/settings). The name of this theme is saved in the Jekyll `_config.yml` configuration file.

### Support or Contact

Having trouble with Pages? Check out our [documentation](https://docs.github.com/categories/github-pages-basics/) or [contact support](https://github.com/contact) and we’ll help you sort it out.
