## Invertible Grayscale

We run this code under [TensorFlow](https://www.tensorflow.org) 1.6 on Ubuntu16.04 with python pakage IPL installed.

### Network Architecture

TensorFlow Implementation of our paper ["Invertible Grayscale"](http://menghanxia.github.io/papers/2018_Invertible_Grayscale_siga.pdf) accepted to SIGGRAPH ASIA 2018.

<div align="center">
	<img src="img/overview.jpg" width="90%">
</div>

### Results

<div align="center">
	<img src="img/examples.jpg" width="90%">
</div>

### Preparation

- You can use any color image set as the training data of the network, as it is a self-supervised learning scheme. 
- The patch size is set to 256x256 in the `model.py` (you may change it to any other size as you like).
- Download the pretrained VGG19 model in [here](https://mega.nz/#!xZ8glS6J!MAnE91ND_WyfZ_8mvkuSa2YcA7q-1ehfSm-Q1fxOvvs).

### Run
- Set your image folders and hyperparameters in `main.py`.

- Start training.
```python
line294: parser.add_argument('--mode', type=str, default='train', help='train, test')
```
```bash
python3 main.py
```

- Start evaluation. (access [pretrained model](https://drive.google.com/open?id=1wUKSzoYijU0dfyp9cl-9gTqyJY20OU2Y ))
```python
line 294: parser.add_argument('--mode', type=str, default='test', help='train, test')
```
```bash
python3 main.py 
```

### Copyright and License
You are granted with the [license](./LICENSE.txt) for both academic and commercial usages.