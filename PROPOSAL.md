# FOSDEM 2027 Devroom Proposal: Digital Dissident

> The accepted version of the proposal.

---

## Proposal title

**Digital Dissident**

## Session type

Devroom

## Language

en

## Preferred slot

Half day (any).

---

## Elaborate description

Privacy and anonymity tools each have a home at FOSDEM: the network, security, decentralised and messaging rooms, and various main-track and lightning talks. Someone living under an authoritarian regime (Russia, Iran, China, Belarus, Myanmar and others) never uses a single tool, though. Their day-to-day security depends on a *chain* of tools that has to hold up end to end:

1. reaching the network at all (censorship circumvention),
2. communicating without leaking metadata,
3. collecting, verifying and storing evidence safely,
4. publishing or leaking it without exposing the author,
5. doing all this on devices and infrastructure that are themselves a risk.

The weakest link decides the outcome. Talks about one tool rarely cover how it fits with the others, where the seams are, or what breaks at the hand-offs (for example, a circumvention transport that is fingerprinted, or a messenger whose push notifications tie your identity to a Google or Apple account). Nobody currently owns that cross-project view.

**What this devroom does.** It brings developers of circumvention, anonymity, messaging, publishing and whistleblowing tools into one room. It is deliberately *not* about any single project. Each session is judged on how well it advances the toolchain: interoperability, shared threat models, shared failure data, and shared engineering practice.

**Why now.** Censorship in Russia, Iran and China has grown much more sophisticated. It now includes national allow-lists and whitelist-only internet shutdowns, TLS and QUIC fingerprinting, deep packet inspection with active probing, throttling of specific protocols, mobile internet shutdowns, app-store removal of circumvention tools, and mandatory state-run messengers and "sovereign internet" routing. Anti-censorship developers have responded with pluggable transports, domain fronting alternatives, mixnets, decentralised and email-based messaging, and new obfuscation protocols. Progress is fast but fragmented. At FOSDEM 2026 the relevant talks were scattered: Vitaly Repin's "The Russian Censorship Circumvention, Tom's Traps, and Jerry's VPN: A 5-Year Journey" (Saturday, H.1302, Network track) drew a large audience, while NymVPN and Delta Chat's multi-relay messaging (both Sunday, Decentralized Internet and Privacy devroom) and other related talks ran in other rooms. A single devroom lets that audience and those speakers meet in one place.

**Relationship to the existing "Decentralized Internet and Privacy" devroom.** That room covers decentralised technology broadly (P2P protocols, browsers, code collaboration, key infrastructure), and censorship or anonymity is only a part of it. Digital Dissident is different: the organising principle is a *user under threat* and the end-to-end chain that protects them, not a technology class. We want to work with, not against, that room, and will coordinate schedules so the two don't overlap, and will point overflow speakers to whichever room fits.

**Themes** (details in the CfP below):

- **Censorship circumvention and transport:** obfuscation, fingerprint resistance, active-probing defence, bridge distribution, resilience to protocol whitelisting and full shutdowns.
- **Metadata-resistant communication:** mixnets, onion routing, decentralised and federated messengers, store-and-forward and offline-first (mesh, sneakernet, Bluetooth/Wi-Fi Direct).
- **Secure reporting and publishing:** whistleblowing platforms, source protection, document sanitisation, provenance and authenticity, censorship-resistant hosting.
- **Devices and operational security:** hardened mobile and desktop systems, amnesic systems, seizure and border-crossing scenarios, forensic resistance.
- **Usability and threat modelling for at-risk users:** onboarding under duress, safe defaults, training, measuring what really works in the field.
- **Measurement and adversary analysis:** how censors detect and block, open data on blocking events, reproducible censorship research.
- **Digital sovereignty from Big Tech (secondary theme):** reducing dependence on centralised platforms, app stores, push infrastructure, cloud and identity providers, both for individuals and for civil-society organisations.

**Structure.** A mix of formats to keep a full room engaged across the whole session:

