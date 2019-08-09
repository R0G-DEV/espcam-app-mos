# Using ESPCAM With Mongoose OS

## Overview
Initializes espcam library https://github.com/R0G-DEV/espcam

## Instructions
    git clone https://github.com/R0G-DEV/espcam-app-mos.git
    mos build --platform esp32 --local --verbose
    mos flash
    mos console
    
## Camera Init Fail
    [Aug  9 10:05:09.611] ?[0;31mE (977) camera: gpio_install_isr_service failed (105)?[0m
    [Aug  9 10:05:09.612] ?[0;31mE (977) camera: Camera init failed with error 0x105?[0m

## Output

    $ mos console
    Using port COM10
    [Aug  9 10:05:07.284] ets Jun  8 2016 00:22:57
    [Aug  9 10:05:07.284]
    [Aug  9 10:05:07.285] rst:0x1 (POWERON_RESET),boot:0x13 (SPI_FAST_FLASH_BOOT)
    [Aug  9 10:05:07.285] configsip: 0, SPIWP:0xee
    [Aug  9 10:05:07.286] clk_drv:0x00,q_drv:0x00,d_drv:0x00,cs0_drv:0x00,hd_drv:0x00,wp_drv:0x00
    [Aug  9 10:05:07.286] mode:DIO, clock div:1
    [Aug  9 10:05:07.286] load:0x3fff0018,len:4
    [Aug  9 10:05:07.286] load:0x3fff001c,len:6188
    [Aug  9 10:05:07.287] load:0x40078000,len:9588
    [Aug  9 10:05:07.287] load:0x40080400,len:6968
    [Aug  9 10:05:07.287] entry 0x40080740
    [Aug  9 10:05:07.288] ?[0;32mI (28) boot: ESP-IDF v3.2-r7 2nd stage bootloader?[0m
    [Aug  9 10:05:07.288] ?[0;32mI (28) boot: compile time 21:05:33?[0m
    [Aug  9 10:05:07.288] ?[0;32mI (29) boot: Enabling RNG early entropy source...?[0m
    [Aug  9 10:05:07.289] ?[0;32mI (33) qio_mode: Enabling default flash chip QIO?[0m
    [Aug  9 10:05:07.289] ?[0;32mI (38) boot: SPI Speed      : 80MHz?[0m
    [Aug  9 10:05:07.289] ?[0;32mI (43) boot: SPI Mode       : QIO?[0m
    [Aug  9 10:05:07.290] ?[0;32mI (47) boot: SPI Flash Size : 4MB?[0m
    [Aug  9 10:05:07.290] ?[0;32mI (51) boot: Partition Table:?[0m
    [Aug  9 10:05:07.290] ?[0;32mI (54) boot: ## Label            Usage          Type ST Offset   Length   Flags?[0m
    [Aug  9 10:05:07.290] ?[0;32mI (62) boot:  0 nvs              WiFi data        01 02 00009000 00004000 00000000?[0m
    [Aug  9 10:05:07.291] ?[0;32mI (70) boot:  1 otadata          OTA
    data         01 00 0000d000 00002000 00000000?[0m
    [Aug  9 10:05:07.291] ?[0;32mI (79) boot:  2 app_0            OTA
    app          00 10 00010000 00180000 00000000?[0m
    [Aug  9 10:05:07.291] ?[0;32mI (87) boot:  3 fs_0             SPIFFS           01 82 00190000 00040000 00000000?[0m
    [Aug  9 10:05:07.292] ?[0;32mI (95) boot:  4 app_1            OTA
    app          00 11 001d0000 00180000 00000000?[0m
    [Aug  9 10:05:07.292] ?[0;32mI (103) boot:  5 fs_1             SPIFFS           01 82 00350000 00040000 00000000?[0m
    [Aug  9 10:05:07.292] ?[0;32mI (112) boot: End of partition table?[0m
    [Aug  9 10:05:07.292] ?[0;32mI (116) boot: OTA data 0: seq 0x00000001, st 0x10, CRC 0x157a2b85, valid? 1?[0m
    [Aug  9 10:05:07.307] ?[0;32mI (124) boot: OTA data 1: seq 0x00000000, st 0x00, CRC 0x00000000, valid? 0?[0m
    [Aug  9 10:05:07.307] ?[0;32mI (131) esp_image: segment 0: paddr=0x00010020 vaddr=0x3f400020 size=0x2a7b0 (174000) map?[0m
    [Aug  9 10:05:07.376] ?[0;32mI (186) esp_image: segment 1: paddr=0x0003a7d8 vaddr=0x3ffb0000 size=0x02c9c ( 11420) load?[0m
    [Aug  9 10:05:07.376] ?[0;32mI (189) esp_image: segment 2: paddr=0x0003d47c vaddr=0x40080000 size=0x00400 (  1024) load?[0m
    [Aug  9 10:05:07.377] ?[0;32mI (193) esp_image: segment 3: paddr=0x0003d884 vaddr=0x40080400 size=0x0278c ( 10124) load?[0m
    [Aug  9 10:05:07.377] ?[0;32mI (204) esp_image: segment 4: paddr=0x00040018 vaddr=0x400d0018 size=0xb24a0 (730272) map?[0m
    [Aug  9 10:05:07.565] ?[0;32mI (401) esp_image: segment 5: paddr=0x000f24c0 vaddr=0x40082b8c size=0x122c0 ( 74432) load?[0m
    [Aug  9 10:05:07.627] ?[0;32mI (435) boot: Loaded app from partition at offset 0x10000?[0m
    [Aug  9 10:05:07.627] ?[0;32mI (436) boot: Disabling RNG early entropy source...?[0m
    [Aug  9 10:05:07.627] ?[0;32mI (436) spiram: Found 64MBit SPI RAM
    device?[0m
    [Aug  9 10:05:07.628] ?[0;32mI (441) spiram: SPI RAM mode: flash 40m sram 40m?[0m
    [Aug  9 10:05:07.628] ?[0;32mI (446) spiram: PSRAM initialized, cache is in normal (1-core) mode.?[0m
    [Aug  9 10:05:07.628] ?[0;32mI (453) cpu_start: Pro cpu up.?[0m
    [Aug  9 10:05:07.629] ?[0;32mI (457) cpu_start: Single core mode?[0m
    [Aug  9 10:05:08.615] ?[0;32mI (1332) spiram: SPI SRAM memory test OK?[0m
    [Aug  9 10:05:08.615] D (1332) memory_layout: Checking 6 reserved
    memory ranges:?[0m
    [Aug  9 10:05:08.616] D (1332) memory_layout: Reserved memory range 0x3f800000 - 0x3fc00000?[0m
    [Aug  9 10:05:08.616] D (1338) memory_layout: Reserved memory range 0x3ffae000 - 0x3ffae6e0?[0m
    [Aug  9 10:05:08.617] D (1344) memory_layout: Reserved memory range 0x3ffb0000 - 0x3ffbacf0?[0m
    [Aug  9 10:05:08.617] D (1351) memory_layout: Reserved memory range 0x3ffe0000 - 0x3ffe0440?[0m
    [Aug  9 10:05:08.617] D (1357) memory_layout: Reserved memory range 0x40070000 - 0x40078000?[0m
    [Aug  9 10:05:08.617] D (1364) memory_layout: Reserved memory range 0x40080000 - 0x40094e4c?[0m
    [Aug  9 10:05:08.618] D (1370) memory_layout: Building list of available memory regions:?[0m
    [Aug  9 10:05:08.618] D (1376) memory_layout: Available memory region 0x3ffae6e0 - 0x3ffb0000?[0m
    [Aug  9 10:05:08.618] D (1383) memory_layout: Available memory region 0x3ffbacf0 - 0x3ffc0000?[0m
    [Aug  9 10:05:08.619] D (1390) memory_layout: Available memory region 0x3ffc0000 - 0x3ffc2000?[0m
    [Aug  9 10:05:08.620] D (1396) memory_layout: Available memory region 0x3ffc2000 - 0x3ffc4000?[0m
    [Aug  9 10:05:08.620] D (1403) memory_layout: Available memory region 0x3ffc4000 - 0x3ffc6000?[0m
    [Aug  9 10:05:08.621] D (1410) memory_layout: Available memory region 0x3ffc6000 - 0x3ffc8000?[0m
    [Aug  9 10:05:08.621] D (1416) memory_layout: Available memory region 0x3ffc8000 - 0x3ffca000?[0m
    [Aug  9 10:05:08.621] D (1423) memory_layout: Available memory region 0x3ffca000 - 0x3ffcc000?[0m
    [Aug  9 10:05:08.622] D (1430) memory_layout: Available memory region 0x3ffcc000 - 0x3ffce000?[0m
    [Aug  9 10:05:08.622] D (1436) memory_layout: Available memory region 0x3ffce000 - 0x3ffd0000?[0m
    [Aug  9 10:05:08.628] D (1443) memory_layout: Available memory region 0x3ffd0000 - 0x3ffd2000?[0m
    [Aug  9 10:05:08.629] D (1450) memory_layout: Available memory region 0x3ffd2000 - 0x3ffd4000?[0m
    [Aug  9 10:05:08.745] D (1457) memory_layout: Available memory region 0x3ffd4000 - 0x3ffd6000?[0m
    [Aug  9 10:05:08.746] D (1463) memory_layout: Available memory region 0x3ffd6000 - 0x3ffd8000?[0m
    [Aug  9 10:05:08.747] D (1470) memory_layout: Available memory region 0x3ffd8000 - 0x3ffda000?[0m
    [Aug  9 10:05:08.747] D (1477) memory_layout: Available memory region 0x3ffda000 - 0x3ffdc000?[0m
    [Aug  9 10:05:08.748] D (1483) memory_layout: Available memory region 0x3ffdc000 - 0x3ffde000?[0m
    [Aug  9 10:05:08.749] D (1490) memory_layout: Available memory region 0x3ffde000 - 0x3ffe0000?[0m
    [Aug  9 10:05:08.749] D (1497) memory_layout: Available memory region 0x3ffe0440 - 0x3ffe4000?[0m
    [Aug  9 10:05:08.750] D (1503) memory_layout: Available memory region 0x3ffe4000 - 0x3ffe8000?[0m
    [Aug  9 10:05:08.750] D (1510) memory_layout: Available memory region 0x3ffe8000 - 0x3fff0000?[0m
    [Aug  9 10:05:08.751] D (1517) memory_layout: Available memory region 0x3fff0000 - 0x3fff8000?[0m
    [Aug  9 10:05:08.751] D (1523) memory_layout: Available memory region 0x3fff8000 - 0x3fffc000?[0m
    [Aug  9 10:05:08.752] D (1530) memory_layout: Available memory region 0x3fffc000 - 0x40000000?[0m
    [Aug  9 10:05:08.753] D (1537) memory_layout: Available memory region 0x40078000 - 0x40080000?[0m
    [Aug  9 10:05:08.754] D (1543) memory_layout: Available memory region 0x40094e4c - 0x40096000?[0m
    [Aug  9 10:05:08.755] D (1550) memory_layout: Available memory region 0x40096000 - 0x40098000?[0m
    [Aug  9 10:05:08.755] D (1557) memory_layout: Available memory region 0x40098000 - 0x4009a000?[0m
    [Aug  9 10:05:08.756] D (1563) memory_layout: Available memory region 0x4009a000 - 0x4009c000?[0m
    [Aug  9 10:05:08.756] D (1570) memory_layout: Available memory region 0x4009c000 - 0x4009e000?[0m
    [Aug  9 10:05:08.757] D (1577) memory_layout: Available memory region 0x4009e000 - 0x400a0000?[0m
    [Aug  9 10:05:08.876] ?[0;32mI (1584) heap_init: Initializing. RAM available for dynamic allocation:?[0m
    [Aug  9 10:05:08.877] D (1591) heap_init: New heap initialised at
    0x3ffae6e0?[0m
    [Aug  9 10:05:08.877] ?[0;32mI (1596) heap_init: At 3FFAE6E0 len 00001920 (6 KiB): DRAM?[0m
    [Aug  9 10:05:08.878] D (1602) heap_init: New heap initialised at
    0x3ffbacf0?[0m
    [Aug  9 10:05:08.879] ?[0;32mI (1607) heap_init: At 3FFBACF0 len 00025310 (148 KiB): DRAM?[0m
    [Aug  9 10:05:08.879] ?[0;32mI (1614) heap_init: At 3FFE0440 len 0001FBC0 (126 KiB): D/IRAM?[0m
    [Aug  9 10:05:08.880] D (1620) heap_init: New heap initialised at
    0x40078000?[0m
    [Aug  9 10:05:08.881] ?[0;32mI (1625) heap_init: At 40078000 len 00008000 (32 KiB): IRAM?[0m
    [Aug  9 10:05:08.892] D (1632) heap_init: New heap initialised at
    0x40094e4c?[0m
    [Aug  9 10:05:08.894] ?[0;32mI (1637) heap_init: At 40094E4C len 0000B1B4 (44 KiB): IRAM?[0m
    [Aug  9 10:05:08.895] ?[0;32mI (1643) cpu_start: Pro cpu start user code?[0m
    [Aug  9 10:05:08.896] ?[0;32mI (1648) spiram: Adding pool of 4096K of external SPI memory to heap allocator?[0m
    [Aug  9 10:05:08.897] D (1663) clk: RTC_SLOW_CLK calibration value: 3382643?[0m
    [Aug  9 10:05:08.898] D (331) intr_alloc: Connected src 57 to int
    2 (cpu 0)?[0m
    [Aug  9 10:05:08.900] D (331) intr_alloc: Connected src 24 to int
    3 (cpu 0)?[0m
    [Aug  9 10:05:08.902] ?[0;32mI (332) cpu_start: Starting scheduler on PRO CPU.?[0m
    [Aug  9 10:05:08.903] D (337) heap_init: New heap initialised at 0x3ffe0440?[0m
    [Aug  9 10:05:08.904] ?[0;32mI (337) spiram: Reserving pool of 32K of internal memory for DMA/internal allocations?[0m
    [Aug  9 10:05:08.904] D (347) spiram: Allocating block of size 32768 bytes?[0m
    [Aug  9 10:05:08.905] D (347) intr_alloc: Connected src 16 to int
    9 (cpu 0)?[0m
    [Aug  9 10:05:08.906] D (367) nvs: nvs_flash_init_custom partition=nvs start=9 count=4?[0m
    [Aug  9 10:05:08.908] D (377) intr_alloc: Connected src 34 to int
    12 (cpu 0)?[0m
    [Aug  9 10:05:08.908]
    [Aug  9 10:05:08.909]
    [Aug  9 10:05:08.909] mgos_freertos.c:175     espcam-master 1.0 (20190809-150244/gfa27005-master-dirty)
    [Aug  9 10:05:08.911] mgos_freertos.c:177     Mongoose OS 2.15.0 (20190809-150242/2.15.0-g787ac38)
    [Aug  9 10:05:08.912] mgos_freertos.c:181     CPU: 160 MHz, FreeRTOS 8.2.0, heap: 4515296 total, 4418348 free
    [Aug  9 10:05:08.914] mgos_freertos.c:183     Newlib 2.2.0
    [Aug  9 10:05:08.914] esp32_main.c:116        ESP-IDF v3.2-r7
    [Aug  9 10:05:08.955] esp32_main.c:119        Boot partition: app_0; flash: 4M
    [Aug  9 10:05:08.955] mg_lwip_ev_mgr.c:93     Mongoose 6.15, LwIP
    2.0.3
    [Aug  9 10:05:08.956] mg_ssl_if_mbedtls.c:57  mbed TLS 2.16.0-cesanta4
    [Aug  9 10:05:08.956] mgos_vfs_dev.c:73       fs_0: esp32part ({"label": "fs_0"}), size 262144
    [Aug  9 10:05:08.957] mgos_vfs_dev.c:73       fs_1: esp32part ({"label": "fs_1"}), size 262144
    [Aug  9 10:05:08.957] mgos_vfs.c:147          /: SPIFFS @ fs_0, opts {"bs": 4096, "ps": 256, "es": 4096}
    [Aug  9 10:05:09.047] mgos_vfs.c:320          /: size 233681, used: 28614, free: 205067
    [Aug  9 10:05:09.047] D (537) intr_alloc: Connected src 22 to int
    13 (cpu 0)?[0m
    [Aug  9 10:05:09.163] mgos_sys_config.c:368   MAC: cc:50:e3:96:54:e8
    [Aug  9 10:05:09.163] mgos_sys_config.c:376   WDT: 30 seconds
    [Aug  9 10:05:09.169] mgos_deps_init.c:78     init i2c...
    [Aug  9 10:05:09.169] mgos_deps_init.c:78     init atca...
    [Aug  9 10:05:09.170] mgos_deps_init.c:78     init espcam...
    [Aug  9 10:05:09.171] initializing CameraD (627) camera: Enabling
    XCLK output?[0m
    [Aug  9 10:05:09.172] D (637) ledc: LEDC_PWM CHANNEL 0|GPIO 00|Duty 0002|Time 0?[0m
    [Aug  9 10:05:09.173] D (647) camera: Initializing SSCB?[0m
    [Aug  9 10:05:09.173] D (647) camera: Resetting camera by power down line?[0m
    [Aug  9 10:05:09.174] ?[0;32mI (647) gpio: GPIO[32]| InputEn: 0| OutputEn: 1| OpenDrain: 0| Pullup: 0| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.177] D (677) camera: Resetting via SCCB?[0m
    [Aug  9 10:05:09.189] D (687) camera: Searching for camera address?[0m
    [Aug  9 10:05:09.204] D (697) camera: Detected camera at address=0x30?[0m
    [Aug  9 10:05:09.228] D (717) camera: Camera PID=0x26 VER=0x42 MIDL=0x7f MIDH=0xa2?[0m
    [Aug  9 10:05:09.229] D (717) ov2640: OV2640 Attached?[0m
    [Aug  9 10:05:09.229] D (717) camera: Doing SW reset of sensor?[0m
    [Aug  9 10:05:09.396] D (767) camera: Detected OV2640 camera?[0m
    [Aug  9 10:05:09.397] D (767) camera: in_bpp: 2, fb_bpp: 2, fb_size: 60000, mode: 3, width: 800 height: 600?[0m
    [Aug  9 10:05:09.397] ?[0;32mI (777) gpio: GPIO[35]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.398] ?[0;32mI (787) gpio: GPIO[34]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.399] ?[0;32mI (797) gpio: GPIO[39]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.399] ?[0;32mI (807) gpio: GPIO[36]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.400] ?[0;32mI (817) gpio: GPIO[21]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.400] ?[0;32mI (827) gpio: GPIO[19]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.401] ?[0;32mI (827) gpio: GPIO[18]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.402] ?[0;32mI (837) gpio: GPIO[5]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.402] ?[0;32mI (847) gpio: GPIO[25]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.403] ?[0;32mI (857) gpio: GPIO[23]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.403] ?[0;32mI (867) gpio: GPIO[22]| InputEn: 1| OutputEn: 0| OpenDrain: 0| Pullup: 1| Pulldown: 0| Intr:0 ?[0m
    [Aug  9 10:05:09.404] D (877) intr_alloc: Connected src 32 to int
    17 (cpu 0)?[0m
    [Aug  9 10:05:09.404] D (877) camera: Line width (for DMA): 6400 bytes?[0m
    [Aug  9 10:05:09.405] D (887) camera: DMA buffer size: 3200, DMA buffers per line: 2?[0m
    [Aug  9 10:05:09.406] D (897) camera: DMA buffer count: 8?[0m
    [Aug  9 10:05:09.407] D (897) camera: DMA buffer total: 25600 bytes?[0m
    [Aug  9 10:05:09.407] D (907) camera: Allocating DMA buffer #0, size=3200?[0m
    [Aug  9 10:05:09.450] D (907) camera: Allocating DMA buffer #1, size=3200?[0m
    [Aug  9 10:05:09.450] D (917) camera: Allocating DMA buffer #2, size=3200?[0m
    [Aug  9 10:05:09.451] D (917) camera: Allocating DMA buffer #3, size=3200?[0m
    [Aug  9 10:05:09.451] D (927) camera: Allocating DMA buffer #4, size=3200?[0m
    [Aug  9 10:05:09.451] D (927) camera: Allocating DMA buffer #5, size=3200?[0m
    [Aug  9 10:05:09.452] D (937) camera: Allocating DMA buffer #6, size=3200?[0m
    [Aug  9 10:05:09.452] D (937) camera: Allocating DMA buffer #7, size=3200?[0m
    [Aug  9 10:05:09.452] ?[0;32mI (937) camera: Allocating 1 frame buffers (58 KB total)?[0m
    [Aug  9 10:05:09.464] ?[0;32mI (957) camera: Allocating 58 KB frame buffer in OnBoard RAM?[0m
    [Aug  9 10:05:09.611] D (967) camera: gpio_install_isr_service state (105)?[0m
    [Aug  9 10:05:09.611] ?[0;31mE (977) camera: gpio_install_isr_service failed (105)?[0m
    [Aug  9 10:05:09.612] ?[0;31mE (977) camera: Camera init failed with error 0x105?[0m
    [Aug  9 10:05:09.612] mgos_deps_init.c:78     init mbedtls...
    [Aug  9 10:05:09.612] mgos_deps_init.c:78     init rpc-common...
    [Aug  9 10:05:09.613] mgos_deps_init.c:78     init rpc-uart...
    [Aug  9 10:05:09.613]  mgos_rpc_channel_ua:313 0x3ffbb1f0 UART0
    [Aug  9 10:05:09.613] mg_rpc.c:539            0x3ffbb1f0 '' UART
    [Aug  9 10:05:09.614] mg_rpc.c:470            0x3ffbb1f0 CHAN OPEN (UART UART0)
    [Aug  9 10:05:09.614] mgos_deps_init.c:78     init spi...
    [Aug  9 10:05:09.614] mgos_deps_init.c:78     init wifi...
    [Aug  9 10:05:09.614] mgos_wifi.c:458         WiFi mode: AP
    [Aug  9 10:05:09.615] esp32_wifi.c:231        cur mode: 0
    [Aug  9 10:05:09.615] esp32_wifi.c:196        WiFi mode: AP
    [Aug  9 10:05:09.615] Camera Init FailedD (1027) nvs: nvs_open_from_partition misc 1?[0m
    [Aug  9 10:05:09.615] D (1037) nvs: nvs_get_str_or_blob log?[0m
    [Aug  9 10:05:09.616] D (1037) nvs: nvs_set_blob log 24?[0m
    [Aug  9 10:05:09.616] I (1047) wifi: wifi driver task: 3ffbbb4c, prio:23, stack:3584, core=0
    [Aug  9 10:05:09.616] I (1047) wifi: wifi firmware version: 693c7b6
    [Aug  9 10:05:09.616] I (1057) wifi: config NVS flash: enabled
    [Aug  9 10:05:09.617] I (1057) wifi: config nano formating: disabled
    [Aug  9 10:05:09.617] D (1067) nvs: nvs_open_from_partition nvs.net80211 1?[0m
    [Aug  9 10:05:09.617] D (1067) nvs: nvs_get opmode 1?[0m
    [Aug  9 10:05:09.617] D (1077) nvs: nvs_set opmode 1 2?[0m
    [Aug  9 10:05:09.618] D (1077) nvs: nvs_get_str_or_blob sta.ssid?[0m
    [Aug  9 10:05:09.618] D (1077) nvs: nvs_set_blob sta.ssid 36?[0m
    [Aug  9 10:05:09.618] D (1087) nvs: nvs_get_str_or_blob sta.mac?[0m
    [Aug  9 10:05:09.619] D (1087) nvs: nvs_set_blob sta.mac 6?[0m
    [Aug  9 10:05:09.619] D (1097) nvs: nvs_get sta.authmode 1?[0m
    [Aug  9 10:05:09.619] D (1097) nvs: nvs_set sta.authmode 1 1?[0m
    [Aug  9 10:05:09.619] D (1097) nvs: nvs_get_str_or_blob sta.pswd?[0m
    [Aug  9 10:05:09.620] D (1107) nvs: nvs_set_blob sta.pswd 65?[0m
    [Aug  9 10:05:09.620] D (1107) nvs: nvs_get_str_or_blob sta.pmk?[0m
    [Aug  9 10:05:09.621] D (1117) nvs: nvs_set_blob sta.pmk 32?[0m
    [Aug  9 10:05:09.621] D (1117) nvs: nvs_get sta.chan 1?[0m
    [Aug  9 10:05:09.621] D (1117) nvs: nvs_set sta.chan 1 0?[0m
    [Aug  9 10:05:09.760] D (1127) nvs: nvs_get auto.conn 1?[0m
    [Aug  9 10:05:09.761] D (1127) nvs: nvs_set auto.conn 1 1?[0m
    [Aug  9 10:05:09.762] D (1127) nvs: nvs_get bssid.set 1?[0m
    [Aug  9 10:05:09.762] D (1137) nvs: nvs_set bssid.set 1 0?[0m
    [Aug  9 10:05:09.762] D (1137) nvs: nvs_get_str_or_blob sta.bssid?
    [0m
    [Aug  9 10:05:09.763] D (1137) nvs: nvs_set_blob sta.bssid 6?[0m
    [Aug  9 10:05:09.763] D (1147) nvs: nvs_get sta.lis_intval 2?[0m
    [Aug  9 10:05:09.764] D (1147) nvs: nvs_set sta.lis_intval 2 3?[0m

    [Aug  9 10:05:09.776] D (1157) nvs: nvs_get sta.phym 1?[0m
    [Aug  9 10:05:09.776] D (1157) nvs: nvs_set sta.phym 1 3?[0m
    [Aug  9 10:05:09.777] D (1157) nvs: nvs_get sta.phybw 1?[0m
    [Aug  9 10:05:09.777] D (1167) nvs: nvs_set sta.phybw 1 2?[0m
    [Aug  9 10:05:09.778] D (1167) nvs: nvs_get_str_or_blob sta.apsw?[
    0m
    [Aug  9 10:05:09.778] D (1177) nvs: nvs_set_blob sta.apsw 2?[0m
    [Aug  9 10:05:09.779] D (1177) nvs: nvs_get_str_or_blob sta.apinfo?[0m
    [Aug  9 10:05:09.779] D (1177) nvs: nvs_set_blob sta.apinfo 700?[0m
    [Aug  9 10:05:09.810] D (1187) nvs: nvs_get sta.scan_method 1?[0m
    [Aug  9 10:05:09.811] D (1187) nvs: nvs_set sta.scan_method 1 0?[0m
    [Aug  9 10:05:09.811] D (1197) nvs: nvs_get sta.sort_method 1?[0m
    [Aug  9 10:05:09.813] D (1197) nvs: nvs_set sta.sort_method 1 0?[0m
    [Aug  9 10:05:09.827] D (1207) nvs: nvs_get sta.minrssi 1?[0m
    [Aug  9 10:05:09.835] D (1207) nvs: nvs_set sta.minrssi 1 -127?[0m
    [Aug  9 10:05:09.836] D (1207) nvs: nvs_get sta.minauth 1?[0m
    [Aug  9 10:05:09.836] D (1217) nvs: nvs_set sta.minauth 1 0?[0m
    [Aug  9 10:05:09.836] D (1217) nvs: nvs_get_str_or_blob ap.ssid?[0m
    [Aug  9 10:05:09.837] D (1217) nvs: nvs_set_blob ap.ssid 36?[0m
    [Aug  9 10:05:09.837] D (1227) nvs: nvs_get_str_or_blob ap.mac?[0m
    [Aug  9 10:05:09.841] D (1227) nvs: nvs_set_blob ap.mac 6?[0m
    [Aug  9 10:05:09.841] D (1237) nvs: nvs_get_str_or_blob ap.passwd?[0m
    [Aug  9 10:05:09.842] D (1237) nvs: nvs_set_blob ap.passwd 65?[0m
    [Aug  9 10:05:09.842] D (1247) nvs: nvs_get_str_or_blob ap.pmk?[0m
    [Aug  9 10:05:09.843] D (1247) nvs: nvs_set_blob ap.pmk 32?[0m
    [Aug  9 10:05:09.844] D (1247) nvs: nvs_get ap.chan 1?[0m
    [Aug  9 10:05:09.844] D (1257) nvs: nvs_set ap.chan 1 1?[0m
    [Aug  9 10:05:09.844] D (1257) nvs: nvs_get ap.authmode 1?[0m
    [Aug  9 10:05:09.895] D (1257) nvs: nvs_set ap.authmode 1 0?[0m
    [Aug  9 10:05:09.895] D (1267) nvs: nvs_get ap.hidden 1?[0m
    [Aug  9 10:05:09.895] D (1267) nvs: nvs_set ap.hidden 1 0?[0m
    [Aug  9 10:05:09.896] D (1267) nvs: nvs_get ap.max.conn 1?[0m
    [Aug  9 10:05:09.896] D (1277) nvs: nvs_set ap.max.conn 1 4?[0m
    [Aug  9 10:05:09.896] D (1277) nvs: nvs_get bcn.interval 2?[0m
    [Aug  9 10:05:09.897] D (1287) nvs: nvs_set bcn.interval 2 100?[0m
    [Aug  9 10:05:09.897] D (1287) nvs: nvs_get ap.phym 1?[0m
    [Aug  9 10:05:09.898] D (1287) nvs: nvs_set ap.phym 1 3?[0m
    [Aug  9 10:05:09.898] D (1297) nvs: nvs_get ap.phybw 1?[0m
    [Aug  9 10:05:09.898] D (1297) nvs: nvs_set ap.phybw 1 2?[0m
    [Aug  9 10:05:09.899] D (1297) nvs: nvs_get ap.sndchan 1?[0m
    [Aug  9 10:05:09.899] D (1307) nvs: nvs_set ap.sndchan 1 1?[0m
    [Aug  9 10:05:09.899] D (1307) nvs: nvs_get lorate 1?[0m
    [Aug  9 10:05:09.900] D (1307) nvs: nvs_set lorate 1 0?[0m
    [Aug  9 10:05:09.900] D (1317) nvs: nvs_set_blob sta.mac 6?[0m
    [Aug  9 10:05:09.900] D (1317) nvs: nvs_set_blob ap.mac 6?[0m
    [Aug  9 10:05:09.900] I (1327) wifi: Init dynamic tx buffer num: 32
    [Aug  9 10:05:09.901] I (1327) wifi: Init data frame dynamic rx buffer num: 64
    [Aug  9 10:05:09.901] I (1337) wifi: Init management frame dynamic rx buffer num: 64
    [Aug  9 10:05:09.901] I (1337) wifi: Init management short buffer num: 32
    [Aug  9 10:05:09.901] I (1347) wifi: Init static tx buffer num: 16
    [Aug  9 10:05:09.902] I (1347) wifi: Init static rx buffer size: 1600
    [Aug  9 10:05:09.902] I (1347) wifi: Init static rx buffer num: 10
    [Aug  9 10:05:09.903] I (1357) wifi: Init dynamic rx buffer num: 0
