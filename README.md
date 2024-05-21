# crypto

Install jupyterlab, to follow along.

Open `CMD` and copy:

    pip install notebook

# Prestavitev

## Ceaser shift

Link za encrypcijo decripcijo ceasrjeve številke [Crypto](https://www.dcode.fr/caesar-cipher).

## Diffie-Hellman

Exchanging information over a public channel. If two people (usually referred to in the cryptographic literature as Alice and Bob)
wish to communicate securely, they need a way to exchange some information that will be known only to them.
In practice, Alice and Bob are communicating remotely (e.g. over the internet) and
have no prearranged way to exchange information.

[key_exchange_wiki_pic](https://en.wikipedia.org/wiki/Diffie%E2%80%93Hellman_key_exchange)
[DHKE](https://cryptobook.nakov.com/key-exchange)
[Link easy DH](https://www.irongeek.com/diffie-hellman.php)

two parties to First share a secret
random number known as a key so how
could two people who have never met
agree on a secret shared key key without
letting Eve who is always listening

first let's explore how this trick
is done using colors how could Alice and
Bob agree on a secret color without Eve
finding it out the trick is based on two
facts one it's easy to mix two colors
together to make a third color and two
given a mixed color it's hard to reverse
it in order to find the exact original
colors this is the basis for a lock easy
in One Direction hard in the reverse
Direction This is known as a oneway
function now the solution works as
follows first they agree publicly on a
starting color say yellow next Alice and
Bob both randomly select private colors
and mix them into the public yellow in
order to disguise their private
colors now Alice keeps her private color
and sends her mixture to Bob and Bob
keeps his private color and sends his
mixture to
Alice now the heart of the
trick Alice and Bob add their private
colors to the other person's mixture and
arrived at a shared secret

color notice how Eve is unable to
determine this exact color since she
needs one of their private colors to do

so and that is the
trick now to do this with numbers we
need a numerical procedure which is easy
in One Direction and hard in the other
this brings us to modular arithmetic
also known as clock arithmetic for
example to find 46 mod 12 we could take
a rope of length 46 units and wrap it
around a clock of 12 units which is
called the modulus and where the Rope
ends is the solution so we say 46 mod 12
is congruent to 10 easy now to make this
work we use a prime modulus such as 17
then we find a primitive root of 17 in
this case 3 which has this important
property that when raised to different
exponents the solution distributes
uniformly Around the
Clock three is known as the generator if
we raise three to any exponent x then
the solution is equally likely to be any
integer between 0 and 17 now the reverse
procedure is hard say given 12 find the
exponent three needs to be raised to
this is called the discrete logarithm
problem and now we have our one-way
function easy to perform but hard to
reverse given 12 we would have to resort
to trial and error to find matching
exponents how hard is this well with
small numbers it's easy but if we use a
prime modulus which is hundreds of
digits long it becomes impractical to
solve even if you had access to all
computational power on Earth it could
take thousands of years to run through
all possibilities so the strength of a
one-way function is based on the time
needed to reverse it now this is our
solution first Alice and Bob agree
publicly on a prime modulus and a
generator in this case 17 and three
then Alice selects a private random
number say 15 and calculates 3 to the

power5 mod 17 and sends this result
publicly to Bob then Bob selects his
private random number say 13 and
calculates 3 to ^ 13 mod 17 and sends

this result publicly to Alice and now
the heart of the trick
Alice takes Bob's public result and
raises it to the power of her private
number to obtain the shared secret which
in this case is 10 Bob takes Alice's
public result and raises it to the power
of his private number resulting in the
same shared secret notice they did the
same calculation though it may not look
like it at first consider Alice the 12
she received from Bob was calculated as
3 to ^ 13 mod 17 so her calculation was
the same as 3 ^ 13 to the power 15 mod
17 now consider Bob the six he received
from Alice was calculated as 3 ^ 15 mod
17 so his calculation was the same as 3
to ^ 15 to ^ 13 notice they did the same
calculation with the exponents in a
different order when you flip the
exponent the result doesn't change so
they both calculated three raised to the
power of their private numbers without
one of these private numbers 15 or 13
Eve will not be able to find the
solution and this is how it's done while
Eve is stuck grinding away at the
discret logarithm problem and with large
enough numbers we can say it's
practically impossible for her to break
the encryption in a reasonable amount of
time this solves the exchange problem it
can be used in conjunction with a pseudo
random generator to encrypt messages
between people who have never met

### Identification

In principle, the only remaining problem was to be sure (or at least confident) that a public key actually belonged to its supposed owner.
Because it is possible to 'spoof' another's identity in any of several ways, this is not a trivial or easily solved problem, particularly
when the two users involved have never met and know nothing about each other.

### Symetric AES

[Try AES](https://anycript.com/crypto)
