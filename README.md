# Subscription Breakeven Analysis

## Assignment
The subscriptions team has exported the latest figures for each subscription plan and wants a quick analysis before deciding which plans to keep, grow, or retire.

## Deliverables
The breakeven point for each plan (the number of subscribers it needs before it stops losing money).
How each plan's profit changes as its subscriber count grows.
A short closing report for the subscriptions team: your recommendation for any plan that isn't working, plus anything they should double-check before relying on the numbers.


## Data Description
dropbox_subscription_plans.csv has one row per subscription plan:

plan_id
plan_name
segment - customer segment the plan targets
fixed_costs - the plan's monthly fixed costs
variable_cost_per_user - monthly cost per subscriber
revenue_per_subscriber - monthly revenue per subscriber
current_subscribers

## Analysis and Findings 

This data set has 16 rows x 7 columns
There are no duplicates or null values or missing values in the data set 
All the column names are readable and in snake case 
The data types for every column is accurate .


**Deliverable 1 : The breakeven point for each plan (the number of subscribers it needs before it stops losing money).**
 
 Breakeven point is  where they do not make any profit or any loss . Basically the breakeven subscribers value will give us an idea about how many users we need to sell the subscription plan to  initially cover the total costs before making any actual revenue/profits.

**Formula : breakeven point = fixed costs/ selling price per item - variable costs per item**

<img width="437" height="514" alt="image" src="https://github.com/user-attachments/assets/dce7385b-fc34-4f1e-8217-9cb0c2550d6e" />

**Deliverable 2 : How each plan's profit changes as its subscriber count grows.**

To analyze how the profit of each plan changes as the subscriber count grows, I added 500 subscribers to the current subscriber count of each plan and recalculated the profit

<img width="948" height="523" alt="image" src="https://github.com/user-attachments/assets/fcf1993f-a6ef-4567-9d51-4d47d1b9f35e" />


The analysis shows that most plans experience an increase in profit when 500 additional subscribers are added.  For example, the Enterprise plans profit increases by $105,000, while the Business plans profit increases by $42,500.Some plans that are currently operating at a loss also improve with additional subscribers. The Family plan moves from a $3,000 loss to a $7,500 profit, 
while the Nonprofit plan improves from a $3,000 loss to a $500 loss.

However, not all plans benefit from the additional subscribers. The Promo plan shows no change in profit, while the Legacy plans profit decreases by $2,000. The On-Prem plan only improves by $1,000 and remains at a significant loss.

Overall, based on the above analysis increasing subscriber numbers can improve profitability for most plans, but the impact varies depending on each plans revenue and variable costs.

## Recommendations
To ensure that the plans are generating profit the main consideration is  revenue_per_subscriber should always be greater than the variable_cost_per_user

The three plans that I would like  closely look at are Promo , Legacy and On-Prem plans.

**Promo Plan**

No matter how many subscribers this plan gains, the profit will remain at the same level because the revenue per subscriber and variable cost per user are the same(8). This means that each additional subscriber generates revenue that is completely offset by the variable cost, leaving no contribution toward the plans fixed costs. To make this plan profitable, the subscriptions team would need to either increase the revenue per subscriber or decrease the variable cost per user. The fixed costs should also be reviewed to determine whether there are opportunities to reduce them.

**Legacy Plan**

The profits tend to decrease when more subscribers are added. This is because the variable cost per user (9) is higher than the revenue per subscriber (5).i.e for every subscriber added we are generating a 4 dollar loss. To ensure that this plan generates profits, we need to reduce the variable cost per user.

**On-Prem Plan**

The fixed costs for this plan are 500,000 and the variable cost per user is 218, while the revenue per subscriber is 220. The contribution is just $2, which is very minimal when compared to the fixed costs. the plan needs 250,000 subscribers just to break even . To ensure that this plan generates profits, we need to make sure that the revenue per subscriber is substantially increased or the variable cost per user is reduced to help offset the fixed costs.
