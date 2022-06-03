---
id: cheed1pahe44d690evqkilq
title: Pytest
desc: ''
updated: 1654269791225
created: 1654269525911
---

## pytest-mock

Context : #[python]() #[test]() #[pytest]() #[mock]() #[pytest-mock]()

A usage example of the ```pytest_mock``` module

### mock object attribute

```python
from pytest_mock import MockerFixture

class A:
    def echo(self, text: str):
        fmt_text = text.upper()
        return fmt_text


def test_foo(mocker: MockerFixture):
    a = A()
    mocker.patch.object(a, 'echo', return_value="MOCKED", autospec=True)
    assert a.echo("hello") == "MOCKED"


def test_foo_no_mock():
    a = A()
    assert a.echo("hello") == "HELLO"
```
