# ptf_vs_bmk
This repository contains the code to perform EDA (performance and allocation) of a portfolio vs its benchmark.

*** INPUT ***
The code reads an .xlsx file that contains all securities contained in a benchmark and its portfoli, with the corresponding
weights.

*** OUTPUT ***
Running the code generates two charts, a so-called <b>market</b> chart and a <b>portfolio</b> chart. In this repository,
there are two examples of charts, one is a market chart (<i>test_mkt.png</i>) and the other is a portfolio chart (<i>test_
ptf.png</i>).

The <b>market</b> chart is a representation of all the securities in the market. The x-axis represent a relative-value
return (e.g. 1-week, 1-month, etc.). The y-axis always represents the YTD relative return. The chart is then split into
four quadrants. Securities in the top right quadrant are those who have been performing well since the beginning of the year
and they are continuing to do so even in the period looked at in the x-axis. Size of points is proportionate to the weight of
the title in the benchmark.
Every chart is <b>focused</b> on a specific sector. Coloured observations are those that belong to the sector analysed.
The colours reflect the sub-sector.
The vertical dashed line in the main chart represents the sector average (weighted by the weights in the benchmark).
The small chart on the top right is the relative average return of each subsector.
All charts are generated automatically via a simple for-loop and they are saved as 1000 dpi images.

The <b>portfolio</b> chart is a representation of the performance and the allocation of a portfolio vs its benchmark. It is
again focused on a specific sector, i.e. all coloured points (non-grey) belong to the same sector.
The x-axis is always a relative value retun (e.g. 1 month, 2 months, etc.). The y-axis represents the ratio (cubic-root
transformed) of the weight of a security in the portfolio over its weight in the portfolio. A ptf/bmk ratio greater than 1
means that a security is over-weighted vs the benchmark.
The vertical dashed line in the main chart represents the sector average relative value return (weighted by the weights
in the benchmark).
The small chart on the top right represents the over/underweight (in %) of each subsector, while the vertical dashed line
represents the average over/underweight of the sector analysed (still in %).
