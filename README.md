# ascii directory tree plugin for GitBook

convert indented lines to ascii directory tree for gitbook.

you can see asciitree in action. [https://jianglibo.gitbooks.io](https://jianglibo.gitbooks.io/broccoli-learning/content/gitbook/BREADME.html)

in:
```
{% asciitree %}
app
-main.js
-helper.js
-others
--Brocfile.js
package.json
{% endasciitree %}
```

out:
```
├── app
|   ├── main.js
|   ├── helper.js
|   └── others
|       └── Brocfile.js
└── package.json
```

Add it to your book.json with a basic configuration:
```json
{
    "plugins": ["asciitree"],
    "pluginsConfig": {
        "asciitree": {
            "leadingChar": "no need, because plugin will guess leadingChar.",
            "trimRight": true
        }
    }
}
```
