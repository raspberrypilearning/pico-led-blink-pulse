Utilisez `blink` pour allumer et éteindre une LED.

Faire clignoter une LED :

--- code ---
---
language: python
line_numbers: false
---
led.blink() # Allumé pendant 1 seconde puis éteint pendant une seconde 
print("Clignotante") # S'exécute immédiatement

sleep(6) 
led.off()

--- /code ---

Clignote un nombre fixe de fois :

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=0.5, n=3, wait=True) 
print("Clignotement terminé") # Fonctionne après 3 clignotements marche/arrêt

--- /code ---

**Astuce :** Si tu ne définis pas off_time, ce sera le même que pour on_time.

Utilise `pulse` pour modifier progressivement la luminosité d'une LED :

--- code ---
---
language: python
line_numbers: false
---
led.pulse() # Prendre 1 seconde pour éclaircir et 1 seconde pour assombrir 
print("Pulsation") # S'exécute immédiatement

--- /code ---

Contrôle la vitesse d'impulsion et le nombre de répétitions :

--- code ---
---
language: python
line_numbers: false
---
led.pulse(fade_in_time=2, fade_out_time=1, n=4, wait=True) # Prendre 2 secondes pour éclaircir et 1 seconde pour atténuer 
print("Pulsation finie") # Fonctionne après 4 impulsions

--- /code ---

Tu peux également combiner des temps d'activation et de désactivation et des temps de fondu pour créer des effets fantaisistes :

--- code ---
---
language: python
line_numbers: false
---
led.blink(on_time=1, off_time=1, fade_in_time=1, fade_out_time=1) # Allumé pendant 1 seconde, éteint pendant 1 seconde, fondu entre 
print("Fantaisiste") # S'exécute immédiatement
--- /code ---

**Astuce :** `blink` et `pulse` fonctionneront jusqu'à ce que `off` soit appelé ou `blink` ou `pulse` soient appelés avec des nouveaux paramètres. Utilise `wait=True` et régle `n` pour clignoter ou pulser un nombre fixe de fois.
