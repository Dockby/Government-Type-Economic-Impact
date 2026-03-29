# Does the Type of Government Actually Affect Business?

I got into an argument with my friend about whether democracies are actually better for business or if that's just something western media pushes. Neither of us could prove our point so I figured I'd just look at the data.

Pulled together info on 44 countries, classified each one by government type, and ran the numbers on GDP, unemployment, tax rates and tax revenue. Some of it confirmed what I expected. A lot of it didn't.



## What I Was Trying to Find Out

- Do democracies actually have stronger economies?
- Are communist/autocratic states really that bad for business?
- Which system taxes businesses the most?
- Is unemployment worse under certain governments?



## Dataset Used

**Global Country Information Dataset 2023** — Kaggle
- 195 countries, 35 columns
- Covers GDP, tax rates, unemployment, labor force participation and more
- I manually classified 44 countries into government types based on Freedom House 2023 and general political science consensus

Government types I used:
- Democracy (20 countries) — USA, India, Germany, Brazil etc.
- Autocracy (14 countries) — Russia, Saudi Arabia, Turkey etc.
- Communism (4 countries) — China, Vietnam, Cuba, Laos
- Dictatorship (6 countries) — North Korea, Zimbabwe, Myanmar etc.



## Key Findings

### 1. Communist states had the highest average GDP — but there's a catch

This sounds insane on paper. Communist countries outperforming democracies in GDP? But the moment you think about it, it makes sense — China is in that group. China alone has a $17 trillion economy and it completely pulls the average up. Remove China and the picture flips entirely.

This is the same problem you run into with any small sample — one massive outlier can tell a completely different story than the actual trend.

### 2. Unemployment was lowest in communist states (2.15%)

Again, China and Vietnam pull this down. But there's also something real here — in state-controlled economies, the government can just... employ people. It's not that the private sector is thriving, it's that unemployment as a concept works differently when the state is the employer of last resort.

Democracies and autocracies were nearly identical here, both around 7.5%.

### 3. Dictatorships had the highest tax rates (47.3%)

This one actually surprised me. I expected communist states to tax the most since the government controls everything. But dictatorships averaged the highest total tax rate. My guess is that dictators need revenue to fund militaries and loyalty networks, and they don't have the same political pressure to keep taxes low that democratic governments face.

### 4. Democracies collected the most tax revenue as % of GDP (16.14%)

Higher tax revenue percentage usually means stronger institutions — better collection systems, less corruption, more compliance. This makes sense for democracies where rule of law is more established.

### 5. The statistical test said the differences aren't significant

Ran an ANOVA test. F-statistic came out to 1.90, p-value 0.1446. That's above the 0.05 threshold, which means statistically speaking, we can't confidently say government type is driving these differences.

Honestly this is a data limitation more than anything. 44 countries is a small sample, and when you have China as an outlier in the communist group it adds a ton of variance. A larger dataset with more communist/dictatorship examples would probably tell a cleaner story.



## What the Data Can't Tell You

Government type is one variable. In reality, a country's business environment is shaped by its geography, natural resources, colonial history, regional trade relationships, and a hundred other things. Singapore is technically a democracy but functions almost like a benevolent autocracy in practice. Saudi Arabia is an autocracy but has one of the most business-friendly environments for foreign investment. India is the world's largest democracy and still has massive bureaucracy and corruption problems.

So no, I don't think you can draw a straight line from "democracy = good for business" based on this data alone. The relationship is way more complicated than that.



## Tools Used

- Python (Pandas, Matplotlib, Seaborn, SciPy)
- Google Colab
- Dataset: Global Country Information 2023 — Kaggle

## Files

- `GOV_Impacting_Businesses.ipynb` — full analysis notebook
- `world-data-2023.csv` — main dataset



