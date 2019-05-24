# ayazar's Notes

[![Build Status](https://travis-ci.com/alperyazar/notes.svg?branch=master)](https://travis-ci.com/alperyazar/notes)
[![Documentation Status](https://readthedocs.org/projects/ayazars-notes/badge/?version=latest)](http://notes.ayazar.com)
[![Website](https://img.shields.io/website/https/ayazars-notes.readthedocs.io.svg)](http://notes.ayazar.com)

[![GitHub License](https://img.shields.io/github/license/alperyazar/notes.svg?style=flat)](https://creativecommons.org/licenses/by-sa/4.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/alperyazar/notes.svg)](https://github.com/alperyazar/notes/graphs/commit-activity)
[![GitHub repo size in bytes](https://img.shields.io/github/repo-size/alperyazar/notes.svg)](https://github.com/alperyazar/notes)

Welcome to source code repository of my personal notes.

I am an electronics engineer interested in computers. So expect that kind of content.

My main purpose is to collect my notes in one place. I prefer to share them
publicly because I believe that this will lead creation of more up-to-date
and more correct resource. Therefore, I would like to hear your feedback,
your comments and corrections.

## Reading Notes

[![Website](https://img.shields.io/website/https/ayazars-notes.readthedocs.io.svg)](http://notes.ayazar.com)

Notes are compiled automatically by readthedocs.org and hosted on
http://notes.ayazar.com OR
http://n.ayazar.com
https://ayazars-notes.readthedocs.io/ OR
https://ayazars-notes.rtfd.io/

## File Organization

Source code of the notes is under `docs` directory. Root directory holds some
auxiliary files like this file.

## Compiling Notes

In order to compile notes on your machine, first install [Sphinx](http://www.sphinx-doc.org). Refer to document of Sphinx if you need help. Then
 `cd` to `docs` directory and run the following commands.

### Windows Users

Cmd.exe

```bat
make.bat html
```

Powershell

```powershell
.\make.bat html
```

### Linux Users

Shell

```bash
make html
```

Above commands will generate `docs/_build/html/index.html` file. This is the
front page of the notes. Open it with your favorite browser.

If you need to compile for PDF or different output format, please check
Sphinx documentation.

## Contributing

[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

I will be happy if you help me to make these notes better. If you are not
familiar with reStructuredText, compiling a Sphinx project
git pull requests or Github then you can create `New issue` on `Issues` page to
talk about your contribution, corrections, fixes, etc.

If you can modify the source files and create pull request,
then please read `CONTRIBUTING.md` page.

## License

[![GitHub License](https://img.shields.io/github/license/alperyazar/notes.svg?style=flat)](https://creativecommons.org/licenses/by-sa/4.0/)

SPDX-License-Identifier:CC-BY-SA-4.0

This project is licensed under CC-BY-SA-4.0 if otherwise stated.
Check `LICENSE` for further information.