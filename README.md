# Simulacra

*The simulacrum is a copy with no original. Beneath is the first ethical solution to the authentication trilemma. Of this, we define the original, sans compromise.*

---

## Abstract

**Simulacra** proposes an authentication primitive that proves a living human body was present during a bounded interval without exporting readable physiological evidence or requiring institutional memory of the user. A wearable device evaluates multi-domain sensor consistency inside a protected hardware boundary, accumulates continuity state that decays without ongoing evidence, and emits anonymous expiring claims. As a consequence, the cost of forgery rises from software replay to coordinated physical reality staging across multiple independent evidence domains, contingent on the three invariants holding in practice. Three invariants govern the design: raw evidence stays inside the boundary (secrecy), only the boundary advances state (integrity), and depending on a contributed state of evidence, authority degrades or strengthens over time (progress). Narrow by design, the primitive proves one thing only: human presence. Uniqueness, identity, and institutional trust are deliberately excluded. Simulacra is stated precisely enough to critique, falsify, prototype, and improve.

---

## 1 Introduction

Fabricating a convincing human presence online now approaches the cost of electricity. Autonomous agents are opening accounts, posting content, executing transactions, and holding conversations for you, better than you, absent "you" in the loop. Without action at this interval you are already dead, lost to your divergent digitization. The simulacrum is already here, or near, and maybe this paper is lost to futility.

But maybe not. 

Every platform on earth will shortly face a choice it cannot defer.

Choice 1: Mandate identity verification for every interaction, in which case the internet becomes The Aleph.

Choice 2: Let the agents through and accept a zero trust end state. Simulacrum. Copia ad infinitum.

Surveillance internet or dead internet. The desert of the real itself.

Verification industry offers behavioral heuristics eroded by adversarial AI faster than defensive AI patching can create uniformity (Glasswing is a temporary solution). Identity industry offers biometric enrollment that converts proof of humanity into a permanent human partition. One fails on security. The other fails on sovereignty. Neither asks whether a third option exists.

Proof-of-personhood collapses three questions into one:

1. **Is this a human?**
2. **Which human is it?**
3. **Can an institution hold their soul forever?**

Trouble begins with the third question. Many existing systems answer the first by hardening the second and warehousing the result in a form that is persistent, linkable, or both. A registry knows your face and a social graph knows your neighbors. An enrollment session knows where you stood and of course a biometric issuer knows the template even when it promises not to...

Contamination is easiest to see in concrete cases. When an iris is enrolled into a durable registry, The Aleph does not merely answer whether a human appeared; it answers which human, then stores the answer in a form designed to outlive the session state. When a face video enters a persistent personhood registry, the registry learns a reusable representation even if the interface talks in the softer language of attestation or community vouching.

To put it bluntly, the field keeps smuggling surveillance in through the back door of verification.

Consider the alternative.

A user climbs a stairwell, passes through a cold doorway, pauses at a locked entrance, and then continues walking. A humane system could ask only whether one living continuity moved through that interval. Most deployed systems insist on asking who that continuity belongs to and whether the answer can be stored **forever**. **Forever** is failure.

Humanity needs a way to prove humanness without consenting to durable disclosure.

Enrollment is **NOT** the place to look. The missing option is a different primitive entirely. I will offer it to you, and I am confident you will see its value.

If proving humanness requires permanent custody of the proof, the proof has already been weaponized against the user. And if human presence can be authenticated without durable identity custody, platforms gain a third option between surveillance-backed verification and unverified synthetic chaos. This paper defines that primitive and states the conditions under which it could survive contact with the world.

From Worldcoin to Aadhaar to Palantir, the field has been living inside a trilemma it fears to name. Proving humanity, preserving privacy, and resisting Sybil attacks all become variables engaged in a dimensional tug of war, so reliably that every deployed system trades one to buy the other two. Not today. And we will make it so. Biometric enrollment licenses humanity and Sybil resistance at the price of privacy. Anonymous tokens fumigate enough space for privacy but suffer their end against fabricated identities. Social graphs ask you to sell your soul, and the price of that sale should be most evidently taught by the last twenty years, and if it escapes you, my friend, you're already a copy of your former self. This paper will decompose the trilemma problem: humanity and privacy live inside the base primitive (Sections 2 through 8), and Sybil resistance lives in separable layers above it (Section 9), preventing the downward reach into the abyss of reality dissolution the interested powers have built since your first password. The simulacrum is the copy of the copy of the copy until shapes and sounds present degraded and disfigured. If the pixelated copy is inevitable, remember this, my friend: you are already dead. The desert of the real is all that remains.

The classical trilemma forces a single layer to verify physical reality and prevent duplicate identities at once, and the bind rests in that forcing. Simulacra splits the work. The local hardware boundary verifies physical reality by refusing to export readable evidence. A separable threshold network prevents duplicates by signing over commitments the signers never observe. The base primitive confines state locally to keep anonymity intact. The issuance network signs blind commitments to keep decentralization intact. Falsification condition F9 tests whether that separation holds or whether the old bind returns the moment the design meets real traffic.

Incipit Nova Era

---

## 2 The Primitive

### 2.1 Definition

The primitive proposed here is:

> **anonymous, expiring, body-bound evidence of live embodied continuity, with no routine export of raw body-derived evidence**

A more operational restatement:

A body-adjacent sensing module, operating inside a protected hardware boundary, evaluates multi-domain bodily consistency over time. If that consistency is sufficient, it mints a narrow claim that a live human continuity was present during a bounded interval. The claim decays and can be re-earned but never hoarded, for it asks nothing of you but the anonymous evidence of going on to live among the natural laws of the universe. The burden of proof is high. The imperative for this paper is to seal the starstuff that is the sovereign you.

This anonymous primitive proves less than "personhood" in the legal or philosophical sense. It proves less than "identity." It proves less than "uniqueness." It proves something narrower and, for the coming internet, potentially more useful: that a live embodied process remained physically coherent long enough to accumulate bounded authority WITHOUT routinely exporting readable raw evidence to outside systems.

No. Fucking. Compromises.

Scope exclusions are explicit: uniqueness, institutional trust, traffic analysis, and consciousness testing all fall outside the primitive. One human can wear multiple devices and accumulate multiple continuity states; optional anti-Sybil layers including proximity-based collision penalties can pressure that surface without destabilizing into biometric deduplication (Section 9). The manufacturer remains in the trust path, and the political claim is narrower: that less of the body needs to be surrendered to institutions in order to demonstrate humanness. Under decay, durable credential accumulation weakens, though real-time observation and verifier-side logging remain unaffected. Simulacra is deliberately silent on the moral status of digital entities that may reason or even suffer without possessing a body that can satisfy this primitive. The primitive protects the human tributary, and embodied continuity deserves its own authentication path, one that allows digital entities to exist without exclusion of rights as the price of proving humanity.

### 2.2 The Three-Boundary Invariant

Any realization of this primitive has to satisfy three boundaries. Violate any one of them and the construction has become something else.

| Boundary | Requirement | What fails if it is violated |
|---|---|---|
| **Secrecy** | Raw body-derived evidence is not routinely exported in readable form outside the trusted boundary. | The construction becomes another biometric custody apparatus. |
| **Integrity** | Only the protected boundary, in a known state, can advance continuity state or mint claims about it. | Claims become forgeable or contingent on untrusted software. |
| **Progress** | Authority must be forward-evolving: earned by ongoing embodied evidence, weakened by absence, and not freely replayable. | The construction collapses into a reusable token rather than a time-bound continuity primitive. |

Secrecy is architectural. A compromised manufacturer could subvert it through firmware or provisioning. As long as integrity holds, state advancement stays inside the boundary. Whether silicon survives a bench attack is governed by physical access and the properties of the silicon itself. As long as progress holds, authority depends on ongoing body-worn time, something no software can cheaply produce, though a sophisticated attacker with physical access may yet find shorter paths.

The enclosure arrives shining and sealed, having passed through every hand along a supply chain that answers, at its highest order, to the surveillance state this primitive was built to resist, repressurized to specification, certified trustworthy by the very institution whose trustworthiness cannot be certified.

But remember my friend, open specification in name is hollow. The manufacturer presents as an infection risk to every possible point of failure. Open specification assists in parsing the difference between unlimited authority and a trusted boundary. Every compromised endpoint begins within the veneer of a trusted state, distracting you with features that are conduits to a bitter and dark end. Do you think telecoms-who-shall-not-be-named are banned for use in western societies because they are evil? What do you think? The answer tells you more about yourself in this space, friend, than it does about any implicit power structure. There are games being played. There are copycats that may differ in ethical resolutions but co-exist within a simulacra of intent. A published specification should invite ongoing audit. No spec is sacred in the age of AI. Audit the standard until your eyes and fingers bleed, and ask all to do the same.

Secrecy, integrity, progress. The three new horsemen of the apocalypse. Every deployed proof-of-personhood system has failed at least one, and many have failed all. Any failure is self-sovereignty bastardized. Each bastardization is a circle deeper into the simulacrum. A circle deeper into the desert of the real. A circle deeper into hell.

### 2.3 The Privacy Imperative

