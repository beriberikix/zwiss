# zwiss
Zwiss is a electronics "Swiss Army Knife" based on the Zephyr RTOS. It enables many useful "shells" built in to Zephyr to easily work with/debug different external devices like I2C. See [this blog](https://blog.golioth.io/how-to-use-zephyr-shell-for-interactive-prototyping-with-i2c-sensors/) for the inspiration.

## Getting started
Make sure to install the correct dependencies for your operating system from Zephyr [Getting Started Guide](https://docs.zephyrproject.org/latest/develop/getting_started/index.html).

Once you're able to build a example project, initialize this code with the following:

```
python3 -m venv ~/zwiss/.venv
source ~/zwiss/.venv/bin/activate
pip install west
west init -m https://github.com/beriberikix/zwiss ~/zwiss
cd ~/zwiss
west update
west zephyr-export
pip install -r ~/zwiss/deps/zephyr/scripts/requirements.txt
```

## Building Zwiss
Zwiss currently targets off the shelf development boards. For example, you can use the Nordic Semiconductor [nRF52840 DK](https://docs.zephyrproject.org/latest/boards/arm/nrf52840dk_nrf52840/doc/index.html).

```
west build -b nrf52840dk_nrf52840 app -p
west flash
```

## Supported shells
As a basic tool, Zwiss enables these Zephyr shells:

* ADC
* DAC
* GPIO
* HWINFO
* I2C
* LED
* PWM
* SENSOR

Also useful are standard shells:

* KERNEL

In the future Zwiss will also support IoT-related shells.