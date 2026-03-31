  
**The Grove Foundation**

**The Autonomaton Pattern as Open Protocol:**

**TCP/IP for the Cognitive Layer**

*Architectural Foundations for Composable, Sovereign,*

*and Economically Self-Optimizing Cognitive Systems*

Jim Calhoun

Founder, The Grove Foundation

March 2026  •  Working Draft

*“Keep it simple. When in doubt during design, choose the simplest solution.”*

— RFC 1958, Architectural Principles of the Internet (1996)

*“Design is philosophy expressed through constraint.”*

— The Grove Foundation

# **Abstract**

The current AI infrastructure buildout concentrates cognitive capability behind API endpoints controlled by a small number of companies. This paper argues that the Autonomaton Pattern—a composable architectural specification for self-authoring software systems—occupies the same structural position for distributed cognition that TCP/IP occupied for distributed networking in the 1970s and 1980s.

We present a formal mapping between the design principles that made TCP/IP the dominant internetworking protocol and the architectural commitments of the Autonomaton Pattern. Specifically, we demonstrate structural equivalence across six dimensions: the hourglass invariant, the end-to-end argument, fate-sharing, layered independence, protocol-over-implementation philosophy, and economic self-optimization. We show that the Autonomaton’s five-stage pipeline (Telemetry → Recognition → Compilation → Approval → Execution), tiered Cognitive Router, and Green/Yellow/Red zone governance model satisfy the composability requirements necessary for a distributed cognitive network—the same requirements TCP/IP satisfied for a distributed information network.

The paper concludes with composition primitives—chain, branch, mesh, hierarchy, and federation—that emerge naturally from the pattern’s protocol properties, and argues that these primitives make centralized cognitive infrastructure economically and architecturally unnecessary for the majority of AI workloads.

**Keywords:** *autonomaton pattern, cognitive architecture, distributed AI, protocol design, TCP/IP, end-to-end principle, self-authoring systems, composable architecture, cognitive sovereignty, declarative governance*

# **I. Introduction: The Missing Protocol**

In 1988, David D. Clark published a paper that changed how an industry thought about infrastructure. “The Design Philosophy of the DARPA Internet Protocols” did not propose new technology. It articulated the architectural reasoning behind technology that already existed—and in doing so, gave the networking community a shared intellectual framework that enabled decades of composable innovation. \[1\]

We are at an equivalent inflection point in cognitive computing. The technology exists. Large language models, local inference engines, retrieval-augmented generation, agentic frameworks—the raw capabilities are proliferating faster than the architectures to govern them. What’s missing is not capability. What’s missing is the protocol layer: the shared set of architectural commitments that allows independently developed cognitive systems to compose, interoperate, and self-optimize without centralized coordination.

This paper proposes that the Autonomaton Pattern fills that gap. Not as a framework to adopt, but as an open architectural specification—a protocol for the cognitive layer—that occupies the same structural position TCP/IP occupied when networking was fragmenting into incompatible proprietary stacks.

The parallel is not metaphorical. It is structural. TCP/IP succeeded not because it was the most capable networking protocol—OSI was arguably more comprehensive—but because its design principles (simplicity, composability, end-to-end sovereignty, implementation independence) created the conditions for a distributed network that no single entity could capture. The Autonomaton Pattern makes the same architectural bet for cognition.

We begin by identifying the specific design principles that made TCP/IP a universal protocol rather than a proprietary stack. We then demonstrate, principle by principle, how the Autonomaton Pattern instantiates each one for the cognitive domain. We close with the composition primitives that emerge from these properties—and their implications for the $650 billion centralized AI infrastructure buildout currently underway.

# **II. The Design Principles That Made TCP/IP Universal**

TCP/IP’s dominance over competing protocols (OSI, SNA, DECnet, XNS) was not predetermined. It emerged from a specific set of design principles, documented across three foundational texts: Clark’s 1988 SIGCOMM paper \[1\], the Saltzer-Reed-Clark end-to-end arguments paper \[2\], and RFC 1958 \[3\], later extended by RFC 3439 \[4\]. These principles were not implementation details. They were philosophical commitments that determined what the protocol could become.

