# LowPin_MCU
Небольшой обзор 32bit MCU с малым количеством выводов (8-32 pin)
Альтернативы STM32 и сравнение

```
ST        - STM32   /  ARM     (Cortex-M0+)
PUYA      - PY32    /  ARM     (Cortex-M0+)
Hangshun  - HK32    /  ARM     (Cortex-M0+)
Xiaohua   - HC32    /  ARM     (Cortex-M0+)
WCH       - CH32    /  RISC-V  (RV32EC; RV32IMAC; RV32IMAFC)
```

### STM32

- очень большой выбор разных конторллеров, вот параметры некторых

STM32C011   - 48MHz; Flash 16K/32K; RAM 6K; so8,tssop20  (2.0-3.6V)<br>
STM32C031   - 48MHz; Flash 16K/32K; RAM 12K; tssop20,qfn28:32,lqfp32  (2.0-3.6V)

STM32G03x   - 64MHz; Flash 32K/64K; RAM 8K; so8,tssop20,lqfp32  (2.0-3.6V)<br>
STM32G05x   - 64MHz; Flash 32K/64K; RAM 18K; tssop20,lqfp32  (2.0-3.6V)

STM32L011   - 32MHz; Flash  8K/16K; RAM 2K; EEPROM 0.5K; tssop14:20,qfn20:28:32,lqfp32  (1.8-3.6V)<br>
STM32L031   - 32MHz; Flash 16K/32K; RAM 8K; EEPROM 1K; tssop20,qfn20:28:32,lqfp32  (1.8-3.6V)

Все остальные серии начинаются с корпусов tssop20 или больше
Контроллеров с малым количеством выводов (< 20)- не так уж и много

### PY32

- количество серий контроллеров немного, но поражает количество возможных корпусов и разной разводки

##### PY32F002A;PY32F003;PY32F030 
  по идее это одинаковый контроллер (чип один и тот же)<br>
  только разные корпуса, порты, разводка и прочее<br>

  24-48MHz; Flash 16-64K; RAM 2-8K; (1.7-5.5V)

Корпуса 
sop8:16:20  qfn16:20:24:28:32  tssop20:24  essop10  msop10  dfn8(3x2)  dfn8(1.5x1.5)  lqfp32

И ещё есть разная разводка в корпусах на что указывает дополнительная циыра в маркировке
например  PY32F003FxyP6  x - 1..6  расположение портов на выводах TSSOP20  y - (6=32K/4K)/(8=64K/8K)

PY32F030K28T6 - lqfp32  64K/8K  up to  30 i/o !!