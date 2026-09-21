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

## Use by Decision Makers

The technical director would open the dashboard during squad planning, filtered by contract expiry and position, to see which players are entering or leaving their window. Club leadership and finance would compare development spend against projected value to judge the return on the academy. Academy coaches would use the same player view to see which players justify continued investment. The dashboard supports those conversations rather than replacing the judgment of the people in them.

## Connection to Chapter 7

This idea sits in the prototyping phase and is moving into engagement. The concept is defined, the intended user is named, and the decisions it supports are specific, but nothing has been built and no recommendation has been tested against a real outcome at Rayon Sports.
## References

Alamar, B. C. (2024). *Sports analytics: A guide for coaches, managers, and other decision makers*. Columbia University Press.
