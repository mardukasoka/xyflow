# Atlas temporal ontology v0.1

A diagram, phenomenon, claim, observation, and scientific model are distinct entities. They can be related without sharing a single timestamp.

## Temporal coordinates (never collapse these into one field)

- `physical_validity`: epoch or interval during which a phenomenon existed, conditional on the physical model; often unbounded or unknown. A fundamental particle is not assigned a discovery date as its date of origin.
- `process_duration`: characteristic elapsed time for a physical process, with units, range and uncertainty.
- `cosmic_event_time`: cosmic age at occurrence, conditional on cosmological parameters.
- `lookback_time`: elapsed time between observation epoch and emission/event epoch, conditional on cosmology.
- `observation_time`: date/time and time standard of the instrument measurement.
- `prediction_time`: date a specific theoretical claim was proposed.
- `discovery_time`: dated discovery event, credited to a source and discovery criteria.
- `acceptance_interval`: historically situated acceptance by a specified scientific community, never a timeless binary property.
- `interpretation_interval`: period in which a named interpretation/model was proposed, evaluated or used.
- `publication_time`: publication date of an image or source.
- `simulation_time`: internal simulated time coordinate, with explicit mapping to physical time if any.

## Spatial / observational coordinates

- `position`: coordinate frame, origin, epoch, units, uncertainty, and reference.
- `distance_kind`: e.g. parallax/geometric, luminosity, angular-diameter, comoving, proper-at-emission, proper-now, light-travel distance.
- `redshift`: measured spectroscopic or photometric redshift, uncertainty and measurement method.
- `emission_epoch`: cosmic time/redshift of photons observed today, under a specified cosmology.
- `observation_epoch`: instrument epoch (e.g. UTC/TDB) and observatory.
- `cosmology`: parameter set, units and model version; required for redshift-to-distance/lookback conversions.

## Epistemic states

Observation, prediction, hypothesis, interpretation, model, derived claim, formal theorem, consensus assessment, and historical account are different types. A claim may be supported by multiple observations and disputed by competing interpretations. Acceptance is contextual to date and community.

## Example: electron (illustrative, not ingested data)

Phenomenon: electron (physical entity, no 'discovered in' existence timestamp).
Discovery event: electron identification in 1897, linked to historical evidence.
Theory: quantum electrodynamics, developed later.
Interpretations: multiple quantum interpretations may address measurement; none is encoded as the electron's singular 'accepted form'.
Characteristic scale: context-specific (e.g. scattering, Compton wavelength), not a fixed classical radius.

## Example: distant galaxy

Object: galaxy with ICRS position and coordinate epoch.
Observation: instrument, observation date, filter, angular position, redshift estimate and uncertainty.
Emission: redshift-inferred cosmic epoch.
Distances: comoving, luminosity and proper-at-emission are separate quantities; no silent substitutions.
Discovery: first published detection and subsequent confirmation may be separate events.

## Diagram placement

Each asset can have many `placements`:
- `scale_view`: based on a measured quantity, with unit and source.
- `cosmic_timeline`: based on physical event/emission epoch.
- `discovery_timeline`: based on human historical event.
- `interpretation_timeline`: based on claims and scientific community.
- `observation_view`: instrument, survey footprint and coordinate frame.
- `concept_graph`: typed conceptual links.

No source-backed placement is inferred solely from appearance or a diagram caption. Unknown is a valid state.
