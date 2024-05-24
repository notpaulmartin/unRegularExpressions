(un)Regular Expressions
=========

Collection of useful regular expressions.

Find it at: [https://unRegularExpressions.com](https://unregularexpressions.com)

### Snippets are in the `_snippets` folder

```
---
name: ISBN-10 & 13
regex: '(ISBN[-]*(1[03])*[ ]*(: ){0,1})*(([0-9Xx][- ]*){13}|([0-9Xx][- ]*){10})'
flags: gm
note: Matches the ISBN number and the check digit
example: https://regex101.com/r/Ole6vp/1
---
```

### Adding/Removing columns

To add or remove columns, edit `_includes/interactive-table.html`:

```html
	<th style="width:10%;"><span class="sort" data-sort="name">Name</span></th>
	<th style="width:30%;"><span class="sort" data-sort="regex">Regex</span></th>
	<th style="width:1%;"><span class="sort" data-sort="flags">Flags</span></th>
	<th style="width:25%;"><span class="sort" data-sort="note">Note</span></th>
	<th style="width:1%;"><span class="sort" data-sort="example">Example</span></th>
```

```html
<tbody class="list">
{% for snippet in site.snippets %}
	<tr>
		<td class="name">{{ snippet.name }}</td>
		<td class="regex"><code class="language-regex">{{ snippet.regex }}</code></td>
		<td class="flags"><code>{{ snippet.flags }}</code></td>
		<td class="note">{{ snippet.note }}</td>
		<td class="example"><a href="{{ snippet.example }}">Link</a></td>
	</tr>
{% endfor %}
</tbody>
```


### Credits

Based on the [Jekyll-DB](https://github.com/rypan/jekyll-db) theme. Uses [ListJS](http://listjs.com/) and [Bootstrap 3](http://getbootstrap.com/).
