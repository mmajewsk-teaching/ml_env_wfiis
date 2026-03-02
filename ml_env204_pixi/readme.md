# Conda/pixi based env for 204 D11, Winter 2026


## using this env

copy
```
dd if=/home/dokt/majewski/Public/ml-env-204.tar of=ml-env-204.tar bs=64M status=progress conv=fsync
```

alternative
```
cp /home/dokt/majewski/Public/ml-env-204.tar .
```

unpack

```
mkdir -p ml-env-206 && cd ml-env-206
tar -xf /path/to/ml-env-206.tar
```

```
source activate.sh
python -c "import torch; print(torch.__version__); print(torch.cuda.is_available()); print(torch.version.cuda)"
```

## creating env (THIS IS NOT FOR STUDENTS!)

```
pixi install
pixi lock
```

install packer


```
pixi global install pixi-pack
```

Then pack it

```
 pixi-pack --environment default --platform linux-64 --output-file ml-env-204.tar
```

