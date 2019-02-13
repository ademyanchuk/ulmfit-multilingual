# MLDoc
## Limiit to 100 examples
```
python -m ulmfit eval --glob="mldoc/*-1/models/sp30k/lstm_nl4.m" --name nl4-100e8 --cuda-id=1 --limit=100 --num-cls-epochs=8
{
    'data/mldoc/it-1/models/sp30k/lstm_nl4-100e8.m': 0.7799999713897705,
    'data/mldoc/de-1/models/sp30k/lstm_nl4-100e8.m': 0.9135000109672546,
    'data/mldoc/ja-1/models/sp30k/lstm_nl4-100e8.m': 0.7112500071525574,
    'data/mldoc/fr-1/models/sp30k/lstm_nl4-100e8.m': 0.8877500295639038,
    'data/mldoc/ru-1/models/sp30k/lstm_nl4-100e8.m': 0.722000002861023,
    'data/mldoc/es-1/models/sp30k/lstm_nl4-100e8.m': 0.8169999718666077
}
```


## Noise  

```
noise=0.13
lang=de
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise}
{'data/mldoc/de-1/models/sp30k/lstm_nl4-noise.m': 0.9449999928474426}

noise=0.18
lang=es
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise} 
{'data/mldoc/es-1/models/sp30k/lstm_nl4-noise.m': 0.9312499761581421}

noise=0.18
lang=fr
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise} 
{'data/mldoc/fr-1/models/sp30k/lstm_nl4-noise.m': 0.9049999713897705}

noise=0.27
lang=it
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise} 
{'data/mldoc/it-1/models/sp30k/lstm_nl4-noise.m': 0.8372499942779541}

noise=0.4
lang=ja
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise} 
{'data/mldoc/ja-1/models/sp30k/lstm_nl4-noise.m': 0.7472500205039978

noise=0.32
lang=ru
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise} 
{'data/mldoc/ru-1/models/sp30k/lstm_nl4-noise.m': 0.7567499876022339}

noise=0.28
lang=zh
python -m ulmfit eval --glob="mldoc/${lang}-1/models/sp30k/lstm_nl4.m" --name nl4-noise --cuda-id=1 --num-cls-epochs=2 --noise=${noise} 
```





