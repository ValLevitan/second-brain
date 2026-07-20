Friends:
 
In reading through the notes of the meeting labeled: CMS- Block Diagram_Arch , I noticed the following definition of the products picked up the AI and defined in a summary in the following manner:
 
3. FlexPay Ecosystem Overview
 - FlexPay Kiosk: Small footprint device for card dispensing and ticket
 scanning
 - FlexPOS: Tabletop point-of-sale device for converting tickets to gift cards
 - FlexPort: Player-facing device with scanner and display (like casino iView)
 - FlexTower: Self-dispensing card unit
 - Currently demoing functional units at Georgia show
 
I do not know if this definition is an AI erroneous interpretation or if this indeed was talked about in your meeting, but I wanted to bring to your attention that the products are defined incorrectly; where Flex-Pay and Flex-Tower definitions should be reversed.
 
Here is the correct definition and the naming convention of the products:
 
3. Transactional Products Ecosystem Overview
 - Flex-Tower: Small footprint device for card dispensing and ticket
 scanning
 - Flex-POS: Tabletop point-of-sale device for converting tickets to gift cards.  
 - Flex-Port: Player-facing device with scanner and display (like casino iView)
 - Flex-Pay (also incorrectly referred to as "Kiosk): Self-dispensing card unit.  Currently demoing functional units at Georgia show
In addition to the these nomination, there is a product called: SMIB - this is an inexpensive bi-directional converter from SAS to WSS.

The summary of the transcript also points to the following three Payment Processing Schemes:
4. Three Payment Processing Schemas
 - Mother Goose Integration: Intercepts legacy pulse-based systems, prints
 receipts for manual card creation
 - E-Wallet: Proprietary protocol using temporary barcode tickets with PIN
 protection
 - Tito/SAS: Standard ticket-in/ticket-out using secondary SAS port (Intralot
 has primary)

I would like to comment on it.
 - Mother Goose Integration: Intercepts legacy pulse-based systems, interprets the value of a win, validates the transaction through Incomm and credits the win onto a Prepaid MC. 
 
We are currently evolving this scheme to further the transaction to autonomously dispensing and actual MC card.
 
I further want to comment on the following summary notes:
5. Architecture Decisions
 - Move to cloud-based architecture for new CMS features
 - Legacy CMS must continue running in parallel during transition
 - First cloud features will be payment device management dashboards
 - Need B2B cloud connection with Incomm (MasterCard processor) for security

I would like to point out that our first course of business is to release the Flex-POS + dispenser into the market.  The most pressing part of this release is the ability to:
install and automatically configure Flex-POS and dispenser out of the box
establish and ACH (automated clearing house) agreement with a location
debit locations' accounts through ACH within 24 hours in accordance to the agreement
present a reconcilable accounting details to locations and master operators
 
 
 
 
I would like to comment on the following summary notes:
6. Master Operator Model
 - Georgia law requires sales through master operators (not direct to
 locations)
 - JVL has limited visibility into machine locations by design
 - Master operators handle all field service and technician support
 - CMS portal needs multi-tenant capabilities for operator self-administration

The above is only true for Slot machines.  The transactional equipment is not bound by the same legislation.
 
Also, I do not understand the comment above: "- CMS portal needs multi-tenant capabilities for operator self-administration."

please elaborate.
 
 
 
 
