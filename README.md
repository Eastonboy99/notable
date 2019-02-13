# Notable 

<p align="center">
  <img src="resources/demo/fork.png" alt="Notable" width="750">
</p>

## Why a fork

Three years ago I started looking at markdown editors to help with some of my professional project-based workflows. At the time, I was dealing with multiple projects at the same time, many of them having weekly checkpoints involving minutes to be gathered, reviewed and shared. I started taking these notes in individual markdown documents, asking that others in the teams do the same. As the projects went along, managing the documentation became an increasingly burdensome task, and my then-single page editor quickly did not suffice. So I started building a small tool to assist. I am back into a multi-projects environment, and again facing the issue of tracking all this information. Time for a new tool.

I ran into Notable, which had the merrit of being both [Open Source (MIT)](https://github.com/lmihalkovic/notable/blob/v1.3.0/LICENSE)  and with a clean, albeit not suited for my purpose, codebase. This repo is a fork started from v1.3.0 of the great work started by [Fabio Spampinato](https://github.com/fabiospampinato).

I may eventually push it all here, but in the meantime, here are a few of the things I am doing

* revert the build to standard [electron-webpack](https://github.com/electron-userland/electron-webpack)
* change the internal data model (eventually with server side support)
* support multiple projects
* start using [RxJS](https://www.learnrxjs.io/)
* remove [CodeMirror](https://codemirror.net/) and replace it with [monaco](https://microsoft.github.io/monaco-editor/)
* change the internal markdown processing workflow
* improve the [monarch](https://microsoft.github.io/monaco-editor/monarch.html) markdown styling
* support new tags (```@todo```, ```@due(date)```, ```@done```)
* add code completion

## Fabio's Intro to Notable

The markdown-based note-taking app that doesn't suck.

I couldn't find a note-taking app that ticked all the boxes I'm interested in: notes are written and rendered in GitHub-flavored Markdown, no WYSIWYG, no proprietary formats, I can run a search & replace across all notes, notes support attachments, the app isn't bloated, the app has a pretty interface, tags are indefinitely nestable and can import Evernote notes (because that's what I was using before).

So I built my own.

## Features

```
/path/to/your/data_directory
├─┬ attachments
│ ├── foo.ext
│ ├── bar.ext
│ └── …
└─┬ notes
  ├── foo.md
  ├── bar.md
  └── …
```

- **No proprietary formats**: Notable is just a pretty front-end for a folder structured as shown above. Notes are plain Markdown files, their metadata is stored as Markdown front matter. Attachments are also plain files, if you attach a `picture.jpg` to a note everything about it will be preserved, and it will remain accessible like any other file.

- **Proper editor**: Notable doesn't use any WYSIWYG editor, you just write some Markdown and it gets rendered as GitHub-flavored Markdown. The built-in editor is [CodeMirror](https://codemirror.net), this means you get things like multi-cursor by default. If you need more advanced editing features with a single shortcut you can open the current note in your default Markdown editor.

- **Indefinitely nestable tags**: Pretty much all the other note-taking apps differentiate between notebooks, tags and templates. IMHO this unnecessarily complicates things. In Notable you can have root tags (`foo`), indefinitely nestable tags (`foo/bar`, `foo/.../qux`) and it still supports notebooks and templates, they are just special tags with a different icon (`Notebooks/foo`, `Templates/foo/bar`).

Upon first instantiation, some tutorial notes will be added to the app, check them out for more in-depth details about the app and how to use it. You can also find the raw version [here](https://github.com/fabiospampinato/notable/tree/master/resources/tutorial/notes).

## [Comparison](resources/comparison/table.png?raw=true)

[![Click to Enlarge](resources/comparison/table.png)](resources/comparison/table.png?raw=true)

Part of this comparison is personal opinion: you may disagree on the UI front, things I consider bloat may be considered features by somebody else etc. but hopefully this comparison did a good job at illustrating the main differences.

## Demo

### Indefinitely Nestable Tags

<img src="resources/demo/tags.png" alt="Indefinitely Nestable Tags" width="750">

### Editor

<img src="resources/demo/editor.png" alt="Editor" width="750">

### Multi-Note Editor

<img src="resources/demo/multi_editor.png" alt="Multi-Note Editor" width="750">

## Contributing

There are multiple ways to contribute to this project, read about them [here](https://github.com/fabiospampinato/notable/blob/master/.github/CONTRIBUTING.md).

## Related

- **[enex-dump](https://github.com/fabiospampinato/enex-dump)**: Dump the content of Evernote's `.enex` files, preserving attachments, some metadata and optionally converting notes to Markdown.
- **[Noty](https://github.com/fabiospampinato/noty)**: Autosaving sticky note with support for multiple notes without needing multiple windows.
- **[Markdown Todo](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-markdown-todo)**: Manage todo lists inside markdown files with ease. Have the same todo-related shortcuts that Notable provides, but in Visual Studio Code.
- **[Todo+](https://marketplace.visualstudio.com/items?itemName=fabiospampinato.vscode-todo-plus)**: Manage todo lists with ease. Powerful, easy to use and customizable.

## License

MIT © Fabio Spampinato
