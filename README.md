<p align="center">
  <img height="100" height="auto" src="https://github.com/freshe4qa/nocturne/assets/85982863/cfae9cab-94b1-4189-9f25-887a4ac62583">
</p>

# Penumbra — PENUMBRA SUMMONING CEREMONY

Official documentation:
>- [Guide](https://summoning.penumbra.zone)

Explorer:
>- [-](-)

### Minimum Hardware Requirements
 - 2x CPUs; the faster clock speed the better
 - 2GB RAM
 - 20GB of storage (SSD or NVME)

```
sudo apt update && sudo apt upgrade -y
```

```
sudo apt install make clang pkg-config libssl-dev build-essential tmux -y
```
```
sudo apt-get install git-lfs
```
```
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
source ~/.cargo/env
```
```
git clone https://github.com/penumbra-zone/penumbra
```
```
cd penumbra && git fetch && git checkout v0.63.1
```
```
cargo build --release --bin pcli
```

Создаем кошелек

```
cargo run --quiet --release --bin pcli init soft-kms generate
```
```
cargo run --quiet --release --bin pcli init soft-kms import-phrase
```

Запрашиваем токены в Discord'e в ветке #testnet-faucet отправив свой адрес кошелька

Участвуем в церемонии

```
screen -S ceremony
```

```
cargo run --quiet --release --bin pcli -- ceremony contribute --phase 1 --bid 60penumbra --coordinator-address penumbra1qvqr8cvqyf4pwrl6svw9kj8eypf3fuunrcs83m30zxh57y2ytk94gygmtq5k82cjdq9y3mlaa3fwctwpdjr6fxnwuzrsy4ezm0u2tqpzw0sed82shzcr42sju55en26mavjnw4
```

Выйти CTRL + A + D
