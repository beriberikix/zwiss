# zwiss
Zwiss is a electronics "Swiss Army Knife" based on the Zephyr RTOS

## Getting started

```
python3 -m venv ~/zwiss/.venv
source ~/zwiss/.venv/bin/activate
pip install west
west init -m https://github.com/beriberikix/zwiss ~/zwiss
cd ~/zwiss
west update
west zephyr-export
pip install -r ~/zwiss/zephyr/scripts/requirements.txt
```