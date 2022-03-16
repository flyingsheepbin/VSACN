## Visual and Semantic Alignment Contrastive Network for Generalized Zero-shot Learning
#### Environment 
This code is running at Windows 10 system, with 4*2080TI, the Cuda version is 11.3.
#### Dependencies
* pip install -r requirements.txt
#### Datasets
Download APY,AWA1,AWA2,CUB,FLO,SUN from http://datasets.d2.mpi-inf.mpg.de/xian/xlsa17.zip, then unzip the xlsa17.zip and change the directory `xlsa17/data` to `xlsa17/datasets`. Finally, move the `datasets` directory to the project directory `./datasets`.
#### Train and Test
Run `python train.py` with the corresponding parameter. For example:
```bash
python train.py --dataset AWA1 --syn_num 600 --attSize 85 --nz 3 --nclass_all 50 --nclass_seen 40 --gpu 2 --k 147 --begin_step 50 --test_epoch 1 --cr 10 --temp 0.06 --reg 20 --lr 0.0002 --d 0.0001 --nepoch 400 --syn_t 13 
```
The parameters for other datasets can be found in `parameters.txt`
