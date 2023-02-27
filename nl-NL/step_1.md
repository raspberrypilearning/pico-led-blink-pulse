Gebruik `blink` (knipperen) om een LED aan en uit te zetten.

Een LED laten knipperen:

--- code ---
---
language: python
line_numbers: false
---
led.blink() # 1 seconde aan en dan 1 seconde uit print("Knipperen") # Taak wordt onmiddelijk uitgevoerd

sleep(6) led.off() --- /code ---

Een vast aantal keren knipperen:

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=0.5, n=3, wait=True) print("Finished blinking") # Runs after 3 on/off blinks

--- /code ---

**Tip:** Als je geen aparte off_time hebt ingesteld zal deze hetzelfde zijn als on_time.

Gebruik `pulse` om geleidelijk de helderheid van een LED te veranderen:

--- code ---
---
language: python
line_numbers: false
---
led.pulse() # take 1 second to brighten and 1 second to dim print("Pulsing") # Runs immediately

--- /code ---

De pulssnelheid en aantal herhalingen controleren:

--- code ---
---
language: python
line_numbers: false
---
led.pulse(fade_in_time=2, fade_out_time=1, n=4, wait=True) # take 2 seconds to brighten and 1 second to dim print("Finished pulsing") # Runs after 4 pulses

--- /code ---

Je kunt ook aan- en uittijden en vervaagtijden combineren om fraaie effecten te maken:

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=1, fade_in_time=1, fade_out_time=1) # On for 1 second, off for 1 second, fade between print("Fancy") # Runs immediately --- /code ---

**Tip:** `blink` en `pulse` gaan door tot `off` wordt aangeroepen of tot `blink` of `pulse` worden aangeroepen met nieuwe instellingen. Gebruik `wait=True` en stel `n` in om een vast aantal keren te knipperen of te pulseren. 
