# Transfer_Fee_Football
## Goal
The goal of this project is to analyse what factors influence the transfer value of a football player. Specifically, I looked at player statistics over a seaseon and tried to figure out what the relationship between these stats and the transfer value of a player is. I only looked at in-game stats of the last season and delibaretly did not try to look at othe important factors (e.g. marketability of a player), since I wanted to analyse how the in-game performance of the season prior to the transfer affected the transfer value. Consequently, I looked at in-game data from the 2018/19 Season and transfer data from the 2019/20 Season. I chose this season, because I wanted to look at the most recent transfer window. While the 2020/21 transfer window would have been more recent, I chose the 2019/20 season because the 2020/21 transfer window adversly affected financial situation of many clubs, which is why I feel that the 2019/20 season will be more representative.
## Data used
For this project I used the following data sources:
- [Transfermarkt.ch](https://www.transfermarkt.ch/) for transfer data and basic player statistics
- [Fbref.com](https://fbref.com/en/) for more detailed football statistics
- A FIFA 19 dataset from [kaggle](https://www.kaggle.com/karangadiya/fifa19) to get the contract length of the player at the time of the transfer
- [Fifaindex.com](https://www.fifaindex.com/de/) to get missing contract length values
## Methods
For all data sources, except the FIFA 19 dataset from kaggle, I had to use webscraping to get the data. I then used different statistical methods to analyse the relationship.
## Packages needed
- [`pandas`](https://pandas.pydata.org/docs/)
- [`numpy`](https://numpy.org/doc/1.20/)
- [`statsmodels`](https://www.statsmodels.org/stable/index.html)
- [`BeatifulSoup`](https://www.crummy.com/software/BeautifulSoup/bs4/doc/)
- [`requests`](https://docs.python-requests.org/en/master/)
- [`difflib`](https://docs.python.org/3/library/difflib.html)
- [`sportsipy.fb.roster`](https://sportsreference.readthedocs.io/en/stable/fb.html)
## How to run
There are several jupyter notebooks in this repository. All notebooks, except *statistical_analysis.ipynb*, are notebooks where I used webscraping to get the data from the sources mentioned in [Data used](#data-used). Since a webrequest needs to be created for every player, running these notebooks takes a while, which is why I would **not** recommend running them. Instead, I have uploaded all datasets you get from these notebooks into the repository and you can just run the *statistical_analysis.ipynb*. However, if you want to also run the other notebooks, you need to run them in the following order:
1. Transfer.ipynb
2. stats_tm.ipynb
3. FBref.ipynb
4. Contracts.ipynb
5. Statistical_Analysis.ipynb
