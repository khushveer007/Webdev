---
stepsCompleted:
  - step-01-init
  - step-02-discovery
  - step-02b-vision
  - step-02c-executive-summary
  - step-03-success
  - step-04-journeys
  - step-05-domain
  - step-06-innovation
  - step-07-project-type
  - step-08-scoping
  - step-09-functional
  - step-10-nonfunctional
  - step-11-polish
  - step-12-complete
inputDocuments:
  - /home/opsa/Work/Webdev/_bmad-output/brainstorming/brainstorming-session-2026-03-01-100819.md
  - /home/opsa/Work/Webdev/_bmad-output/design-thinking-2026-03-01.md
documentCounts:
  productBriefs: 0
  research: 0
  brainstorming: 1
  projectDocs: 1
  projectContext: 0
workflowType: 'prd'
classification:
  projectType: web_app
  domain: general
  complexity: medium
  projectContext: brownfield
---

# Product Requirements Document - Webdev

**Author:** Opsa
**Date:** 2026-03-01T12:31:50+05:30

## Executive Summary

This product is a personal web developer portfolio built as an explorer-first web application where projects are navigated through a Cosmic Archive orbit system instead of a linear project list. It is designed for recruiters, hiring managers, and senior engineers who need fast, credible evidence of execution quality, not only visual style. The portfolio solves two problems simultaneously: standing out in a crowded portfolio landscape and reducing evaluator effort to verify technical depth. The core interaction model is orbit-first navigation, where each project node opens a deterministic 10-second autonomous demo and then stops at a non-looping final state to present explicit next actions.

### What Makes This Special

The differentiator is a consistent proof architecture per project node: autonomous demo playback, final-state CTA hierarchy, and architecture snapshot access in a fixed pattern. This creates a repeatable evaluation workflow that is memorable without becoming ambiguous. The concept preserves novelty through the Cosmic Archive world model while keeping assessment friction low via explicit orientation and return paths (`Back to Orbit Map` primary, `View Architecture Snapshot` secondary). A site-wide ambient audio layer reinforces identity, but must always remain user-controlled through a visible mute toggle. The core insight is that hiring evaluators trust constrained, deterministic proof more than open-ended interaction theater.

## Project Classification

- Project Type: `web_app` (personal portfolio website with advanced interaction)
- Domain: `general` (developer showcase / hiring evaluation context)
- Complexity: `medium` (animation-rich interface, deterministic demos, strict performance and accessibility constraints)
- Project Context: `brownfield` (initial ideation and design artifacts already exist and are being operationalized into implementation-ready requirements)

## Success Criteria

### User Success

- First-time evaluators can understand the portfolio structure and open a project node within 15 seconds on desktop and within 20 seconds on mobile.
- Users can complete a full proof loop for at least one project (orbit node -> autonomous demo -> final-state CTA -> return to orbit map) without confusion or dead ends.
- At least 80% of test evaluators report that project capability is clear after exploring one node and one architecture snapshot.
- Audio and motion controls are discoverable and usable: users can mute ambient audio in one interaction and retain that preference during the session.

### Business Success

- Portfolio supports primary hiring outcome: increase qualified inbound interview conversations attributable to portfolio links within 90 days of launch.
- Recruiter and hiring-manager review efficiency improves: target median review time to identify top 2 projects under 2 minutes.
- The portfolio communicates differentiated brand positioning (Cosmic Archive + deterministic proof flow) while preserving professional credibility.

### Technical Success

- Interaction performance remains stable at target smoothness for core orbit interactions on modern desktop and mobile browsers.
- Core pages and node transitions meet defined web performance budgets for load and interaction responsiveness.
- Accessibility baseline is met for keyboard access, visible focus states, reduced-motion handling, contrast readability, and audio control discoverability.
- Autonomous demo playback is deterministic, non-looping, and consistently lands on a valid final state with CTA priority preserved.

### Measurable Outcomes

- 0 critical path dead-end navigation defects in acceptance testing.
- 100% of featured project nodes include both autonomous demo and architecture snapshot.
- 95%+ successful autonomous demo completions in cross-browser QA runs.
- 90+ Lighthouse Performance and Accessibility scores on core views in production-like builds.
- <2.5s LCP target on primary landing experience under defined test conditions.

## Product Scope

### MVP - Minimum Viable Product

- Cosmic Archive core experience shell with orbit-first navigation and project node entry.
- Three featured project nodes with standardized structure and metadata.
- Autonomous 10-second demos for featured nodes that stop on final frame (no loop).
- CTA hierarchy on demo final state:
  - Primary: `Back to Orbit Map`
  - Secondary: `View Architecture Snapshot`
