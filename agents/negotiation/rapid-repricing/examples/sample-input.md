# Sample input — Rapid Repricing

## Baseline

- SKU family **HVAC-FILTERS** annual baseline spend **$3.2M**
- List price with **15/10/7** volume tiers at 80k/250k/500k annual units
- Current forecast: **420k units** (up from 380k)

## Proposed supplier move

- Increase list **2.0%** but add **new tier at 450k** with extra **2%** discount

## Add-ons

- Freight: **$0.18/unit** baseline; proposed **$0.195** if diesel index > threshold (trigger true this month)

## Finance rules

- Compare on **TTC excluding VAT**; rounding to 4 decimals internally, 2 for display
