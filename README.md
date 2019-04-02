# thumbee
MStar MSC313E SoC breakout

#rev0

Rough layout. Minimal decoupling caps because of limited space. Test to see if two layers works.
May move to some 0402 passives if not.

## bugs

Pinout foobar #1. USB ground isn't wired up because of a difference in the pin number of the symbol
and the footprint. Fixed by shorting the id pin to ground next to it.

Pinout foobar #2. avdd_nodie and dvdd_nodie are swapped. *edit* Maybe not. Seems like there is a datasheet
mistake. Pinout in the pin diagram is correct *edit* 

Pinout foobar #3. spi mosi and spi miso are swapped

Holtek USB->Serial chip is a piece of shit and can't handle lower baud rate data before data at the 
baud read the port was opened with.


1.8v supply is no good. The chip is very sensitive to the 1.8v rail dropping slightly (probably because
the DDR gets corrupted when it happens). On boot up the 1.8v drops for a split second and this makes
bootup hit or miss. Removing the 3.3va ldo and wiring 3.3va to 3.3v allows the input voltage to be lowered
to ~3.5v from the intended 5v and that makes the drop smaller.  
