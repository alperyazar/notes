# comp.arch Notes

[![Build Status](https://travis-ci.com/alperyazar/comp.arch-notes.svg?branch=master)](https://travis-ci.com/alperyazar/comp.arch-notes)
[![Documentation Status](https://readthedocs.org/projects/comparch-notes/badge/?version=latest)](https://comparch-notes.readthedocs.io/en/latest/?badge=latest)
[![Website](https://img.shields.io/website/https/comparch-notes.readthedocs.io.svg)](https://comparch-notes.readthedocs.io)

[![GitHub License](https://img.shields.io/github/license/alperyazar/comp.arch-notes.svg?style=flat)](https://creativecommons.org/licenses/by-sa/4.0/)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat)](http://makeapullrequest.com)

[![GitHub commit activity](https://img.shields.io/github/commit-activity/m/alperyazar/comp.arch-notes.svg)](https://github.com/alperyazar/comp.arch-notes/graphs/commit-activity)
[![Percentage of issues still open](https://isitmaintained.com/badge/open/alperyazar/comp.arch-notes.svg)](https://isitmaintained.com/project/alperyazar/comp.arch-notes)
[![Average time to resolve an issue](https://isitmaintained.com/badge/resolution/alperyazar/comp.arch-notes.svg)](https://isitmaintained.com/project/alperyazar/comp.arch-notes)
[![GitHub repo size in bytes](https://img.shields.io/github/repo-size/alperyazar/comp.arch-notes.svg)](https://github.com/alperyazar/comp.arch-notes)

Welcome to source code repository of notes on computer architecture.

This is a collection of mostly my personal notes.
Notes are (will be) mixture of:

* Lecture notes on courses offered in universities or other institutions
* Processor history
* Paradigms like reconfigurable computing

but **NOT** about:

* Programming
* VHDL/Verilog
* Details of FPGA based designs

My main purpose is to collect my notes in one place. I prefer to share them
publicly because I believe that this will lead creation of more up-to-date
and more correct resource. Therefore, I would like to hear your feedback,
your comments and corrections.

## Reading Notes

[![Website](https://img.shields.io/website/https/comparch-notes.readthedocs.io.svg)](https://comparch-notes.readthedocs.io)

Notes are compiled automatically by readthedocs.org and hosted on
https://comparch-notes.readthedocs.io/ OR
https://comparch-notes.rtfd.io/

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

[![GitHub License](https://img.shields.io/github/license/alperyazar/comp.arch-notes.svg?style=flat)](https://creativecommons.org/licenses/by-sa/4.0/)

SPDX-License-Identifier:CC-BY-SA-4.0

This project is licensed under CC-BY-SA-4.0 if otherwise stated.
Check `LICENSE` for further information.