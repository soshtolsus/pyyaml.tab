PyYAML.TAB - The next generation YAML parser and emitter for Python,
	TAB edition: Tabs Ain't Bad

The defining feature of this parser/emitter is that it solely uses
tabs for indentation. The discussion of whether to use tabs or spaces,
or to allow mixed tabs and spaces, for indentation is insane. There are
several reasons tabs are the natural choice for indentation:
* Indentation is precisely what they are good for, and the only thing
they are good for.
* Only a single character need be used, rather than an unknown and variable
number. This simplifies editing, parsing, and emission. For the latter
two points, see the diff for proof.
* While a tab is only a single character, it can be displayed differently
according to one's preferenecs, without affecting how others see it.
* Being a single character, it is atomic: it is either present or not,
with no intermediate state possible.

**NOTE**: This does not conform to the YAML spec, of any version.
It is mostly a proof of concept to show that it isn't tabs that
are evil, it is space-indentation, mixed-character indentation,
and the concept that a tab is merely a shortcut fora number of spaces
is the true evil.

To install, type `python setup.py install`. 

By default, the setup.py script checks whether LibYAML is installed
and if so, builds and installs LibYAML bindings.  To skip the check
and force installation of LibYAML bindings, use the option `--with-libyaml`:
`python setup.py --with-libyaml install`.  To disable the check and
skip building and installing LibYAML bindings, use `--without-libyaml`:
`python setup.py --without-libyaml install`.

When LibYAML bindings are installed, you may use fast LibYAML-based
parser and emitter as follows:

```
yaml.load(stream, Loader=yaml.CLoader)
yaml.dump(data, Dumper=yaml.CDumper)
```

PyYAML includes a comprehensive test suite.  To run the tests,
type `python setup.py test`.

For more information, check the PyYAML homepage:
http://pyyaml.org/wiki/PyYAML.

For PyYAML tutorial and reference, see:
http://pyyaml.org/wiki/PyYAMLDocumentation.

Post your questions and opinions to the YAML-Core mailing list:
http://lists.sourceforge.net/lists/listinfo/yaml-core.

Submit bug reports and feature requests to the PyYAML bug tracker:
http://pyyaml.org/newticket?component=pyyaml.

PyYAML is written by Kirill Simonov <xi@resolvent.net>. The TAB variant
is written by soshtolsus <qdchzrucvfmv.code.kuav@gmail.com>. It is
released under the MIT license. See the file LICENSE for more details.

