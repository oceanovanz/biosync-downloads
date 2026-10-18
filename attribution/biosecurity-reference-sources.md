# NZ marine biosecurity target preset

Version 2026-10-15.4, sources checked 15 October 2026. This is a 13-taxon community surveillance preset, not an exhaustive invasive-species list, legal register, live distribution layer or validated classifier.

The Marine Biosecurity Porthole overview identifies 11 priority pests, including targets not known in NZ; MPI separately identifies the two exotic caulerpa species. Presence labels are dated summaries of these sources, never evidence from this application:

- https://marinebiosecurity.org.nz/what-are-marine-pests
- https://www.mpi.govt.nz/biosecurity/exotic-pests-and-diseases-in-new-zealand/long-term-biosecurity-management-programmes/exotic-caulerpa-seaweeds/exotic-caulerpa-in-new-zealand-where-it-is-and-the-work-underway
- https://www.marinespecies.org/aphia.php?p=webservice

Taxa absent from the occurrence-derived reference library are added as surveillance targets with zero occurrence records. No model sighting is created by installing the list. Scientific/common aliases are retained, including Musculista/Arcuatula senhousia and Charybdis japonica / Charybdis (Charybdis) japonica.

## Reference photographs

Nine additional global community photographs fill existing gaps. Four other target taxa already have photographs in assets/reference/images.json. All 13 targets therefore have at least one indexed example. One photograph is limited coverage, not species validation. Photograph licences are checked individually; original downloaded bytes, author credit, source URL, SHA-256 and model-versioned vectors are in nz-marine-targets.json. These photographs are separate assets under their own licences.

- (c) André Ambrozio, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/742058031 (observation: https://www.inaturalist.org/observations/404105603).
- (c) Letizia Weichgrebe, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/750384989 (observation: https://www.inaturalist.org/observations/408240954).
- (c) Ross McCallum, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/747342945 (observation: https://www.inaturalist.org/observations/406740476).
- (c) Seth Marshall, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/683020646 (observation: https://www.inaturalist.org/observations/373724908).
- (c) Robin White, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/616321148 (observation: https://www.inaturalist.org/observations/338860352).
- (c) Javier, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/728801523 (observation: https://www.inaturalist.org/observations/397362811).
- (c) Jiro Iguchi, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/733784489 (observation: https://www.inaturalist.org/observations/399918479).
- (c) Shaun Lee, some rights reserved (CC BY) — cc-by — https://www.inaturalist.org/photos/355152263 (observation: https://www.inaturalist.org/observations/201213707).
- no rights reserved — cc0 — https://www.inaturalist.org/photos/660882655 (observation: https://www.inaturalist.org/observations/362109940).

The preview image uses the Caulerpa brachypus reference credited above. Licence versions are as specified at each linked photograph, not inferred from the API's abbreviated code. Community identifications are not independently verified underwater ground truth.

## Propagation and review

On first updated launch, the pack merges into the local watchlist without deleting custom entries or re-enabling disabled entries. Explicit removal/clearing remains respected. Library → NZ pests filters the 13 targets; Add NZ pest targets adds them to active inference priorities atomically within the 16-target limit. Existing targets are never silently removed. Apply targets / reanalyse begins a new pass.

Only an exact explicit identity/common alias or scientific-name suggestion triggers a suspected flag. A retrieved reference candidate or generic crab/seaweed label alone does not. Review confirmation, correction and rejection update flags in the video overlay, catalogue, existing map markers and observation CSV/GeoJSON exports. Confirmation is an attributed local review, not official agency confirmation. Rejected and corrected native identities clear the flag. Exotic caulerpa group suggestions remain unresolved at species level where appropriate.

The JSON preset and nine images ship in the desktop source archive for offline distribution; NZ-Marine-Invasive-Targets.csv is a standalone human-readable list. No reports, sightings or locations are transmitted automatically. Updates require refreshed, checked source metadata and a version change.