### LIMIT LOgs
```
python -m ulmfit eval --name nl4-100e8 --cuda-id=1 --limit=100 --num-cls-epochs=8                                                                         ✘ 130
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k/lstm_nl4-100e8.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/it.dev.csv
Tokenized data loaded, lm.trn 13500, lm.val 1500
Limiting data set to: 100
Tokenized data loaded, cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁,', '▁.', '▁di', "▁&'", "'", '▁e', '▁il', '▁la', 'e', '▁in']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k/lstm_nl4-100e8.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.214805    1.382632    0.280000
epoch     train_loss  valid_loss  accuracy
1         0.977314    1.269534    0.450000
epoch     train_loss  valid_loss  accuracy
1         0.856274    1.223441    0.530000
epoch     train_loss  valid_loss  accuracy
1         0.718223    1.188048    0.620000
2         0.735718    1.130525    0.730000
3         0.730894    1.069027    0.710000
4         0.715334    1.015253    0.710000
5         0.716080    0.965223    0.720000
6         0.695554    0.918456    0.730000
7         0.689949    0.892840    0.730000
8         0.675208    0.876222    0.720000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/it-1/models/sp30k/lstm_nl4-100e8.m
Loss and accuracy using (cls_best): [0.7090041, tensor(0.7800)]
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k/lstm_nl4-100e8.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/de.dev.csv
Tokenized data loaded, lm.trn 13500, lm.val 1500
Limiting data set to: 100
Running tokenization...
Saving tokenized: cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁.', '▁,', '▁der', '▁die', '▁und', '▁in', 'en', "▁&'", 's', '-']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k/lstm_nl4-100e8.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.141527    1.328262    0.280000
epoch     train_loss  valid_loss  accuracy
1         0.703434    1.170250    0.510000
epoch     train_loss  valid_loss  accuracy
1         0.568693    1.051980    0.780000
epoch     train_loss  valid_loss  accuracy
1         0.455238    0.990438    0.800000
2         0.475659    0.928943    0.850000
3         0.477652    0.848537    0.920000
4         0.455583    0.769415    0.930000
5         0.450824    0.690618    0.930000
6         0.443699    0.633900    0.940000
7         0.430881    0.563667    0.950000
8         0.419999    0.524655    0.950000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/de-1/models/sp30k/lstm_nl4-100e8.m
Loss and accuracy using (cls_best): [0.45835665, tensor(0.9135)]
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k/lstm_nl4-100e8.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/ja.dev.csv
Tokenized data loaded, lm.trn 13500, lm.val 1500
Limiting data set to: 100
Tokenized data loaded, cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁、', '▁の', '▁。', '▁に', '▁を', '▁は', '▁年', '▁が', '▁)', '▁(']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k/lstm_nl4-100e8.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.342269    1.399389    0.230000
epoch     train_loss  valid_loss  accuracy
1         0.957341    1.344665    0.280000
epoch     train_loss  valid_loss  accuracy
1         0.881869    1.301798    0.450000
epoch     train_loss  valid_loss  accuracy
1         0.887575    1.280226    0.440000
2         0.835731    1.257639    0.450000
3         0.813987    1.219512    0.510000
4         0.792665    1.181309    0.520000
5         0.785690    1.151372    0.510000
6         0.784095    1.152232    0.500000
7         0.768115    1.133895    0.520000
8         0.769684    1.124231    0.530000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ja-1/models/sp30k/lstm_nl4-100e8.m
Loss and accuracy using (cls_best): [0.8863698, tensor(0.7113)]
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k/lstm_nl4-100e8.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/fr.dev.csv
Tokenized data loaded, lm.trn 13500, lm.val 1500
Limiting data set to: 100
Running tokenization...
Saving tokenized: cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁de', '▁,', '▁.', "'", 's', '▁la', '▁le', '▁et', '▁l', '▁à']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k/lstm_nl4-100e8.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.220506    1.413276    0.200000
epoch     train_loss  valid_loss  accuracy
1         0.791777    1.306999    0.290000
epoch     train_loss  valid_loss  accuracy
1         0.572241    1.190053    0.580000
epoch     train_loss  valid_loss  accuracy
1         0.502800    1.130456    0.710000
2         0.515115    1.056434    0.770000
3         0.522720    0.974482    0.780000
4         0.518296    0.881002    0.840000
5         0.496588    0.825646    0.880000
6         0.490416    0.771587    0.860000
7         0.497172    0.722874    0.850000
8         0.491894    0.682278    0.850000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/fr-1/models/sp30k/lstm_nl4-100e8.m
Loss and accuracy using (cls_best): [0.5428351, tensor(0.8878)]
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k/lstm_nl4-100e8.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/ru.dev.csv
Tokenized data loaded, lm.trn 9195, lm.val 1021
Limiting data set to: 100
Running tokenization...
Saving tokenized: cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁,', '▁.', '▁в', 'а', '▁и', 'е', 'и', 'й', '▁на', 'х']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k/lstm_nl4-100e8.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.367201    1.409767    0.240000
epoch     train_loss  valid_loss  accuracy
1         1.099071    1.320811    0.330000
epoch     train_loss  valid_loss  accuracy
1         0.875845    1.253172    0.410000
epoch     train_loss  valid_loss  accuracy
1         0.775657    1.215067    0.580000
2         0.774420    1.171324    0.660000
3         0.766028    1.118901    0.680000
4         0.744478    1.074021    0.680000
5         0.738797    1.033736    0.660000
6         0.733380    0.997304    0.660000
7         0.723470    0.977280    0.670000
8         0.710699    0.953586    0.640000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/ru-1/models/sp30k/lstm_nl4-100e8.m
Loss and accuracy using (cls_best): [0.8535175, tensor(0.7220)]
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4-100e8.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/es.dev.csv
Tokenized data loaded, lm.trn 13013, lm.val 1445
Limiting data set to: 100
Running tokenization...
Saving tokenized: cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁de', '▁,', '▁la', '▁.', '▁en', '▁el', '▁y', 's', '▁a', '▁que']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4-100e8.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.142170    1.330161    0.300000
epoch     train_loss  valid_loss  accuracy
1         0.767807    1.212253    0.420000
epoch     train_loss  valid_loss  accuracy
1         0.636803    1.099303    0.540000
epoch     train_loss  valid_loss  accuracy
1         0.584241    0.997207    0.610000
2         0.578480    0.907674    0.710000
3         0.548451    0.830268    0.730000
4         0.535560    0.762040    0.750000
5         0.522172    0.746566    0.740000
6         0.506584    0.676038    0.770000
7         0.493665    0.651112    0.770000
8         0.493031    0.621689    0.770000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4-100e8.m
Loss and accuracy using (cls_best): [0.54911107, tensor(0.8170)]
{'data/mldoc/it-1/models/sp30k/lstm_nl4-100e8.m': 0.7799999713897705, 'data/mldoc/de-1/models/sp30k/lstm_nl4-100e8.m': 0.9135000109672546, 'data/mldoc/ja-1/models/sp30k/lstm_nl4-100e8.m': 0.7112500071525574, 'data/mldoc/fr-1/models/sp30k/lstm_nl4-100e8.m': 0.8877500295639038, 'data/mldoc/ru-1/models/sp30k/lstm_nl4-100e8.m': 0.722000002861023, 'data/mldoc/es-1/models/sp30k/lstm_nl4-100e8.m': 0.8169999718666077}

python -m ulmfit eval --glob="mldoc/es-1/models/sp30k/lstm_nl4.m" --name nl4-100-2nd --cuda-id=1 --num-cls-epochs=8 --limit=100
Max vocab: 30000
Cache dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k
Model dir: /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4-100-2nd.m
Training
Loading validation /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/es.dev.csv
Tokenized data loaded, lm.trn 13013, lm.val 1445
Limiting data set to: 100
Tokenized data loaded, cls.trn 100, cls.val 100
Size of vocabulary: 30000
First 20 words in vocab: ['xxunk', 'xxpad', 'xxbos', 'xxfld', 'xxmaj', 'xxup', 'xxrep', 'xxwrep', '<unk>', '▁', '▁de', '▁,', '▁la', '▁.', '▁en', '▁el', '▁y', 's', '▁a', '▁que']
Training args:  {'tie_weights': True, 'clip': 0.12, 'bptt': 70, 'pretrained_fnames': [PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4.m/lm_best'), PosixPath('/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4.m/../itos')], 'pretrained_model': None, 'drop_mult': 0.3} dps:  [0.25 0.1  0.2  0.02 0.15]
Unknown tokens 0, first 100: []
/home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k
Saving info /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4-100-2nd.m/info.json
Starting classifier training
epoch     train_loss  valid_loss  accuracy
1         1.243127    1.354496    0.290000
epoch     train_loss  valid_loss  accuracy
1         0.840900    1.213333    0.460000
epoch     train_loss  valid_loss  accuracy
1         0.656407    1.055138    0.750000
epoch     train_loss  valid_loss  accuracy
1         0.558013    0.983957    0.780000
2         0.554590    0.915244    0.750000
3         0.536740    0.840074    0.770000
4         0.521179    0.759908    0.790000
5         0.515218    0.692961    0.810000
6         0.500587    0.639504    0.810000
7         0.486596    0.593410    0.840000
8         0.472318    0.550126    0.830000
Saving models at /home/pczapla/workspace/ulmfit-multilingual/data/mldoc/es-1/models/sp30k/lstm_nl4-100-2nd.m
Loss and accuracy using (cls_best): [0.5382241, tensor(0.8332)]
{'data/mldoc/es-1/models/sp30k/lstm_nl4-100-2nd.m': 0.8332499861717224}

```