Six principles matter most for our purposes:

## **Principle 1: The Hourglass Invariant**

The Internet architecture is commonly described as an hourglass \[4\]. The narrow waist—the IP layer—is the single invariant through which all traffic passes, regardless of what physical layer sits below it or what application sits above it. Ethernet, Wi-Fi, fiber, satellite—all converge at IP. HTTP, SMTP, FTP, SSH—all diverge from IP. The invariant is deliberately minimal. It does one thing: route packets. This minimalism is the source of the architecture’s composability. Because the invariant is small, anything can sit above or below it.

## **Principle 2: The End-to-End Argument**

Saltzer, Reed, and Clark’s 1984 paper \[2\] established a principle that became foundational: functions required by applications should be implemented at the endpoints, not inside the network. The network should be simple. Intelligence belongs at the edges. This principle had a direct sovereignty implication, though the authors did not frame it that way: by keeping intelligence at the endpoints, the network cannot impose policy on the applications that use it. End-to-end is a freedom guarantee disguised as a performance optimization.

## **Principle 3: Fate-Sharing**

Clark’s 1988 paper introduced a concept he called “fate-sharing” \[1\]: the state required for a communication session should be stored at the endpoints, not in the network. If a node fails, only its own sessions fail—the rest of the network continues. This design choice traded efficiency for resilience. The network has no single point of failure because the network holds no state. Each node is sovereign over its own sessions.

## **Principle 4: Layered Independence**

TCP/IP separates transport (TCP/UDP), internetworking (IP), and link-layer concerns into independent layers. Each layer can evolve without disrupting the others. Jonathan Postel’s 1978 decision to split the original Transmission Control Program into IP (connectionless) and TCP (reliable, connection-oriented) was the defining architectural moment \[5\]. It created the independence that allowed innovation at each layer to proceed without coordination—the hallmark of a composable system.

## **Principle 5: Protocol Over Implementation**

RFC 1958 states the requirement explicitly: designs must scale to very many nodes per site and to many millions of sites \[3\]. TCP/IP achieved this by specifying a protocol, not an implementation. Any hardware, any operating system, any programming language could implement the protocol. The specification was open. Compliance was testable. The result: TCP/IP runs on devices its designers never imagined, from thermostats to satellites.

## **Principle 6: Simplicity as Scaling Strategy**

RFC 3439 extended RFC 1958 with a principle its authors called “the Simplicity Principle”: complexity is the primary mechanism that impedes efficient scaling \[4\]. Every feature added to the network core makes composition harder, coupling tighter, and failure modes less predictable. TCP/IP won not by having more features than OSI, but by having fewer. The network does one thing—deliver packets—and does it at planetary scale.

# **III. The Autonomaton Pattern: Same Principles, Cognitive Domain**

The Autonomaton Pattern is an open architectural specification (CC BY 4.0) for self-authoring software systems. It defines five commitments: a five-stage processing pipeline, a tiered Cognitive Router, a Green/Yellow/Red zone governance model, a Skill Flywheel for autonomous learning, and model-agnostic execution. These commitments are structural, not technological. They can be implemented in any language, on any stack, with any cognitive engine.

We now demonstrate that each TCP/IP design principle maps directly to an Autonomaton architectural commitment.

## **The Hourglass: The Five-Stage Pipeline as Invariant**

In TCP/IP, IP is the thin waist of the hourglass. In the Autonomaton Pattern, the five-stage pipeline—Telemetry → Recognition → Compilation → Approval → Execution—is the thin waist of the cognitive hourglass.

Below the pipeline: any data source, any sensor, any user interface, any webhook, any event bus. Above the pipeline: any cognitive model, any skill library, any output surface, any downstream system. The pipeline is deliberately minimal. It does not specify how to classify intent, which model to call, or what actions to take. It specifies that every cognitive interaction must pass through the same five stages in the same order—and that each stage produces a structured trace.

