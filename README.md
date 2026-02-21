# MindColumn_backend_crm_db_PROCviews_public
MindColumn db convenient views for best practices and standardized PROCedures, which are made public under permissive license

Here are the invented — since _"everything comes out of nothing" ~Tao Te Ching_, 400BC. — and then standardized views and checks. As a curiosity, some vendors like _SAS_ also uses denominations similar to those in this repo.

The whole _distribution of responsibilities_ is not closed, some things may change but **loads of things** are working right now.

Following is the current brief. *`wf-`* means _workforce_:

## Profile Top-down Strategy related
##### Main tables
`SM_overbooking`\
`SM_purview`\
`SM_strat`\
`SM_strat_level_info`
#### _STRAT_ extended views

_PROC-INFO_: `wf-AA1?-AA12-AA14-AA17-PURVIEW[-N]`\
_TABLE_: `SM_purview` _explained with_: `SM_strat`, `profileKeywords`, `page`\
_connected with_: `SM_channel`\
**same length**\
_filtered by:_ root, critic / root / all / leaf\
_TECHNICAL STATUS_: __WORKING 100%. Seems optimized but not thorough analysis__

_PROC-INFO_: `wf-AA21-AA22-SM_STRAT_FIXation`\
_TABLE_: `SM_strat`\
_explained with_: `Purview_FIXED`: `count(SM_channel)>0`\
_inferred from_: `SM_purview`\
**same length**\
_duplicated by:_ union no editable / editable\
_TECHNICAL STATUS_: __WORKING 100%. Two different, trivial implementations for convenience__

_PROC-INFO_: `wf-PN11-SMPROFILE_explain`\
_TABLE_: `profile` _multiplied by_: **3x**`SM_strat` (3 potential uses each, plus modifications and **semantic** filters applied to **`implicationType`**) , _explained with_:`profileKeywords`\
_calculated fields_: `pRealm`, `implicationType`\
**cartesian product with posible cases, plus applied filter length**
  - [x] Semantic _LOGIC (no data...)_ reviewed against `legacy Excel and Publisher data` _ID flow scheme_ (up to 2026-02-21Z)

_TECHNICAL STATUS_: __WORKING 100%. Relatively complex logic made easy but not thorough analysis__\
*Realm logic:* secret as the Coca-Cola formula

_PROC-INFO_: `wf-PN17-OVERBOOKING`\
_TABLE_: `SM_overbooking` _explained with_: `SM_strat`, `profileKeywords` and *`overall deployment`*\
**same length**\
_ordered by:_ grip (Bridgestone's ways)
## Auto Dynamics related
Ongoing effort\
_TECHNICAL STATUS_: __Too old to know, to review, IDK__
## Full Review
Ongoing effort\
_TECHNICAL STATUS_: __WORKING 100%, but weird implementation based on frames, FULL refactor needed, only for reference__
## Publishing
Ongoing effort\
_TECHNICAL STATUS_: __STABLE, trivial implementation__
## Account
Ongoing effort & studying accounting for this\
_TECHNICAL STATUS_: __STABLE, MINOR Changes needed till today__
