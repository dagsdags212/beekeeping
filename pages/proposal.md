---
kernelspec:
  name: python3
  display_name: 'Python 3'
---
```{code-cell} python
---
tags: [remove-input]
---
import polars as pl
import numpy as np
import altair as alt
from IPython.display import display, Markdown
```
# 5-Year Business Plan

## Summary of Objectives

- multiply hive count and honey yield for the first 5 years
- gradually introduce value-added products from other bee products
- optimize protocols for monitoring, biosafety, and processing
- incrementally build brand presence and prepare permits needed for export
- recruit and train staff for service-based offerings (pollination, queen rearing)

## Year 1: Foundation and Focus on Honey Production

:::{hint} Goal
Build stable operations, establish brand, and learn local market.
:::

### Hive management

- start with 5 _Apis mellifera_ hives
- aim for ~20 kg honey yield per hive/year
- develop SOPs for hive management practices that focus on colony health:
  - supplemental feeding
  - monitoring
  - mite management
  - forage planning
- develop tracing strategy
  - establish database for keeping track of hive data
  - brainstorm strategies for improving (remote) monitoring

### Products

- raw honey (bottled)
- beeswax to be sold as blocks or starter candles
  - can be stored long-term

### Sales and Marketing

- establish brand identity
  - farm name
  - logo
  - social media presence