This is the composability property. Because the invariant is small and universal, any cognitive workload can traverse it. A customer service bot and a pharmaceutical research assistant use different models, different skill libraries, different zone configurations—but the same pipeline. They produce structurally compatible telemetry. They can be composed into larger systems without custom integration, for the same reason HTTP and SMTP can share the same IP network without custom routing: they share the invariant.

## **End-to-End: The Zone Model as Sovereignty Guarantee**

The Autonomaton’s Green/Yellow/Red zone governance model is the end-to-end argument applied to cognitive systems. Governance functions belong at the endpoints—with the human operator—not inside the cognitive layer.

Green zone: the system acts autonomously on confirmed skills. Yellow zone: the system proposes, the human approves. Red zone: human-only—the system surfaces information but takes no action. These classifications live in declarative configuration files (zones.schema), not in code. The operator controls them. The cognitive layer cannot override them.

This is structurally identical to the end-to-end argument’s claim that network infrastructure should not impose policy on applications. The Autonomaton’s cognitive engine—whether it’s Claude, GPT, Llama, or a local model—cannot impose policy on the operator. Governance is an endpoint function. The operator defines the zones. The system respects them.

The sovereignty implication is the same one Saltzer, Reed, and Clark identified in 1984, transposed to the cognitive domain: by keeping governance at the endpoints, the cognitive infrastructure cannot capture the operator. No API provider can restrict what the operator has classified as Green. No model vendor can require human approval for what the operator has classified as autonomous. The zone model is a freedom guarantee expressed as architecture.

## **Fate-Sharing: Sovereign State at the Node**

Each Autonomaton maintains its own state: its routing configuration, its zone schema, its telemetry log, its skill cache, its learned patterns. No external service holds this state. If a cloud API goes down, the Autonomaton continues operating on its local tiers (Tier 0: pattern cache, Tier 1: local models). If another Autonomaton in a composed system fails, only its sessions are affected. The network of Autonomatons has no single point of failure because no node depends on another node’s state.

Clark’s fate-sharing principle traded efficiency for resilience. The Autonomaton makes the same trade: maintaining state locally is less efficient than centralizing it, but it makes the system structurally resistant to both failure and capture. The operator’s data, patterns, and governance never leave the node unless the operator explicitly shares them.

## **Layered Independence: Cognition as a Swappable Dependency**

The Autonomaton Pattern enforces strict layer separation. The governance layer (zone model) is independent of the cognitive layer (model selection). The cognitive layer is independent of the execution layer (actions taken). The telemetry layer is independent of all three.

This creates the same evolutionary property Postel’s TCP/IP split created: each layer can improve without disrupting the others. Swap Claude for Llama—the governance layer doesn’t change. Add a new output surface—the cognitive routing doesn’t change. Introduce a new telemetry source—the zone model doesn’t change.

The practical consequence is model agnosticism as an architectural guarantee, not a marketing claim. The Cognitive Router treats the model as a dependency to be dispatched to, not an authority to be deferred to. Tier 0 (local pattern cache) requires no model at all. Tier 1 (cheap/local models) handles the majority of requests. Tier 2 and Tier 3 (cloud APIs, frontier models) handle only what the lower tiers cannot. Intelligence lives in the structure—the routing config, the zone schema, the skill cache—not in the model.

## **Protocol Over Implementation: Three Files and a Loop**

TCP/IP is a protocol, not a product. The Autonomaton Pattern is a pattern, not a framework. The minimum viable Autonomaton is three files and a loop: routing.config (maps intents to tiers and zones), zones.schema (defines governance boundaries), and telemetry.log (structured interaction traces). Any language, any stack, any model.

The test for compliance is architectural, not technological—exactly as TCP/IP compliance is testable against the specification, not against a reference implementation. Does behavior governance live in declarative config? Does the Cognitive Router route by tier? Does the zone model classify every action? Does the system produce structured telemetry? Does it learn from usage? Does it fail honestly? If yes, it’s an Autonomaton. If no, you know exactly what to fix.

RFC 1958’s requirement that designs scale to millions of sites \[3\] maps directly: the Autonomaton Pattern can run on a Raspberry Pi or a data center cluster, because the specification constrains structure, not resources. The two billion personal computers already deployed worldwide can each run an Autonomaton. No new infrastructure required.

