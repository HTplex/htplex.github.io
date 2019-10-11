### args
```python
import argparse

parser = argparse.ArgumentParser()
parser.add_argument("-i",
                    "--input_path",
                    type=str,
                    default='../data',
                    help="path of directory of input file")

def main(args):
    print(args.input_path)

if __name__ == '__main__'
    args = parser.parse_args()
    main(args)
```
### multiprocessing pool
### project config

[home](/index/)