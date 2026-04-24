## Wi-Fi/Bluetooth Module
<table>
  <tr>
    <th>MCU Pin</th>
    <th>Module Pin</th>
    <th>Direction</th>
    <th>Notes</th>
  </tr>
  <tr>
    <td>TODO</td>
    <td>UART_CTSn</td>
    <td>MCU &rarr; Module</td>
    <td>
      <ul>
        <li>Normally an input, but asserts LOW when PDn is LOW</li>
        <li>Microcontroller should use open-drain output with pull-up resistor to avoid driver contention</li>
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
</table>