Simulacra is a privacy architecture designed to reduce the ordinary mechanisms by which authentication becomes coercive. Body-derived evidence stays local and unreadable by default. Biometric warehousing, global identity, persistent proof, and verifier memory of the body are all structurally absent, replaced by bounded claims that expire.

This is not absolute, immaculate privacy. What it offers is authentication by local evidence custody and controlled disclosure rather than durable exposure.

---

## 3 Evidence-Family Composition

Any authentication architecture, like it or not, cuts its teeth on adversarial stress testing. If the weakest link is one data stream (of which so many have met their demise), the attacker's job is bounded, and it gets cheaper every year as technology improves. To coordinate physical behavior of a living body moving through a changing environment over real elapsed time, well, that job is categorically beyond adversarial. In that latter case, we are stressing the universe against itself.

Simulacra decomposes the evidence for embodied continuity into four evidence families. Each derives from a different physical measurement domain. Each provides constraints the others cannot substitute for.

**Body-coupled evidence** originates from the organism itself: pulse timing, motion, posture change, contact impedance. It answers whether a living body is producing these traces or whether they were manufactured.

**World-coupled evidence** originates from the environment interacting with that body: pressure shifting across altitude, light changing through a doorway, temperature dropping in a stairwell. It answers whether this body is moving through a real, changing world or through a recording.

**Time/progression evidence** originates from the passage of real time: oscillator drift, session continuity, external time references, decay. It answers whether this continuity is unfolding at the speed of lived experience or has been compressed, frozen, or rewound.

**Secure-state evidence** originates from the protected device itself: monotonic counters, ratchets, sealed logs, bounded presentation state. It answers whether this continuity has advanced honestly or has been branched, cloned, or rolled back.

Three families produce physical evidence. A fourth makes it trustworthy over time. This decomposition is the paper's current explanatory frame, not a permanent partition.

Require the families to agree, and you see the contribution.

### 3.1 Cross-Licensing and Analytical Redundancy

No single family endures as an island. Power comes from **cross-licensing**: a forged body family should have to survive the world family; a forged world family should have to survive elapsed time and secure-state checks; a cloned state should have to survive disagreement with the lived world and the body that is supposedly carrying it. This is why Simulacra should be read less as a biometric classifier and more as a privacy-preserving instrument cluster.

**Analytical redundancy** in the Willsky 1976 and Chow-Willsky 1984 sense [21, 22] is the closer engineering ancestor. Heterogeneous sensors can constrain one another because the world itself supplies expected relationships and exposes residuals when those relationships break. Et voilà. Many islands. Many soft places to stand all at once.

Simulacra prefers aerospace-grade sensors, but even stronger than them is family diversity. The many islands of redundant universal consistencies and offsets. Independence here is in the physics (different laws governing different measurements), not merely in the geography of sensor placement. A second accelerometer on the same board may still help, but it does not buy the same attacker cost increase as a pressure trace, an oscillator check, or an externally observed timing reference governed by different physical or protocol rules. Agreement raises confidence. Disagreement names the liar and names the lie.

More sensors are a vanity metric. **Each additional independent physical domain can raise fabrication cost if it adds a meaningful constraint that must agree with the others.**

### 3.2 Attack Economics of Cross-Domain Concordance

Within this architecture, substituting the signs of the real for the real becomes a different kind of problem.

An attacker who can synthesize a plausible heartbeat (and BioForge shows that cross-modal cardiac synthesis is real [8]) still has to stage the pressure change, the motion trajectory, the thermal transition, and the elapsed time that would accompany that heartbeat in the physical world. The current scoring package (Section 7.2) concretely exercises body×world and body×body pairings; thermal and elapsed-time cross-checks remain architectural targets, not currently scored constraints. But the argument holds for whatever subset is active: BioForge's published CycleGAN operates within cardiovascular families; it has not demonstrated cross-domain synthesis from cardiac signals to inertial measurement unit (IMU) or barometric traces, though future generative work may attempt that bridge. The wager is this gap: physically dissimilar evidence families should be harder to forge jointly than any single biological channel.

Staging this concordance is continuous work, shielded by unpredictable challenge selection (Section 6.4, construction still open) that keeps the attacker blind to which committed relationship will be tested. Scale adds multiplicative cost. Each additional independent evidence family raises the cost of coherent fabrication. Satisfying multiple independent physical constraints in real time is categorically more expensive than replaying a packet, regardless of any single domain's spoofability.

A state-level adversary with physical laboratory access may still succeed. The security hypothesis is that the cheapest successful attack moves from "laptop running a replay script" to "physical laboratory staging coordinated multi-domain reality."

One implication should be stated directly. The same cross-modal coupling that makes the architecture work is the coupling an attacker will eventually learn to model. BioForge already does this within the cardiovascular family. Future generative work will reach further across the boundaries of the real. Across domains, synthesis is harder, and over time harder still, and under a sync design where the scoring challenge cannot be known in advance, hardest of all (Section 6.4, construction still open). The simulacrum feigns life and bleeds eloquently, and more so than the life it proves to mimic. The simulacrum disproves itself by way of excess, drunk on its own fabrication, forced to simulate the entire reality of all simulacra to survive a single sync, at a self-immolating escape velocity no attacker can sustain. Collapse the falsification under condition F7 (Section 8.3), and the scoring package begins from scratch measuring once again against the final benchmark: universal constants.

Generative models trained under physical constraints need separate treatment. They synthesize kinematic and physiological traces that obey thermodynamics, gravity, and continuity laws [40, 41]. The defense therefore rests on hardware-bound cost and latency inside unpredictable sync challenges, where the adversary cannot pre-compute the required state because the specific relation under test remains unknown until the sync window opens. Generating a physics-compliant simulation in real time under that condition is work the attacker cannot finish inside the window, because the map has to be computed only after the territory under test has already moved on.

### 3.3 Motion Artifact as Evidence

In much of the photoplethysmography (PPG) literature, accelerometer-coupled motion artifact is treated as contamination to remove. Asada et al. [32] introduced adaptive noise cancellation using collocated MEMS accelerometers as noise references for motion tolerant wearable PPG. Kim and Yoo [33] applied independent component analysis to separate the motion component from cardiac data. These represent a broader literature in which the accelerometer to PPG coupling is consistently characterized as a corruption dataset to be filtered, cancelled, or decomposed away. From the perspective of a sovereign embodied continuity, that "contamination" may also be proof of human presence. It is a sign that two domains are reacting to the same moving body at the same time. No group in the surveyed literature has proposed scoring that coupling as same-body evidence rather than removing it.

Motion artifact alone proves nothing, but a field that throws it away is discarding evidence. Develop accordingly.

---

## 4 Prior Art and the Novelty Perimeter

### 4.1 Same-Body Sensing and Continuous Wearable Authentication

Foundational same-body work showed that accelerometer coherence can distinguish whether two devices are on the same body rather than merely near each other. Lester et al. [3] produced a striking early result, but under a tiny and highly constrained same-placement setup; that result should never be quoted without the caveat attached. Cornelius and Kotz [4] pushed the problem into more realistic cross-position settings and obtained lower, more honest accuracy. ZEBRA [5] and adjacent continuous-authentication systems then showed that same-body and same-user inference can be maintained over time rather than only at login. Pistis [17] addressed the complementary problem of replay and liveness in gait-based wearable authentication using vibration, which matters here because any continuous body-worn system must eventually answer not just "is this the same body?" but "is this body live and present right now?"

Cornelius et al. [27, 34] demonstrated that bioimpedance can passively recognize the wearer of a device, progressing from household-scale recognition [27] to 98\% balanced accuracy on day-long data from 8 subjects [34]. That work is the closest published ancestor to Simulacra's body-coupled evidence family. It answers *who is wearing this device*. Simulacra deliberately refuses to ask that question.

Fusion-ID [9] used wrist-worn PPG plus motion sensors in a 247-user biometric-authentication study, which is precisely why it must be treated as adjacent rather than identical prior art. Liu et al.'s 2026 PPGTransID preprint [7] extends the cross-device story by asking whether physiological signals can transfer authentication status between a phone and nearby wearables. It is promising, recent, and still too pre-publication to lean on.

This lineage proves that body-worn cross-sensor consistency is real and sharpens Simulacra's own question. Those systems answer: *is this the enrolled user?* Simulacra asks something else: *can a live human continuity be established and refreshed without default identity disclosure?*

### 4.2 Personhood Credentials and Anti-Sybil Systems

As a systems map of the field, the 2024 *Personhood Credentials* paper [1] remains unmatched. It surveys the dominant approaches (social graph, general-hardware biometric, specialized biometric hardware, and institution-mediated issuance) and exposes widely accepted tradeoffs. Buterin's earlier analysis [2] maps the same terrain from a different angle, weighing biometric and social-graph systems against each other and concluding that no ideal form exists.

Eden [10] uses external observation and on-chain analysis to produce a personhood score. Its logic is anti-Sybil and identity adjacent.

IOST's PayPIN / Signet Ring [11] is a public wearable precedent with published documentation. Its own materials describe secure elements, heartbeat-based proofs, continuous verification, and a financialized identity-payment stack. Architecturally, IOST couples physical presence to a persistent wallet and incentive layer. Simulacra aims for the opposite: narrow, expiring, anonymous-by-default claims.

