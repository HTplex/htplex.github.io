### recurrsive glob

get all filename in directory that satisifies given re
```python
from pathlib import Path
for filename in Path('./imgs').glob('**/*.png'):
    print(filename)
```
[home](/index/)