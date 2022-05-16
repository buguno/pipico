# Raspberry Pi Pico

## Especificação Técnica

Raspberry Pi Pico é uma placa microcontroladora de alta performance e baixo custo com interfaces digitais flexíveis. Os principais recursos incluem:

- Chip microcontrolador [RP2040](https://www.raspberrypi.com/documentation/microcontrollers/rp2040.html#welcome-to-rp2040) projetado pela Raspberry no Reino Unido
- Processador dual-core Arm Cortex M0+, com clock flexível rodando até 133 MHz
- 264KB de SRAM, e 2MB de memória flash integrada
- Além dos pinos de entradas/saídas em furos, eles também estão disponíveis de forma castelada (com isso você pode integrar a placa diretamente no seu projeto)
- Possui suporte a USB 1.1 Host e Device
- Modos de suspensão e inatividade de baixo consumo
- A programação por clicar e arrastar pode ser usada por armazenamento via USB
- 26 × pinos GPIO multifuncionais
- 2×SPI, 2×I2C, 2×UART, 3×12-bit ADC, 16×canais PWM controláveis
- RTC (Real Time Counter) de alta precisão
- Sensor de temperatura
- Possui bibliotecas para tratar ponto flutuante
- 8 × Máquinas de estado de I/O programáveis (PIO) para suporte periférico personalizado

### Pinagem

![Pico-R3-SDK11-Pinout](images/Pico-R3-SDK11-Pinout.svg)

- Download do [diagrama de pinagem](https://datasheets.raspberrypi.com/pico/Pico-R3-A4-Pinout.pdf) (PDF)

### Arquivos de design

- Download dos [arquivos de design](https://datasheets.raspberrypi.com/pico/RPi-Pico-R3-PUBLIC-20200119.zip) (Cadence Allegro)
- Download do [arquivo STEP](https://datasheets.raspberrypi.com/pico/Pico-R3-step.zip)
- Download do [arquivo do Fritzing](https://datasheets.raspberrypi.com/pico/Pico-R3-Fritzing.fzpz)

NOTE: More information on Fritzing is available on the [fritzing.org](https://fritzing.org/) web site.

## Setup com SDK

### SDK C/C++

[Introdução ao SDK C/C++](https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html)

Se você não está usando o Raspberry Pi Pico em um Raspberry Pi, use os passos abaixo.

Os comandos abaixo é um passo a passo para configurar seu ambiente de desenvolvimento para o pipico.

### Obtendo o SDK e os exemplos

O [repositório de exemplos para o pipico](https://github.com/raspberrypi/pico-examples) fornece um conjunto de exemplos que usam o [SDK do pipico](https://github.com/raspberrypi/pico-sdk). Antes de clonar os repositórios de exemplos e de SDK siga as instruções abaixo.

```bash
cd ~/
mkdir pico
cd pico
```

Em seguida, clone os repositórios pico-sdk e pico-examples.

```bash
git clone -b master https://github.com/raspberrypi/pico-sdk.git
cd pico-sdk
git submodule update --init
cd ..
git clone -b master https://github.com/raspberrypi/pico-examples.git
```

### Instalando as ferramentas

Para fazer a compilação dos scripts no repositório pico-examples, você precisa instalar algumas ferramentas extras. Para fazer a compilação você irá precisar do [CMake](https://cmake.org/), e também o [GNU Embedded Toolchain for Arm](https://developer.arm.com/tools-and-software/open-source-software/developer-tools/gnu-toolchain/gnu-rm/downloads). Você pode instalar ambos usando os comandos abaixo pelo apt via bash.

```bash
sudo apt update
sudo apt install cmake gcc-arm-none-eabi libnewlib-arm-none-eabi build-essential
```

1. GCC e G++ são necessários para compilar pioasm e elf2uf2

`Usuários do Debian e seus derivados também podem precisar instalar libstdc++-arm-none-eabi-newlib.`

## Referências

- [Technical Specification](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/microcontrollers/raspberry-pi-pico/about_pico.adoc)
- [Raspberry Pi Documentation](https://www.raspberrypi.com/documentation/microcontrollers/)
- [Getting started with Raspberry Pi Pico C/C++ development with Raspberry Pi Pico and other RP2040-based microcontroller boards](https://datasheets.raspberrypi.com/pico/getting-started-with-pico.pdf) (PDF)
