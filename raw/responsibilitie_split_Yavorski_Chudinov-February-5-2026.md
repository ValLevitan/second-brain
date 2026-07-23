How the responsibilities are split between Eugune Yavorski and Dzime Chudinov.  (Detailes are in the attached)


Yavorski
owns the Flex-Port side — he's the one who designs
the WSS protocol messages and builds the embedded firmware that runs
on the hardware board inside the slot machine. He handles bill
validator communication, cash-out logic at the hardware level,
firmware updates, encryption, and on-device logging. He's currently
juggling several in-progress items with Feb deadlines clustering
together.
Chudinov owns the Flex-Pay kiosk side
— he takes those same WSS messages and implements them on the
payment terminal. He also handles everything upstream: server
integration, Payment Hub API, TITO ticket processing, InComm
parameters, and backend reporting. He's got a strong delivery track
record (21 closed + 2 done) and recently knocked out a batch of
transaction bug fixes.
The WSS protocol is the contract between them. The document
includes a full responsibility matrix with JIRA ticket references,
current status for both, and the key point about why the knowledge
transfer matters — Yavorski is currently a single point of
knowledge on the protocol specification.
