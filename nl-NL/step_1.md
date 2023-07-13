Gebruik `blink` (knipperen) om een LED aan en uit te zetten.

Een LED laten knipperen:

--- code ---
---
language: python
line_numbers: false
---
led.blink() # 1 seconde aan en dan 1 seconde uit 
print("Knipperen") # Taak onmiddellijk uitvoeren

sleep(6) 
led.off()

--- /code ---

Een vast aantal keren knipperen:

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=0.5, n=3, wait=True) 
print("Knipperen voltooid") # 1 seconde aan en dan 1 seconde uit

--- /code ---

**Tip:** Als je geen aparte off_time hebt ingesteld zal deze hetzelfde zijn als on_time.

Gebruik `pulse` om geleidelijk de helderheid van een LED te veranderen:

--- code ---
---
language: python
line_numbers: false
---
led.pulse() # neem 1 seconde om op te lichten en 1 seconde om te dimmen
print("Pulseren") # Taak onmiddellijk uitvoeren

--- /code ---

De pulssnelheid en aantal herhalingen controleren:

--- code ---
---
language: python
line_numbers: false
---
led.pulse(fade_in_time=2, fade_out_time=1, n=4, wait=True) # neem 2 seconden om op te lichten en 1 seconde om te dimmen 
print("Pulseren voltooid") # Voert taak out na 4 pulsen

--- /code ---

Je kunt ook aan- en uittijden en vervaagtijden combineren om fraaie effecten te maken:

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=1, fade_in_time=1, fade_out_time=1) # 1 seconde aan, 1 seconde uit, en er tussenin vervagen 
print("Fraai") # Taak onmiddellijk uitvoeren
--- /code ---

**Tip:** `blink` en `pulse` gaan door tot `off` wordt aangeroepen of tot `blink` of `pulse` worden aangeroepen met nieuwe instellingen. Gebruik `wait=True` en stel `n` in om een vast aantal keren te knipperen of te pulseren.