## **Simplicity as Scaling Strategy: Declarative Governance**

The Autonomaton Pattern’s governance model is declarative, not procedural. Zone classifications are config entries, not code branches. Routing rules are key-value mappings, not decision trees. This is the Simplicity Principle applied to cognitive systems: every governance feature that requires code to change makes the system harder to compose, audit, and scale.

The contrast with current AI architectures is instructive. Most enterprise AI deployments embed governance in application code—guardrails are hardcoded, routing logic is procedural, audit trails are afterthoughts. This is the OSI mistake repeated for the cognitive era: feature richness at the protocol level that impedes composability. The Autonomaton Pattern makes the opposite bet. The governance layer is minimal and declarative. Complexity lives in the skills and the cognitive models—above the thin waist—not in the pipeline itself.

# **IV. Composition Primitives: What the Protocol Makes Possible**

TCP/IP’s design principles did not merely enable the internet. They enabled patterns of composition—client-server, peer-to-peer, publish-subscribe, mesh networking—that the protocol designers did not anticipate. The protocol created the conditions; the ecosystem discovered the configurations.

The Autonomaton Pattern’s protocol properties create equivalent composition primitives for cognitive systems. Because the pipeline is invariant, the telemetry format is structured, the zone model is declarative, and the Cognitive Router is tiered, independently developed Autonomatons can compose without custom integration. The following primitives emerge naturally from the architecture:

## **Chain Composition**

Autonomaton A’s execution output becomes Autonomaton B’s telemetry input. A content analysis system’s output feeds a distribution system’s telemetry stage as a structured event. Each node maintains independent zone governance. The handoff is structured data traversing a shared pipeline shape. No custom integration required. The chain can extend indefinitely because the pipeline shape is invariant.

## **Branch / Fan-Out**

A single recognition event triggers multiple parallel Autonomatons. A customer interaction classified by one Cognitive Router fans to billing, technical support, and sentiment monitoring Autonomatons simultaneously. Each runs its own pipeline independently. Zone inheritance propagates downward: if the parent classified a request as Yellow (requires approval), children inherit that constraint. Red always propagates. This is governance composability—the zone model scales from single node to fleet without changing its specification.

## **Supervisor / Worker Hierarchy**

A master Autonomaton whose pipeline routes work to specialized workers. The master’s Cognitive Router classifies and dispatches; the workers execute. The master runs on Tier 0/Tier 1 (routing is classification, not generation—cheap compute). Workers fire expensive models only when needed. The master’s Skill Flywheel learns which worker handles what best. This is the tiered compute thesis at fleet scale: the orchestration layer costs nearly nothing; the inference layer is precisely targeted.

## **Peer Mesh / Swarm**

Autonomous Autonomatons sharing a common telemetry bus, self-selecting into work that matches their routing configuration. No hierarchy. No central dispatcher. Each node watches the same event stream and picks up events its Cognitive Router is configured to recognize. Emergent specialization—the routing configs themselves create the division of labor. Governance is fully distributed; each node controls its own zones. This is the purest expression of the distributed compute thesis: two hundred machines, each sovereign, collectively handling workloads no single node could address.

## **Hierarchical Zone Nesting**

Enterprise-level zone boundaries that constrain all child Autonomatons beneath them. The enterprise declares: nothing in this fleet auto-deploys to production (Red zone at the parent level). Team-level Autonomatons set their own Green/Yellow/Red within that envelope but cannot exceed the parent’s ceiling. Zone governance becomes a tree—the CTO sets the outer boundary, team leads set inner boundaries, individual practitioners set the innermost. This is the regulatory compliance story expressed as one architectural property. EU AI Act requirements, SEC audit mandates, and Colorado AI Act provisions map directly to zone tree configurations.

## **Federation**

