# FOAF Foundation Frequently Asked Questions

This page answers common questions about FOAF, GrowOperative, mutual credit, and the broader marketplace.

---

## Getting Started

### What is FOAF?

FOAF stands for Friend of a Friend. It is a network for trust-based trading. Instead of relying on banks or big platforms, people exchange value directly through their contacts and the contacts of their contacts.

### What is GrowOperative?

GrowOperative is the first app built on the FOAF network. It lets gardeners and neighbours trade surplus food and other goods with one another. It supports mutual credit and trust-based routing, with no need for tokens or cash up front.

### How do I start?

You can join through a trusted contact, a local resilience group, or by signing up on the platform. Once you are in, you can list something you have or request something already listed. The onboarding videos and materials will walk you through the rest.

### Do I need tokens to participate?

No. You do not need to buy any tokens to participate. Verified new users receive Five Free FOAF tokens via a custodial wallet on signup. No seed phrase, no gas fees, no crypto knowledge required.

Fees, when they activate in later phases, are paid in RHEO and flow automatically through trust paths. You can join through a friend or community contact and start trading without ever setting up a wallet yourself.

### Can I use this if I do not have a smartphone?

Yes. You can access the system through a browser using the PWA. In the future, trusted node operators may offer printed listings, in-person matching, or community kiosks.

---

## How It Works

### What is mutual credit?

Mutual credit is a system where people give and receive without needing cash at the moment of trade. When you provide value, your account goes positive. When you receive something, you might go negative. It is like a running balance between friends, but supported by simple records and trust.

### How does the handoff work when something passes through multiple people?

For direct transactions between you and someone you are directly connected to, the handoff works like any local exchange. You and the other person agree on how to physically exchange the item, where, and when.

For multi-hop transactions where the item travels through trust connections, the credit ledger routes automatically through the intermediaries, but the physical handoff depends on the situation and the people involved. This part of the design is still evolving as we learn what works in practice. The introductions feature will give intermediaries and end parties more ways to coordinate directly when both sides want that.

### What happens if I owe someone and do not pay?

The system works through relationships. If you owe someone and do not settle, your reputation will affect how others choose to interact with you. Trades are visible to those involved and to your trust path, which creates gentle accountability.

### Is this like barter?

No. Barter requires two people to want what each other has at the same time. FOAF uses credit and trust to let value flow through the network more freely. You can receive something now and provide something later to someone else.

---

## Design Choices

### Why is the original seller hidden from buyers by default?

When a listing travels through trust connections to reach you, it shows up framed by whoever passed it along, not by the original seller. This is a deliberate design choice with three reasons behind it.

First, it matches how trust actually travels in real life. "My friend recommended this" carries different weight than "a stranger says this," even if the underlying item is identical. The connector framing carries the trust.

Second, it gives the people in your trust path actual skin in the game. If they relay junk to you, they look bad. Spam stays out of the network organically.

Third, it preserves privacy on both ends. The original seller does not have their inventory exposed to strangers. The buyer does not have to identify themselves to a stranger to browse.

When both parties want to be known to each other, an introductions feature will let them opt in. Privacy is the default for cases where it matters, not a mandatory mask.

### Will I be expected to be a middleman for my friends?

Only as much as you want to be. The intermediary role is opt-in and configurable.

You set your own markup on connections going through you, including zero. At zero markup, you just enable the connection without taking a cut. The credit routing through your trustlines is automatic if your limits allow it, so there is no per-transaction work or approval required from you.

If you would rather not be part of routing for others at all, that is a valid configuration too. You can use the app purely as a buyer and seller within your direct connections.

### Is this like a farmers market?

No. A farmers market is a public space where strangers discover each other through visible stalls. FOAF is for exchange within existing trust networks. If meeting new growers face-to-face in a public venue is what you want, the farmers market is the right tool.

