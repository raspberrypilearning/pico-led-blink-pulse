Utilisez `blink` pour allumer et éteindre une LED.

Faire clignoter une LED :

--- code ---
---
language: python
line_numbers: false
---
led.blink() # allumé pendant 1 seconde puis éteint pendant une seconde print("Clignotant") # S'exécute immédiatement

sleep(6) led.off() --- /code ---

Clignote un nombre fixe de fois :

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=0.5, n=3, wait=True) print("Finished blinking") # Runs after 3 on/off blinks

--- /code ---

**Astuce :** Si tu ne définis pas off_time, ce sera le même que pour on_time.

Utilise `pulse` pour modifier progressivement la luminosité d'une LED :

--- code ---
---
language: python
line_numbers: false
---
led.pulse() # take 1 second to brighten and 1 second to dim print("Pulsing") # Runs immediately

--- /code ---

Contrôle la vitesse d'impulsion et le nombre de répétitions :

--- code ---
---
language: python
line_numbers: false
---
led.pulse(fade_in_time=2, fade_out_time=1, n=4, wait=True) # take 2 seconds to brighten and 1 second to dim print("Finished pulsing") # Runs after 4 pulses

--- /code ---

Tu peux également combiner des temps d'activation et de désactivation et des temps de fondu pour créer des effets fantaisistes :

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=1, fade_in_time=1, fade_out_time=1) # On for 1 second, off for 1 second, fade between print("Fancy") # Runs immediately --- /code ---

**Tip:** `blink` and `pulse` will run until `off` is called or `blink` or `pulse` are called with new settings. Use `wait=True` and set `n` to blink or pulse a fixed number of times. 