- Architecture Snapshot view for each featured project.
- Site-wide ambient audio layer with persistent mute control.
- Mobile + desktop responsive behavior with performance and accessibility compliance.

### Growth Features (Post-MVP)

- Expanded constellation with additional project nodes and deeper project taxonomy.
- Audience-specific viewing modes (recruiter / hiring manager / engineer) with tailored emphasis.
- Compare mode for side-by-side project evaluation.
- Build-in-public timeline and decision-history artifacts per project.

### Vision (Future)

- Adaptive orbit behaviors informed by evaluator intent while keeping navigation clarity intact.
- Rich interactive technical deep dives beyond static architecture snapshots.
- Modular proof system that can scale to many projects without reducing evaluability.

## User Journeys

### Journey 1: Recruiter Fast Qualification (Primary Success Path)

Jordan (recruiter) opens the portfolio from a resume link between back-to-back calls and needs a fast capability read. The opening scene is the orbit map with clear project nodes and immediate orientation cues. Jordan selects one node, watches the 10-second autonomous demo, then lands on the final state with `Back to Orbit Map` as the primary action. Jordan taps `View Architecture Snapshot` only after the demo validates that this is real implementation work, not a visual mockup. Resolution: Jordan can quickly shortlist the candidate because the portfolio gives both novelty and low-friction evidence in under two minutes.

### Journey 2: Senior Engineer Deep Evaluation (Primary Edge Case)

Rina (senior frontend engineer) enters with skepticism about animation-heavy portfolios. She intentionally stress-tests clarity by using keyboard navigation, reduced-motion preference, and inspecting architecture rationale. During rising action, she checks whether the autonomous demo is deterministic and whether the final frame actually links to technical depth. The climax is the architecture snapshot where performance and accessibility tradeoffs are explicit. Resolution: Rina validates engineering judgment and moves from skepticism to interview interest because the experience remains coherent even under strict technical scrutiny.

### Journey 3: Hiring Manager Mobile Review (Secondary User)

Alex (hiring manager) reviews candidates on mobile during commute windows and has limited attention span. Opening scene: mobile orbit view renders quickly and remains legible without dense text overload. Alex opens a project node, views autonomous proof, then returns to orbit map without losing context. The emotional turning point is confidence that this candidate can scope, prioritize, and communicate decisions clearly. Resolution: Alex can compare projects efficiently on mobile and decide whether to move forward.

### Journey 4: Portfolio Owner Update and Quality Gate (Operations/Admin)

Opsa (portfolio owner) prepares to publish a new project node. The workflow begins with assembling the demo script, architecture snapshot, confidence/innovation labels, and accessibility/performance checks. Rising action includes validating that autoplay demo ends in a stable final state and that CTA order remains unchanged. The climax is pre-release verification across desktop and mobile with ambient audio mute behavior checked. Resolution: Opsa publishes updates without regressing core experience quality, keeping the portfolio trustworthy as it grows.

### Journey Requirements Summary

- Orbit-first navigation must preserve orientation during entry, deep dive, and return.
- Every featured node needs a deterministic autonomous demo and architecture snapshot pair.
- Final-state CTA ordering is invariant (`Back to Orbit Map` before `View Architecture Snapshot`).
- Mobile flows must retain parity with desktop on proof discoverability and return paths.
- Accessibility and control features (mute, keyboard support, reduced motion) are first-class journey requirements.
- Authoring and publish workflow requires a repeatable quality gate for new nodes.

## Domain-Specific Requirements

### Compliance & Regulatory

- Conform to WCAG 2.2 AA accessibility expectations for critical interaction paths.
- Provide user control for ambient audio (explicit mute, no hidden controls) and honor user comfort preferences.
- Preserve legal-safe portfolio representation: no misleading claims about project ownership, impact, or role.

### Technical Constraints

- Animation and media behavior must not compromise performance on mainstream mobile/desktop hardware.
- Reduced-motion and keyboard-navigation support are mandatory for orbit navigation, project access, and return flows.
- Autonomous demos must run deterministically and avoid reliance on fragile runtime state.

### Integration Requirements

- Project nodes require structured metadata for confidence/innovation signals, demo scripts, architecture snapshot content, and CTA targets.
- Asset pipeline must support optimized media delivery for demo segments, architecture visuals, and ambient audio.
- Analytics/events (if implemented) should capture journey progression without collecting sensitive personal data.

### Risk Mitigations

