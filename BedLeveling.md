## Excelente tutorial sobre auto alinhamento do Eixo Z
[All Things Z - Deep Dive - Marlin Tricks - Chris's Basement](https://www.youtube.com/watch?v=3jAFQdTk8iw)

````
STRING_CONFIG_H_AUTHOR
````

````
MOTHERBOARD BOARD_MKS_GEN_L_V21
````

````
BAUDRATE 250000
BAUD_RATE_GCODE
````

````
CUSTOM_MACHINE_NAME
````

````
MACHINE_UUID
````

````
X_DRIVER_TYPE  TMC2209
Y_DRIVER_TYPE  TMC2209
Z_DRIVER_TYPE  TMC2209
Z2_DRIVER_TYPE TMC2209
E0_DRIVER_TYPE TMC2209_STANDALONE
````

TEMP_SENSOR_BED 1

PIDs do Hotend E3DV6
````
DEFAULT_Kp 34.49
DEFAULT_Ki 3.86
DEFAULT_Kd 76.99	
````

PIDs da Mesa de 246mm
````
PIDTEMPBED
DEFAULT_bedKp 407.68
DEFAULT_bedKi 61.44
DEFAULT_bedKd 676.29
````

````
EXTRUDE_MAXLENGTH 600
````

````
ENDSTOPPULLUP_XMIN
ENDSTOPPULLUP_YMIN
ENDSTOPPULLUP_ZMIN
````

````
DEFAULT_AXIS_STEPS_PER_UNIT   { 80, 80, 400, 138.78 }
DEFAULT_MAX_FEEDRATE          { 400, 400, 20, 50 }
DEFAULT_MAX_ACCELERATION      { 2000, 2000, 100, 10000 }
````



````
DEFAULT_ACCELERATION          400
DEFAULT_RETRACT_ACCELERATION  1000
DEFAULT_TRAVEL_ACCELERATION   1000 
````

Desabilitar
````
Z_MIN_PROBE_USES_Z_MIN_ENDSTOP_PIN
Z_MIN_PROBE_PIN 32
Z_PROBE_SERVO_NR 0
Z_SERVO_ANGLES { 46, 1 }
````

````
NOZZLE_TO_PROBE_OFFSET { -42, -7, 0 }
PROBING_MARGIN 42
````

````
INVERT_X_DIR true
INVERT_Y_DIR true
INVERT_Z_DIR true
INVERT_E0_DIR false
````

````
X_BED_SIZE 246
Y_BED_SIZE 246
X_MIN_POS -4
Z_MAX_POS 240
````

````
MIN_SOFTWARE_ENDSTOPS
````

````
AUTO_BED_LEVELING_BILINEAR
````

````
LCD_BED_TRAMMING
````

````
HOMING_FEEDRATE_MM_M { (100*60), (100*60), (4*60) }
````

````
EEPROM_SETTINGS
````

````
PREHEAT_1_TEMP_HOTEND 180
PREHEAT_1_TEMP_BED     70
````

````
PREHEAT_2_TEMP_HOTEND 240
PREHEAT_2_TEMP_BED    110
````

````
NOZZLE_PARK_FEATURE
NOZZLE_PARK_POINT { (X_MIN_POS + 10), (Y_MAX_POS - 10), 20 }
````

````
PRINTCOUNTER
````

````
DISPLAY_CHARSET_HD44780 WESTERN
````

````
SDSUPPORT
````

````
REVERSE_ENCODER_DIRECTION
````

````
SPEAKER
````

````
REPRAP_DISCOUNT_FULL_GRAPHIC_SMART_CONTROLLER
````


````
FAN_SOFT_PWM
````

````
RGB_LED_R_PIN 34
RGB_LED_G_PIN 43
RGB_LED_B_PIN 35
````

````
NEOPIXEL2_PIN               25
NEOPIXEL_BRIGHTNESS         200
````

````
NUM_SERVOS 3
SERVO_DELAY { 300, 0, 0 }
DEACTIVATE_SERVOS_AFTER_MOVE
EDITABLE_SERVO_ANGLES
````

````
Z_MIN_PROBE_PIN 32
Z_MIN_PROBE_ENDSTOP_INVERTING
````

````
Z_PROBE_SERVO_NR 0  
Z_SERVO_ANGLES { 46, 1 } 
````



 
      +-- BACK ---+
      |    [+]    |
    L |        1  | R <-- Example "1" (right+,  back+)
    E |  2        | I <-- Example "2" ( left-,  back+)
    F |[-]  N  [+]| G <-- Nozzle
    T |       3   | H <-- Example "3" (right+, front-)
      | 4         | T <-- Example "4" ( left-, front-)
      |    [-]    |
      O-- FRONT --+
 
```` 
NOZZLE_TO_PROBE_OFFSET { 42, 7, 0 }
````

Most probes should stay away from the edges of the bed, but
with NOZZLE_AS_PROBE this can be negative for a wider probing area.
````
PROBING_MARGIN 42
````

X and Y axis travel speed (mm/min) between probes
````
XY_PROBE_FEEDRATE (133*60)
````
Feedrate (mm/min) for the first approach when double-probing (MULTIPLE_PROBING == 2)
````
Z_PROBE_FEEDRATE_FAST (4*60)
````

Feedrate (mm/min) for the "accurate" probe of each point
````
Z_PROBE_FEEDRATE_SLOW (Z_PROBE_FEEDRATE_FAST / 2)
````

````
MULTIPLE_PROBING 2
````

````
AUTO_BED_LEVELING_BILINEAR
````

````
RESTORE_LEVELING_AFTER_G28
````

Testar essa configuração
````
PREHEAT_BEFORE_LEVELING
````

Ligar essa
````
DEBUG_LEVELING_FEATURE
````

Testar
````
ENABLE_LEVELING_FADE_HEIGHT
````

Conferir
````
Z_SAFE_HOMING
````

Ajustar. Parece estar muito rápido
````
HOMING_FEEDRATE_MM_M { (100*60), (100*60), (4*60) }
````