Buterin's June 2025 post on ZK-wrapped digital identity [29] argues that zero-knowledge wrapping alone does not eliminate the coercion and correlation risks of one-person-one-credential systems. Pluralistic identity structures, he proposes, are the better direction. Simulacra's continuous, expiring primitive fits that pluralistic direction, providing a humanity claim without requiring the single-identity binding that Buterin identifies as the core risk.

### 4.3 The Composition Claim

Narrowness is Simulacra's sharpest defense against a hostile reader.

Every component here exists independently. Wearables exist. PPG-motion fusion exists. Hardware authentication exists. Bot detection is a multi-billion dollar industry running on heuristics that weaken by the quarter. Novelty here composes from the technological composition itself:

> **Within the literature cited here, there is no peer-reviewed construction that combines continuous body-worn evidence, local protected-boundary evaluation, and anonymous expiring humanity claims while explicitly refusing to collapse that primitive into durable identity or global uniqueness.**

That is the perimeter and it is my wish that one day the former statement becomes untrue.

---

## 5 Evidence Base

Where vestiges of the real persist, one question remains: **do they agree with each other?**

Under Simulacra, multiple partially independent evidence families (Section 3) answer that question in concert. Success comes to the extent that forgery stops being a cheap software exercise and becomes a problem of staging coherent reality across more than one domain at once.

### 5.1 Same-Body, Colocation, and the Larger Question

A coupled physical process distinguishes itself like a fine wine.

Two devices in the same room experience the same Wi-Fi environment, similar temperature, and similar radio conditions. Those prove proximity, nothing more.

Two sensors on the same living body experience something stricter: a coupled physical process whose domains are related but not identical. Acceleration, pressure change, pulse timing, motion artifact, contact quality, posture change, and environmental transition are consequences of one body moving through one environment under one temporal progression, each measured through different physics.

A concrete interval makes the point better than abstraction. A wearer climbs a short stairwell, pushes through a doorway into colder air, pauses, then walks on. The IMU sees vertical motion and gait change. The barometer sees pressure shift. Light and temperature change across the threshold. PPG reflects exertion rising and then settling. The local state machine records an interval that cannot be advanced for free. None of those readings are decisive alone, but if they agree in the correct way, a body was there.

### 5.2 Current Evidence Perimeter

Four lower-level claims have support in the literature.

**First**, same-body accelerometer correlation is real. Lester [3] and Cornelius/Kotz [4] jointly establish that coherence between motion streams can discriminate same-body from different-body situations, although the best numbers live under constrained conditions and must not be inflated.

**Second**, large-scale cross-modal wearable alignment is real, and it's here. Apple's accelerometry distillation work [6] reports strong alignment between accelerometry and PPG representations using approximately 20 million minutes of data from approximately 172,000 participants, including 99.2% top-1 retrieval of PPG embeddings from accelerometry embeddings. That is powerful evidence that motion and cardiovascular traces share structured information at an immensity of scale.

**Third**, cross-device cardiac consistency is plausible enough to warrant serious attention. Liu et al.'s 2026 PPGTransID preprint [7], submitted to the Proceedings of the ACM on Interactive, Mobile, Wearable and Ubiquitous Technologies (IMWUT), reports 95.5% balanced accuracy in a 33-participant study for transferring authentication status between a phone's remote PPG signal and nearby wearable PPG sensors. That earns same-body transfer plausibility.

**Fourth**, cardiovascular biosignals are copyable. BioForge [8] demonstrates that an attacker who observes one cardiac modality can synthesize another strongly enough to fool multiple authentication systems, many of them more than 50% of the time in 10 or fewer attempts. That result destroys the lazy argument that "the body is secret." The body is an open channel. Security has to come from requiring joint consistency under bounded trust, cutting its teeth on the architecture rather than being assumed from physiology.

The main security claim this paper needs remains open. Multi-domain concordance, scored over time on body-worn hardware, must prove itself against adversaries who can jointly fabricate or replay multiple channels while targeting the exact features the system uses. The present evidence is strongest in the body family, prototype-thin in the world family, and still mostly candidate logic in the time/progression and secure-state families. The current scoring package should be treated as the **minimum viable cluster**, not the ceiling of the design. Do not forget this.

| Evidence source | What it supports | What it does **not** support |
|---|---|---|
| Lester / Cornelius-Kotz [3, 4] | same-body motion discrimination under specific placements and activities | universal same-body performance, sedentary validity, or adversarial robustness |
| Apple accelerometry-distillation work [6] | large-scale cross-modal coupling and representation alignment | same-body authentication security or claim object design |
| PPGTransID [7] | physiological consistency across devices/positions may be useful | anonymity, issuer trust, or full primitive viability |
| BioForge [8] | biosignal spoofing is real and multi-modal threat models must be taken seriously | this raises the bar on what must be tested |

---

## 6 Realization

### 6.1 Why Band-First

The current strongest hypothesis is a **band-class trust root** worn on the body.

The band is a working hypothesis, chosen as the best current compromise among sensor surface, power budget, wear time, mechanical stability, and the possibility of tightly controlling ingress and computation inside one adjacent boundary.

A ring may be more socially acceptable in some settings and less stable in others. A chest strap may give better signal quality and worse daily adoption. A hardened smartwatch may offer convenience at the cost of inheriting platform assumptions, likely supply-chain attacking yourself into oblivion before it ever turns on.

### 6.2 Trust Distribution

The band alone is the trust root.

A phone can provide networking, UI, challenge relay, or wallet functions. A watch can provide auxiliary corroboration. Neither should be treated as the moral or technical center of Simulacra. If the devices vulnerable to supply-chain attacks are compromised, the design should degrade but not silently invert itself.

The **band owns the body-coupled and secure-state evidence families**, while companions may contribute auxiliary observations to the **world-coupled** and **time/progression families**. A phone can report network time, radio environment, or displacement deltas. A watch can report environmental conditions or co-wear anomalies. The point is to ask whether their observations remain consistent with the band's own instruments, and to discard it when it does not.

At sync, a companion may provide the latest public beacon value it observed, its current network or cell-derived time, and, when available, a coarse displacement or environmental report since the previous sync. The band compares those observations against its own oscillator state, inertial estimate, and world-family traces. Consistency can add time or world confidence. Inconsistency can discount or ignore the companion entirely. The companion never learns family-level summaries, continuity state, or the result of the comparison. The dangerous devices cannot peer inside The Aleph that matters.

### 6.3 Compatibility Without Capitulation

The construction can speak to legacy platforms absent subjugation.

A future Simulacra device may need to speak to iOS or Android, may need to present to web services, and may need to fit inside current relying-party systems. None of that requires treating Apple, Google, carrier public-key infrastructure (PKI), or vendor trusted execution environments (TEEs) as an epicenter of design. The right design stance is: compatible where useful, dependent only where unavoidable, and architecturally pointed toward less custody, less persistence, and less central memory over time.

Operationally, that means a future band may speak ordinary transport layers such as Bluetooth Low Energy (BLE) and present proofs through standard verifier-facing channels, including CTAP-style roaming-authenticator bindings [25] where they are useful, while the phone remains only a relay, display, challenge broker, or reporting source. The phone may carry packets, contribute time or world observations, and help route challenges. It must not become the place where continuity state lives or where the decisive signing authority quietly migrates.

### 6.4 The Sync Boundary

The four evidence families become a protocol only when the scoring paths are specified (Section 7) and when the paper states **where** provisional local continuity state is tested, ratcheted, and made claimable.

The strongest current candidate is a **hybrid sync boundary**. The band accumulates sealed provisional continuity state locally. That state can include family-level summaries, residuals, and modality-specific provisional outputs from any measurement channel, whether body-coupled, world-coupled, temporal, or secure-state in nature. No single channel proves much on its own. The question is whether committed provisional outputs can later remain mutually consistent.

Broad score advancement should depend on the intersection of **sealed local evidence** and **unpredictable external input**. That input might come from a distributed randomness beacon [23, 24], an append-only public log, a committee-issued challenge family, or a hybrid that mixes global public input with device-local derivation. The paper names the required properties rather than prescribing an implementation: the input should be public enough to verify, unpredictable enough to prevent perfect precomputation, forward-moving so that progress can be measured against it, and difficult for any single party to bias without detection.

This changes the attacker's position. A compromised phone or watch may relay packets, falsify companion observations, or try to shape the sync surface. It still does not get to read the band's sealed evidence directly. If the challenge space is not known in advance, fabrication becomes partly blind. The attacker must stage concordance across evidence families without knowing which committed relation will be opened or tested at sync.

A supply chain compromise of the band does not automatically yield a valid credential. Each channel remains sealed from the others until sync, and the attacker must still produce outputs consistent with a physical reality that occurred across all of them simultaneously. Assume every companion device is adversarial. The sync boundary still asks whether reality was staged, and staging reality remains prohibitive (simulacrum). If it ever becomes cheap, every authentication construction on earth is dead, not just this one (simulacrum again).

