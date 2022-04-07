
## kwargs, dict 개념

kwargs는 key와 value의 파라미터를 동적으로 지정할 수 있는 파이썬의 좋은 문법이다. 코딩하다보면 사용할 일이 은근 많다. 하지만 웹 서비스를 구현할 때에 kwargs를 파라미터로 설정해두고 dictionary 형태로 데이터를 받고 싶은 경우가 있다.

<br>

그렇다면 파라미터가 kwargs 형태일때 dict으로 어떻게 데이터를 넘길까

### kwargs function
```python
class Basic:
    def kwargs_test(**kwargs):
        print("Basic kwargs : ",kwargs)
        for args in kwargs.items():
            print(f"this is {args}")
```

### dict으로 data 넘기기
```python
data_set = dict()
data_set = {
    "name":"hello",
    "content":"this is hello content",
    "date":"2020-2-3"
}

Basic.kwargs_test(**data_set)
```