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

<ul>
 <li>Navigate to your HOME (/home/sysadmin) directory where you created the Lucky_Duck_Investigations directory and run the following command to set up the evidence files:</li>
 <ul>
  <li>wget "https://drive.google.com/uc?id=1ZLY_fuFu3wz7tOlxf-GUrnvp3htuGKSa" -O 3-HW-setup-evidence && chmod +x ./3-HW-setup-evidence && ./3-HW-setup-evidence</li>
 </ul>
 
</ul>
  
