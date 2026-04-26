## Wi-Fi/Bluetooth Module
<table>
  <tr>
    <th>MCU Pin</th>
    <th>Module Pin</th>
    <th>Direction</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>GPIO_DISP_B2_13</td>
    <td>UART_CTSn</td>
    <td>MCU &rarr; Module</td>
    <td>
      <ul>
        <li>Normally an input, but asserts LOW when PDn is LOW</li>
        <li>Microcontroller should use open-drain output with pull-up resistor to avoid driver contention<sup>1</sup></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>TODO</td>
    <td>PDn</td>
    <td>MCU &rarr; Module</td>
    <td>
      <ul>
        <li>Powers down the module if set to LOW</li>
        <li>Internal 10k pull-up resistor to module's 1.8V rail</li>
        <li>Accepts inputs from 1.8V to 4.5V</li>
        <li>Firmware download is required every time PDn is asserted</li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>GPIO_SD_B2_05</td>
    <td>SD_CMD</td>
    <td>MCU &harr; Module</td>
    <td>
      <ul>
        <li>Requires microcontroller's internal pull-up resistor<sup>1</sup></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>GPIO_SD_B2_03</td>
    <td>SD_DAT[0]</td>
    <td>MCU &harr; Module</td>
    <td>
      <ul>
        <li>Requires microcontroller's internal pull-up resistor<sup>1</sup></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>GPIO_SD_B2_02</td>
    <td>SD_DAT[1]</td>
    <td>MCU &harr; Module</td>
    <td>
      <ul>
        <li>Requires microcontroller's internal pull-up resistor<sup>1</sup></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>GPIO_SD_B2_01</td>
    <td>SD_DAT[2]</td>
    <td>MCU &harr; Module</td>
    <td>
      <ul>
        <li>Requires microcontroller's internal pull-up resistor<sup>1</sup></li>
      </ul>
    </td>
  </tr>
  <tr>
    <td>GPIO_SD_B2_00</td>
    <td>SD_DAT[3]</td>
    <td>MCU &harr; Module</td>
    <td>
      <ul>
        <li>Requires microcontroller's internal pull-up resistor<sup>1</sup></li>
      </ul>
    </td>
  </tr>
</table>

<sup>1</sup> Requires modification to Zephyr device tree. For SDIO specifically, see the following references:
* [MIMXRT1170-EVK overlay](https://github.com/zephyrproject-rtos/zephyr/blob/main/boards/nxp/mimxrt1170_evk/mimxrt1170_evk-pinctrl.dtsi)
* [NXP Wi-Fi shield overlay](https://github.com/zephyrproject-rtos/zephyr/blob/main/boards/shields/nxp_m2_wifi_bt/boards/mimxrt1060_evk_mimxrt1062_qspi_C.overlay)
