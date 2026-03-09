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

consider copying to /tmp 

```
mkdir /tmp/ml204env/
cp /home/dokt/majewski/Public/ml-env-204.tar /tmp/ml204env/
```

```
pixi global install pixi-unpack
```

unpack
```
pixi-unpack ml-env-204.tar
```

```
source activate.sh
```

test the environment
```
python -c "import torch; print(torch.__version__); print(torch.cuda.is_available()); print(torch.version.cuda)"
```

## creating env (THIS IS NOT FOR STUDENTS!)

Assumes pixi.toml is present in the directory where commands are run

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

