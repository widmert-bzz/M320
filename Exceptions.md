```python
class NumberFormatException(Exception):  
    def __init__(self, text: str):  
        super().__init__(f'ERROR: {text} ist ein ungültiger Zahlenwert')
        
```

```python
raise OperationException
```