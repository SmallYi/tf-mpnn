# tf-mpnn

Copy-paste in particleflow/test

## Run using load (just to make sure it works when elements are fed in):

```
singularity exec -B /storage --nv ~jpata/gpuservers/singularity/images/pytorch.simg  python3 test/tf_model2.py --target cand --ntrain 400 --ntest 100 --nepochs 5 --lr 0.00005  --datapath /storage/group/gpu/bigdata/particleflow/TTbar_14TeV_TuneCUETP8M1_cfi  --nhidden 128 --distance-dim 128 --num-conv 4 --weights inverse --lr-decay 0.99 --convlayer ghconv --load PFNet

```

## Run without load (pow of NoneType error)

```
singularity exec -B /storage --nv ~jpata/gpuservers/singularity/images/pytorch.simg  python3 test/tf_model2.py --target cand --ntrain 400 --ntest 100 --nepochs 5 --lr 0.00005  --datapath /storage/group/gpu/bigdata/particleflow/TTbar_14TeV_TuneCUETP8M1_cfi  --nhidden 128 --distance-dim 128 --num-conv 4 --weights inverse --lr-decay 0.99 --convlayer ghconv
```
