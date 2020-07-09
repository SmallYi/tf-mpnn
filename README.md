# tf-mpnn

Copy-paste in particleflow/test

## Run tf-model2.py

```
singularity exec -B /storage --nv ~jpata/gpuservers/singularity/images/pytorch.simg  python3 test/tf_model2.py --target cand --ntrain 20000 --ntest 5000 --nepochs 5 --lr 0.00005  --datapath /storage/group/gpu/bigdata/particleflow/TTbar_14TeV_TuneCUETP8M1_cfi  --nhidden 128 --distance-dim 128 --num-conv 4 --weights inverse --lr-decay 0.99 --convlayer ghconv
```

## Run pred_tf_model.py

(change the run accordingly)
```
singularity exec -B /storage --nv ~jpata/gpuservers/singularity/images/pytorch.simg  python3 test/pred_tf_model2.py --weights experiments/run_86/weights.10-7423.303108.hdf5 --nhidden 128 --distance-dim 128 --num-conv 4 --ntrain 20000 --ntest 5000 --convlayer ghconv 

```
## Run plots.py

```
singularity exec -B /storage --nv ~jpata/gpuservers/singularity/images/pytorch.simg  python3 test/plots.py --target cand --pkl df_1.pkl.bz2
```
