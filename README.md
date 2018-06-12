# yichin

`$ pip3 install yichin`

This algorithm use Zero-width space to hide the message into string "yichin".

https://pypi.org/project/yichin/

## Example Usage

```
import yichin

# input type string return type string
yichin.encode("Jellyfish")
>> 'yic⁤⁪⁦⁥⁦⁬⁦⁬⁧⁩⁦⁦⁦⁩⁧⁣⁦⁨hin'

# input type string return type string
yichin.decode("yic⁤⁪⁦⁥⁦⁬⁦⁬⁧⁩⁦⁦⁦⁩⁧⁣⁦⁨hin")
>> 'Jellyfish'
```

## pypi tutorial

`$ nano ~/.pypirc`

```
[distutils]
index-servers =
  pypi
  pypitest

[pypi]
repository: https://upload.pypi.org/legacy/
username: <your_username>
password: <your_password>

[pypitest]
repository: https://test.pypi.org/legacy/
username: <your_username>
password: <your_password>
```

`$ nano setup.py`

```
from distutils.core import setup

setup(
  name = <package_name>,
  packages = [<package_name>], # this must be the same as the name above
  version = '0.1',
  description = <description>,
  author = <author>,
  author_email = <author_email>',
  url = <your_github_repo_link>,
  keywords = [<keyword>, <keyword>, <keyword>], # arbitrary keywords
  classifiers = [],
)
```

`$ python3 setup.py check`

`$ python3 setup.py sdist`

`$ python3 setup.py sdist register upload -r pypitest`

`$ python3 setup.py sdist register upload -r pypi`