- sell direct-to-consumer (farm gate, farmers'/weekend markets, online)
- target ₱1/gram for premium raw honey
- establish social media channels
  - Facebook, Instagram
  - YouTube channel
  - TikTok
- establish online retail channels
  - Facebook marketplace
  - Lazada
  - Shoppee

### Learning

- gain experience with seasonal honey flows in Laguna
- build connections with local farmer cooperatives for future pollination services

## Year 2: Efficiency and Initial Diversification

:::{hint} Goal
Improve honey yield per hive and introduce first value-added products.
:::

### Expansion

- expand hive count to 20 colonies through splits
- aim for yield target of 440kg honey/year
- introduce new products:
  - Propolis to be sold raw or as tinctures
  - Beeswax as candles or simple cosmetic formulations (e.g. lip balms)
- partner with local health stores, cafes, and eco-shops
- offer honey subscriptions with monthly deliveries

### Operations

- standardize processing
  - moisture control
  - storage tanks
  - food-grade extraction facility
- formalize SOPs
  - to be used for future plans of offering training services
- begin packaging in premium jars
  

## Year 3: Further Diversification and Service Entry

:::{hint} Goal
Add new revenue streams and reduce dependency on honey sales.
:::

### Expansion

- reach ~50 hives 
- target annual yield of 1,250 kg honey/year
- offer new produces and services:
  - pollen collection and drying
  - expanded beeswax products (candles, soaps, skin creams)
  - pollination services for 20-30 hives @ PHP 2,000 per hive/season

### Marketing

- develop "single-origin" honey lines (e.g. wild forest honey, coconut honey)
- explore export feasibility of premium PH honey

### Operations

- train staff in queen rearing techniques
- acquire small-scale cold storage for pollen and royal jelly trials

## Year 4: Queen Rearing and Scaling Value-Added Products

:::{hint} Goal
Establish higher-margin product lines and bee breeding program.
:::

### Expansion

- reach 100 hives
- target annual yield of 2,800 kg honey/year
- offer new products and services:
  - queen rearing program to produce and sell 200-400 queens/year @ PHP 1000/queen
  - scale up propolis tinctures and pollen supplements
  - launch branded "wellness line" (honey-pollen mix)
- approach eco-tourism resorts in Tagaytay and Batangas

### Operations

- invest in semi-automated honey extraction/processing
- begin testing royal jelly harvesting in small batches

## Year 5: Full Diversification and Export Readiness

:::{hint} Goal
Mature business with multiple revenue streams and strong brand identity.
:::

### Expansion

- reach 150 hives
- target annual yield of 4,500 kg honey/year
- setup agrotourism infrastructure

### Marketing

- apply for FDA certification for functional products
- position brand for export

### Operations

- formalize cooperative or corporation structure
- employ dedicated staff for marketing, production, and R&D
- seek DOLE/DOST/DA support for export readiness programs

## Revenue Mix

:::{hint} Goal
Diversify on value-added bee products and decrease revenue reliance on honey.
:::


::::{tab-set}

:::{tab-item} Year 1

:::{grid} 2

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources-y1

revenue_sources = pl.DataFrame({
  "source": ["Honey", "Beeswax"],
  "proportion": [95, 5],
})

revenue_sources.to_pandas()
```

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources

alt.Chart(revenue_sources).mark_arc(innerRadius=50).encode(
  alt.Theta("proportion"),
  alt.Color("source", legend=None),
  tooltip=["source"],
).properties(width=240)
```

:::

:::{tab-item} Year 2

:::{grid} 2

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources-y2

revenue_sources = pl.DataFrame({
  "source": ["Honey", "Beeswax", "Propolis"],
  "proportion": [85, 10, 5],
})

revenue_sources.to_pandas()
```

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources

alt.Chart(revenue_sources).mark_arc(innerRadius=50).encode(
  alt.Theta("proportion"),
  alt.Color("source", legend=None),
  tooltip=["source"],
).properties(width=240)
```

:::

:::{tab-item} Year 3

:::{grid} 2

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources-y3

revenue_sources = pl.DataFrame({
  "source": ["Honey", "Beeswax", "Propolis", "Pollen"],
  "proportion": [75, 10, 10, 5],
})

revenue_sources.to_pandas()
```

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources

alt.Chart(revenue_sources).mark_arc(innerRadius=50).encode(
  alt.Theta("proportion"),
  alt.Color("source", legend=None),
  tooltip=["source"],
).properties(width=240)
```

:::

:::{tab-item} Year 4
:::{grid} 2

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources-y4

revenue_sources = pl.DataFrame({
  "source": ["Honey", "Beeswax", "Propolis", "Pollen", "Royal Jelly", "Queens & Nucs", "Pollination services"],
  "proportion": [60, 10, 10, 5, 2, 10, 3],
})

revenue_sources.to_pandas()
```

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources

alt.Chart(revenue_sources).mark_arc(innerRadius=50).encode(
  alt.Theta("proportion"),
  alt.Color("source", legend=None),
  tooltip=["source"],
).properties(width=240)
```
:::

:::{tab-item} Year 5

:::{grid} 2

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources-y5

revenue_sources = pl.DataFrame({
  "source": ["Honey", "Beeswax", "Propolis", "Pollen", "Royal Jelly", 
             "Queens & Nucs", "Pollination services", "Training and Seminars", "Agrotourism"],
  "proportion": [40, 10, 10, 10, 5, 10, 5, 5, 5],
})

revenue_sources.to_pandas()
```

```{code-cell} python
#| tags: [remove-input]
#| label: revenue-sources

alt.Chart(revenue_sources).mark_arc(innerRadius=50).encode(
  alt.Theta("proportion"),
  alt.Color("source", legend=None),
  tooltip=["source"],
).properties(width=240)
```
:::

:::

::::


## Projections

|Year|Hives|Yield (kg/hive)|Honey Harvest (kg)|Honey Revenue (₱)|By-Products (₱)|Total Revenue (₱)|OPEX (₱)|CAPEX (₱)|Net (₱)|
|----|-----|---------------|------------------|-----------------|---------------|-----------------|--------|---------|-------|
|1|5|20|100|70,000|NA|70,000|17,500|75,000|**-22,500**|
|2|20|22|440|308,000|46,000|354,000|70,000|225,000|**59,000**|
|3|50|24|1,250|875,000|130,000|1,005,000|175,000|450,000|**380,000**|
|4|100|26|2,800|1,960,000|300,000|2,260,000|350,000|750,000|**1,160,000**|
|5|150|28|4,500|3,150,000|470,000|3,620,000|525,000|750,000|**2,345,000**|

```{code-cell} python
#| tags: [remove-input, remove-output]

HONEY_PRICE = 800

projections = pl.DataFrame({
  "year": np.array(range(1, 6)),
  'hives': np.array([5, 20, 50, 100, 150]),
  'yield': np.arange(20, 30, 2),
  'OPEX': np.array([17500, 70000, 175000, 350000, 525000]),
  'CAPEX': np.array([75000, 225000, 450000, 750000, 750000]),
  'other_revenue': np.array([0, 46000, 130000, 300000, 470000]),
})

projections = projections.with_columns(
  honey_harvest=pl.col("hives") * pl.col("yield"),
).with_columns(  
  honey_revenue=pl.col("honey_harvest") * HONEY_PRICE,
).with_columns(
  total_revenue=pl.col("honey_revenue") + pl.col("other_revenue"),
).with_columns(
  net=pl.col("total_revenue") - pl.col("OPEX") - pl.col("CAPEX"),
).select(
  pl.col("year").alias("Year"),
  pl.col("hives").alias("Hive Count"),
  pl.col("yield").alias("Yield (kg/hive)"),
  pl.col("honey_harvest").alias("Honey Harvest (kg)"),
  pl.col("honey_revenue").alias("Honey Revenue (₱)"),
  pl.col("other_revenue").alias("Other Revenue (₱)"),
  pl.col("total_revenue").alias("Total Revenue (₱)"),
  pl.col("OPEX").alias("OPEX (₱)"),
  pl.col("CAPEX").alias("CAPEX (₱)"),
  pl.col("net").alias("Net (₱)"),
)

projections
```

```{code-cell} python
#| tags: [remove-input, remove-output]

base = alt.Chart(projections)

revenue_plot = base.mark_bar(opacity=0.5, color='gray').encode(
  alt.X("Year:O").scale(zero=False),
  alt.Y("Total Revenue (₱):Q"),
)

profit_plot = base.mark_bar(opacity=0.5, color='lightgreen').encode(
  alt.X("Year:O").scale(zero=False),
  alt.Y("Net (₱):Q"),
)

(revenue_plot + profit_plot).properties(
  width=500,
)
```
