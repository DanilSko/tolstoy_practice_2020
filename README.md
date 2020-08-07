## Инструкция по разметке семантических ролей в романе "Война и мир" для практикантов


### Основная задача (легкая)
[Вот тут]()лежат XML-документы с главами "Войны и мира". В этих текстах размечены:
1. Упоминания персонажей, в т.ч. анафорические. Тег [<rs>](https://tei-c.org/release/doc/tei-p5-doc/en/html/ref-rs.html) из стандарта TEI (rs означает referring string, то есть любая строка, за которой стоит сущность-референт; т.е. семантика этого тега в TEI -- примерно "любая именованная сущность"). Всем персонажам романа, кроме эпизодических, присвоены уникальные ID ("Pierre_Bezukhov", "Natasha_Rostova", "Vasili_Kuragin" и т.п.), ссылка на которые хранится в атрибуте @ref. Выглядит как-то так:

```<rs ref="Pierre_Bezukhov">Он</rs>, казалось, не мог переносить вида слез```

прямая речь персонажа с указанием ID говорящего 

### Дополнительная задача (посложнее; можно пытаться в автоматизацию)

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
