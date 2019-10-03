# 5. Remakes

This page explains whether a game should be remade when a player gets stuck in a glitch they cannot get out of or disconnects. The rare glitch where two players permanently stop moving on each others' screens is also a ground for a remake. Exceptions can be made when necessary. These are simply guidlelines.

The variables used in the following equations are defined as:

$$
s = \mathrm{score} \\
t = \mathrm{time} \\
p = \mathrm{players}
$$

## Manhunt



A game is always remade if a player disconnects or gets glitched in the first round. For the second round, the equation that determines the required score difference for  a manhunt game to be remade is:

$$
s_\mathrm{team1} - s_\mathrm{team2} = t ^ {1.3} \times p \times 2.2 \, \mathrm{\frac{points}{time \times players}} + 960 \, \mathrm{points}
$$

![](.gitbook/assets/curved_manhunt%20%282%29.svg)

If the score difference is higher than the calculated required score difference, the game is not remade. If it is equal to or less, the game is remade.

## Escort

In escort, along with disconnects and immobility glitches, VIPs failing to respawn and VIP protectors having a detection meter can force a remake. Whether an escort game should be remade is determined by whether the percentage score difference between the two teams falls under or over the following curve, whereby over implies no remake and equal or under implies a remake to be necessary: 

$$
t ^ {1.42} \times 29 \times 10 ^ {-5} \,\mathrm{\frac{\%}{s}} + .067\,\% = \begin{cases}\frac{ s_\mathrm{team1} - s_\mathrm{team2} } {s_\mathrm{team1}} & s_\mathrm{team1} \geq s_\mathrm{team2} \\ \frac{ s_\mathrm{team2} - s_\mathrm{team1} } {s_\mathrm{team2}} & s_\mathrm{team1} < s_\mathrm{team2} \end{cases}
$$

![](.gitbook/assets/escort%20%281%29.svg)

## Assassinate

In assassinate, the glitch where a poisoned player receives their poisoner only constitutes a remake when the two affected players are in first and second place and the score difference at the end of the game is less than or equal to the points made by the non-poison kill with the streak bonus on the poison kill subtracted if applicable:

$$
| s_\mathrm{player1} - s_\mathrm{player2} | \leq | s_\mathrm{poison} - s_\mathrm{streak} |
$$

For glitches in which someone gets stuck, the following equation determines whether an assassinate game should be remade:

$$
\LaTeX
$$