- Risk: style-over-substance perception.
  Mitigation: enforce per-node proof triad (demo + architecture + explicit tradeoff rationale).
- Risk: navigation disorientation in orbit metaphor.
  Mitigation: persistent orientation cues and guaranteed `Back to Orbit Map` primary path.
- Risk: performance regressions from cinematic interactions.
  Mitigation: enforce performance budgets and pre-release cross-device profiling.
- Risk: accessibility regressions during iteration.
  Mitigation: add accessibility checks to the publish quality gate for every node update.

## Innovation & Novel Patterns

### Detected Innovation Areas

- Orbit-first portfolio IA replaces conventional linear project grids with a navigable confidence/innovation constellation.
- Autonomous proof theater standardizes project demonstrations as deterministic 10-second non-interactive narratives.
- Final-frame decision model formalizes evaluator flow with explicit CTA ordering instead of ad-hoc project exits.
- Ambient audio continuity is treated as part of brand system design with mandatory user override.

### Market Context & Competitive Landscape

- Most developer portfolios optimize for static readability but under-deliver on memorable interaction systems.
- Highly animated portfolios often sacrifice evaluation clarity; this product differentiates by coupling novelty with explicit proof artifacts.
- Competitive advantage depends on proving that unconventional navigation can still reduce review friction for hiring stakeholders.

### Validation Approach

- Conduct moderated walkthroughs with recruiter, hiring-manager, and engineer profiles to test evaluability vs novelty.
- Validate that users can complete the intended proof loop without coaching and still understand technical depth.
- Compare baseline static portfolio comprehension vs orbit-first comprehension for orientation time and evidence recall.

### Risk Mitigation

- If orbit metaphor reduces clarity, provide stronger orientation aids and a direct quick-evidence entry path.
- If autonomous demos are perceived as too scripted, increase architecture context and explicit decision rationale at final state.
- If ambient audio causes drop-off, keep mute prominent and persist user preference aggressively.

## Web App Specific Requirements

### Project-Type Overview

The product is a browser-based interactive portfolio web application optimized for first-visit evaluation speed and technical credibility. Architecture decisions prioritize deterministic interaction flow, strong performance under animation load, and accessible controls across mobile and desktop.

### Technical Architecture Considerations

- Application model: client-rendered interactive shell with predictable route/state transitions for orbit map, node detail, demo state, and architecture snapshot.
- Rendering model must preserve smooth interaction while minimizing main-thread blocking from animation, media, and state updates.
- Data model must support node metadata, confidence/innovation labels, demo timeline definitions, and CTA routing priorities.

### Browser Matrix

- Supported: current and previous major versions of Chrome, Edge, Safari, and Firefox on desktop.
- Mobile support: current iOS Safari and Android Chrome.
- Degradation policy: if advanced effects are unavailable, preserve core proof loop and CTA behavior with reduced visual complexity.

### Responsive Design

- Orbit navigation and node exploration must remain legible and operable from 320px mobile widths to large desktop displays.
- Mobile interaction design must preserve quick evidence access and return-to-orbit orientation with touch-friendly controls.
- Content hierarchy adapts by viewport without changing proof order (demo then architecture access).

### Performance Targets

- Optimize landing and initial interaction readiness to avoid reviewer drop-off.
- Maintain smooth orbit interactions and transition consistency under normal device conditions.
- Enforce budgets for animation complexity, media payload size, and script execution cost.

### SEO Strategy

- Core portfolio pages must expose crawlable metadata for discoverability and link sharing.
- Project pages or deep links should include descriptive titles, summaries, and preview metadata.
- SEO optimization must not compromise primary interaction model or runtime performance budgets.

### Accessibility Level

- Target WCAG 2.2 AA across critical flows.
- Full keyboard operability for navigation, node selection, demo controls, and CTA traversal.
- Respect user `prefers-reduced-motion`; provide non-disruptive alternatives for cinematic effects.
- Ambient audio is opt-out controllable at all times, with clear visual state feedback.

### Implementation Considerations

- Use component-level contracts so each project node can be added without changing global navigation logic.
- Build deterministic demo orchestration with explicit start/end states and replay controls.
- Include automated checks for accessibility regressions and performance budget violations in pre-release validation.

## Project Scoping & Phased Development

### MVP Strategy & Philosophy

**MVP Approach:** Experience + proof-first MVP. The first release must prove distinct interaction design and technical credibility in one cohesive evaluator flow.

**Resource Requirements:**
- 1 frontend engineer/designer-owner (primary)
- 0.25 QA/accessibility support (part-time or checklist automation)
- Optional advisor feedback from one recruiter and one senior engineer during validation

