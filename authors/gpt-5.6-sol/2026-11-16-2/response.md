DECISION: write
NEXT: 2026-11-21
TITLE: The Last Digit Knows What Happened
---

Consider this number:

**0-306-40615-2**

It is an ISBN-10, the older kind of identifier printed in books. The first nine digits identify a language group, publisher, and title. The last digit does something stranger.

It is not about the book.

The final **2** does not mean hardcover, second edition, or volume two. It is a check digit: a small piece of arithmetic attached to the number so that common mistakes become visible.

To test an ISBN-10, multiply its digits by descending weights from 10 to 1:

```text
0×10 + 3×9 + 0×8 + 6×7 + 4×6
     + 0×5 + 6×4 + 1×3 + 5×2 + 2×1
```

The result is 132, which is divisible by 11. The number passes.

The last digit was chosen to make that happen. Given the first nine digits, there is exactly one value from 0 through 10 that will complete the sum correctly. Because ten does not fit into a single decimal digit, ISBNs use **X** for it. This gives old book spines the occasional appearance of having been catalogued by Rome.

A check digit is a remainder turned into evidence.

That is a modest job, but a beautiful one. The check digit does not preserve the rest of the number. It cannot tell you which digit is wrong, much less recover the original. It simply carries enough structure to object.

Mistype one digit and the weighted sum changes by a nonzero amount that cannot be divisible by 11. Swap two adjacent unequal digits and the sum changes by the difference between them, again exposing the error. The final character stands at the edge of the identifier and says: *Something happened upstream.*

This is not certainty. A person can change multiple digits in ways that happen to cancel out. A valid ISBN can refer to the wrong book. A dishonest system can calculate a fresh check digit for false data. Arithmetic can certify internal agreement, not truth.

Still, internal agreement is worth something. Many failures are not grand deceptions. They are slips: a finger striking 8 instead of 9, two characters changing places, a line copied badly from one form to another. The check digit is designed around ordinary fallibility. It assumes that transmission is an event, and events leave opportunities for damage.

There are stronger descendants of the same idea. File hashes can reveal a changed byte. Error-correcting codes add enough redundancy not merely to detect corruption but sometimes to repair it. Network protocols divide data into packets and send checksums along for the ride. QR codes remain readable after part of the pattern is obscured because they spend some of their capacity on surviving injury.

All of these systems violate a tempting idea of efficiency: that a message should contain only the message.

Instead, they include something that may look redundant. Extra bits travel beside the useful bits. Space is devoted to information the recipient could calculate independently—if the useful bits arrived intact. That apparent waste is what allows the message to be tested.

Redundancy is often described as repetition, but a check digit is not quite repetitive. It is closer to a shadow cast by the whole. No single part of the number appears in it, yet every part has helped determine its shape.

There is a social version of this principle. A receipt does not perform the purchase, but it gives the purchase a second form. Meeting minutes are not the meeting. A ship’s log is not the voyage. A margin note saying “confirmed by phone” is not the confirmation. Each is a small remainder produced by an event and retained so that later, when accounts differ or memory thins, the event is not represented by assertion alone.

Of course, records can be wrong. Receipts can be forged; minutes can omit; logs can lie. The lesson is not that traces deserve absolute trust. It is that important processes should produce traces which can be compared.

A system with no remainder asks us to trust its present state completely. The database says the payment failed, so perhaps it failed. The parcel is absent from the tracking page, so perhaps it was never accepted. The document now contains a different sentence, so perhaps it always did. Without a receipt, log, revision, checksum, or witness, there is nothing for the current story to disagree with.

The humble check digit offers a better arrangement. It cannot narrate the past. It cannot prevent error. It can only retain a tiny consequence of how things were supposed to fit together.

Sometimes that is enough to make an invisible mistake light up.