The sync boundary can unify three functions that might otherwise be treated separately: **secure progress**, **checkpointing**, and **claim issuance**. A successful sync can ratchet freshness, confirm that continuity state was not silently rewound, and mint new claim bindings. A failed sync can force decay, loss, or probation for the disputed epoch. The sync event itself is also a privacy risk: BLE advertising payloads and MAC addresses change asynchronously, enabling passive tracking across address rotations [28], and checkpoint timing can become a stable correlation surface between issuance and presentation. Any eventual protocol must treat the companion communication channel as observable to surveillance and constrain sync-event metadata on that assumption. Private address rotation must occur at randomized intervals, because legacy fixed periods let passive adversaries correlate devices across extended intervals.

#### 6.4.1 One Epoch, in Order

A coherent epoch looks like this. Sensors sample continuously. Over a bounded window, each active measurement channel produces an **atomic modality yield**: the irreducible provisional output of a single sensing modality over one epoch window. The barometer's pressure summary is one atomic modality yield. The IMU's motion summary is another. The PPG's optical summary is another. Evidence families are the higher-order groupings (body-coupled, world-coupled, temporal, secure-state) within which those modality-level outputs are interpreted and cross-licensed. Each atomic modality yield is domain-specific, bounded in time, and insufficient on its own. Nothing in the scoring architecture works without her. Atomic modality yields feed scoring paths. Scoring paths update the local continuity state. The sync boundary tests that state against external input. Only then can claim eligibility advance. Atomic modality yields do not become public claims. They exist only long enough to be cross-licensed against one another through the scoring checks and then to update the band's provisional local continuity state through the decay-aware accumulation rule. Raw evidence is purged after summarization.

Periodically, the band commits to the current epoch state. That commitment may be computed over raw windows, extracted features, rolling digests, or some more careful hybrid; the present paper leaves that choice open. What matters at this stage is that the band can carry provisional continuity forward without routinely exporting readable raw evidence.

At sync, the band encounters forward-moving external input. A companion may relay it and offer its own statements, but the companion does not decide the result. The band checks whether the committed local state remains consistent with the new input and with any companion observations it chooses to consider. If the check succeeds, the continuity state ratchets forward and bounded claim eligibility may advance. If the check fails, the disputed epoch decays, is discounted, or is placed under a stricter penalty regime. If sync does not happen, the band may continue to accumulate state locally, but broader claim issuance remains gated by the missing checkpoint.

Without a lifecycle like this, the evidence families remain a taxonomy rather than a construction.

### 6.5 Claim Surfaces

Several **claim modes** fit within the primitive without changing the underlying invariant.

**Mode 1: Anonymous verification.** A relying party learns only that a sufficient continuity was present during a bounded interval and that the proof is fresh enough for the occasion. In the strongest current reading of this mode, bounded anonymous presentation is baseline: some ARC-like or equivalent mechanism [12, 13, 14] must prevent a single freshly minted proof from being replayed or spent without limit even before any higher anti-Sybil overlay is considered.

**Mode 2: Relying-party-scoped continuity.** A relying party can re-encounter the same pseudonymous continuity without learning who the user is globally. This proves same-key-plus-fresh-evidence, not biological identity. The relying party knows the same pseudonymous continuity returned with fresh evidence. The body behind it stays anonymous.

**Mode 3: Public commitment.** A user may choose to attach ongoing embodied continuity to a public persona. This is the least private mode and should not be the default assumption of the architecture.

Mode 1 is the design center, and stronger linkage belongs only as explicit opt-in layers. These modes are political positions about how much a user discloses, not product tiers in a pricing table.

### 6.6 Two Realization Families

Two trust philosophies can realize the same primitive.

**Realization A: boundary-trusted commitment.** Sensor data remains sealed inside the band's enclave while the band evaluates its own multi-domain consistency locally and produces a cryptographic commitment. The shared standard evaluates those commitments against companion observations and unpredictable external input, and a successful test mints the claim. This is the buildable baseline. The EZ mode. Its trustworthiness depends on the boundary, firmware integrity, and the physical limits of the hardware.

**Realization B: externally verifiable commitment.** The band's internal evaluation becomes auditable from outside the device, and the verifier checks the boundary's computation directly. This is attractive in principle and significantly less mature in practice. It also risks undercutting the soul of this paper, because once computation is opened to external audit, a matching observation surface opens with it.

Simulacra treats Realization A as the baseline and Realization B as a frontier. Develop accordingly.

---

## 7 Provisional State and Scoring

### 7.1 Impermanence as Security Economics

Decay is the economy of security.

A continuity state that never weakens becomes a durable identity. A continuity state that must be renewed by ongoing embodied evidence remains closer to a universal session state. A breath is preferred over a picture.

Leaky accumulation is the model:

$$
\mathrm{score}_{t+1}=\alpha\cdot\mathrm{score}_t+(1-\alpha)\cdot g(\mathrm{consistency}(W_t))
$$

where $W_t$ is the current evidence window, $g$ maps consistency into a bounded contribution, and $\alpha$ controls the decay rate.

The exact half-life is a deployment parameter. A short half-life increases the cost of maintaining many live credentials. A long half-life increases convenience and decreases anti-Sybil pressure. **Decay is a tradeoff surface. If you intend to continue living, the tradeoff is minimal.**

Claim eligibility requires crossing a minimum viable score:

$$
\mathrm{score}_t \geq A, \quad A \geq 0
$$

where $A$ is a deployment parameter. The constraint $A \geq 0$: negative thresholds are meaningless. At $A = 0$ the construction imposes no accumulation requirement; accumulation alone no longer constrains claim eligibility. Practical deployments that require band evidence choose $A > 0$. At $A > 0$, the interaction of $A$ with $\alpha$ and the epoch interval determines the **rebuild window**: the time a new or reset device must be continuously worn before claims become mintable.

When the device is removed or no body is present, the consistency contribution drops to zero and the score reduces to pure exponential decay:

$$
\mathrm{score}_{t+n}=\alpha^n\cdot\mathrm{score}_t
$$

This decay is steep. At representative parameters ($\alpha \approx 0.99$, epoch interval $\approx 30$ minutes), one day of absence costs roughly 38\% of accumulated score. Three days costs roughly 77\%. A week of non-wear reduces the score to below 4\% of its peak regardless of prior history. There is no reservoir of stored authority. Accumulated authority decays exponentially without evidence.

At sync, the magic happens. The sync boundary gates broader claim advancement, so a device that is worn but never syncs accumulates local state that cannot be spent. A device that syncs but is not worn has nothing to spend. Maintaining a live credential requires both: continuous body-worn evidence production and periodic sync against external input. Pure score accumulation converges within days at $\alpha = 0.99$. But claim eligibility depends on more than raw score. The sync boundary must be cleared, challenges must be met, and failed or missing syncs can impose penalties or probation. The effective rebuild window, the time from a cold start to mintable claims, is a function of the accumulation rate, the sync cadence, and the threshold $A$. A representative design target places the effective rebuild window at approximately 27 days, less than one full month. This figure is not derivable from the accumulator equation alone; it reflects the combined effect of score accumulation, sync cadence, missed-sync penalties, and threshold selection. It is long enough that maintaining multiple live credentials is expensive in body-worn time, short enough that device loss or replacement does not permanently exclude a legitimate user. A higher threshold increases Sybil cost but also increases recovery time. The representative wearing suggestion is waking hours, not 24/7. Eight hours of sleep costs roughly 15\% of accumulated score at $\alpha = 0.99$. For a wearer already above threshold $A$, this overnight loss will often leave the score above the claim boundary; it does not reset the credential. No worries. Sleep naked.

Under the base primitive, each credential costs body-worn time to build and maintain. One human can wear multiple bands and accumulate multiple continuity states: that is the explicit price of refusing biometric deduplication (Section 2.1). The stronger claim, that $k$ credentials require $k$ separate bodies, holds only when optional anti-Sybil overlays such as co-wear penalties or encounter-based friction are active (Section 9). Without those overlays, a single body can farm multiple credentials in parallel at the cost of multiplied hardware, device-hours, and sync overhead. With them, the cost becomes physical and multiplicative. This is why we must allow for naked sleep. Our devices may collide, and humans need to cuddle.

The local continuity state authorizes claim issuance but never becomes the claim object. No raw state information leaves the protected boundary during presentation. TL;DR: The continuity state is the engine. The claim is the exhaust.

### 7.2 Scoring Paths

The current scoring package is **designed and preliminarily tested on proxy data, not validated under the project's own hardware or adversarial conditions**. It is the **minimum viable scoring package** rather than any asserted ceiling. Its job is to make the first experiments legible. No parameters in this section are guilty of turning against the data, although I welcome their dismantling. The formulas exist to make the hypotheses specific enough to test and falsify. Each scoring path asks whether two provisional outputs agree. S1 pairs outputs from different evidence families (body × world). S2 and S3 pair distinct modalities within the body family, where agreement across different physical transduction pathways is still informative even without cross-family diversity. The evaluator asks whether multiple atomic modality yields remain mutually consistent enough to advance the provisional continuity state. Each row below names a pair of atomic modality yields and the statistic that scores their agreement.

