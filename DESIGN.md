# Supermarket — source-based design brief

Proposal 8. Source reviewed 2026-09-30: [Program Descriptions](http://daviddfriedman.com/Living_Paper/Program_Descriptions/program_descriptions.htm) and [Living Paper index](http://daviddfriedman.com/Living_Paper/living_paper.htm).

**This is the source-based design brief.** Eric selected the v1 scope on 2026-10-02; implemented decisions are in [SPECIFICATION.md](SPECIFICATION.md). The prototype is frozen for David's review.

## Learning objective

Explore queue equilibria, negative feedback, search costs, and imperfect information.

## Confirmed mechanics in the source

- The baseline simulation shows shoppers moving from cart sources to checkout lanes, waiting, checking out, and leaving. Carts carry different numbers of items.
- The described checkout duration is the number of items plus three time units. A lane meter exposes estimated waiting time to the student, while shopper decisions depend on their available information.
- Total arrivals depend on grocery demand and generalized cost: the monetary price plus waiting and search costs. Moving or adding cart sources changes arrival locations rather than total demand.
- The baseline shopper compares two nearby lanes. Additional described strategies inspect item counts or search more lanes, accounting for the time spent gathering information and moving.
- Display average total exit time separately for searching and non-searching shoppers; searching time includes both search and queue time.
- Express lanes restrict eligible item counts. The source separately describes rational search, in which the mix and depth of search respond to observed payoffs.

## Optional variants and adaptation notes

- Select among fixed search strategies, express lanes, and endogenous rational search when defining scope.
- A manager game adds costs and profit scoring, lets the player set price, and makes demand and shopper behavior constraints rather than player-controlled strategies. Mirrors can reduce shopper search costs.

## Original design questions

Resolved for the review prototype in SPECIFICATION.md: exploratory simulation, fixed arrivals as an explicit departure, paired seeded comparisons, and equivalent tables. David can revisit these decisions in review.

1. Should the first release be an exploratory simulation or a profit-maximizing manager game?
2. Which arrival, item-count, lane-service, and search-time assumptions should be retained?
3. What textual and tabular views will explain animated queues without requiring students to track motion?
4. Which random outcomes should be held fixed when comparing policies?

## Source and accessibility constraints

The index links an older Supermarket source archive; its contents and runtime have not been inspected. [Legacy archive link](http://daviddfriedman.com/Living_Paper/Supermarket.sit); recorded from the index, not inspected.

Write fresh browser code by default; follow source-use notes (in the authoring collection) before any reuse. Keep keyboard and single-pointer alternatives for drawing/dragging, labeled numeric data and text/table equivalents for visual output, and verified focus/reflow behavior. These adaptation requirements do not imply that the original desktop UI meets current accessibility standards.

## Next task

Collect David's review of the frozen prototype through Eric; fold in feedback before the release audit.

SPECIFICATION.md records the chosen model, controls, timing, randomness, accessibility design, and acceptance scenarios. Source-described generalized-cost demand, manager gameplay, and adaptive search are explicitly deferred.
