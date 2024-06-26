<p align="center">
  <img height="100" height="auto" src="https://github.com/freshe4qa/nocturne/assets/85982863/cfae9cab-94b1-4189-9f25-887a4ac62583">
</p>

# Penumbra — PENUMBRA SUMMONING CEREMONY PHASE 2

Official documentation:
>- [Guide](https://summoning.penumbra.zone)

Explorer:
>- [-](-)

### Minimum Hardware Requirements
 - 2x CPUs; the faster clock speed the better
 - 4GB RAM
 - 100GB of storage (SSD or NVME)
 - Ubuntu 22.04

```
sudo apt update && sudo apt upgrade -y
```

```
sudo apt install make clang pkg-config libssl-dev build-essential tmux -y
```
```
sudo apt-get install build-essential pkg-config libssl-dev clang git-lfs
```
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source ~/.cargo/env
```
```
curl --proto '=https' --tlsv1.2 -LsSf https://github.com/penumbra-zone/penumbra/releases/download/v0.77.2/pcli-installer.sh | sh
```

Создаем кошелек

```
pcli init soft-kms generate
```
```
pcli init soft-kms import-phrase
```

Запрашиваем токены в Discord'e в ветке #testnet-faucet отправив свой адрес кошелька

Участвуем в церемонии

```
screen -S ceremony
```

```
pcli ceremony contribute --phase 2 --bid 60penumbra
```

Выйти CTRL + A + D
