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

if __name__ == '__main__':
    args = parser.parse_args()
    main(args)
```
### multipocessing magic
```bash
<script to list args> | xargs -n1 -P<n_proc> -I {} sh -c "<script>using {} as args"

# example:
find -mindepth 3 -maxdepth 3 -type d | xargs -n1 -P18 -I {} sh -c "python gen.py -i {}"

find ./segmentation_data_new -maxdepth 2 -mindepth 2 -type d | while read line; do echo "0 $line"; read line; echo "1 $line"; done | xargs -I -P2 {} sh -c 'CUDA_VISIBLE_DEVICES=$0 python -W ignore Deblur_GAN_test_wrapper.py -i $1'
```
### egrep (RegEx in shell)
```bash
ls | egrep '[[:digit:]]{0,9}_[[:digit:]]{0,9}_[[:digit:]]{0,9}_[[:digit:]]{0,9}.png'| while read line; do echo $line; done
```
### multiprocessing pool

### project config

[home](/index)