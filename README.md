# libpwm

  A user-space library for controlling the PWMv2.0 IP core provided by Digilent [here](https://github.com/digilent/vivado-library).
  
  
  This library contains basic methods for setting the frequency of the PWM controller, and setting the duty-cycle and polarity of each individual PWM channel.
  
  The number of PWM channels available is selected when placing the PWM IP core in your Vivado project.
  Additionally, this library depends on having the PWM IP core set up as a generic UIO device in the device tree. For examples, check out the device-tree at one of our other projects on github:[Arty-Z7-20](https://github.com/Digilent/Petalinux-Arty-Z7-20), and [Zybo-Z7-20](https://github.com/Digilent/Petalinux-Zybo-Z7-20).
  
  This library utilizes the libuio library located here: [libuio](https://github.com/mitchellorsucci/libuio). To properly initialize the PWM hardware in your library, you must pass the UIO device number and the UIO map number to PWM_init().
  
  For an example program that utilizes this library, check out our PWM demo program, which can be found here: [PWMdemo](https://github.com/mitchellorsucci/pwmdemo)
