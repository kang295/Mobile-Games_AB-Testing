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
        <li>However, according to our chi-squared test, there was no significant difference in retention rates between the two versions at the 5% significance level. We do not have enough evidence to reject our null hypothesis that retention rate is the same for the two versions.</li>
        <li>From our bayesian analysis, the probability that 1-day retention is greater when the gate is at level 30 is 96.7%.</li>
    </ul>
    <h3>7-day retention</h3>
    <ul>
        <li>There was also a slight decrease in 7-day retention when the gate was moved from level 30 (19.0%) to level 40 (18.2%).</li>
       