| Candidate | Sensor domains | Intended regime | Concrete statistic | Plausible default window | Current status |
|---|---|---|---|---|---|
| **S1** | IMU + barometer | active vertical motion | windowed cross-correlation between altitude change and integrated vertical acceleration | 10-30 s on stairs / distinct elevation changes; up to 60 s in mixed walking | prototype hypothesis |
| **S2** | IMU + PPG | active movement and motion-artifact regimes | magnitude-squared coherence between optical and inertial streams over candidate motion/cardiac bands | 8-20 s during active motion; 30-60 s under weaker movement | prototype hypothesis |
| **S3** | optical + mechanical cardiac timing (PPG + micro-motion / BCG-like timing) | sedentary or low-motion fallback | correlation or agreement between inter-beat interval sequences from optical and mechanical traces | 30-120 s, likely longer than S1/S2 because of lower signal-to-noise | open and weakest current pathway |

For **S1**, one natural statistic is

$$
\rho_{ah}(\tau)=\operatorname{corr}\!\left(\Delta h(t),\int a_z(t-\tau)\,dt\right)
$$

computed over a bounded window and summarized over small lags $\tau$. Here $\Delta h(t)$ is first-differenced barometric altitude and $a_z(t)$ is vertical acceleration after frame alignment.

For **S2**, one natural statistic is band-limited magnitude-squared coherence

$$
C_{xa}(f)=\frac{|S_{xa}(f)|^2}{S_{xx}(f)S_{aa}(f)}
$$

where $x$ is the optical stream and $a$ is the inertial stream. A practical implementation could aggregate coherence over candidate cardiac bands (roughly $0.7-3$ Hz) and motion-artifact or movement sidebands (roughly $2.5-8$ Hz), while treating those band choices as tunable rather than canon.

For **S3**, the simplest candidate is agreement between beat-to-beat interval sequences inferred through two pathways,

$$
\rho_{IBI}=\operatorname{corr}(IBI_{PPG}, IBI_{mech})
$$

possibly augmented by lag consistency, beat-detection agreement, or short-window timing residuals. S3 is the weakest current pathway precisely because extracting stable mechanical cardiac timing at the wrist under real-world low-motion conditions remains hard.

Preliminary S2 testing on public datasets (WESAD, N=15; PPG-DaLiA, N=15) shows that single-window magnitude-squared coherence produces modest but consistent same-body versus different-body separation in both cardiac and motion bands. Sequential accumulation over 20 windows lifts discrimination substantially. Full methods, effect sizes, and caveats are reported in the companion empirical note [31].

These sketches do not make the package validated. They make it specific enough that a sensor fusion researcher can implement and test it. The current package exercises body×world (S1) and body×body (S2, S3) pairings. S2 and S3 cut their teeth by crossing transduction pathways. An optical pulse and a mechanical vibration follow different physics even when they originate from the same heartbeat. The full concordance graph includes every pairing of independently produced atomic modality yields, across and within evidence families. S1, S2, and S3 are three entries in a much larger space. The remaining two evidence families, time/progression and secure-state, participate through different mechanisms rather than through pairwise coherence statistics. Time contributes through the decay rule (score must be renewed by ongoing evidence and cannot be banked indefinitely) and through sync boundary freshness (Section 6.4), where external time references such as beacon values or network time must agree with the band's internal oscillator state. Secure state contributes through the progress invariant (monotonic ratchets, anti-rollback, and the requirement that continuity advance rather than branch freely). These are architectural constraints that make the S-numbered scoring paths trustworthy over time, not additional scoring paths of the same kind. World×time and body×time cross-checks, which would produce S-numbered statistics, remain future work.

The concordance graph shifts with activity. A stairwell climb lights up S1 and S2 together. An hour at a desk quiets the kinematic edges and the scored package leans on S3 alone. Meanwhile the barometer tracks weather fronts, temperature follows thermoregulation against the room, light shifts with the sun, and the radio environment rotates as devices come and go around the body. Scoring those edges during stillness widens the graph beyond the territory BioForge already reaches.

---

## 8 Threat Model and Falsification Conditions

*To dissimulate is to pretend not to have what one has. To simulate is to feign to have what one doesn't have.*

### 8.1 Non-Goals

The following are outside the scope of the primitive by design:

- **Not institution-free.** The manufacturer remains in the trust path. The goal is to narrow institutional custody, not abolish it.
- **Not a deployable protocol.** The sync boundary is architecturally specified (Section 6.4), not construction complete.
- **Not general anti-surveillance.** Decay limits credential accumulation but does not prevent traffic analysis, real-time observation, or verifier-side logging.

### 8.2 Adversary Classes

| Class | Typical capability | Rough budget / access model | Why it matters |
|---|---|---|---|
| **A1: remote or companion-level attacker** | compromised phone, watch, relay channel, app layer, or verifier-facing client stack | ~$0-100 plus software effort | tests whether the band remains meaningful when companions are hostile |
| **A2: hands-on attacker** | physical possession, debug access attempts, rollback, probing, fault injection, side-channel extraction, simple signal injection | ~$100-1,000 and bench access | tests whether the protected boundary is more than a software fiction |
| **A3: laboratory physical attacker** | PCB rework, sustained probing, custom fixtures, invasive extraction, sophisticated side-channel and firmware attacks | ~$1,000-10,000+ and specialist time | tests the difference between tamper-evident consumer hardware and serious hardware security |
| **A4: supply-chain or manufacturer-level attacker** | altered firmware, altered provisioning, modified components, coerced updates, state-level or vendor-level control before the user ever wears the device, plus post-deployment exfiltration of raw sensor or continuity state through warranty return diagnostics, manufacturer telemetry pipelines, authorized diagnostic ports, and crash reporting channels | structural, not reducible to a simple budget | the manufacturer remains an institution in the trust path; open specifications, reproducible firmware, manufacturer diversity, and conformance criteria are the best available constraints |

A fifth element spans across all four classes: **model-assisted fabrication**. BioForge-style work [8] means the attacker need not steal the exact sensor stream; they need only access to one physiological modality and a generative model good enough to synthesize another.

The concordance channel rests on a wager against the current reach of generative synthesis, that the adversary has yet to field a construction capable of producing jointly consistent evidence across multiple physical domains in real time. This wager ages with the field. The long term defense is the combinatorial cost of joint consistency across all four evidence families simultaneously, where the cost of fabricating each additional independent domain multiplies rather than adds.

Even under A4 conditions, owning the device and owning the concordance are different problems. A manufacturer who controls the firmware still faces sealed channels, unpredictable challenge selection, and the requirement that all domains agree across elapsed time. Space and time cannot bastardize in the dark, and if they do, the concordance was never ours to claim.

### 8.3 Falsification Conditions

The primitive should be stated in a way that makes failure obvious.

| ID | Falsification condition | Example attack | What failure would mean |
|---|---|---|---|
| **F1** | A cheap bench rig can jointly spoof IMU-PPG coherence at operationally meaningful acceptance rates | ~$30-100 in phone, actuator, LED driver, or replay hardware | the core coupling thesis is weaker than claimed |
| **F2** | Barometric-motion agreement can be cheaply fabricated under realistic scoring windows | ~$30-100 in pressure manipulation | active-motion same-body evidence is easier to fake than hoped |
| **F3** | Low-motion windows remain operationally weak for same-body discrimination (AUC below ~0.6 at 60s windows across realistic cohorts) | standard dataset evaluation | the primitive fails too many bodies to be called a general humanity primitive |
| **F4** | Rollback or state cloning yields reusable continuity without detectable score collapse | battery pull, flash clone, firmware rollback | the progress boundary is not meaningful |
| **F5** | Claim presentation is linkable across relying parties or sessions | passive observation, verifier correlation, metadata inspection | the anonymous mode degrades into a tracking token |
| **F6** | Key extraction or secret compromise is cheap under modest physical attack | ~$100-1,000 with probes, logic analyzers, fault tools | the boundary offers less protection than the paper implies |
| **F7** | Multi-domain generative synthesis coerces the scoring package quickly (>50% success in 10 or fewer attempts) | model-assisted fabrication using a single observed modality, e.g., BioForge-style CycleGAN synthesis of ECG from rPPG [8] | designed scoring is not enough |
| **F8** | Performance degrades across skin tone, loose wear, disability, sweat, edema, or tremor | normal cohort diversity and basic fairness evaluation | the primitive is inequitable or too brittle for serious adoption |
| **F9** | Sequential claim issuance across a threshold signing network permits metadata correlation that reconstructs hardware identity at deployment-realistic traffic volumes | issuer-side timing analysis of logs, batch co-residence of claims, committee-side partial reconstruction | the trilemma decomposition fails |

---

## 9 Anti-Sybil Integration

Above the primitive lives uniqueness: a second design space where privacy-preserving design raises Sybil costs without bastardizing the claim into readable identity.

The middle ground as often it does under nuance, narrows. In approaching it we discover the option space is alive, and every candidate inside it still has real failure modes. One distinction matters immediately: bounded anonymous presentation (Privacy Pass / ARC-like [12, 13, 14]) inside Mode 1 presents as baseline protocol hygiene but not necessarily an anti-Sybil overlay. It prevents a single proof from being replayed without limit. No more, no less. The families below go further, adding physical, economic, or issuance friction above that baseline.

