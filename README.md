# Autoringen/Sharebox Process

This repository documents the Autoringen/Sharebox workflow for managing used cars, designed to handle up to 1,200 cars per year with a 4-day service-level agreement (SLA, excluding weekends). The process integrates an ERP system with Sharebox (SB) for secure key management, streamlining registration, delivery, preparation, and auction. Below are three visualizations of the process and space requirements, created with Mermaid for clarity and stakeholder review.

## 1. Timeline (9-Day Process from Drop-Off to Pick-Up)

This Gantt chart shows the timeline from car drop-off (Day 0) to pick-up or return (up to Day 9), including preparation (4-day SLA) and buffers for auctions or retries.

```mermaid
gantt
    title Autoringen/Sharebox Timeline (9 Days)
    dateFormat  YYYY-MM-DD
    axisFormat  Day %e
    section Process
    Drop-Off (Received)      :done, d0, 2025-10-01, 1d
    Clean (Waiting for Photo):done, d1, after d0, 1d
    Photo (Waiting for Test) :done, d2, after d1, 2d
    Test (Ready for Sale)    :done, d3, after d2, 1d
    Auction (Wait to Sell)   :done, d4, after d3, 3d
    Pick-Up/Return           :done, d7, after d4, 3d
