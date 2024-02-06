## NFL Quarterback Records vs Winning Teams

### Inspiration

For better or worse, wins in the NFL are a quarterback stat. Quarterbacks are the most important player on the field and as such, the onus for the wins and losses falls entirely on them, even if that's an unfair mantle to place upon them.

Several years ago, there was a lot of discourse on social media about Matthew Stafford and Kirk Cousins, calling them overrated because they rarely beat winning teams. The argument went that these QBs couldn't get it done against stiff competition, meaning they weren't nearly as effective as their statistics indicted. The problem with this argument to my mind is that by definition, QBs that play against teams with winning records, by definition of a 'winning record' lose more often than they win. I tried to find numbers on QBs records against winning teams but the only data I could find was cursory, a couple top ten lists years out of date and little else.

I decided to look into it myself.

## Questions

•	What is the typical QB record against teams with a winning record?

•	Does this align with awards given to higher performing Quarterbacks? Namely, the Pro Bowl, first team All-Pro, and the Hall of the Fame?

### Process

The first step was pulling data from stathead, where I learned a lot about browser cookies and their authentication processes due to the fact that I used google to sign into stathead, not a traditional account. I finally stumbled on the browser-cookie method and got it working.* With this, I created a few functions to pull the QB gamelogs from stathead, organized the data how I wanted it, pulled in the Pro Bowl, All Pro, and Hall of Fame lists, and finally got the chart I wanted at the end.

(*If you're trying to recreate this, it's a significantly more complicated process if you use Google Chrome. I did not try any other browsers.)

### Limitations and Decisions

First off, I decided to limit my data to the Super Bowl era. There are arguments to be made for more modern times, with recent rule changes heavily favoring offense and increasing the importance of the quarterback to the game's outcome, or for limiting the search to the salary cap era, but I chose the super bowl era. As with any cutoff point, this means that quarterbacks who played only partially in the Super Bowl era don't have their full careers represented, but unless I went back to the creation of the QB position or the NFL itself, there's no way to avoid this problem.

Secondly, how I assigned a game to each quarterback is using stathead/PFR's 'QB Start' statistic. This leads to individual oddities where Quarterbacks who started games and got immediately hurt and unable to play received a win, loss, or tie they had little to no hand in causing. This is unfair, and ideally I would use something more indicitive of play, such as assigning the QB who played at least 50% of offensive snaps the outcome, but this was a more complicated procedure and I presumed its effect on the overall results would be minimal, and not worth the effort.

Thirdly, while there are 2 All-Pro teams (first and second) and traditionally both teams are considered "All-Pros", stathead only returns the results for 1st team All-Pros, unfairly neglected QBs who only won 2nd teams in their careers. 

Fourth, here are some clarifications or judgement calls made on the data itself:

  • I considered a team to have a winning record if they have a winning percentage of .501 or higher. A team that finished 8-8, or 8-8-1, is not considered a winning record.

  • Ties were counted the same as the official NFL standings do, .5 of a win and .5 of a loss. 
  
  • The final chart displays only QBs that started at least 10 games against winning teams. A QB that starts for 2 whole seasons in the modern usually gets at least 10 games, as 6-7 games vs winners a season was relatively standard in the modern. For comparison, this data was pulled after the 2023 regular season, and Brock Purdy, who has started a season and a half, made the cutoff. I did include a chart of all QBs, regardless of sample size, for comparison.
 
 • This includes only regular season games. Postseason is not included.

### Data Source and Technologies

All data sourced from stathead.com/Pro Football Reference

Built and created in Jupyter Notebooks using Python

### Conclusions:

The results looked and felt authentic, giving me hope in the general metric. The higher-status QBs, such as All-Pros and Hall of Famers, tended to have better records, while QBs who never received such honors tended to score lower. These were the results I expected, passing the "smell test", as it were.

Specifically regarding Matthew Stafford and Kirk Cousins, Kirk's record has improved significantly since the days of this argument being thrown around, and I haven't heard anyone say this about either QB for years. Stafford remains an anomaly even after winning a Super Bowl, coming in with the 3rd-worst record of the Super Bowl era with the 10 game cutoff. However, the data includes several such anomalies, and I'm comfortable saying it's not a perfect bullet. Notorious 1st overall bust JaMarcus Russell boasts a higher-than-average winning percentage of around 40%. Brock Osweiler boasts a >50% record. NFL seasons are small sample sizes compared to other sports, and eliminating roughly half the games reduces it even further, meaning some oddities are going to leak through.

In addition, while QB is the most important position in football, it is not the only position. Anyone who's watched the sport has seen excellent QB games lost because of the failure of the team around them, or because the other team simply performed even better. Stafford spent most of his career weighed down by the ineptitude of the late 00s-10s Lions, a completely dysfunctional organization from top to bottom who failed to achieve any manner of success despite drafting Stafford, Calvin Johnson, and Ndamukong Suh.
