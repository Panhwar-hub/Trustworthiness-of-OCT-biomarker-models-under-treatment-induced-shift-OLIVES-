# OLIVES data audit: auto summary

Generated 2026-10-24 from `/Users/parvezali/Research Proposal/OLIVES`.

## Counts: expected vs found

| index | expected | found |
| --- | --- | --- |
| patients | 87 | 96 |
| eyes | 96 | 190 |
| PRIME eyes | 40 | 79 |
| TREX eyes | 56 | 111 |
| volumes | 1,268 (paper) / 1,590 (MIRAGE) | 3119 |
| B-scans | 78,108-78,822 (sources disagree) | 159281 |

## Per trial

| study | patients | eyes | volumes | bscans |
| --- | --- | --- | --- | --- |
| PRIME | 40 | 79 | 1284 | 65520 |
| TREX | 56 | 111 | 1835 | 93761 |
| ALL | 96 | 190 | 3119 | 159281 |

## Visits per eye

| study | count | mean | std | min | 25% | 50% | 75% | max |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| PRIME | 79.0 | 16.3 | 4.9 | 3.0 | 14.0 | 19.0 | 20.0 | 21.0 |
| TREX | 111.0 | 16.5 | 6.3 | 3.0 | 12.0 | 16.0 | 22.0 | 27.0 |

## Label files

- Biomarker file: `/Users/parvezali/Research Proposal/OLIVES_Dataset_Labels/ml_centric_labels/Biomarker_Clinical_Data_Images.csv`
- Clinical file: `None`

## Study biomarkers: prevalence first vs last visit (all eyes)

| biomarker | study_role | pct_scans_first | pct_scans_last | change_pp_scans | pos_eyes_first | pos_eyes_last | usable |
| --- | --- | --- | --- | --- | --- | --- | --- |
| Fluid (IRF) | treatment-responsive | 58.0 | 28.9 | -29.0 | 92.0 | 82.0 | True |
| DRT/ME | treatment-responsive | 47.9 | 15.9 | -32.0 | 70.0 | 44.0 | True |
| IR HRF | treatment-responsive | 77.1 | 57.7 | -19.4 | 96.0 | 96.0 | True |
| Fully attached vitreous face | control | 57.5 | 53.5 | -4.0 | 69.0 | 65.0 | True |
| Partially attached vitreous face | control | 32.3 | 31.2 | -1.2 | 57.0 | 53.0 | True |

## Flags

| check | detail | count |
| --- | --- | --- |
| folder layout | image files outside the trial/patient/visit/eye layout | 1800.0 |
| counts | patients: expected 87, found 96 |  |
| counts | eyes: expected 96, found 190 |  |
| counts | PRIME eyes: expected 40, found 79 |  |
| counts | TREX eyes: expected 56, found 111 |  |
| scans per volume | volumes without exactly 49 B-scans | 3118.0 |
| scans per volume | volumes with missing or duplicated scan numbers | 3118.0 |
| labels | clinical label file not found under the project folder |  |
| biomarker labels | empty entries: {'Partially attached vitreous face': 6, 'Fully attached vitreous face': 3, 'Preretinal tissue/hemorrhage': 2, 'Vitreous debris': 8} | 19.0 |
| label-image match | eyes on disk with no biomarker labels: ['PRIME|01-001|OD', 'PRIME|01-002|OS', 'PRIME|01-012|OS', 'PRIME|01-013|OS', 'PRIME|01-014|OD', 'PRIME|01-020|OD', 'PRIME|01-023|OS', 'PRIME|01-025|OS', 'PRIME|01-026|OS', 'PRIME|01-027|OD'] | 94.0 |
| duplicate volumes | 187 sets of identical volumes (183 span different eyes) | 374.0 |
| image properties | more than one image size: ['504x496', '768x768'] |  |
| image properties | more than one colour mode: ['L', 'RGB'] |  |