Independent organizations, each running sovereign Autonomaton fleets with their own zone governance, choosing to share specific skill caches or telemetry streams across organizational boundaries. The shared protocol is the pipeline shape and the telemetry format. Nothing else needs to be shared. Organization A’s Autonomaton discovers a routing optimization and publishes it as a skill. Organization B’s Autonomaton adopts the skill into its own Flywheel without sharing underlying data. Skills flow across the network. Data does not.

This is the open-source model applied to cognitive infrastructure—the same structural dynamic the Linux Foundation exploits for compute sovereignty, transposed to the cognitive layer.

## **The Recursive Case: Autonomatons That Build Autonomatons**

An Autonomaton whose pipeline watches workflow telemetry, recognizes repeating patterns, compiles a routing config and zone schema for a new Autonomaton, proposes the new Autonomaton in the Yellow zone (always supervised), and on approval, spawns it. The meta-Autonomaton’s Skill Flywheel learns what kinds of Autonomatons work well, what zone configurations reduce friction, and what routing patterns produce the best outcomes. It gets better at creating Autonomatons over time—a self-authoring system that authors self-authoring systems.

# **V. The Economic Argument: The Reverse Tax**

TCP/IP did not merely enable distributed networking. It made distributed networking cheaper than centralized alternatives. The end-to-end principle pushed complexity to the edges, where Moore’s Law continuously reduced the cost of endpoint intelligence. The network stayed simple and cheap to operate. The endpoints got more capable for free.

The Autonomaton Pattern creates an equivalent economic dynamic through what we call the Reverse Tax. The Cognitive Router’s tiered compute model is structurally incentivized to push work downward—from Tier 3 (expensive frontier models) toward Tier 0 (local pattern cache, zero marginal cost). Every confirmed skill in the Skill Flywheel represents a query that never needs to call an API again. The system gets cheaper as it gets smarter.

METR data shows frontier AI capabilities propagating to consumer hardware on a roughly 21-month lag \[6\]. What requires a cloud API call today runs locally in 2027\. Architecture that assumes specific model capabilities becomes technical debt on a 21-month depreciation curve. Architecture that validates outputs against structure—regardless of which model produced them—gets better automatically as models improve and costs decline.

At fleet scale, the Reverse Tax compounds. A supervisor Autonomaton notices that 80% of a worker’s requests hit Tier 1\. It proposes migrating those patterns to Tier 0—local execution, zero API cost. Approved. Now the worker runs 80% of its cognitive workload for free. Multiply by a hundred workers. The fleet’s aggregate cost declines with every learning cycle.

This is the structural asymmetry that made TCP/IP unbeatable against centralized alternatives. Centralized AI providers need users to keep calling the API. The Autonomaton Pattern is architecturally incentivized to reduce API calls to zero. The centralized model’s revenue is the distributed model’s waste. The two billion personal computers already deployed represent more aggregate compute than any planned data center buildout—already powered, already owned by the people who benefit from what they produce.

# **VI. The Governance Innovation: What TCP/IP Lacked**

The parallel between TCP/IP and the Autonomaton Pattern is structural, not total. TCP/IP famously omitted security from its original design priorities \[1\]. Clark’s 1988 paper acknowledged this gap, and the internet has spent decades retrofitting security as an afterthought—TLS, firewalls, NAT traversal, certificate authorities—all bolted onto an architecture that was not designed for adversarial environments.

The Autonomaton Pattern includes governance as a first-class architectural commitment, not an afterthought. The zone model is not a feature. It is part of the pipeline invariant. Every interaction traverses it. Every action is classified. Every trace is auditable.

This is the TCP/IP lesson applied forward: the principle you omit from the protocol becomes the problem the ecosystem spends decades compensating for. TCP/IP omitted security. The current generation of AI systems omits governance. Guardrails are hardcoded. Audit trails are optional. Zone boundaries don’t exist as a concept, let alone as inspectable configuration. The Autonomaton Pattern treats governance the way TCP/IP should have treated security—as a structural commitment baked into the invariant, not a policy layer bolted on later.

