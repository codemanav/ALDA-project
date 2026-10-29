# ALDA Soccer Analytics

Fall 2024 project for analyzing European soccer data with exploratory data
analysis, match-outcome prediction, and data-driven transfer recommendations.

## Overview

The project combines match, player, team, league, and country information to
answer three questions:

1. What patterns can be found in team, player, league, and match performance?
2. Can historical team and match attributes be used to predict match outcomes?
3. Which players could address a team's weaknesses and become transfer
   candidates?

The repository is the complete course submission, including the proposal,
midway work, presentation, final report, source notebooks, and prepared
datasets.

## Data model

The analysis uses the following related tables from the European Soccer
Database:

- `Country` - country identifiers and names.
- `League` - league identifiers, names, and country relationships.
- `Match` - match dates, seasons, teams, scores, and betting odds.
- `Player` - player identity and physical attributes.
- `Player_Attributes` - dated player ratings, skills, work rates, and
  goalkeeping attributes.
- `Team` - team identity and names.
- `Team_Attributes` - dated tactical and team-style attributes.

The complete column inventory is documented in [`columns.txt`](./columns.txt).
The final codebase also includes prepared team-to-league and country mapping
files.

## Analysis workflow

The project follows this general workflow:

1. Inspect and clean the source tables.
2. Explore distributions and relationships among players, teams, leagues, and
   matches.
3. Build features from historical team and match data.
4. Evaluate match-outcome predictions.
5. Analyze player performance and team needs.
6. Rank potential transfer candidates.
7. Summarize findings in the final report and presentation.

## Repository structure

### `1_project_proposal/`

Initial project proposal, submission materials, and LaTeX source.

### `2_midway/`

Midway exploratory analysis, early prediction notebooks, report, figures, and
submission materials.

### `3_project_presentation/`

Final presentation files and the transfer-candidate table used in the
presentation.

### `4_final_report/`

Final written report and its supporting LaTeX source, figures, and references.

### `5_final_codebase/`

The final analysis notebooks and prepared CSV datasets. This is the best place
to start when reproducing or reviewing the completed analysis.

## Final notebooks

The notebooks in `5_final_codebase/` serve different stages of the analysis:

- `columns.ipynb` - Inspects the source-table schemas.
- `Matches_eda.ipynb` - Explores match, league, season, and scoring data.
- `Teams_eda.ipynb` - Explores teams and team attributes.
- `players_eda.ipynb` - Explores player attributes and player performance.
- `match_outcome_prediction.ipynb` - Builds and evaluates match-outcome
  predictions.
- `Transfer_prediction.ipynb` - Identifies and ranks potential transfer
  candidates.
- `alda-project.ipynb` - Consolidated project analysis notebook.

## Reviewing the project

For a quick overview, read the final report:

[`4_final_report/P28_Soccer_Sage.pdf`](./4_final_report/P28_Soccer_Sage.pdf)

For the original scope and methodology, review:

- [`1_project_proposal/Project_Proposal.pdf`](./1_project_proposal/Project_Proposal.pdf)
- [`2_midway/Midway_report.pdf`](./2_midway/Midway_report.pdf)
- [`3_project_presentation/Nov20_3_P28_Soccer.pdf`](./3_project_presentation/Nov20_3_P28_Soccer.pdf)

For implementation details, open the notebooks in
[`5_final_codebase/`](./5_final_codebase/).

## Running the notebooks

The analysis is implemented as Jupyter notebooks. To review it locally:

1. Clone this repository.
2. Install Jupyter and the Python libraries imported by the notebook you want
   to run.
3. Open a notebook from `5_final_codebase/`.
4. Run the cells in order and confirm that the expected source data is
   available in the notebook's working directory.

The committed CSV files can be used directly for the final mapping and
prepared-data portions of the analysis. Some exploratory notebooks reference
the original relational soccer database, which may need to be supplied
separately because it is not included in this repository.

## Outputs

Project outputs include:

- Exploratory plots and descriptive analysis.
- Match-outcome prediction experiments.
- Player and team performance summaries.
- Transfer-candidate rankings.
- Midway and final written reports.
- A final project presentation.

## Historical context

This repository was originally developed as team project P28 for the Fall
2024 ALDA course. The Git history preserves the progression from proposal and
midway analysis through the final report and codebase.

## License

See [`LICENSE`](./LICENSE).
