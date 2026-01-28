# Smart Coffee Mug with Temperature Controller ☕

An Arduino-based temperature control system for keeping your coffee at the perfect temperature!

## Features

- **Real-time Temperature Monitoring**: Uses a thermistor to accurately measure mug temperature
- **Automatic Heating Control**: PWM-based heating system maintains desired temperature range
- **LCD Display**: 16x2 LCD shows current temperature and heating percentage
- **Adjustable Temperature Settings**: Set custom low and high temperature thresholds
- **EEPROM Memory**: Saves your temperature preferences
- **Buzzer Alert**: Alerts when temperature exceeds the maximum threshold
- **User-Friendly Interface**: Three buttons for easy temperature adjustment

## Hardware Components

- Arduino Microcontroller
- Thermistor (Temperature Sensor)
- 16x2 LCD Display
- Heating Element
- Buzzer
- Push Buttons (3x)
- 10kΩ Resistor

## Pin Configuration

| Component | Pin |
|-----------|-----|
| LCD RS | 2 |
| LCD Enable | 3 |
| LCD D4-D7 | 4, 5, 6, 7 |
| Thermistor | A0 |
| Set Button | A3 |
| Up Button | A4 |
| Down Button | A5 |
| Heater | 9 |
| Buzzer | 13 |

## How It Works

1. The thermistor continuously monitors the coffee temperature
2. When temperature falls below the low threshold, heating begins
3. PWM control adjusts heating intensity to maintain optimal temperature
4. When temperature exceeds the high threshold, the buzzer alerts you
5. Temperature settings are stored in EEPROM for persistence

## Default Settings

- Low Temperature: 30.5°C
- High Temperature: 39.5°C

## Usage

1. Upload the code to your Arduino
2. Power on - you'll see a welcome message
3. Press SET button to enter setting mode
4. Use UP/DOWN buttons to adjust temperature thresholds
5. Press SET again to save and return to normal mode

## Temperature Control Algorithm

Uses the Steinhart-Hart equation for accurate thermistor temperature conversion:
- Converts ADC value to resistance
- Applies Steinhart-Hart coefficients
- Converts from Kelvin to Celsius
- PWM duty cycle adjusts based on temperature difference

## License

Open Source - Feel free to modify and improve!

## Author

Created with ❤️ for coffee lovers everywhere!

---

**YOLO Deployment**: Because sometimes you just need that perfect cup of coffee NOW! 🚀