FOAF is more useful when the answer to "who would actually want this thing I have" is best routed through people you already know, with the credit infrastructure handling payment so you do not have to manage cash, change, or invoicing.

### Is this like crypto?

Not really. FOAF uses blockchain to manage governance and fees, but the system works through social trust, not speculation. You can participate without understanding crypto or ever touching a wallet.

---

## Tokens and Fees

### What is FOAF (the token)?

FOAF is the governance token of the network. It has a fixed supply of 25 million, deployed to Ethereum mainnet in December 2018. It is used to vote on proposals and help shape the future of the network. Some contributors and organizers may earn FOAF through participation.

### What is RHEO?

RHEO is the utility credit used to power the FOAF network. It is not a transferable token and not a currency. It carries the cost of using the system. Most users will never need to hold it directly. It flows behind the scenes through trusted participants.

### How are fees handled?

In Phase 1, all network fees are zero. The protocol supports fees, but no rates are active yet.

In future phases, fees will activate progressively and will be denominated in RHEO. The exact rates and how they are split between node operators, the foundation treasury, and burn are DAO-governable parameters, not fixed constants. Each trade will include a small base fee, and multi-hop transactions may include a small per-hop routing premium that compensates the intermediaries who carry your trust path. All of these rates are subject to community governance once the DAO is active.

---

## Privacy and Data

### What data do you collect and how is it stored?

Right now the GrowOperative app runs on a centralized Rails and MySQL backend hosted on AWS. What it stores: your account information, your contacts and trustlines, your listings, and your transaction ledger entries. Authentication uses RS256-signed JWTs with hashed passwords. There is no advertising, no third-party data sharing, and no behavioural analytics resold.

The architectural intent for later phases is content-private gossip-routed listings, meaning listings would travel between devices along trust paths rather than living in a central database. This is documented in the protocol vision but is not built yet. Right now you are trusting Foundation infrastructure for that piece. The mutual credit ledger will also move on-chain to Radix in Phase 3.

What is already structural today: nothing you post is publicly browsable. Listings only travel to people you are connected to, or people connected to them, up to a configurable hop limit. They are never scraped by strangers searching the internet. That part is not a policy promise, it is how the visibility model is built.

---

## Bigger Picture

### What is the actual goal of FOAF?

The deeper goal of FOAF is to bootstrap community-scale mutual credit networks. GrowOperative is the first app on top of that infrastructure, with food sharing as the wedge into communities that already share informally.

Mutual credit systems have been tried many times (LETS, time banks, WIR, Sardex). They mostly stall before take-off because the credit is the thing. Users have to learn and commit to an abstract accounting concept before they get any value from it. The system feels like overhead, not utility.

FOAF inverts that. People come for apps they actually want to use (GrowOperative for food, Orchardly for harvest operations, foaf.exchange for goods and services, and others as the ecosystem grows). The mutual credit network grows as a byproduct of app usage rather than as a thing users have to consciously believe in.

### Has anything like this worked at scale before?

Yes, in different forms.

WIR Bank in Switzerland has operated a mutual credit network for small businesses since 1934 and is still active.

Sardex in Sardinia has connected thousands of small and medium businesses through mutual credit since 2009, with hundreds of millions of euros in annual trading volume.

The global cannabis industry has operated as a trust-routed economy for decades. Growers who did not want exposure, buyers who knew their connection but not the grower, intermediaries who took a cut for being the path. It worked at scale despite, or because of, the privacy layer. The same structural pattern FOAF formalizes.

What is new is wrapping these patterns in a modern app layer that lowers the barrier to entry from "learn an abstract accounting system" to "use an app that happens to use credit underneath."

### Who runs the network?

Nobody and everybody. The FOAF Foundation coordinates early development, but the network is governed by its users. Anyone who earns or holds FOAF can participate in proposals and help guide future decisions.

---

Explore more in [onboarding](../growoperative/onboarding.md), [contribution](../community/contribution.md), or [explainer videos](../education/explainer-guide.md).
