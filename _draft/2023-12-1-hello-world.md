---
title: Hello World
author: "Yacine"
---



## First things first
  In each case, we'll implement a simple blinking LED application.
It is not particularly interesting in itself, but for the sake of completeness you can
find the code reproduced below.
In each case, we'll implement a simple blinking LED application. It is not
particularly interesting in itself, but for the sake of completeness you can
find the code reproduced below.
In each case, we'll implement a simple blinking LED application. It is not
particularly interesting in itself, but for the sake of completeness you can
find the code reproduced below.
#ae81ff00
```c
#include <samd21g18a.h>

#include <port.h>
#include <stdbool.h>
#include <stdint.h>

#define LED_0_PIN PIN_PA17

static void set_output(const uint8_t pin) {
  struct port_config config_port_pin;
  port_get_config_defaults(&config_port_pin);
  config_port_pin.direction = PORT_PIN_DIR_OUTPUT;
  port_pin_set_config(pin, &config_port_pin);
  port_pin_set_output_level(pin, false);
}

int main() {
  set_output(LED_0_PIN);
  while (true) {
    port_pin_toggle_output_level(LED_0_PIN);
    for (volatile int i = 0; i < 100000; ++i) {}
  }
}
```
Lorem ipsum dolor sit amet, consectetur adipisicing elit. Totam quasi maxime quas repudiandae nam id temporibus, at et non officiis consectetur voluptate deserunt officia minima placeat tempore illum asperiores quo assumenda praesentium? Facilis libero error ratione doloribus debitis delectus asperiores minima ab velit quam. Natus ea, vero totam recusandae autem, corporis minima, animi eos perferendis omnis ut asperiores magni tempore. Repellendus aliquam saepe perspiciatis laborum, excepturi sit libero dignissimos debitis eaque itaque quos, accusantium sed amet tempora temporibus perferendis possimus, quisquam minus fuga! Laudantium, tenetur, consectetur! Quas itaque hic consequatur accusamus consectetur, quia odio eos amet quasi pariatur! Ratione, similique.