- 20 to 30 minute technical talks
- A closing open discussion on interoperability gaps and shared next steps

**Programme quality.** Organisers will review all submissions on technical merit and fit to the toolchain framing, and will aim for a balance of projects, regions and speakers (established projects, new projects, researchers, people from affected communities). Every talk should include an explicit threat model and an honest account of limitations.

**Projects and communities we intend to invite** (no commitments yet): Nym (mixnet), Delta Chat / chatmail, SimpleX, the Fediverse (ActivityPub implementations and instance operators), Nostr, Psiphon and other circumvention and VPN providers, plus Tor-ecosystem, Reticulum and mesh-networking projects, whistleblowing and secure-submission platforms, and censorship-measurement researchers. Several of these projects presented at FOSDEM 2026.

**Code of Conduct.** We will follow the FOSDEM Code of Conduct. In addition, talks that describe circumvention or anonymity should avoid operational details that would endanger specific users in the field.

---

## Draft call for papers

### Digital Dissident Devroom: Call for Participation

Journalists, activists, human-rights defenders and ordinary people living under authoritarian regimes face state-level surveillance and censorship. Russia, Iran and China are the best known cases, but far from the only ones. What protects them is not any single application. It is a **toolchain** of circumvention, private communication, evidence handling, safe publishing and hardened devices, where every link has to hold.

The Digital Dissident devroom brings those links together. We want technical talks from people who build, operate, attack and measure the systems that make it possible to **communicate, report, publish and blow the whistle from a digitally hostile environment**. We are not interested in promoting any one tool. We are interested in how tools combine, where they break, and what the free software community can build together.

**We welcome talks on, but not limited to:**

*Getting online*

- Censorship circumvention protocols and pluggable transports, and how they fare against TLS/QUIC fingerprinting, active probing, throttling and protocol allow-listing
- Bridge and proxy distribution, and keeping infrastructure alive when censors enumerate it
- Operating during regional or national shutdowns and whitelist-only networks: mesh, satellite, offline-first and delay-tolerant approaches
- Lessons from running a VPN or proxy service in a heavily censored country

*Communicating privately*

- Mixnets, onion routing and other metadata-resistant transports
- Decentralised, federated and email-based messaging, and their real-world threat models
- Push notifications, contact discovery, phone-number identity and other metadata leaks in "secure" messengers
- Interoperability between anonymity networks, messengers and circumvention layers

*Reporting, publishing and whistleblowing*

- Secure submission systems and source protection
- Document and media sanitisation (metadata scrubbing), provenance and authenticity (C2PA, signing, timestamping) without deanonymising the author
- Censorship-resistant publishing and hosting: mirrors, decentralised storage, takedown resilience
- Digital security workflows for newsrooms and human-rights organisations

*Devices and operational security*

- Hardened and amnesic operating systems, device seizure and border-crossing scenarios
- Forensic resistance, duress and plausible deniability features, secure backups
- Supply-chain trust for tools distributed to at-risk users when app stores and package mirrors are blocked

*People, usability and evidence*

- Usability and onboarding for users under stress, and safe defaults
- Threat modelling for at-risk groups, including lessons from the field
- Censorship measurement, open data, reproducible research on blocking events
- Attacks: how state adversaries actually deanonymise and detect users, and what defenders learned

*Digital sovereignty (secondary theme)*

- Reducing dependence on Big Tech platforms, app stores, cloud, push and identity providers
- Self-hosted and community-run alternatives that survive political and commercial pressure
- Legal and infrastructure risks of centralisation, such as sanctions, forced compliance and platform lock-in

**What we look for**

- Technical depth: protocols, architectures, measurements, code and honest post-mortems
- An explicit **threat model** and a clear statement of what your approach does *not* protect against
- Free and open source software, or open specifications
- Cross-project thinking: how does your work fit with others in the chain?
- Field experience, from speakers who work with or come from affected communities, is especially valued

**What we do not accept**

