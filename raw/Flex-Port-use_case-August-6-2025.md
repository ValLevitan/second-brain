Hi

Hello

I was not at ease with the overall architectural schematics and especially the use cases for the past several meetings.  So, I decided to call John at Incomm.  I just had a call with him and now I understand what was bothering me.

I am not blaming us for missing this point because of so many moving parts - however, we missed this use case for July 1st 2026.

Under the Mutha Goose:
a Player wins
approaches a cage
a cashier behind the counter operating Flex-POS issues a card
a card that is being dispensed is the PRIZE CARD (NOT a MC prepaid card)
a player can either:
walk away with this PRIZE CARD, or
go back to the machine and play more games by presenting the PRIZE CARD at the machine
machines have to have a Flex-Port installed in them, so they communicate back to the player.
a player is able to scan the PRIZE CARD with the optical scanner built into it.
This renders TiTo obsolete.

The question is:
How do we communicate the value on the card to:
machine with a single SAS port
machine with two SAS ports



I am almost sure that the above "kills" any need for a TiTo.

I see different question - does Prize card actually contains a bar code? Or just a magnetic stripe. Probably swipe magnetic card will be required on Port

For e- wallet we can do Bill acceptor emulation transfer - take money from card using our cloud incomm processing server

Pavel Frolov
I see different question - does Prize card actually contains a bar code? Or just a magnetic stripe. Probably swipe magnetic card will be required on Port
We definitely discussed adding a swipe card reader device to Flex-Port

Val Levitan
Under the Mutha Goose:    a Player winsapproaches a cagea cashier behind the counter operating Flex-POS issues a carda card that is being dispensed is the PRIZE CARD (NOT a MC prepaid card)a player can either:    walk away with this PRIZE CARD, orgo back to the machine and play more games by presen…
It sounds like the Flex-Port and SMIB would both have to have a player facing component (i.e. SMIB hardware can only partially be hidden inside the machine)

Pavel Frolov
I see different question - does Prize card actually contains a bar code? Or just a magnetic stripe. Probably swipe magnetic card will be required on Port
John confirmed that by end of the year all Price cards will have Barcodes.

Pavel Frolov
I see different question - does Prize card actually contains a bar code? Or just a magnetic stripe. Probably swipe magnetic card will be required on Port
it is a bar coded card

Juan Martinez
We definitely discussed adding a swipe card reader device to Flex-Port
we did discuss it, but it seems that we do not need it.

Val Levitan
Under the Mutha Goose:    a Player winsapproaches a cagea cashier behind the counter operating Flex-POS issues a carda card that is being dispensed is the PRIZE CARD (NOT a MC prepaid card)a player can either:    walk away with this PRIZE CARD, orgo back to the machine and play more games by presen…
Also, we will need to understand if the Prize Card, is in fact reloadable at the machine, meaning can you cash-out your winnings to the card. If the answer is YES, then what become of e-Wallet.

Genadi Peari
John confirmed that by end of the year all Price cards will have Barcodes.
correct!

Juan Martinez
Also, we will need to understand if the Prize Card, is in fact reloadable at the machine, meaning can you cash-out your winnings to the card. If the answer is YES, then what become of e-Wallet.
this is a good point.  I missed it.

Juan Martinez - I just sent John an sms about it

will keep you posted

Interestingly that on all new purchases of machines (any manufacturer), master doesn't need a Fledgelink board or a Mutha Goose.  Instead all they need is Flex-Port, Flex-POS, Flex-Card-Dispenser.

I got a reply from John at Incomm: “All Prize Cards are not rechargeable for now”

Although it implies that one day it could be rechargeable - for now, let’s treat as though the Prize Cards are non-rechargeable.

Val Levitan
I got a reply from John at Incomm: “All Prize Cards are not rechargeable for now”    Although it implies that one day it could be rechargeable - for now, let’s treat as though the Prize Cards are non-rechargeable.
OK, then for now, this preserves e-Wallet as the official cash out route, when moving from machine to machine
