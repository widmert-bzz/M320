```python
from abc import ABC, abstractmethod  
  
class MathOp(ABC):

    @abstractmethod  
    def execute_op(self, val1: float, val2: float):  
        pass
```