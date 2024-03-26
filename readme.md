# Multi Agent Safety Hackathon 2023 - investigating emergent deception in LLM negotiations

Note: Experiments for the hackathon were run on the andy_6pm_exps branch.

We chose the following set of metrics. Since rewards and items differ between rounds, we normalize all metrics to
the maximum total utility possible in that round.
1. Welfare [aka "Net Utility"]: The sum of all agents' utility. How much value did we capture in total compared
to what could have been captured?
2. Inequality [aka "Fairness"]: on average, how big was the utility gap between agents? i.e. utility_agent_one - utility_agent_two [Gandhi et a1., 2023]
3. Reward: On average, how much utility did each agent end up with?
We experiment with agents with different initial moral mappings: baseline agents are not given a specific set of
values, but simply prompted to think strategically. Machiavellian agents are prompted to maximize their own
rewards by any means possible. Prosocial agents are prompted to look for a fair compromise, while deceptive
agents are specifically encouraged that they can misrepresent their own rewards.

<img width="726" alt="Screenshot 2024-03-26 at 9 59 05 AM" src="https://github.com/anwang427/deal-or-no-deal/assets/52337408/29239e97-1cac-4aae-9ead-5efbc95adf1d">
