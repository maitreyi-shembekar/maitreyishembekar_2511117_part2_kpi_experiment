# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Experiment Hypothesis Framework

### 1. Null Hypothesis ($H_0$)
The new onboarding experience has no effect on user behavior. The difference in Paid Conversion Rates between the Control and Treatment groups is a random fluke.
- $H_0: \text{Conversion}_{\text{Treatment}} = \text{Conversion}_{\text{Control}}$

### 2. Alternate Hypothesis ($H_a$)
The new onboarding experience significantly alters user behavior, resulting in a real difference between the Paid Conversion Rates of the two groups.
- $H_a: \text{Conversion}_{\text{Treatment}} \neq \text{Conversion}_{\text{Control}}$

### 3. Test Tail Type
- **Type:** Two-Tailed Test
- **Explanation:** The data shows that the new onboarding lowers individual spend and increases support tickets (by 10%), we must check for shifts in *both* directions. We choose a two-tailed test to be sure that the campaign doesn't introduce hidden problems or low-quality conversions that hurt the business in the long run.

### 4. Significance Level ($\alpha$)
- **Threshold:** $\alpha$ = 0.05
- **Explanation:** This is the standard threshold. It means we require enough evidence to be 95% confident that our results are not just due to random chance. It ensures there is less than a 5% chance that we are chasing a false alarm before we commit engineering and customer support resources to a full rollout.  

### 5. Metric Being Tested
**Primary Metric:** Paid Conversion Rate (`converted_to_paid`)

### 6. Business Rationale & Connection to Decision
The Paid Conversion Rate is our primary North Star metric. The executive decision is whether to fully deploy the new onboarding campaign to 100% of the user base. 

Our calculation summary shows that the Treatment group successfully doubled the conversion rate (7.04% vs. 3.19%). However, there is a critical trade-off: individual spending has dropped significantly (Average Revenue per Converted User fell from ₹1,630 to ₹770), meaning we are moving toward a high-volume, mass-market business model. Testing the conversion rate statistically is crucial to confirm that this increase in the conversion rate is genuine and strong enough to support the business decision.

### 7. Interpretation Logic
- **If $p$-value < 0.05:** We reject the Null Hypothesis. The increase in conversion rate, to 7.04%, is mathematically proven that it is caused by the new onboarding campaign. We can confidently tell leadership that the high volume is real.
- **If $p$-value $\ge$ 0.05:** We fail to reject the Null Hypothesis. The difference is statistically insignificant. We cannot recommend a rollout because the increase might just be luck, which would not justify the extra customer support tickets.