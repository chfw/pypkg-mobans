# pypkg-mobans

The moban repository is made for pyecharts pypkg extension developers

## Usage

All you need to do is:

```
git clone https://github.com/chfw/pypkg-mobans.git
export YEHUA_FILE=/ABSOLUTE/PATH/TO/pypkg-mobans/yehua.yml
```

Then

```
pip install yehua
```

Lastly, go to a work folder and type in and take echarts-united-kingdom-pypkg as an example:

```
$ yh
Yehua will walk you through creating a pyecharts pypkg package.
Press ^C to quit at any time.

project name: echarts-united-kingdom-pypkg
npm project name: echarts-united-kingdom-js
description: pyecharts map extension - united kingdom maps - python package
license: MIT
author: C.W.
contact email: wangc_2011@hotmail.com
github profile/organisation: chfw
copyright owner: C.W.
```

You will be shown what happens next. Since it will dump a lot text, let me bring the last step forward here. When the command finishes, you should do:

```
git submodule add https://github.com/chfw/echarts-united-kingdom-js.git echarts_united_kingdom_pypkg/resources
```

### More on usage

This is what happens automatically next:

```
Cloning into 'mobans'...
remote: Counting objects: 214, done.
remote: Compressing objects: 100% (11/11), done.
remote: Total 214 (delta 8), reused 12 (delta 5), pack-reused 198
Receiving objects: 100% (214/214), 30.31 KiB | 17.00 KiB/s, done.
Resolving deltas: 100% (126/126), done.
Templating CUSTOM_README.rst.jj2 to README.rst
Templating custom_setup.py.jj2 to setup.py
Templating requirements.txt.jj2 to requirements.txt
Templating tests/custom_requirements.txt.jj2 to tests/requirements.txt
Templating docs/source/conf.py.jj2 to docs/source/conf.py
Templating test.script.jj2 to test.sh
Templating _version.py.jj2 to echarts_united_kingdom_pypkg/_version.py
Templating gitignore.jj2 to .gitignore
Templating travis.yml.jj2 to .travis.yml
Templated 9 files.
Initialized empty Git repository in /private/tmp/echarts-united-kingdom-pypkg/.git/
Please review changes before commit!
```

All is done. Let's see what was the output:

```
pyecharts-host:tmp chfw$ cd echarts-united-kingdom-pypkg/
pyecharts-host:echarts-united-kingdom-pypkg chfw$ ls
CHANGELOG.rst				README.rst				echarts_united_kingdom_pypkg		setup.cfg				tests
MANIFEST.in				docs					mobans					setup.py
Makefile				echarts-united-kingdom-pypkg.yml	requirements.txt			test.sh
```

And let's see what was ready for commit:

```
pyecharts-host:echarts-united-kingdom-pypkg chfw$ git status
On branch master

No commits yet

Changes to be committed:
  (use "git rm --cached <file>..." to unstage)

	new file:   .gitignore
	new file:   .moban.d/CUSTOM_README.rst.jj2
	new file:   .moban.d/custom_setup.py.jj2
	new file:   .moban.d/tests/custom_requirements.txt.jj2
	new file:   .moban.yml
	new file:   .travis.yml
	new file:   CHANGELOG.rst
	new file:   MANIFEST.in
	new file:   Makefile
	new file:   README.rst
	new file:   docs/source/conf.py
	new file:   echarts-united-kingdom-pypkg.yml
	new file:   echarts_united_kingdom_pypkg/__init__.py
	new file:   echarts_united_kingdom_pypkg/_version.py
	new file:   requirements.txt
	new file:   setup.cfg
	new file:   setup.py
	new file:   test.sh
	new file:   tests/requirements.txt
	new file:   tests/test_pypkg.py

Untracked files:
  (use "git add <file>..." to include in what will be committed)

	mobans/
```

What about unit test?

```
$ make
.
Name                                       Stmts   Miss  Cover
--------------------------------------------------------------
echarts_united_kingdom_pypkg.py                8      0   100%
echarts_united_kingdom_pypkg/_version.py       2      0   100%
--------------------------------------------------------------
TOTAL                                         10      0   100%
----------------------------------------------------------------------
Ran 1 test in 0.003s
```


## License

MIT
