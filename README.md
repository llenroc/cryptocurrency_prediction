![reinforcement_learning](https://img.shields.io/badge/reinforcement_learning-cryptocurrencys-8440c4.svg?colorA=32073d&longCache=true&style=for-the-badge "reinforcement learning cryptocurrencys")

![lucasdraichi](https://img.shields.io/badge/made_by-lucas_draichi-32073d.svg?colorA=8440c4&longCache=true&style=for-the-badge "lucas draichi")

# Cryptocurrency prediction

Deep tecnical analysis with **ANY** cryptocurrency

## Setup

Go to `configs/vars` and edit these lines:
```python
coins = ['bitcoin','nano','binancecoin','steem']
days = 90
currency = 'usd'
```
---
## Run

```sh
git clone https://github.com/Draichi/cryptocurrency_prediction.git
cd cryptocurrency_prediction
pip3 install -r requirements.txt
```

```sh
python3 forecast.py [asset] [how_many_days]
# e.g.: python3 forecast.py bitcoin 5
```
<div>
    <a href="https://plot.ly/~randy_marsh/9/?share_key=s1LOA27GbNRR8n1TZmEWL9" target="_blank" title="bitcoin 120 days forecast" style="display: block; text-align: center;"><img src="https://plot.ly/~randy_marsh/9.png?share_key=s1LOA27GbNRR8n1TZmEWL9" alt="bitcoin 120 days forecast" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
</div>

<div>
    <a href="https://plot.ly/~randy_marsh/19/?share_key=TVMTXwPLQ051PC4h6Fp9CO" target="_blank" title="24-8 bitcoin 0.01" style="display: block; text-align: center;"><img src="https://plot.ly/~randy_marsh/19.png?share_key=TVMTXwPLQ051PC4h6Fp9CO" alt="24-8 bitcoin 0.01" style="max-width: 100%;width: 600px;"  width="600" onerror="this.onerror=null;this.src='https://plot.ly/404.png';" /></a>
</div>


```sh
python3 scatter.py log
# log/linear = layout type
```

![10-8-2018](imgs/log.png "10-8-2018")

## Genetic Algorithm

```sh
python3 train.py [asset] [window_size] [how_many_episodes]
# e.g.: python3 train.py bitcoin 10 1000
```

![trainning](imgs/trainning.gif)

Use historical data to train a model and evaluate with fresh data

```sh
python3 evaluate.py [asset] [model]
# e.g.: python3 evaluate.py bitcoin 10-8_bitcoin_d90_e20_w12_c50_usd
```

![evaluate](imgs/evaluating.gif)

Price in: blue = buy, yellow = sell, white = hold

## Credits
- Analyzing cryptocurrency markets using python: [article](https://blog.patricktriest.com/analyzing-cryptocurrencies-python/)
- Q-trader: [repo](https://github.com/edwardhdlu/q-trader)

## To-do
- [x] grab data from coingekko
- [x] use genetic algorithm
- [ ] implement model with exchanges or gekko

![python](https://img.shields.io/badge/i_accept-pull_requests-2d72e2.svg?colorA=ae2ce2&longCache=true&style=for-the-badge "python")