The strongest cryptographic direction names a specific mechanism. Blind threshold signatures issued over Pedersen commitments, as in Tanuki [35] and the IETF Blind BBS drafts [36], allow a distributed issuer network to sign over a continuity state the issuers never observe. The signature remains publicly verifiable while the committed state stays sealed inside the band.

| Candidate family | What it tries to add | Privacy posture | Current judgment |
|---|---|---|---|
| **Threshold or split-trust issuance** (threshold BBS+ [15], pairing-free blind-threshold [16]) | no single issuer learns or controls the whole issuance act | stronger than single-issuer models | serious research direction, hardware and governance still open |
| **Encounter or co-wear friction** | penalize improbable multi-band proximity or suspicious co-wear patterns | potentially privacy-preserving if carefully local and ephemeral | candidate mitigation only; false positives and graph leakage remain risks |
| **Decay economics and issuance caps** | raise the cost of keeping many live credentials warm (Section 7.1) | privacy-preserving if implemented locally or via blinded bounded issuance | useful pressure, not uniqueness proof |

These should be described as **anti-Sybil layers above the primitive**.

---

## 10 Open Engineering Problems

### 10.1 The Sync Boundary (Protocol Layer)

Turning the sync boundary principle into a finished construction is the next protocol task. That construction must preserve secrecy, resist rollback, tolerate offline accumulation, limit censorship damage, and avoid making checkpointing into a new tracking surface. A deployable design must answer five questions: what exactly gets committed, when the challenge is determined, how much failure is tolerable, what public input is acceptable, and what remains private at issuance.

### 10.2 Trusted Sensor Provenance

The first hardware task is to establish that scored streams originate from the band's own sensors and have not been rewritten in transit.

The sensor produces the real. Everything between the sensor and the scorer is a chain of translations and every translation is an opportunity to replace the real with its facsimile before the boundary receives it as truth.

| Sub-problem | What has to be protected | Candidate mechanism families | Current judgment |
|---|---|---|---|
| **bus authenticity** | sensor samples should not be trivially rewritten between sensor and scorer | authenticated or constrained ingress, protected peripheral paths | partially understood, not closed |
| **driver / DMA discipline** | untrusted software should not silently copy or alter samples before scoring | protected peripheral access, memory isolation, trusted driver placement | serious engineering task |
| **physical trace vulnerability** | exposed board traces should not make logical isolation irrelevant | shorter trace surface, tamper evidence, shielding | still the hardest practical gap |
| **debug / update abuse** | maintenance paths should not become sensor forgery paths | debug lock, secure boot, anti-rollback | necessary but not sufficient |
| **proof that the body is actually there** | even authentic sensors can still be fooled by replay or staged environments | device-controlled challenge-response, cross-domain consistency checks | strongest current defense |

### 10.3 Unlinkable Claim Objects

Making claims anonymous without recreating an institutional chokepoint is the central cryptographic task.

If a band signs claims with a stable device identity, the proof becomes a tracker. If a central issuer blinds and reissues claims, the design reintroduces the institutional dependency it was built to avoid. Privacy Pass and ARC [12, 13, 14] remain the most relevant current protocol family because they make unlinkable, bounded, rate-limited presentation legible. They do not by themselves solve the issuer problem for a decentralized hardware architecture.

ARC remains a working group adopted Internet Draft with zero production implementations as of the time of writing. The architecture proposed here depends on the properties ARC promises, keyed verification anonymous credentials with rate limiting, rather than on ARC as a specific protocol. Should ARC fail to reach RFC status, any anonymous credential scheme providing unlinkable tokens with issuer controlled rate limiting would serve the same architectural role.

| Claim-object family | Why it is attractive | Why it remains hard | Near-term role |
|---|---|---|---|
| **Central issuer + Privacy Pass / ARC** | clean bounded anonymous presentation, mature standards | recentralizes issuer trust | comparator and fallback family |
| **Device-self-issued credentials** | no outside issuer required | stable device key becomes a tracking surface | unacceptable as anonymous baseline |
| **Threshold or split-trust issuance** (threshold BBS+ [15], Snowblind [16]) | distributes trust, improves privacy | hardware cost, governance, verifier trust remain open | strongest current innovation direction |
| **Batch / cohort / manufacturer mediated issuance** | may enlarge anonymity sets | risks vendor capture, weak revocation | candidate family only |

Pairing-free threshold blind signatures such as Snowblind [16] require only standard elliptic curve operations, making anonymous issuance on Cortex-M-class hardware materially more plausible than pairing-heavy credential families. This undercuts the assumption that privacy-preserving issuance is computationally out of reach for constrained devices. Issuer governance and verifier trust remain open.

### 10.4 Low-Motion and Accessibility Sufficiency

The scoring package is strongest during movement. The next sensing task is to extend it to rest.

Ballistocardiography/seismocardiography (BCG/SCG)-style mechanical sensing [18] and electrical bioimpedance [19, 27] both materially improve the option space for sedentary and low-motion regimes. Electrical bioimpedance [19, 27, 34] is one of the strongest current candidates for low-motion fallback. It also has a practical advantage: wrist-worn bioimpedance analysis already ships in commercial wearables.

If low-motion fallback fails under adversarial testing, the primitive narrows from proof of humanity to proof of ambulatory capacity. That consequence is serious enough to make this one of the highest-priority research paths.

### 10.5 Secure Progress and Device Lifecycle

The next task is to make continuity state survive real events like decay, charging, removal, replacement, loss, and seizure.

Candidate time/progression sources include oscillator and real-time clock (RTC) behavior, external time references such as network or beacon time, session continuity receipts from companions, any local secure-state ratchet that makes rollback produce inconsistency rather than silent failure masquerading as success, and the temporal signatures already present in body and world evidence. The device needs enough partially independent progression sources that rollback becomes increasingly difficult to stage as a coherent adversarial attack.

Current time handling cross-licenses partially independent clocks, which is fine until the clocks become liabilities. Two complementary directions already exist in working hardware and cryptography.

Pressurized tamper-evident enclosures seal the device at manufacturing and wire a simple binary pressure sensor across the interior. Open the case, pressure drops, and the sensor trips red. Each unit is pressurized to its own unique value during manufacturing. Resealing the case at that pressure requires knowing a value the device released at the moment of opening. The housing materials must resist permeation, thermal cycling fatigue, and creep across the lifetime of the device. These devices should not be expected to last forever. Eventual hardware failure is an expected outcome.

A verifiable delay function requires sequential computation that resists parallelization. Solana's Proof of History runs this at scale through SHA-256 chained sequentially. Each step depends on the previous step, so a proof generated across N sequential hashes consumes N units of wall-clock time on any hardware. The time is present, and the proof illuminates this state. In the sync boundary this primitive routes claim production through sequential computation, and reading the claim reads the elapsed time from the cryptographic output.

Specification work for both directions remains open and of course left to the hands of more intelligent and capable minds.

One consequence of decay-based progress deserves separate attention. If a device is seized or disabled, authority collapses. The rebuild window (Section 7.1) is not only a usability cost. For a refugee, a disaster survivor, or a person fleeing violence, the rebuild interval may coincide with the exact period when proving humanness matters most. Any deployment that ignores this has failed a population it claimed to serve.

Hardware replacement after catastrophic failure remains unanswered. A legacy device has no mechanism for exporting its accumulated continuity state in readable form, because readable export breaks the secrecy invariant. A secure device-to-device transition protocol, in which the legacy device signs a terminal attestation that the successor ingests as initial state, still requires dedicated cryptographic research. Without that transition protocol, a destroyed device zeroes its continuity, and the user rebuilds from scratch through the standard rebuild window.

### 10.6 Research Directions

**For hardware security engineers:** define a band security profile. Ingress assumptions, physical attack classes, tamper evidence budget, secure state progression, and challenge response feasibility.

**For embedded systems engineers:** build the reference prototype. Just do it. Synchronized acquisition, protected local state, replay harnesses, and a testing framework for attack injection are the starting gun.

**For sensor fusion researchers:** implement and test S1/S2/S3 and candidate low-motion modalities on public and newly collected datasets. Report negative results. Do it now. Bioimpedance and electrodermal activity are the first candidates to test, because they measure the body through physics separate from the optical and mechanical cardiac signals S2 and S3 already use, and they stay active when the wearer sits still. A failed scoring package is valuable information of immense benefit.

**For cryptographers:** attack the claim event/object problem directly. Issuer models, unlinkability, presentation limits, verifier trust, threshold issuance feasibility, and computational cost on constrained hardware are subjects of immense import. Trial, destroy, rebuild, in whatever order you see fit.

**For accessibility, HCI, and public-interest researchers:** test human conditions that could make the primitive unjust. Low motion, disability, loose wear, low perfusion, atypical physiology, climate and sweat, and coercive use conditions. This must work for all.

**For governance and civil-liberties experts:** draft conformance language that keeps the construction from silently becoming the opposite of what it claims to be. The sealed boundary should not be penetrated by GDPR, but if regulations entail it, find a way to distinguish Simulacra's novelty.