IBM’s Autonomic Computing manifesto identified the correct vision—self-configuring, self-healing, self-optimizing, self-protecting systems \[7\]—but lacked the governance layer to make self-management safe at scale. The MAPE-K loop (Monitor, Analyze, Plan, Execute with Knowledge) operates without explicit human sovereignty boundaries \[8\]. The Autonomaton Pattern completes the vision by adding what IBM’s framework omitted: the zone model that determines which self-management functions are autonomous, which require human approval, and which are reserved for human-only decision-making.

# **VII. Structural Correspondence**

The following table summarizes the principle-by-principle mapping between TCP/IP and the Autonomaton Pattern:

| Design Principle | TCP/IP Instantiation | Autonomaton Instantiation |
| :---- | :---- | :---- |
| Hourglass Invariant | IP layer: minimal packet routing that all traffic traverses regardless of physical or application layer | Five-stage pipeline: Telemetry → Recognition → Compilation → Approval → Execution. All cognitive interactions traverse same stages. |
| End-to-End Argument | Intelligence at endpoints, not in the network. Network cannot impose policy on applications. | Zone Model governance at the operator (endpoint), not in the cognitive engine. Model cannot override operator’s zone config. |
| Fate-Sharing | Session state at endpoints. Node failure affects only local sessions. No centralized state. | Routing config, zone schema, skill cache, and telemetry maintained locally. No external dependency for core operation. |
| Layered Independence | Transport (TCP), internetwork (IP), and link layers evolve independently. | Governance (zones), cognition (model), and execution layers evolve independently. Model is a swappable dependency. |
| Protocol Over Implementation | Specification, not product. Any hardware, OS, or language. Compliance testable against spec. | Pattern, not framework. Three files and a loop. Any stack, any model. Compliance testable against architectural commitments. |
| Simplicity Principle | Minimal network core. Complexity at edges. OSI lost to TCP/IP by having more features in the protocol layer. | Declarative governance. Minimal pipeline. Complexity in skills and models (above the thin waist), not in the pipeline itself. |
| Governance (added) | Omitted from original design. Retrofitted via TLS, firewalls, CAs. Decades of compensating infrastructure. | First-class commitment. Zone Model is part of the pipeline invariant. Every action classified. Every trace auditable. |

# **VIII. Implications and Open Questions**

## **For the Industry**

If the Autonomaton Pattern’s protocol properties hold, the $650 billion centralized AI infrastructure buildout faces the same structural challenge that mainframe computing faced in the 1980s. The internet did not beat mainframes by being more powerful. It beat them by being architecturally uncontrollable. A distributed network of sovereign Autonomatons, each optimizing its own cost curve via the Reverse Tax, each governed by its own zone model, each composable with every other via the shared pipeline invariant—this network is structurally cheaper, more resilient, and more auditable than any centralized alternative.

## **For Standards Bodies**

The Autonomaton Pattern is published under CC BY 4.0 because the thesis requires it. Distributed cognition that depends on a single vendor’s implementation is not distributed. The architecture must be replicable, inspectable, and independently operable. RFC 1958 established the precedent: nothing gets standardized until there are multiple instances of running code \[3\]. Atlas, the reference implementation, is one instance. The pattern awaits its second and third—from independent teams, in independent stacks, proving that the specification is sufficient.

## **For Practitioners**

The Autonomaton Pattern asks for three files and a loop. routing.config, zones.schema, telemetry.log, and a pipeline that connects them. A practitioner can build a compliant Autonomaton in a weekend. The composition primitives described in Section IV emerge from the protocol properties without additional tooling. Chain two Autonomatons by connecting one’s execution output to another’s telemetry input. The governance, provenance, and interoperability come from the structure, not from a dependency.

## **Open Questions**

Several questions remain open and represent opportunities for the research community. First, formal verification: can the pipeline invariant and zone model be formally verified for safety properties in composed configurations? Second, telemetry schema standardization: what is the minimal telemetry schema sufficient for cross-node composition? Third, economic modeling: how does the Reverse Tax compound across different network topologies and workload distributions? Fourth, trust federation: what are the minimum requirements for cross-organizational skill sharing with provenance integrity? These questions invite exactly the kind of distributed, independent investigation that made the IETF’s RFC process successful: rough consensus and running code.

