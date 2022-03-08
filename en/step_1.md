Use `blink` to turn an LED on and off. 

Blink an LED:  

--- code ---
---
language: python
line_numbers: false
---
led.blink() # on for 1 second then off for one second
print("Blinking") # Runs immediately

sleep(6)
led.off()
--- /code ---

Blink a fixed number of times:

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=0.5, n=3, wait=True)
print("Finished blinking") # Runs after 3 on/off blinks

--- /code ---

**Tip:** If you don't set off_time then it will be the same as on_time. 

Use `pulse` to gradually change the brightness of an LED:

--- code ---
---
language: python
line_numbers: false
---
led.pulse() # take 1 second to brighten and 1 second to dim
print("Pulsing") # Runs immediately

--- /code ---

Control the pulse speed and number of repeats:

--- code ---
---
language: python
line_numbers: false
---
led.pulse(fade_in_time=2, fade_out_time=1, n=4, wait=True) # take 2 seconds to brighten and 1 second to dim
print("Finished pulsing") # Runs after 4 pulses

--- /code ---

You can also combine on and off times and fade in out out times to create fancy effects:

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=1, fade_in_time=1, fade_out_time=1) # On for 1 second, off for 1 second, fade between
print("Fancy") # Runs immediately 
--- /code ---

**Tip:** `blink` and `pulse` will run until `off` is called or `blink` or `pulse` are called with new settings. Use `wait=True` and set `n` to blink or pulse a fixed number of times. 