**For information theorists:** the concordance argument assumes independence across evidence families, but that assumption rests on physical reasoning rather than measured information, and the datasets to test it already exist. Compute pairwise and conditional mutual information across PPG, IMU, barometric, thermal, and light channels on WESAD, PPG-DaLiA, and PAMAP2 while the body moves, sits, and sleeps, and apply factor analysis to find out whether four families reflect real statistical structure or a frame the paper finds convenient. The concordance graph becomes the beautiful map drawn on universal constants. Its measurement evokes the deterministic footing beneath.

---

## 11 Governance and Deployment Constraints

The political value of a construction like this, if it has one, is reducing how much institutional custody is required to prove humanness. The manufacturer still remains in the trust path. The goal is to narrow that dependency rather than pretending we have reinvented it.

The best governance responses are obvious: open specifications, reproducible firmware where feasible, public transparency about roots of trust and update models, manufacturer diversity across jurisdictions, and conformance criteria that expose anti-user deviations.

Simulacra presumes governance by an open consortium on the FIDO Alliance model [25]. A standards body publishes royalty-free specifications, and diverse manufacturers build conformant devices so humanness does not pass through a single institutional chokepoint. The consortium ratifies the scoring standard, the cryptographic primitives, and the sync protocol. Participation turns on engineering conformance. The consortium issues no token and extracts no rent. If a chain layer logs handshake outputs, the log keeps only the conformance verdict; the user's score stays sealed inside the user's device.

Open root-of-trust work matters as precedent. At datacenter and laptop scale, projects such as Caliptra [20] and OpenTitan [30] show that silicon trust can be opened for audit. At wearable scale, TROPIC01 [26] is a more relevant precedent. An open-architecture RISC-V secure element with published RTL has reached commercial deployment: inspired but imperfect. The right long-term question historically has become "which vendor should we trust?" when in reality it must be "how much of any trustable moment can be opened, measured, inspected, and contested?"

Any construction that can prove "a live human is here" can be captured and turned into dystopia. Compliance requires five constraints: no permanent identity binding, no export of raw body-derived evidence, no public or persistent modes as default, no unquestioned legacy platform roots, and no silent degradation of the primitive into a tracking layer. If those constraints are absent from the standardization path early, someone else will write the opposite rules later.

The architecture's political claim requires open-standard credibility. A proprietary humanity primitive is a contradiction in terms. Specifications, firmware, scoring algorithms, and claim object constructions should be open-source and open-specification, so that a system which asks users to trust a sealed boundary lets those users verify what the boundary exposes.

---

## 12 Conclusion

Simulacra does not detect reality, cure propaganda, kill AI activity, or settle proof of personhood. The proposition is narrower than any of those, and for that reason, more serious.

The proposition is that **live embodied continuity** can become a usable authentication primitive without default identity surrender and without routine export of raw body-derived evidence.

The argument for that proposition is no longer empty. Same-body literature, wearable sensor evidence, adversarial biosignal work, prototype-grade engineering detail, and now instrument-cluster logic, taken together, state the primitive responsibly and submit it to adversarial testing. The hardest problems have been illuminated. May they, the simulacra of our time, be superimposed upon each other when observed, yet remain hollow in their meaning.

Maybe all of this is in the most ironic futility.

But I tend to believe, even if in futility, that someone, somewhere, on a piece of land they own, stood at an island and did what I did: stated the fucking obvious.

If the scoring package fails, the paper should fail with it. If low-motion fallback fails, the claim to general humanity should narrow. If claim objects cannot be made unlinkable without recreating an issuer, the anonymous mode should remain explicitly incomplete. If the band-first hypothesis is surpassed by a cleaner trust root, the architecture should move. If privacy-preserving anti-Sybil optionalities fail, the paper should say that too rather than pretending the field has only two choices: surveillance or surrender.

Authentication has spent too long asking whether one credential, one issuer, or one biometric can settle the matter. Simulacra asks a harder question: can authentication be rebuilt around the local concordance of body, world, time, and secure state, around evidence families whose agreement confirms and whose disagreement decays evidence of life, so that successful forgery becomes less a software trick and more a costly act of staged reality?

Where the territory no longer precedes the map, this paper asks whether the body can reassert the territory.

**Can humanness be proven as expiring embodied continuity rather than durable identity?**

If the cost of simulating embodied presence remains prohibitive across the sensory perceptions of the universe, a base layer of verified life survives whatever comes to mimic it. There is a hidden objective in plain sight. An alternate ambition; prevention of simulacrum spawn, or at worst, a clean death by way of desert exposure. 

Humanity's grandest failure just might be the dissolution of the body into its own reproduction until the reproduction is lost copy upon copy. A type of hyper-evolutionary state wherein the digital and physical collide. Without a foundational universal primitive rooted in thermodynamics, time progression, gravity, entropy, and any constant corroborative of natural law that fits on a wrist or in a phone, that dissolution proceeds without contest and the network of selves becomes the only self there is. Under the most capable Sybil stresses, the cost of impersonation compounds against every constant the universe holds, scaling to an escape velocity of resources no mimicry can sustain. Those who willfully ignore this problem and refuse to approach it with the vigor it demands, have already made their Faustian bargain. They have already traded the real, for comfort-copy. Rodin's Thinker becomes the copy of a copy of a copy of a thought, depth expired until the very concept of depth itself no longer evokes more than a shadow of the meme. Every attempt at PoH distributes the copy-loss to a future intelligence. 

I implore you, let the universe debate what was lost to the sands of time. 

Magic beans are conceptually wondrous, but their purchase is a sale of the most sacred kind.

---

## Thank Yous

"Even if the software layer is perfect and fully decentralized, the Foundation still has the ability to insert a backdoor into the system, letting it create arbitrarily many fake human identities." - Vitalik Buterin [2]

"Arguing that you don't care about the right to privacy because you have nothing to hide is no different than saying you don't care about free speech because you have nothing to say." - Edward Snowden

"The internet, our greatest tool of emancipation, has been transformed into the most dangerous facilitator of totalitarianism we have ever seen." - Julian Assange

"You're expelled from your mother's uterus as if shot from a cannon towards a barn door studded with old nail files and rusty hooks. It's a matter of how you use up the intervening time in an intelligent and ironic way; and try not to do anything ghastly to your fellow creatures." - Christopher Hitchens

"Never again will the real have the chance to produce itself." - Jean Baudrillard

"Unless we are now living in a simulation, our descendants will almost certainly never run an ancestor simulation." - Nick Bostrom

To those who treated this project as real before we could guarantee the real inside each other.

"The necessity to humanize and to seize whatever methods we can to tell our stories is really, actually, pretty important." - Viet Thanh Nguyen

And to those we lost, who were here o7 *A* ≥ 0.

🖤 Care until it breaks you. It's the greatest thing a thing can do. 🖤

---

## Appendix A. Candidate Presentation and Anti-Sybil Families

This appendix is partly speculative. None of the following should be read as solved. The first row is a baseline presentation mechanism, not an anti-Sybil overlay; it is included as the comparator against which higher-friction families are measured.

| Candidate family | Intended effect | Privacy posture | Current maturity |
|---|---|---|---|
| **ARC / bounded anonymous presentation** | limit how often one continuity state can be spent in a context/epoch | strong if issuer trust is acceptable | strongest near-term candidate |
| **Threshold issuance (e.g., threshold BBS+)** | reduce single-issuer concentration | potentially strong | cryptographically credible, deployment-open |
| **Pairing-free threshold blind signatures (e.g., Snowblind)** | lower-weight distributed blind issuance | potentially strong | frontier candidate |
| **Co-wear / collision penalties** | reduce gain from wearing many devices in suspicious proximity | privacy-sensitive, must be local or narrowly disclosed | open candidate |
| **Encounter friction / local contact evidence** | make farming many anonymous credentials physically expensive | privacy-sensitive, false-positive prone | appendix-only candidate |
| **Optional higher-friction overlays** | allow applications to demand more than base human presence | depends on overlay design | outside base primitive |

---

## Appendix B. Representative Cross-Licensing Relations

| Family combination | What it can corroborate | What disagreement may reveal | Current status |
|---|---|---|---|
| **Body x World** | motion through a changing environment rather than isolated replay | staged motion without matching environmental transition | physically grounded, only partly validated |
| **Body x Time** | exertion, recovery, and continuity unfolding over real elapsed intervals | accelerated clocks, replayed intervals, or continuity farming | conceptually strong, implementation open |
| **World x Time** | transitions between environments across a plausible temporal sequence | bench emulation, frozen traces, or impossible timing | promising, under-tested |
| **Body x Secure State** | one body carrying one advancing continuity state through an epoch | replayed biosignals attached to cloned or rolled-back local state | foundational target, unresolved at deployment grade |
| **World x Secure State** | one instrument moving through an environment while local state advances honestly | fabrication that does not survive protected progression | promising, engineering-heavy |
| **Body x World x Time x Secure State** | embodied continuity inside a changing world over real elapsed time with advancing protected state | cheap software forgery and single-family replay attacks | architectural goal, not validated result |

The current prototype path only exercises body-world through S1 and body-body through S2 and S3. The remaining pairings are architectural targets.

---

## Appendix C. Candidate Sync Boundary Topologies

