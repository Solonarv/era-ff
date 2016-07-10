# Mana system

## What is mana

Mana represents the amount of your body's energy store available to be converted into magical energy. Your mana *can* exceed your total energy store.

## Mana stats

### Maximum mana

Determines how large your mana pool can grow. Depends on:

### Maxium mana regeneration rate

Your mana pool fills at a constant rate, once it's reached the threshold. This stat determines the regeneration rate.

### Mana threshold

If your current mana pool is below this threshold, it regenerates at an accelerating rate.

### Maximum mana transduction rate

The rate at which your mana can be converted to useful work when casting a spell. This should be set high enough to not be
noticeable outside of high-energy magic.

## Regeneration curve

### Variables
 
 - m: maximum mana
 - c: current mana
 - s: mana threshold
 - r: maximum mana regeneration rate
 - u: minimum mana regeneration rate 

 ### Formulae

#### While below mana threshold:
    
    d/dt c = r * c/s
    c = u * e^(t * r/q)

#### While above mana threshold

    d/dt c = r
    c = r * t