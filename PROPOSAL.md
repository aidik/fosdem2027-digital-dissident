# FOSDEM 2027 Devroom Proposal: Digital Dissident

> Draft for the FOSDEM 2027 devroom form (deadline: **4 October 2026**).
> Items marked **[TODO]** need input from the organisers before submitting.

---

## Proposal title

**Digital Dissident: Building Toolchains for Life Under Digital Repression**

*(Short form: "Digital Dissident Devroom")*

## Session type

Devroom

## Preferred slot

Half day (any). We can also fill a full day if FOSDEM pairs us with a compatible half-day room.

---

## Elaborate description

*(For the FOSDEM programme team only. Not public.)*

**The gap.** Privacy and anonymity tools each have a home at FOSDEM: the network, security, decentralised and messaging rooms, and various main-track and lightning talks. Someone living under an authoritarian regime (Russia, Iran, China, Belarus, Myanmar and others) never uses a single tool, though. Their day-to-day security depends on a *chain* of tools that has to hold up end to end:

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

- 20 to 30 minute technical talks (majority)
- 10 minute lightning talks on field reports and new ideas
- One or two short panel or "toolchain teardown" sessions, where speakers from several projects walk through a realistic journalist or activist workflow and show where each tool helps or breaks
- A closing open discussion on interoperability gaps and shared next steps

**Programme quality.** Organisers will review all submissions on technical merit and fit to the toolchain framing, and will aim for a balance of projects, regions and speakers (established projects, new projects, researchers, people from affected communities). Pure product pitches and marketing talks will be declined. Every talk should include an explicit threat model and an honest account of limitations.

**Organisers.** FOSDEM requires at least two named managers who can respond promptly to schedule emails around the 7 December 2026 deadline. We are recruiting co-organisers from last year's speakers and from the projects listed below.
**[TODO: name at least two managers, with affiliations and contact addresses, before submitting.]**

**Projects and communities we intend to invite** (no commitments yet; we will confirm before the 20 October announcement if possible): Nym (mixnet), Delta Chat / chatmail, SimpleX, the Fediverse (ActivityPub implementations and instance operators), Nostr, Psiphon and other circumvention and VPN providers, plus Tor-ecosystem, Reticulum and mesh-networking projects, whistleblowing and secure-submission platforms, and censorship-measurement researchers. Several of these projects presented at FOSDEM 2026.

**Code of Conduct.** We will follow the FOSDEM Code of Conduct. In addition, talks that describe circumvention or anonymity should avoid operational details that would endanger specific users in the field.

---

## Draft call for papers

*(Public.)*

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
- Generic privacy talks with no connection to hostile or high-risk environments

**Formats:** 20 to 30 minute talks, 10 minute lightning talks, and short panel or "toolchain teardown" sessions.

---

## Why does this proposal fit FOSDEM?

*(Public.)*

- **Cross-project collaboration in a niche with no home.** FOSDEM favours rooms that bring together many projects in areas that don't otherwise have a space. Censorship-circumvention, anonymity, secure messaging, whistleblowing and hardened-OS projects are currently spread across separate rooms, or missing entirely. This devroom joins them around one shared user need instead of one shared technology.
- **Community over corporate backing.** The projects involved are mostly small or volunteer-driven, or non-profit, and nearly all are free and open source. They rarely have a conference space of their own.
- **Proven audience interest.** At FOSDEM 2026, "The Russian Censorship Circumvention, Tom's Traps, and Jerry's VPN" (Vitaly Repin), "NymVPN: The First Real-World Decentralized Noise-Generating Mixnet for Anonymity" (Harry Halpin, Alexis Roussel) and "Multi-relay chat messaging & cryptographic identities with Delta Chat and Chatmail relays" (Holger Krekel, missytake) all addressed this audience, but in different rooms. Delta Chat also presented in 2025 and Nym in 2023. **[TODO: add attendance figures if known.]**
- **Aligned with FOSDEM's values.** Free software, user freedom and privacy are core FOSDEM themes. A conference held in Brussels, the seat of EU institutions, is a fitting place to discuss the technical reality of digital repression and sovereignty.
- **Practical outcome.** The toolchain framing should produce concrete results: a shared threat-model vocabulary, documented interoperability gaps, and new collaboration between projects that have never met.

## Submitters' affinity to the topic

*(Public.)*

**[TODO: fill in for each organiser. Suggested structure:]**

- Name, role and affiliation
- Projects you develop, contribute to or operate in this space
- Experience with at-risk users, NGOs, newsrooms or censorship research
- Past FOSDEM involvement (speaker, devroom manager, volunteer)
- Personal connection to the topic, if you wish to share it

## Relevant URLs

*(Public.)*

**[TODO: add real links.]**

- Organiser project pages and repositories
- [The Russian Censorship Circumvention, Tom's Traps, and Jerry's VPN (FOSDEM 2026)](https://fosdem.org/2026/events/attachments/LJDUCD-rus-censorship-2026-fosdem/slides/266923/fosdem-vp_0eoesvl.pdf)
- [NymVPN mixnet talk (FOSDEM 2026)](https://archive.fosdem.org/2026/schedule/event/U3UCKS-nym-mixnet/)
- [Delta Chat multi-relay talk (FOSDEM 2026)](https://archive.fosdem.org/2026/schedule/event/3F9VTU-deltachat-chatmail-relays-multi-transport/)
- [Delta Chat talk (FOSDEM 2025)](https://archive.fosdem.org/2025/schedule/event/fosdem-2025-5853-delta-chat-from-e-mail-messaging-to-peer-to-peer-realtime-networking/)
- [FOSDEM 2026 Decentralized Internet and Privacy devroom](https://archive.fosdem.org/2026/schedule/track/decentralized-internet-and-privacy/)
- Recordings: https://video.fosdem.org/2026/
- Organiser blog posts or talks on the topic
- Censorship measurement resources such as OONI, Censored Planet and GFW Report, as background on why this room is needed

## Special requirements

*(Public.)*

- Standard FOSDEM devroom setup (projector, microphones, streaming and recording).
- A room large enough for a topic that we expect to be popular, given the audience for last year's talks.
- Scheduling the room so that it doesn't overlap with the Network, security or Decentralized Internet and Privacy rooms, if possible, so the audiences can attend both.

## Resources

*(Public.)*

- None to upload at this stage.
- **[Optional]** A one-page overview of the toolchain framing (a diagram of the "get online → communicate → report → publish → device" chain, with the projects at each step) could be added to help reviewers.
