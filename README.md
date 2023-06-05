# ItemRec

ItemRec(Item Perspective Recommendation) is a re-ranking framework which enables items "select" users.  Our experiments is conducted based on [RecBole](https://github.com/RUCAIBox/RecBole).



## Train

For instance, the following instruction represents that training the model ENMF model on dataset MovieLens-1M.

```
python run_recbole.py --model ENMF --dataset ml-1m
```



## Test

We provide two types of testing methods.

ItemRec:

```
python run_recbole_test.py --model ENMF --dataset ml-1m --ckpt saved/ml_1m/ENMF-Jan-15-2023_19-13-48.pth --M 50 --k_item 5
```

where  `--ckpt` represents the checkpoint used to resume, `--M` and `--k_item` represent the parameters in ItemRec.



Traditional top-k recommendation:

```
python run_recbole_test.py --model ENMF --dataset ml-1m --ckpt saved/ml_1m/ENMF-Jan-15-2023_19-13-48.pth 
```

 Comparing to ItemRec, `--M` and `--k_item` are missing here.



For more other settings like the value of top-`k`, the way of splitting datasets and so on, please see the guides in [RecBole](https://github.com/RUCAIBox/RecBole).



## License

ItemRec uses [MIT License](https://github.com/RUCAIBox/RecBole/blob/master/LICENSE). All data and code in this project can only be used for academic purposes.