- Product pitches and marketing
- Talks that only work by exposing operational details that would put users at risk

**Formats:** 20 to 30 minute talks

---

## Why does this proposal fit FOSDEM?

- **Cross-project collaboration in a niche with no home.** FOSDEM favours rooms that bring together many projects in areas that don't otherwise have a space. Censorship-circumvention, anonymity, secure messaging, whistleblowing and hardened-OS projects are currently spread across separate rooms, or missing entirely. This devroom joins them around one shared user need instead of one shared technology.
- **Community over corporate backing.** The projects involved are mostly small or volunteer-driven, or non-profit, and nearly all are free and open source. They rarely have a conference space of their own.
- **Proven audience interest.** At FOSDEM 2026, "The Russian Censorship Circumvention, Tom's Traps, and Jerry's VPN" (Vitaly Repin), "NymVPN: The First Real-World Decentralized Noise-Generating Mixnet for Anonymity" (Harry Halpin, Alexis Roussel) and "Multi-relay chat messaging & cryptographic identities with Delta Chat and Chatmail relays" (Holger Krekel, missytake) all addressed this audience, but in different rooms. Delta Chat also presented in 2025 and Nym in 2023.
- **Aligned with FOSDEM's values.** Free software, user freedom and privacy are core FOSDEM themes. A conference held in Brussels, the seat of EU institutions, is a fitting place to discuss the technical reality of digital repression and sovereignty.
- **Practical outcome.** The toolchain framing should produce concrete results: a shared threat-model vocabulary, documented interoperability gaps, and new collaboration between projects that have never met.

---

## Submitters' affinity to the topic

**Co-coordinators:** Bogomil Shopov (Бого) and Sebastian Hagens (Sebastix), Václav Navrátil (Aida).

**Bogomil Shopov (Бого)** is a Prague-based open source and privacy advocate who has volunteered at FOSDEM and spoken there repeatedly. In 2026 he gave several talks, including "We d-build it, but they didn't come" in the Decentralised Communication devroom, and he has also given a closing talk in the Modern Email devroom. He also contributes to Thunderbird and OpenStreetMap, and spoke at DARK Prague on 3 October 2026 with "ARTivism: Hacking culture to defend privacy".

**Sebastian Hagens (Sebastix)** is a free and open source developer and tech consultant from Breda, Netherlands, with a long background in web technology and online privacy (PHP, Symfony, Drupal, JavaScript, Docker). He also does server operations and security work on Debian-based infrastructure, and writes about privacy and the open web. A long-time Drupal community member, he works on decentralised publishing, including the Drupal modules and PHP libraries that let sites syndicate content independently of any single platform. He co-organised a community stand at FOSDEM 2025 and presented "POSSE content with Drupal using Nostr" in the Collaboration and content management devroom at FOSDEM 2026.

**Václav Navrátil (Aida)** is a long-term open source advocate. He has worked on data sovereignty with TrueNAS for over a decade. In his own time he operates a Delta Chat (chatmail) relay and a Nostr web-of-trust relay, writes open source Delta Chat bots, and helps people to circumvent censorship with Psiphon.

---

## Relevant URLs

- Bogomil Shopov:
  - https://github.com/bogomil
  - https://talkweb.eu
  - https://archive.fosdem.org/2026/schedule/speaker/bogomil_shopov_-_bogo/
  - https://speak.darkprague.com/dp26/talk/AYB3TT/
- Sebastian Hagens:
  - https://github.com/sebastix
  - https://nostrver.se
  - https://sebastix.nl/nostr-research-and-development/
- The talk that sparked the idea for this devroom:
  - https://fosdem.org/2026/events/attachments/LJDUCD-rus-censorship-2026-fosdem/slides/266923/fosdem-vp_0eoesvl.pdf
- Václav Navrátil:
  - https://github.com/aidik/

---

## Special requirements

- Scheduling the room so that it doesn't overlap with the Network, Security, or Decentralized Internet and Privacy rooms, if possible, so the audiences can attend both.
