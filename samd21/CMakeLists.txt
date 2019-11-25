add_library(asf4
    hal/src/hal_io.c
    hpl/systick/hpl_systick.c
    gcc/gcc/startup_samd21.c
    hal/src/hal_spi_m_dma.c
    usb/class/hid/device/hiddf_generic.c
    usb/class/cdc/device/cdcdf_acm.c
    hal/utils/src/utils_syscalls.c
    hpl/nvmctrl/hpl_nvmctrl.c
    usb/class/msc/device/mscdf.c
    hal/src/hal_spi_m_sync.c
    hal/src/hal_timer.c
    hal/src/hal_pwm.c
    hpl/usb/hpl_usb.c
    hal/src/hal_i2c_m_sync.c
    hal/src/hal_delay.c
    hpl/sysctrl/hpl_sysctrl.c
    hpl/core/hpl_init.c
    hal/utils/src/utils_list.c
    hpl/core/hpl_core_m0plus_base.c
    hal/utils/src/utils_assert.c
    hpl/dmac/hpl_dmac.c
    hpl/pm/hpl_pm.c
    usb/class/hid/device/hiddf_keyboard.c
    usb/usb_protocol.c
    hpl/dac/hpl_dac.c
    hpl/gclk/hpl_gclk.c
    hal/src/hal_flash.c
    hal/src/hal_init.c
    hal/src/hal_usb_device.c
    gcc/system_samd21.c
    hpl/rtc/hpl_rtc.c
    driver_init.c
    hal/src/hal_usart_async.c
    hal/src/hal_adc_sync.c
    hal/src/hal_dac_sync.c
    hpl/sercom/hpl_sercom.c
    hal/utils/src/utils_ringbuffer.c
    hal/src/hal_gpio.c
    usb/class/hid/device/hiddf_mouse.c
    hal/utils/src/utils_event.c
    hal/src/hal_sleep.c
    usb_start.c
    atmel_start.c
    usb/device/usbdc.c
    hpl/tc/hpl_tc.c
    hal/src/hal_atomic.c
    hpl/adc/hpl_adc.c
    #main.c
    #examples/driver_examples.c
    )

target_include_directories(asf4 PUBLIC
    .
    config
    include
    hal/include
    hal/utils/include
    hpl/adc
    hpl/core
    hpl/dac
    hpl/dmac
    hpl/gclk
    hpl/nvmctrl
    hpl/pm
    hpl/port
    hpl/rtc
    hpl/sercom
    hpl/sysctrl
    hpl/systick
    hpl/tc
    hpl/usb
    hri
    usb
    usb/class/cdc
    usb/class/cdc/device
    usb/class/composite/device
    usb/class/hid
    usb/class/hid/device
    usb/class/hub
    usb/class/msc
    usb/class/msc/device
    usb/class/vendor
    usb/device
    CMSIS/Include
    samd21a/include
)

#target_compile_definitions(asf4 PUBLIC
#    -DDEBUG=1
#    -D__SAMD21G18A__=1
#    )
#
#target_compile_options(asf4 PUBLIC
#    -ffunction-sections -mlong-calls -g3 -Wall -c -std=gnu99
#    -mcpu=cortex-m0plus
#    )

