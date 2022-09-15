# Election_Analysis
_______________________________________________________________________________________________________________________________________________________________________
### Project Overview
_______________________________________________________________________________________________________________________________________________________________________
![Diana DeGette](https://user-images.githubusercontent.com/111723067/190506038-594ae5e6-7259-4fbb-a511-6ca5f79b553c.png)

A Colorado Board of Elections employee has given the following tasks to complete the
election audit of a recent local congressional election.

1. Calculate the total number of votes cast.
2. Get a complete list of candidates who received votes.
3. Calculate the total number of votes each candidate received.
4. Calculate the percentage of votes each candidate won.
5. Determine the winner of the election based on popular vote.

### Resources
_______________________________________________________________________________________________________________________________________________________________________
* Data Source: election_results.csv
* Software: Python 3.6.1, Visual Studio Code, 1.38.1

### Summary
_______________________________________________________________________________________________________________________________________________________________________

The analysis of the election shows that:

![election results 2](https://user-images.githubusercontent.com/111723067/190504383-081b0dae-35ee-4763-a23d-d212c5b6b2f0.png)

* There were 369,711 total votes cast in the election. 

        total_votes += 1

* The candidates were:
   * Diana DeGette
   * Charles Casper Stockham
   * Raymon Anthony Doane

* The candidate results were:

   *  Diana DeGette received 73.8% of the vote and 272,892 votes.
   *  Charles Casper Stockham received 23.0% of the vote and 85,213 votes.
   *  Raymon Anthony Doane received 3.1% of the vote and 11,606 votes.

             votes = candidate_votes.get(candidate_name)
             vote_percentage = float(votes) / float(total_votes) * 100
             candidate_results = (
             f"{candidate_name}: {vote_percentage:.1f}% ({votes:,})\n")

* The winner of the election was:
  * Diana DeGette, who received 73.8% of the vote and a total of 272,892 votes.

         if (votes > winning_count) and (vote_percentage > winning_percentage):
            winning_count = votes
            winning_candidate = candidate_name
            winning_percentage = vote_percentage


* Votes by county: 
  * Jefferson: 10.5% (38,855 total votes).
  * Denver: 82.8% (306,055 total votes).
  * Arapahoe: 6.7% (24,801 total votes).

        county_vote_percentage = float(area_votes) / float(total_votes) * 100
        county_results = (
            f"{county}: {county_vote_percentage:.1f}% ({area_votes:,})\n")

* County with largest number of votes:
  * Denver: 82.8% (306,055 total votes).

        if (area_votes > most_votes):
            most_votes = area_votes
            largest_county = county
            
### Challenge Overview
_______________________________________________________________________________________________________________________________________________________________________
* Creating this code was useful in helping me organize and search for the total votes, total votes per candidate, winning candidate, percentage of votes each canditate received, as well as election results based on the individual counties of Denver, Jefferson, and Arapahoe.

### Challenge Summary
_______________________________________________________________________________________________________________________________________________________________________
* Diane DeGette was the winnder of the Colorado election, she beat the other candidates by a whopping 73.8% of votes! The majority of votes came from Denver county, totaling at 306,055 votes.
* This script can be used for any election! With modifications, of course. Editing the script can be useful  finding totals of elections around the world and using any categories. This specific data set was straight-forward and based on counties and candidates. It is possible to modify this script to include factors such as age, gender, ethnicity, and much more.
![image](https://user-images.githubusercontent.com/111723067/190506649-73c3ff4c-e006-4008-8391-b2aebd0f77b1.png)