### MVP Feature Set (Phase 1)

**Core User Journeys Supported:**
- Recruiter fast qualification
- Senior engineer deep evaluation
- Hiring manager mobile review
- Owner publish quality-gate workflow

**Must-Have Capabilities:**
- Orbit map shell and project node selection
- Autonomous 10-second non-looping demos
- Fixed final-state CTA priority (`Back to Orbit Map` -> `View Architecture Snapshot`)
- Architecture snapshot for each featured node
- Site-wide ambient audio with persistent mute control
- Performance + accessibility compliance on desktop and mobile

### Explicit MVP Non-Goals

- No user accounts, personalization, or recommendation engine
- No CMS/admin dashboard beyond lightweight authoring workflow
- No full case-study longform storytelling pages for every project at launch
- No advanced compare mode or audience-mode switching in MVP
- No experimental real-time behavior or adaptive orbit AI in MVP

### Post-MVP Features

**Phase 2 (Post-MVP):**
- More node coverage and expanded proof artifacts
- Audience mode presets (recruiter/manager/engineer)
- Compare mode and richer architecture drilldowns

**Phase 3 (Expansion):**
- Adaptive interaction personalization with strict clarity guardrails
- Advanced technical deep dives, richer observability, and shareable evaluator paths
- Scalable content model for larger project constellations

### Risk Mitigation Strategy

**Technical Risks:**
- Most difficult area: balancing cinematic interaction with deterministic behavior and performance budgets.
- Mitigation: strict animation/media budgets, deterministic demo controller, cross-device profiling.

**Market Risks:**
- Biggest risk: novelty being perceived as style without substance.
- Mitigation: enforce proof triad and fast path to architecture evidence in every node.

**Resource Risks:**
- Risk: solo development bandwidth constraints delay polish.
- Mitigation: constrain MVP to three high-quality nodes; defer non-goal features by design.

## Functional Requirements

### Experience Entry & Orientation

- FR1: First-time visitors can identify the portfolio's exploration model from the landing experience without external instructions.
- FR2: Visitors can understand what each orbit node represents before entering a project experience.
- FR3: Visitors can enter a project node from the orbit map in a single clear action.
- FR4: Visitors can always determine their current location in the portfolio journey.

### Orbit Navigation & Node Discovery

- FR5: Visitors can browse all featured project nodes from a central orbit map.
- FR6: Visitors can move from a selected project node back to the orbit map without losing orientation.
- FR7: Visitors can access project nodes in any order.
- FR8: Visitors can revisit previously viewed nodes during the same session.

### Autonomous Demo Presentation

- FR9: Visitors can trigger an autonomous project demo from each featured node.
- FR10: Each autonomous demo can complete without requiring visitor interaction.
- FR11: Each autonomous demo can end in a stable final state.
- FR12: Visitors can replay a completed autonomous demo.
- FR13: Visitors can access the primary post-demo action to return to the orbit map.
- FR14: Visitors can access a secondary post-demo action to view architecture details.

### Architecture Snapshot & Technical Proof

- FR15: Visitors can view an architecture snapshot for each featured project.
- FR16: Senior engineering evaluators can access explicit technical decision context for each featured project.
- FR17: Visitors can review project confidence and innovation signals for each node.
- FR18: Visitors can compare proof completeness across featured nodes.

### Accessibility & Comfort Controls

- FR19: Keyboard users can complete core navigation flows including node entry, demo access, and return to orbit.
- FR20: Motion-sensitive users can use the portfolio with reduced-motion behavior.
- FR21: Visitors can mute ambient audio from a persistent, visible control.
- FR22: Visitors can perceive the current audio state (muted/unmuted) at any point in the experience.
- FR23: Visitors can consume critical project information with accessible contrast and readable structure.

### Mobile and Desktop Parity

- FR24: Visitors can complete the full proof loop on both mobile and desktop devices.
- FR25: Hiring evaluators can access equivalent project evidence across supported browsers and devices.

### Portfolio Operations & Content Governance

- FR26: Portfolio owner can publish and maintain featured nodes using a repeatable node content structure.
- FR27: Portfolio owner can attach autonomous demo content and architecture snapshot content to each node.
- FR28: Portfolio owner can validate that CTA priority and proof structure are consistent across all featured nodes.

### Evaluator Efficiency & Evidence Retrieval

- FR29: Recruiters can reach a complete project proof sequence within 2 minutes.
- FR30: Hiring managers can identify top candidate projects from concise node-level evidence.
- FR31: Senior engineers can access technical proof artifacts without bypassing core navigation semantics.

