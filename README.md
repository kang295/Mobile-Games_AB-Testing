<h1>A/B Testing - Cookie Cats</h1>
<p>Mobile Games A/B Testing with Cookie Cats</p>

<h2>Problem Statement</h2>
<p>Cookie Cats is a hugely popular mobile puzzle game developed by Tactile Entertainment. It is a classic "connect three" style puzzle game where the player must connect tiles of the same color in order to clear the board and win the level. As players progress through the game they will encounter gates that force them to wait some time before they can progress or make an in-app purchase. In this project, we will analyze the result of an A/B test where the first gate in Cookie Cats was moved from level 30 to level 40. In particular, we will analyze the impact on player retention.</p>

<h2>Data Dictionary</h2>
<table class="data-table">
    <tr>
        <th>Feature</th>
        <th>Type</th>
        <th>Description</th>
    </tr>
    <tr>
        <td>userid</td>
        <td>id</td>
        <td>A unique number that identifies each player.</td>
    </tr>
    <tr>
        <td>version</td>
        <td>string</td>
        <td>Whether the player was put in the control group (gate_30 - a gate at level 30) or the group with the moved gate (gate_40 - a gate at level 40).</td>
    </tr>
    <tr>
        <td>sum_gamerounds</td>
        <td>integer</td>
        <td>The number of game rounds played by the player during the first 14 days after install.</td>
    </tr>
    <tr>
        <td>retention_1</td>
        <td>boolean</td>
        <td>Did the player come back and play 1 day after installing?</td>
    </tr>
    <tr>
        <td>retention_7</td>
        <td>boolean</td>
        <td>Did the player come back and play 7 days after installing?</td>
    </tr>
</table>

<div class="results-section">
    <h2>Results</h2>
    <h3>1-day retention</h3>
    <ul>
        <li>There was a slight decrease in 1-day retention when the gate was moved from level 30 (44.8%) to level 40 (44.2%).</li>
        <li>It tells that 1-day retention rate was higher in players who were assigned with version (gate_30) with 96.2%. It is obvious that setting the forced stop moment at gate 30 is efficient to make player's retention rate higher..</li>
        <li>**However**, since players have only been playing the game for one day, it is likely that most players haven't reached level 30 yet. That is, many players won't have been affected by the gate, even if it's as early as level 30.</li>
    </ul>
    <h3>7-day retention</h3>
    <ul>
        <li>There was also a slight decrease in 7-day retention when the gate was moved from level 30 (19.0%) to level 40 (18.2%).</li>
        <li>Here, we can see that the overall 7-days retention rate for players decreased from about 44% to 18% compared to 1-day retention rate. It shows that a lot of people stopped playing game within a week. Also, it is similar that players assigned with gate_30 shows higher 7-days retention rate. We can get a hint that still making players stop playing games at gate 30 is effective way to engage players and drive in-app purchases.</li>
        <li>The bootstrap result tells us that there is strong evidence that 7-day retention is higher when the gate is at level 30 than when it is at level 40. **The conclusion is: If we want to keep retention high — both 1-day and 7-day retention — we should not move the gate from level 30 to level 40**. There are, of course, other metrics we could look at, like the number of game rounds played or how much in-game purchases are made by the two AB-groups. But retention is one of the most important metrics. If we don't retain our player base, it doesn't matter how much money they spend in-game.</li>
       