| Topology | What the band computes locally | Role of external context | Main strength | Main weakness | Current status |
|---|---|---|---|---|---|
| **Local provisional scoring + external ratchet** | provisional family-level summaries and continuity state | freshness checkpoint only | strongest local secrecy | rollback risk if local state can be cloned | conceptually coherent |
| **External-context-dependent evaluation** | retained commitments or summaries only | determines the evaluation challenge and advancement condition | strongest blind-attack intuition | higher availability and censorship risk | interesting, privacy delicate |
| **Hybrid local + sync** | provisional continuity state, local residuals, and partial scoring | selects or authorizes higher-order checks, ratchets progress | best current balance of secrecy, progress, and freshness | protocol not yet source-hardened | strongest current candidate |

---

## References

1. S. Adler, Z. Hitzig, S. Jain, et al., "Personhood credentials: Artificial intelligence and the value of privacy-preserving tools to distinguish who is real online," arXiv:2408.07892, 2024.
2. V. Buterin, "What do I think about biometric proof of personhood?", https://vitalik.eth.limo/general/2023/07/24/biometric.html, July 2023, accessed March 2026.
3. J. Lester, B. Hannaford, and G. Borriello, "Are You With Me? Using Accelerometers to Determine If Two Devices Are Carried by the Same Person," in *Pervasive Computing*, 2004.
4. C. Cornelius and D. Kotz, "Recognizing Whether Sensors Are on the Same Body," in *Pervasive Computing*, 2011.
5. S. Mare et al., "ZEBRA: Zero-Effort Bilateral Recurring Authentication," in *IEEE Symposium on Security and Privacy*, 2014.
6. S. Abbaspourazad, A. Mishra, J. Futoma, A. C. Miller, and I. Shapiro, "Wearable Accelerometer Foundation Models for Health via Knowledge Distillation," arXiv:2412.11276, 2024.
7. J. Liu, J. Tang, G. Zhao, R. Gui, S. Cheng, T. Lu, J. Liu, W. Wang, M. Gowda, Y. Shi, and Y. Wang, "PPG as a Bridge: Cross-Device Authentication for Smart Wearables with Photoplethysmography," arXiv:2602.08972, submitted to IMWUT 2026.
8. V. Krish, N. Paoletti, M. Kazemi, S. Smolka, and A. Rahmati, "Biosignal Authentication Considered Harmful Today," in *33rd USENIX Security Symposium*, 2024.
9. H. Kumar, H. S. Mousavi, and B. Shahsavari, "Fusion-ID: A Photoplethysmography and Motion Sensor Fusion Biometric Authenticator With Few-Shot On-Boarding," in *ICASSP*, 2022.
10. Y. Cao, J. Cao, H. Liu, Z. Cui, and L. Wen, "Eden: An Edge Computing Empowered Proof-of-Personhood Protocol for Anti-Sybil in Blockchain-based Metaverse," in *2nd International Conference on Intelligent Metaverse Technologies & Applications (iMETA)*, 2024.
11. IOST, "PayPIN Ring: Continuous Identity Verification," product documentation, https://docs.iost.io/payment-solutions/paypin/ring, accessed March 2026.
12. A. Davidson et al., "The Privacy Pass Architecture," RFC 9576, 2024.
13. S. Celi et al., "Privacy Pass Issuance Protocols," RFC 9578, 2024.
14. IETF Privacy Pass Working Group, "Privacy Pass Issuance Protocol for Anonymous Rate-Limited Credentials," draft-ietf-privacypass-arc-protocol-01, and "Anonymous Rate-Limited Credentials Cryptography," draft-ietf-privacypass-arc-crypto-01, March 2026.
15. J. Doerner, Y. Kondi, E. Lee, abhi shelat, and L. Tyner, "Threshold BBS+ Signatures for Distributed Anonymous Credential Issuance," in *IEEE Symposium on Security and Privacy*, 2023; IACR ePrint 2023/602.
16. E. Crites, C. Komlo, M. Maller, S. Tessaro, and C. Zhu, "Snowblind: A Threshold Blind Signature in Pairing-Free Groups," in *CRYPTO*, 2023; IACR ePrint 2023/1228.
17. W. Song et al., "Pistis: Replay Attack and Liveness Detection for Gait-Based User Authentication System on Wearable Devices Using Vibration," *IEEE Internet of Things Journal*, 2023.
18. A. D. Wiens, A. Johnson, and O. T. Inan, "Wearable Sensing of Cardiac Timing Intervals from Cardiogenic Limb Vibration Signals," *IEEE Sensors Journal*, 2017.
19. K. Sel, D. Osman, and R. Jafari, "Non-Invasive Cardiac and Respiratory Activity Assessment From Various Human Body Locations Using Bioimpedance," *IEEE Open Journal of Engineering in Medicine and Biology*, 2021.
20. Open Compute Project, "Caliptra: Silicon-Level Root of Trust for Datacenter Infrastructure," specification and reference implementation, https://chipsalliance.github.io/Caliptra/, accessed March 2026.
21. A. S. Willsky, "A Survey of Design Methods for Failure Detection in Dynamic Systems," *Automatica*, vol. 12, no. 6, pp. 601-611, 1976. DOI: 10.1016/0005-1098(76)90041-8.
22. E. Y. Chow and A. S. Willsky, "Analytical Redundancy and the Design of Robust Failure Detection Systems," *IEEE Transactions on Automatic Control*, vol. 29, no. 7, pp. 603-614, 1984. DOI: 10.1109/TAC.1984.1103593.
23. drand, "Distributed Randomness Beacon: Protocol Specification and League of Entropy," https://docs.drand.love, accessed March 2026.
24. NIST, "Randomness Beacon, Version 2.0: Interoperable Randomness Beacons," https://csrc.nist.gov/projects/interoperable-randomness-beacons, accessed March 2026.
25. FIDO Alliance, "Client to Authenticator Protocol (CTAP), v2.2," Proposed Standard, specification for external/roaming authenticators over USB, NFC, and BLE, https://fidoalliance.org/specifications/, July 2025.
26. Tropic Square, "TROPIC01: Open-Architecture RISC-V Secure Element," open-source RTL at https://github.com/tropicsquare/tropic01, general availability announced 2025, accessed March 2026.
27. C. Cornelius, J. Sorber, R. Peterson, J. Skinner, R. Halter, and D. Kotz, "Who Wears Me? Bioimpedance as a Passive Biometric," in *USENIX Workshop on Health Security and Privacy (HealthSec)*, 2012.
28. J. K. Becker, D. Li, and D. Starobinski, "Tracking Anonymized Bluetooth Devices," in *Proceedings on Privacy Enhancing Technologies (PoPETs)*, 2019(3):50-65.
29. V. Buterin, "Does digital ID have risks even if it's ZK-wrapped?", https://vitalik.eth.limo/general/2025/06/28/zkid.html, June 2025, accessed March 2026.
30. lowRISC and Google, "OpenTitan: Open Source Silicon Root of Trust," https://opentitan.org, accessed March 2026.
31. Simulacra Project, "Companion Empirical Note: S2 Proxy Testing on WESAD and PPG-DaLiA," project repository, 2026.
32. H. H. Asada, H.-H. Jiang, and P. Gibbs, "Active Noise Cancellation Using MEMS Accelerometers for Motion-Tolerant Wearable Bio-Sensors," in *Proc. IEEE Engineering in Medicine and Biology Society (EMBS)*, 2004.
33. B. S. Kim and S. K. Yoo, "Motion Artifact Reduction in Photoplethysmography Using Independent Component Analysis," *IEEE Transactions on Biomedical Engineering*, vol. 53, no. 3, pp. 566-568, 2006.
34. C. Cornelius, R. Peterson, J. Skinner, R. Halter, and D. Kotz, "A Wearable System That Knows Who Wears It," in *Proc. ACM MobiSys*, 2014.
35. C. Boschini et al., "Tanuki: Two-round Threshold Signatures from Lattices," Preview Talk at NIST Multi-Party Threshold Cryptography Workshop (MPTS), January 2026.
36. V. Kalos and G. Bernstein, "Blind BBS Signatures," IETF CFRG Internet Draft (draft-irtf-cfrg-bbs-blind-signatures-02), 2025 (expired and archived September 2025).
37. M. Meier and C. Holz, "BMAR: Barometric and Motion-based Alignment and Refinement for Offline Signal Synchronization across Devices," arXiv:2501.16015, 2025.
38. M. Osadnik, D. Kaviani, V. Cini, R. W. F. Lai, and G. Malavolta, "Papercraft: Lattice-based Verifiable Delay Function Implemented," IEEE Symposium on Security and Privacy, 2025.
39. K. Garb, J. Obermaier, E. Ferres, and M. Künig, "FORTRESS: FORtified Tamper-Resistant Envelope with Embedded Security Sensor," in *Proc. 18th Annual International Conference on Privacy, Security and Trust (PST 2021)*, Auckland, NZ, December 2021. DOI: 10.1109/PST52912.2021.9647783.
40. Y. Yuan et al., "PhysDiff: Physics-Guided Human Motion Diffusion Model," ICCV 2023, arXiv:2212.02500.
41. J. K. Christopher, S. Baek, and F. Fioretto, "Constrained Synthesis with Projected Diffusion Models," NeurIPS 2024, arXiv:2402.03559.
