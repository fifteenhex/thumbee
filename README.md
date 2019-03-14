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
