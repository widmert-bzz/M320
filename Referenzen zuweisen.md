- Damit ein Objekt A ein anderes Objekt B ansprechen kann. entweder Konstruktor oder Methode
	- einseitige Beziehungen
	- zweiseitige Beziehungen

## Einseitig

### Optional
![[Pasted image 20230930115619.png]]![[Pasted image 20230930115633.png]]

### Pflicht
![[Pasted image 20230930115724.png]]![[Pasted image 20230930115725.png]]

## Zweiseitig

- Um sicherzugehen, dass immer eine zweiseitige Beziehung besteht, wird in der jeweiligen set-Methode gleich auch die “Rückbeziehung” gesetzt.
- _Hinweis:_ Programmtechnisch muss einfach sichergestellt werden, dass eine schon bestehende Beziehung nicht noch einmal zugewiesen wird.

![[Pasted image 20230930115801.png]]![[Pasted image 20230930115803.png]]

## Beispiel
### Einseitig

```python
    @property            
    def wallet(self):       
        return self._wallet
    @wallet.setter    
    def wallet(self, wallet):
	    self._wallet = wallet
```

### Zweiseitig

```python
@teacher.setter
    def teacher(self, teacher):                                               
        self._ref2teacher = teacher                                               
        teacher.student = self


@student.setter    
    def student(self, student):
        self._ref2student = student
        student.teacher = self
```