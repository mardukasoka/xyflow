# Atlas Axiom Space — working specification v0.1

## Purpose
The user's reference diagrams are **entry points into a unified knowledge graph**, not axioms by default. Their claims must be extracted, attributed, tested, and mapped to typed relationships before promotion to validated knowledge. Historical and disputed diagrams remain valuable evidence of epistemic development.

## Core distinctions
- **Axiom**: an explicitly declared starting assumption within a named formal system, with scope and consequences. Not a synonym for universally proven truth.
- **Definition**: a convention specifying a term, unit, coordinate frame, or object.
- **Observation**: an instrument- or source-bound measurement with uncertainty and epoch.
- **Model**: a representation that makes predictions under assumptions.
- **Theorem/derived claim**: a statement with derivation or proof in a specified system.
- **Hypothesis**: a falsifiable or otherwise testable proposal, not yet confirmed.
- **Historical claim**: a dated assertion, potentially superseded.
- **Visualization**: an authored depiction of one or more claims; not automatically a primary source.

## Typed relations
`is_a`, `part_of`, `subset_of`, `derived_from`, `measured_by`, `depicts`, `supports`, `contradicts`, `depends_on`, `transforms_to`, `evolved_from`, `located_in`, `contemporary_with`, `implemented_by`.

Never conflate `subset_of` with `part_of`, genealogy with similarity, or correlation with causation.

## Axes and reference frames
1. **Scale:** radius_m, mass_kg, energy_eV, frequency_Hz, temperature_K, pressure_Pa, magnetic_field_T, time_s; units and uncertainties mandatory where numerical.
2. **Time:** cosmic age, lookback time, redshift (cosmology-dependent), geological Ma, historical calendar date, discovery/observation date; no silent conversions.
3. **Space:** ICRS/equatorial, galactic, supergalactic, ecliptic, heliocentric and geocentric; frame, origin, epoch, projection, handedness, units mandatory.
4. **Classification:** mathematics, fundamental particles, nuclides, matter phases, astronomical bodies, biology, archaeology, language, human knowledge.
5. **Epistemology:** observation, inference, simulation, formal proof, speculation, historiography, uncertainty and provenance.
6. **Agency:** project, task, agent, workflow, tool, artifact, test, deployment, approval.

## Image ingestion pipeline
`ImageAsset -> SourceAttribution -> DiagramType -> ClaimExtraction -> EntityResolution -> Unit/Frame Validation -> EvidenceReview -> KnowledgeGraph -> AtlasViews`.

Keep original image bytes/hash and licensing separately from extracted claims. No automated claim becomes validated merely by appearing in a diagram.

## Initial image clusters
- Number systems, mathematical history, logic, control theory
- Standard Model, quark/hadron spectra, nucleosynthesis
- Electromagnetic, acoustic, seismic, gravitational-wave frequency scales
- Phase diagrams, magnetism, stellar HR diagrams
- Solar System object sizes, spacecraft encounters
- Galactic and supergalactic maps and survey footprints
- Cosmological eras and logarithmic timescales
- Evolutionary phylogenies and human origins
- Historical chronology, writing systems, linguistic spatial relations
- Archaeological earthquake evidence

## Progress model
Each project milestone has `weight`, `state`, `acceptance_criteria`, `evidence_refs`, `verified_by`, and `verified_at`. Parent completion = sum of verified milestone weights / sum of all milestone weights. Unknown or unverified is not complete. User-visible status is separate from percentage.

## Near-term implementation sequence
1. Build and browser-test project tracker and radial graph.
2. Create durable project inventory and milestone acceptance evidence.
3. Create image asset manifest and attribution workflow.
4. Extract first 10 diagrams into typed claims with manual review.
5. Build scale/time/space projections from one canonical graph.
6. Add authorized agent execution only after audit, rollback and containment are verified.

## Boundaries
No production repo changes, automated merges, API key use, agent autonomy or deployment are authorized by this document. This branch is an isolated prototype. Local browser edits are not synchronized across devices.