# **IX. Conclusion**

Christopher Alexander published A Pattern Language in 1977—a book that described 253 patterns for designing the built environment \[9\]. The patterns were not instructions. They were philosophical positions with structural implications: here is a problem that recurs; here is the core of its solution; here is why this solution produces environments where humans thrive. Alexander’s work directly inspired the software design patterns movement \[10\], the Wiki itself \[11\], and a tradition of thinking about architecture as philosophy expressed through constraint.

The Autonomaton Pattern is a direct descendant of that tradition. It does not specify which model to use, which language to write in, or which cloud to deploy on. It specifies a set of architectural commitments—a pipeline, a router, a zone model, a flywheel, and a telemetry stream—that together create the conditions for software systems that are self-authoring, self-optimizing, sovereignty-preserving, and composable.

TCP/IP did the same thing for networking. It specified a protocol—not a product—and the protocol’s design principles created the conditions for a global network that no single entity could capture. The principles documented in Clark \[1\], Saltzer et al. \[2\], RFC 1958 \[3\], and RFC 3439 \[4\] were not implementation guides. They were architectural philosophy. They described the structural commitments that made the internet possible.

We are at the same moment for cognitive systems. The raw capability exists. The governance does not. The composability does not. The sovereignty guarantee does not. What’s missing is the protocol layer.

The Autonomaton Pattern is a proposal for that layer. It is open, composable, governance-native, model-agnostic, and economically self-optimizing. It asks to be tested the way TCP/IP was tested: by independent teams, building independent implementations, discovering whether the architectural commitments are sufficient for the systems they want to build.

The centralized AI buildout assumes that whoever controls the frontier controls cognition. TCP/IP proved that assumption wrong for information. The Autonomaton Pattern makes the same bet for intelligence.

# **References**

\[1\]  D. D. Clark, “The Design Philosophy of the DARPA Internet Protocols,” Proc. ACM SIGCOMM ’88, Computer Communication Review, Vol. 18, No. 4, August 1988, pp. 106–114. Revised 2013\.

\[2\]  J. H. Saltzer, D. P. Reed, and D. D. Clark, “End-to-End Arguments in System Design,” ACM Transactions on Computer Systems, Vol. 2, No. 4, November 1984, pp. 277–288.

\[3\]  B. Carpenter, Ed., “Architectural Principles of the Internet,” RFC 1958, Internet Architecture Board, June 1996\.

\[4\]  R. Bush and D. Meyer, “Some Internet Architectural Guidelines and Philosophy,” RFC 3439, December 2002\.

\[5\]  V. Cerf and R. Kahn, “A Protocol for Packet Network Intercommunication,” IEEE Transactions on Communications, Vol. COM-22, No. 5, May 1974, pp. 637–648.

\[6\]  METR, “AI Capability Trajectory Analysis,” Frontier Model Forum Technical Report, 2025\.

\[7\]  IBM, “Autonomic Computing: IBM’s Perspective on the State of Information Technology,” IBM White Paper, October 2001\.

\[8\]  J. O. Kephart and D. M. Chess, “The Vision of Autonomic Computing,” IEEE Computer, Vol. 36, No. 1, January 2003, pp. 41–50.

\[9\]  C. Alexander, S. Ishikawa, and M. Silverstein, A Pattern Language: Towns, Buildings, Construction. New York: Oxford University Press, 1977\.

\[10\] E. Gamma, R. Helm, R. Johnson, and J. Vlissides, Design Patterns: Elements of Reusable Object-Oriented Software. Reading, MA: Addison-Wesley, 1994\.

\[11\] W. Cunningham and K. Beck, “Using Pattern Languages for Object-Oriented Programs,” OOPSLA ’87 Workshop on Specification and Design for Object-Oriented Programming, 1987\.

\[12\] J. Calhoun, “The Grove Autonomaton Pattern: Toward Self-Authoring Software Systems,” The Grove Foundation, Draft 1.4, February 2026\. CC BY 4.0.

**The Grove Foundation**  
the-grove.ai

*This work is licensed under CC BY 4.0*