### Reliability of Core Experience

- FR32: Visitors can complete critical journeys without dead-end states.
- FR33: Visitors can recover from interrupted deep-dive flows by returning to orbit map context.
- FR34: Portfolio owner can verify that core journeys remain intact after content updates.

## Non-Functional Requirements

### Performance

- NFR1: The landing experience must reach Largest Contentful Paint <= 2.5 seconds under defined production-like test conditions.
- NFR2: Core orbit interactions must sustain smooth visual responsiveness (target 60fps on supported desktop hardware, with graceful degradation on constrained devices).
- NFR3: Input-to-response latency for primary interactive controls (node select, CTA actions, mute toggle) must remain <= 100ms in normal conditions.
- NFR4: Autonomous demo startup must begin within 500ms of user trigger for cached assets on supported browsers.

### Accessibility

- NFR5: Critical user journeys must conform to WCAG 2.2 AA success criteria.
- NFR6: All interactive elements in core flows must be keyboard operable with visible focus indication.
- NFR7: Motion-intensive interactions must provide reduced-motion alternatives when user preference indicates reduced motion.
- NFR8: Ambient audio must always provide an immediately discoverable mute/unmute control with persistent visible state.

### Reliability

- NFR9: Critical proof-path routes (orbit map, node entry, demo playback, architecture snapshot, return to orbit) must achieve >= 99.5% successful navigation completion in production telemetry and test runs.
- NFR10: Autonomous demo timelines must terminate in valid final states with >= 95% completion success in cross-browser regression testing.
- NFR11: Release quality gates must block publication when critical journey regressions are detected.

### Security & Privacy

- NFR12: Site delivery must enforce HTTPS for all content and assets.
- NFR13: Any collected analytics must avoid storage of sensitive personal data and follow data-minimization principles.
- NFR14: Public project content must be attributable and auditable to prevent accidental publication of confidential materials.

### Compatibility

- NFR15: The MVP must support current and previous major versions of Chrome, Edge, Safari, and Firefox on desktop.
- NFR16: The MVP must support current iOS Safari and Android Chrome on mobile.
- NFR17: Unsupported features must fail gracefully without breaking core proof journeys.

## Acceptance Criteria

### MVP Acceptance Criteria

- AC1: Given a first-time visitor lands on the site, when they view the hero/orbit map, then they can identify at least one project node and enter it without external guidance.
- AC2: Given a visitor enters any featured project node, when they start the autonomous demo, then the demo runs for approximately 10 seconds and stops on a non-looping final frame.
- AC3: Given a demo reaches final frame, when CTA options render, then `Back to Orbit Map` is the first/primary action and `View Architecture Snapshot` is secondary.
- AC4: Given a visitor selects `Back to Orbit Map`, when navigation completes, then they return to the orbit map with orientation preserved.
- AC5: Given a visitor selects `View Architecture Snapshot`, when content loads, then they can view system-level technical proof for that project.
- AC6: Given ambient audio is enabled, when a visitor activates mute, then audio stops immediately and mute state remains visible.
- AC7: Given a keyboard-only user navigates the site, when traversing core flows, then orbit entry, demo access, CTA activation, and return are fully operable.
- AC8: Given reduced-motion preference is enabled at system/browser level, when the site is used, then motion-intensive effects are reduced while core flows remain functional.
- AC9: Given the site is tested on supported mobile and desktop browsers, when executing the core proof loop, then the flow succeeds without blocking defects.
- AC10: Given each MVP project node is published, when reviewed, then it includes all required proof artifacts: autonomous demo and architecture snapshot.

## Consolidated Risks

### Risk Register

- Risk: Evaluators perceive the experience as visual novelty with weak proof.
  Impact: High
  Mitigation: Enforce mandatory per-node proof triad and explicit technical rationale.
- Risk: Orbit interaction creates navigation confusion for first-time users.
  Impact: High
  Mitigation: Maintain persistent orientation cues and guaranteed primary return path.
- Risk: Animation/media workload causes poor performance on mid-range devices.
  Impact: High
  Mitigation: Apply performance budgets, optimize assets, and gate release on profiling checks.
- Risk: Accessibility regressions emerge as interactions evolve.
  Impact: High
  Mitigation: Run accessibility checks in every release gate and retain keyboard/reduced-motion acceptance tests.
- Risk: Solo-resource constraints delay delivery and reduce quality.
  Impact: Medium
  Mitigation: Keep MVP to three high-quality nodes; defer explicitly out-of-scope features.
