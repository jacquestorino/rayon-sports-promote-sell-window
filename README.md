# Promote and Sell Window Dashboard
### Rayon Sports FC, Rwanda Premier League

A soccer analytics project documented by a Junior Analytics Associate.

## Project Overview

This project proposes a dashboard for Rayon Sports FC, a Rwanda Premier League soccer club, that identifies a promote and sell window for each academy and fringe first team player. The window is the period when a player's value to the squad and the player's market value are both near their peak. For every player the dashboard shows a projected value curve, the development cost invested to date, and a recommended action of develop, promote, retain, or sell. The technical director would use it during squad planning.

## Decision-Making Problem

Rayon Sports invests roughly $55,000 per player across a full academy cycle, which is a meaningful share of the club's annual budget. The club has to decide who to keep developing, who to promote into the first team, who to retain, and who to sell while the player still carries market value in regional and European feeder markets. Those decisions are currently made from scout opinion, coach memory, and separate spreadsheets held by different departments. Acting too early gives away a player before the club recovers its investment. Acting too late means selling a player whose value has already fallen, or losing him at the end of a contract for nothing.

## Proposed Analytics Approach

The analysis would draw on match and training data from the Rwanda Premier League and academy fixtures (minutes, position, performance per 90, availability and injury days), player age and contract length, development spend per player, age curves built from comparable East African players, and transfer comparables for players who have moved from the region to North Africa, the Gulf, or Europe.

Performance measures would be adjusted for age and level of competition, then combined into a projected value curve for each player. The window is flagged where the projected curve peaks relative to contract expiry. The approach would be checked against players Rayon Sports has already sold or released, to see whether the model would have flagged the right window at the time. No implementation is required at this stage.

## Prototype Enhancement

**What is being changed.** The original design reports one projected valuation per player. This enhancement replaces that single number with three scenarios, a base case, a low case, and a high case, built on different assumptions about performance trajectory and market demand. It also adds a short sensitivity view showing which inputs move the window the most.

**Why this change could improve decision-making.** Projected valuations depend heavily on assumptions that can shift within a single season, and transfer demand for Rwandan players is thin enough that one or two deals can move the market. A single point estimate hides that risk and makes a recommendation look more certain than it is. With three scenarios, leadership can ask whether the recommended commercial action still holds if a player's form dips or the market cools. That turns the dashboard from a forecast into a decision tool, and it directly answers a question raised in project review.

## Use by Decision Makers

The technical director would open the dashboard during squad planning, filtered by contract expiry and position, to see which players are entering or leaving their window. Club leadership and finance would compare development spend against projected value to judge the return on the academy. Academy coaches would use the same player view to see which players justify continued investment. The dashboard supports those conversations rather than replacing the judgment of the people in them.

## Connection to Chapter 7

This idea sits in the prototyping phase and is moving into engagement. The concept is defined, the intended user is named, and the decisions it supports are specific, but nothing has been built and no recommendation has been tested against a real outcome at Rayon Sports.

## Prototype Evaluation

**Should the prototype enhancement be integrated?** Yes. The scenario view uses inputs the model already relies on, it does not change the underlying method, and it makes the uncertainty visible instead of hiding it. It is the change most likely to build leadership confidence in the recommendations.

**What feedback from decision makers would influence this decision?** Reviewer feedback has already pointed to two conditions. First, the dashboard needs a way to validate that recommended windows actually improve outcomes. That means logging each recommendation and then tracking it against actual player performance, transfer activity, and financial results over a set period, so the tool can report its own hit rate back to club leadership. Second, the scenario view only helps if the technical director finds three numbers usable in a planning meeting rather than confusing. If leadership asks for a single figure to act on, the presentation needs to lead with the base case and keep the range one click away. The reliability of transfer comparables would also have to be confirmed, since the number of recorded deals out of the Rwanda Premier League is small.

## Reflection on Innovation and Version Control

**How branches support low-risk experimentation.** A branch lets an analyst change a metric definition, add a data source, or rework how results are presented without touching the version the club is using. The experiment sits beside the working product instead of on top of it. If it does not hold up, the branch is abandoned and nothing is lost. That lowers the cost of being wrong, which is what makes experimentation possible in an organization that cannot afford broken reporting in the middle of a season.

**How GitHub helps analytics ideas gain traction.** Most analytics ideas fail for reasons that have little to do with the math. They fail because the reasoning was never written down, because decision makers saw the idea too late, or because no one could tell what changed between versions. A repository addresses much of that. The README states the decision the idea serves in plain language, commit messages record why each change was made, and a pull request gives decision makers a place to review and respond before anything is adopted.

**How this workflow aligns with the innovation framework in Chapter 7.** The four phases map onto the tools closely. The creative phase is the README written on the main branch. Prototyping is the separate branch. Engagement is the review that happens before the merge, including the evaluation section written in response to reviewer questions. Build is the merge itself, which makes the enhancement part of the shared project. Version control does not create innovation, but it gives the cycle a structure and a record, which is what helps an idea survive long enough to be implemented.

## References

Alamar, B. C. (2024). *Sports analytics: A guide for coaches, managers, and other decision makers*. Columbia University Press.
