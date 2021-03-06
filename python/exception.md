# 예외 처리

## 예외 종류

- NameError
- TypeError
- ValueError
- ZeroDivision
- IndexError
- KeyError
- ModuleError
- ImportError

## try-except

### 기본형태

```python
try:
    <코드블럭 1>
except:
    <코드블럭 2>
```

### 확장형태

```python
try:
    <코드 블럭1>
except 예외1: # 예외별로 다른 코드를 실행 시킬 수 있다.
    <코드블럭2>
except 예외2, 예외 3:
    <코드브럭3>
except 예외4 as e:
    <코드블럭4>
else: # 예외 발생하지 않을 시에만 실행
    <코드블럭5>
finally: # 예외 발생하든 안 하든 관계 없이 무조건 실행
    <코드블럭6>
```

## 예외 발생 시키기

### `raise`

예외를 강제로 발생 `raise ValueError('숫자를 입력해주세요')`

### `assert`

상태를 주로 검증하기 위해서 `assert Boolean expression, error message`

```python
x = '10'
assert type(x) == int, '숫자형이 아닙니다.'
```

```python
Traceback (most recent call last):
  File "test.py", line 3, in <module>
    assert type(a) == int, '숫자형이 아닙니다.'
AssertionError: 숫자형이 아닙니다.
```
