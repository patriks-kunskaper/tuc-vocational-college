Threat Landscape Analysis: Key Trends Q1 2026
ENISA, SÄPO, MUST, Omegapoint, CERT-SE, CERT-Polska, Truesec

About This Document
This is a personal synthesis and analysis based on primary source documents reviewed in February 2026. Sources include ENISA ETL 2025, Omegapoint Säkerhetsindex 2026, SÄPO Annual Report 2024, MUST Årsöversikt 2025, OpenAI Threat Report October 2025, CERT-SE Newsletters February 2026, and incident reporting from Truesec and CERT-Polska on the Ghost Blizzard Polish energy infrastructure attack.

1. AI Is an Amplifier, Not a Replacement
AI is not enabling fundamentally new attack types. It lowers the cost and skill threshold for executing known attacks, generating phishing content faster, automating reconnaissance, and assisting with malware code. The more sophisticated emerging pattern is multi-model chaining, where attackers orchestrate multiple LLMs across different attack phases to evade detection systems tuned to single-tool signatures. The strategic implication is that AI is making existing threats faster and cheaper, not inventing new ones, but the acceleration effect is real and compounding.
Sources: ENISA ETL 2025, OpenAI Threat Report October 2025

2. The Awareness-Execution Gap
Swedish organizations broadly understand that threats exist but fail to implement adequate controls at a matching pace. Cross-functional security collaboration is strongly correlated with regulatory obligation. Organizations subject to NIS2 or SSL show significantly better implementation than those outside regulated frameworks. Governance pressure, not threat awareness alone, drives actual security improvement.
SÄPO's intelligence-derived view adds an important correction: many organizations do not actually know what their protective assets are, and therefore cannot recognize when those assets are being targeted. This creates a methodological tension worth noting. Omegapoint's findings are based on self-reported surveys reflecting how organizations perceive themselves, while SÄPO's findings are based on observed targeting and real incidents. Self-reported awareness is not the same as verified awareness. An organization can simultaneously know that ransomware is a threat while being entirely unaware that a foreign intelligence service has identified their HR database as a high-value target. SÄPO's ground-truth perspective is arguably the harder one to argue with.
The simplest framing: Omegapoint asked organizations what they think about their security. SÄPO watched what actually happens when organizations are targeted. The gap between how secure an organization thinks it is and how secure it actually is may be the most dangerous gap of all.
Sources: Omegapoint Säkerhetsindex 2026, SÄPO Annual Report 2024

3. How Attackers Actually Get In
Phishing accounts for approximately 60% of initial access vectors across EU incidents and remains the dominant entry point by significant margin. Vulnerability exploitation accounts for 21.3%, but 68% of those exploitation events result in malware deployment. This makes unpatched systems disproportionately dangerous relative to their frequency: lower likelihood of being the entry point, but a reliably severe outcome when they are. Together, phishing and vulnerability exploitation account for roughly 81% of documented entry points, meaning email security controls, MFA, and patch management address the vast majority of real-world attack surfaces.
Sources: ENISA ETL 2025

4. OT/ICS Is No Longer a Niche Concern
Industrial and operational technology systems are now a mainstream attack surface across all threat categories, not just ransomware. Three newly tracked threat groups illustrate the specialization emerging in this space. One is focused on gaining and selling initial access to industrial environments. One collects operational data and system configurations for downstream use. One specializes in crossing the boundary between IT and OT networks via social engineering and supply chain exploitation. A roughly 50% year-over-year increase in ransomware specifically targeting OT environments was also documented.
The significance is that OT attacks used to be rare, sophisticated, and primarily state-actor territory. The ecosystem is now professionalizing, with specialized roles mirroring the maturity seen in IT-focused cybercrime.
Sources: CERT-SE Newsletters February 2026, Dragos

5. The Polish Incident: A Strategic Inflection Point
In December 2025, Russian threat actor Ghost Blizzard conducted destructive cyberattacks against Polish energy infrastructure, representing the first confirmed destructive attack by this actor against NATO infrastructure. The targets included renewable energy farms, a combined heat and power plant, and a manufacturing facility. Entry was gained through VPN devices with absent MFA and default credentials. The objective was not financial. It was destruction of operational capability using wiper malware targeting industrial control systems.
The strategic significance is the shift from reconnaissance and intelligence collection to active destruction. This is not an escalation in capability. It is an escalation in intent. The controls that failed, including MFA, credential hygiene, and network segmentation, are foundational and well-documented. The gap was not knowledge. It was implementation.
Sources: CERT-SE Newsletters February 2026, Truesec, CERT-Polska

6. Russia and China: Different Threats, Same Adversary Tier
Russia is the dimensioning threat for Sweden and the EU, defining the ceiling of required defensive capability. Its operational pattern has shifted toward proxy-based operations using disposable assets recruited via gig economy platforms, reducing attribution exposure while maintaining operational reach. Ghost Blizzard (FSB-attributed) and Sandworm (GRU-attributed) are distinct actors within the Russian apparatus. The former has historically focused on energy sector pre-positioning. The latter is responsible for some of the most destructive cyberattacks ever recorded, including NotPetya and the Ukrainian power grid attacks.
China operates on a longer horizon, focused on supply chain access, technology acquisition, and infrastructure positioning without the same immediate destructive intent. Iran occupies a third tier, primarily opportunistic and regionally focused.
Sources: SÄPO Annual Report 2024, MUST Årsöversikt 2025, ENISA ETL 2025

7. Hacktivism: High Volume, Low Impact
79.4% of assessed EU threat objectives were ideology-driven, with a single pro-Russian group responsible for over 60% of DDoS claims. Only 2% of these incidents caused actual service disruption. The risk for organizations and analysts is over-indexing on hacktivist noise. It is visible, frequent, and easy to track, but operationally marginal compared to ransomware and state-nexus intrusions.
Sources: ENISA ETL 2025

8. Technology Sovereignty as Structural Risk
43% of Swedish IT decision-makers want to reduce reliance on US technology partners. 71% lack credible European alternatives. This is not a problem that patching or hardening resolves. It is an architectural dependency with NIS2 and national security implications. As geopolitical tensions persist and EU digital sovereignty becomes a policy priority, this gap will increasingly surface in security strategy and procurement conversations.
Sources: Omegapoint Säkerhetsindex 2026

9. Influence Operations Are Active and Election-Correlated
Russia-aligned foreign information manipulation operations are actively targeting EU audiences, with activity spikes correlating with elections and member state policy positions on Ukraine. For Sweden specifically, NATO accession and domestic political cohesion are documented high-priority targets. This is a distinct threat category from cyberattacks. The objective is shaping perception and undermining institutional trust, not compromising systems.
Sources: ENISA ETL 2025, SÄPO Annual Report 2024, MUST Årsöversikt 2025

Overarching Theme
Across all sources, the consistent pattern is not a shortage of threat awareness. It is a shortage of implementation. The controls that failed in the Polish attack are foundational. The posture gap Omegapoint documents is not about organizations lacking knowledge of what to do. SÄPO adds the harder truth: many organizations do not even know what they need to protect. The threat landscape is maturing and specializing faster than most organizations are responding, and the distance between those two curves is where the real risk lives.
