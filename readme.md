# Electoral statistics 2000-2024
The code was used for the report  ["How to uncover electoral fraud in Russia using statistics: a complete guide"](https://cedarus.io/research/evolution-of-russian-elections). Detailed descriptions of the applied methods can be found there.

## Code description
The code consists of the following parts:
- Data loading and processing
 - **Shpilkin's method**, which is used to calculate the amount of *vbrosy* -- additional ballots for the leading candidate that are inserted in the ballot box
	 - Applied to each region and year individually
	 - Total for Russia for each year
- **Integer anomalies** -- exceed votes for leader or polling stations with integer percentage, that appear when a member of the election commission rewrites the results of the protocol
	- Illustration for 1d-case (considering only integer values on leader's result or turnout)
	- Calculations considering both the leader's result and turnout

## Results of the analysis
The folder "region_analysis_tables" includes two csv tables with falsification rates for regions based on our calculations with Shpilkin's method:
- *absolute_values_vbrosy.csv* is an absolute value of *vbrosy* per region per year
- *leader_percent_vbrosy.csv* is a percentage added to the leader's result with *vbrosy*. It is equal to the absolute value of *vbrosy* divided by the total number of ballots for the leader.

If Shpilkin's method is not applicable for some elections in some regions, the value in the table is "N/A" -- it usually indicates mass falsifications. If there is no data from the Russian Central Election Committee, the cell is empty. If the value in the table is negative, it is statistical error and should be treated as zero.

**To request data that were used for the calculations, please contact us: contact@cedarus.io**
