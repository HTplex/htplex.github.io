### recurrsive glob

get all filename in directory that satisifies given re
```python
from pathlib import Path
f_list = []
for filename in Path('./imgs').glob('**/*.png'):
    f_list.append(str(filename))
```

### read file line by line
```python
filepath = 'test.txt'
with open(filepath) as fp:
    line = fp.readline()
    while line:
        string = line.strip()
        print(string)
```

### save and read txt
```python
# save
import json

with open('data.txt', 'w+') as fp:
    fp.write(string)

# load
with open('data.txt', 'r') as fp:
    string = fp.read()

```

### save and read dict to json file
```python
# save
import json

with open('data.json', 'w') as fp:
    json.dump(data, fp, sort_keys=True, indent=4)

# load
with open('data.json', 'r') as fp:
    data = json.load(fp)

```

### create folder when not exist, recreate if exists
```python
import os
import shutil

def check_out_dir(folder_path):
    '''
    make a dir if the input path doesn't exist, else
    empty the directory
    :param folder_path: path to the folder to be checked
    :return: None
    '''
    if not os.path.exists(folder_path):
        os.makedirs(folder_path)
    else:
        shutil.rmtree(folder_path)
        os.makedirs(folder_path)
```
[home](/index)