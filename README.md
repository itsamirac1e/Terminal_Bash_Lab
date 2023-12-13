<h1>Linux Terminal Lab - "A High-Stakes Investigation"</h1>

<h2>Description</h2>

In this Linux lab, as a security analyst for Lucky Duck Casino, the objective was to investigate and mitigate significant losses at the roulette tables on March 10, 12, and 15. Suspecting collusion between a player and a dealer, I utilized command-line skills to navigate, modify, and analyze the casino's database. The goal was to swiftly identify the rogue duo and prepare evidence files for potential prosecution, given the casino's financial constraints. The urgent findings were summarized for Lucky Duck's management, aiming to expose and prevent further fraudulent activities.
<br />


<h2>Languages and Utilities Used</h2>

- <b>BASH</b> 
- <b>Linux Terminal</b>

<h2>Environments Used </h2>

- <b>Apache Guacamole on Ubuntu VM</b>

<h2>Program walk-through:</h2>
<p>Using basic command-line skills, I uncovered the identities of the rogue casino player and dealer colluding to scam Lucky Duck out of thousands of dollars. These steps were conducted on my Ubuntu VM hosted on Apache Guacamole provided by UT Austin's Cybersecurity Bootcamp team.</p>

<h2>Step 1: Investigation Preparation</h2>
<ul>
 <li>Navigate to your HOME directory</li>
 <ul>
  <li><i>cd /home/sysadmin</i></li>
 </ul>
 <li>Make a single directory titled Lucky_Duck_Investigations then navigate to this new directory.</li>
 <ul>
  <li><i>mkdir Lucky_Duck_Investigations</i></li>
  <li><i>cd Lucky_Duck_Investigations</i></li>
 </ul>
 <li>In the Lucky_Duck_Investigations directory, create a directory for this specific investigation titled Roulette_Loss_Investigation.</li>
 <ul>
  <li><i>mkdir Roulette_Loss_Investigation</i></li>
 </ul>
 <li>In Roulette_Loss_Investigation, create the following directories:</li>
 <ul>
  <li>Player_Analysis to investigate the casino player. - <i>mkdir Player_Analysis</i></li>
  <li>Dealer_Analysis to investigate the dealers. - <i>mkdir Dealer_Analysis</i></li>
  <li>Player_Dealer_Correlation to summarize your findings about the collusion. - <i>mkdir Player_Dealer_Correlation</i></li>
 </ul>
 <li>Create empty files called Notes_<Directory_Name>.txt under each subdirectory to store investigation notes.</li>
  <ul>
   <li><i>touch Player_Analysis/Notes_Player_Analysis.txt</i></li>
   <li><i>touch Dealer_Analysis/Notes_Dealer_Analysis.txt</i></li>
   <li><i>touch Player_Dealer_Correlation/Notes_Player_Dealer_Correlation.txt</i></li>
  </ul>
</ul>
<p align="center">
Launch the utility: <br/>
<img src="https://i.imgur.com/62TgaWL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
</p>

<h2>Step 2: Gathering Evidence</h2>
<p>In this task, I moved evidecne from the specific dats on which Lucky Duck experience heavy losses at the roulette tables using the following commands:</p>

<ol>
 <li>Navigate to your HOME (/home/sysadmin) directory where you created the Lucky_Duck_Investigations directory and run the following command to set up the evidence files:</li>
 <ul>
  <li><i>cd /home/sysadmin/</i></li>
  <li><i>wget "https://drive.google.com/uc?id=1ZLY_fuFu3wz7tOlxf-GUrnvp3htuGKSa" -O 3-HW-setup-evidence && chmod +x ./3-HW-setup-evidence && ./3-HW-setup-evidence</i></li>
 </ul>
 <li>After running this command, your current directory should have the following subdirectories:</li>
 <ul>
  <li>Dealer_Schedules_0310: Contains the dealer schedules.</li>
  <li>Lucky_Duck_Investigations: Contains the investigation directories and notes files you created.</li>
  <li>Roulette_Player_WinLoss_0310: Contains the data for player wins and losses.</li>
 </ul>
 <li>The Dealer_Schedules_0310 and Roulette_Player_WinLoss_0310 directories contain the dealer schedules and win/loss player data from the roulette tables during the week of March 10.</li>
 <ul>
  <li>Since the losses occurred on March 10, 12, and 15, move the schedules for those days into the directory Dealer_Analysis.</li>
  <li>Move the files for those days into the directory Player_Analysis.</li>
 </ul>
</ol>

<h2>Step 3: Correlating the Evidence</h2>
<p>In this next task, I correlated the large losses from the roulette tables with the dealer schedule. This helped to determine which dealer and player are colluding to steal money from Lucky Duck.</p>

<ol>
 <li>Navigate to the Player_Analysis directory.</li>
 <li>Use grep to isolate all of the losses that occurred on March 10, 12, and 15.</li>
 <li>Place those results in a file called Roulette_Losses.txt.</li>
 <li>Preview the file Roulette_Losses.txt and analyze the data.</li>
 <ul>
  <li>Recorded the following in the Notes_Player_Analysis.txt file:</li>
  <ul>
   <li>The times the losses occurred on each day.</li>
   <li>Whether there is a certain player who was playing during each of those times.</li>
   <li>The total count of times this player was playing. > Hint: Use the wc command to find this value.</li>
  </ul>
 </ul>
</ol>
<p>Next, I completed the following steps for Dealer Analysis</p>
<ol>
 <li>Navigate to the Dealer_Analysis directory.</li>
 <li>This file contains the dealer schedules for the various Lucky Duck casino games: Blackjack, Roulette, and Texas Hold 'Em.</li>
 <ul>
  <li>Preview the schedule to view the format and to understand how the data is separated.</li>
 </ul>
 <li>Using my findings from the player analysis, I then created a separate script to look at each day and time that I determined losses occurred. I used awk, pipes, and grep to isolate out the following four fields:</li>
 <ul>
  <li>Time</li>
  <li>a.m./p.m.</li>
  <li>First/Last name of roulette dealer</li>
 </ul>
 <li>Run all of the scripts and append those results to a file called Dealers_working_during_losses.txt.</li>
 <li>Preview your file Dealers_working_during_losses.txt, and analyze the data.</li>
 <ul>
  <li>Recorded the following in the Notes_Dealer_Analysis.txt file:</li>
  <ul>
   <li>The primary dealer working at the times where losses occurred.</li>
   <li>How many times the dealer worked when major losses occurred.</li>
  </ul>
  <li>Completed the player/employee correlation</li>
  <ul>
   <li>In the notes file of the Player_Dealer_Correlation directory, add a summary of your findings noting the player and dealer you believe are colluding to scam Lucky Duck.</li>
 </ul>
</ol>

<h2>Step 4: Scripting My Tasks</h2>
<p>In this step, I've been tasked with building a shell script that can easily analyze future employee schedules. This script will then be used to determine which employee was working at a given time in the case of future losses.</p>
<ol>
 <li>Remaining in the Dealer_Analysis directory, I developed the following shell script called roulette_dealer_finder_by_time.sh that can analyze the employee schedule to easily find the roulette dealer at a specific time.</li>
 <li>Insert picture of shell script here</li>
</ol>















