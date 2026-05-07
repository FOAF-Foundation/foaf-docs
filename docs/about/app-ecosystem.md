# FOAF App Ecosystem

This is the running list of app ideas that could be built on FOAF.

FOAF itself is not one of these apps. FOAF is the shared infrastructure layer: identity, contacts, memberships, invitations, trustlines, claims, subnets, routing, and mutual-credit primitives. Apps use those primitives for specific community workflows.

This document is intentionally a registry, not a commitment. Some ideas are active products, some are planned, and some are only sketches worth remembering.

---

## Current and Active

### GrowOperative

**Status:** Active reference app.

GrowOperative is the first FOAF app: local food exchange using trust-routed relationships and mutual credit. It focuses on producers, retailers, consumers, brokers, item requests, orders, inventory, settlement, and local food resilience.

**FOAF primitives used:** identity, contacts, invitations, trustlines, mutual credit, routing, subnets, fulfillment primitives.

### Orchardly

**Status:** Active app in development.

Orchardly is a harvest operations app for orchards and similar crews. It tracks crews, tallies, harvest work, blocks, batches, pay rules, and operational records while aligning identity and roster concepts with FOAF's social graph.

**FOAF primitives used:** identity, contacts, memberships, invitations, claims, app-scoped roles.

---

## Planned or Likely

### General Marketplace

**Status:** Planned direction, partly captured in the FOAF Marketplace docs.

A broader marketplace for non-food goods, services, tools, skills, and local help. It should not simply be a public classifieds board. Its FOAF-specific value is trust-scoped visibility: listings can be direct-contact only, community-scoped, or propagated through contacts-of-contacts with a visible trust path.

**Possible modes:** buy, sell, trade, give away, request help, offer services.

**FOAF primitives used:** identity, contacts, trust paths, mutual credit, routing, claims, community visibility rules.

### Personal Lending App

**Status:** Concept; needs a name. Do not use "Lendly" as the public name.

A peer-to-peer app for lending, borrowing, or renting physical goods directly between people: tools, vehicles, trailers, farm equipment, camping gear, kitchen equipment, and other durable assets.

The key insight is privacy. Regular people generally do not want a public internet inventory of their possessions. FOAF's trust-graph visibility changes the shape: a listing can travel only to trusted contacts, contacts-of-contacts, or specific communities.

**Possible flows:** request to borrow, owner approval, deposit or credit terms, handoff confirmation, before/after condition photos, return confirmation, dispute record.

**FOAF primitives used:** identity, contacts, communities, trust paths, claims, mutual credit, signed agreements.

---

## Early Ideas

### Neotribes

**Status:** Idea; possible name for the social app.

Neotribes is a possible name for the FOAF social app. It is a social network organized around subnets, communities, and trust paths rather than global algorithmic recommendation.

People in the same subnet or group may be able to see each other even when they are not directly connected. This gives a community a shared social space without requiring every member to add every other member as a direct contact.

It can also have a "grapevine" repost mechanic: a post reaches someone outside the author's direct audience when one of that person's contacts explicitly reposts or relays it. The product question is not "what is trending?" but "who passed this to me, and why do I trust that path?"

**Possible flows:** post, repost, quote, subnet feed, group feed, grapevine relay, trust-path display, mute/block/report, hop-limit controls.

**FOAF primitives used:** identity, contacts, subnets, communities, memberships, trust paths, claims, relay metadata.

### Skill and Labor Exchange

**Status:** Idea; shape unresolved.

A way for people to offer or request skills, labor, lessons, repairs, care work, farm help, odd jobs, or professional services through trusted relationships.

This is worth preserving as an idea, but the product shape is not clear yet. It may belong inside the General Marketplace, or it may need its own app if scheduling, rates, references, safety, recurring work, or worker protections become central enough.

**Open questions:**

- Is this a listings marketplace, a booking app, a mutual-aid board, or a work-coordination app?
- How should pricing work: hourly, task-based, barter, mutual credit, volunteer, or mixed?
- What safety and reputation signals matter for childcare, in-home services, and higher-trust work?
- Which parts are FOAF infrastructure versus app-specific workflow?

**FOAF primitives likely used:** identity, contacts, communities, claims, reputation signals, mutual credit, scheduling hooks.

### Events, Classes, and Festivals

**Status:** Idea.

An app for organizing classes, workshops, meetups, community events, retreats, conferences, and eventually festival-scale gatherings.

At the small end, this could handle class registration, attendance, waitlists, instructor profiles, ticketing, volunteer roles, and community-credit payments. At the larger end, it could support multi-day schedules, venues, stages, crews, vendor booths, participant groups, access passes, and organizer dashboards.

The FOAF-specific angle is that event participation can be scoped by community, subnet, invitation, or trust path. A workshop can be open to a subnet, visible to contacts-of-contacts, or invite-only through known organizers. Instructors, vendors, volunteers, and attendees can carry claims or badges across events.

**Possible flows:** create class, register, join waitlist, pay or pledge credit, check in, manage volunteers, assign organizer roles, publish festival schedule, issue attendance or facilitator badges.

**FOAF primitives likely used:** identity, communities, memberships, invitations, claims, roles, mutual credit, subnet visibility, signed attendance records.

### Childcare Swaps and Care Networks

**Status:** Idea; possibly part of Skill and Labor Exchange.

Childcare swaps and care networks are a high-trust form of local labor exchange. They may need stricter claims, permissions, references, and community governance than ordinary marketplace work.

**FOAF primitives likely used:** identity, contacts, communities, claims, guardian/household relationships, reputation signals.

### Tool Library Hub

**Status:** Idea; related to the Personal Lending App, but distinct.

A tool library app for community-owned or co-op-owned inventories of shared tools and equipment.

This is different from the Personal Lending App. The lending app is mainly direct person-to-person lending: Robin lends a car, trailer, weed whacker, or chainsaw to someone he trusts. A tool library is a hub with its own identity, memberships, policies, inventory, checkout rules, and credit account.

The hub may own some tools directly while also surfacing supplemental tools listed by members connected to it. A community could therefore operate a shared catalog that mixes library-owned inventory with member-owned inventory, while keeping the accounting clear.

**Possible flows:** member signup, tool checkout, return confirmation, late/damage handling, maintenance status, member-contributed listings, community inventory reports.

**FOAF primitives likely used:** communities, memberships, roles, entity identity, credit account, inventory visibility, signed checkout/return events, claims.

---

## App Boundary Rule

When evaluating a new app idea, use this split:

```text
FOAF owns:
identity, contacts, memberships, claims, invitations, trustlines, routing, credit primitives

Apps own:
vertical workflows, domain records, UI, search/discovery, fulfillment details, business model
```

An app should not capture identity, credit relationships, or the social graph in app-specific structures if those should be portable across the ecosystem. Conversely, FOAF should not absorb every app's domain data just because multiple apps use identity or credit.

---

## Related Docs

- [Design Principles](./design-principles.md) — especially "FOAF is infrastructure; apps are the ecosystem"
- [FOAF Marketplace Vision](../foaf-marketplace/vision.md)
- [FOAF Marketplace Roadmap](../foaf-marketplace/roadmap.md)
