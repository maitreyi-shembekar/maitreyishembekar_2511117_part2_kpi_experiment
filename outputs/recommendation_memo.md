# Part 2: KPI Framework, Business Experiment Analysis & Decision Recommendation

## Task 9: Onboarding Recommendation Memo

### Business Problem Statement
**What decision needs to be made?**  
To decide whether the company should permanently implement the new onboarding experience to all customers and deprecate the old onboarding experience, or not.  

**Who the decision impacts?**  
- **New users -** People who directly experience the new or old onboarding experience.
- **Product and Marketing teams -** who are responsible for maintaining and optimizing the user experience.
- **Customer Support team -** who are affected by any negative experience or problems from the customers.  

**What metric should improve?**  
- **Conversion Rate -** the number of new users who successfully transition to the subscription after the onboarding experience.
- **Customer Engagement -** the average interaction frequency of the user with the product.  

**What risks must be monitored?**  
- **Churn/Cancellation rates -** to ensure the new campaign does not make customers to cancel their subscriptions early.
- **Customer Support Tickets -** to monitor support requests, which would show if the new onboarding campaign is confusing or has technical difficulties.  

**What evidence is required before making a recommendation?**  
- **Statistical proof -** a 2 sample hypothesis test showing improvement in primary metrics and achieving a p-value less than alpha (0.05).
- **Financial proof -** to show that the change will make enough profits to make it worth the effort.  
__________
### 1. Executive Summary
This memo evaluates the performance of the new onboarding and activation campaign tested across 1,400 unique users. The experiment was a success for top-of-funnel volume, doubling our North Star Paid Conversion Rate from 3.19% to 7.04%. This is backed by statistical significance (p = 0.001026).  
However, guardrail analysis revealed critical trade-offs: individual customer spend dropped by 52.7% (indicating a shift to a mass-market business model), and customer support tickets spiked by 10%.  
To grow without overwhelming operations or losing high-value revenue, a targeted launch exclusive to Mobile and Tablet users in the East and West regions is recommended, while delaying a 100% global rollout until the product team addresses underlying user friction.  
___________
### 2. North Star Metric
**(Paid) Conversion Rate**  
The percentage of new customers who convert to a paid subscription.  

**Why this metric is the main success metric?**  
The goal of this campaign is successful onboarding and customer subscription activation. The Conversion Rate measures how effective the new onboarding experience is. If the new onboarding is successful, more people will subscribe. It directly measures the ultimate goal of the campaign.

**Why other metrics are supporting metrics instead of the North Star?**  
Conversion Rate is the main metric because it is the main source of profit and growth. Other metrics like "Click Through Rates", "Time Spent" are just supporting the main goal. These are **supporting metrics**. They tell us how users are behaving, but the North Star tells us if that behavior resulted in a win for the business.  

**How this metric connects to business growth?**  
When more customers convert to a paid subscription, that equals more revenue, which in turn can be used to build new features, hire more people and acquire more users. This is a growth loop. Growth is driven by recurring revenue.  

**What could go wrong if this metric is optimized blindly?**  
Blind optimization may lead to misleading or bad design. This could increase the conversion rate but only for a short time and is very unsustainable. Customers could cancel subscriptions, leave bad reviews, which affects the company negatively overall, in the long term.  
__________
### 3. KPI Tree Explanation
**The North Star:** Paid Conversion Rate  

**Driver 1:** Trial Activation  
**Sub-drivers:** Onboarding tutorial completion and Account profile setup.

*Explanation: We look at Trial Activation because a user can't convert if they never actually start using the app. We measure this by checking if they finished the tutorial and set up their profile. If these two metrics increase, it means more users are actively engaging with the product, which gives a higher chance of converting later.*  

**Driver 2:** Early Feature Adoption  
**Sub-drivers:** 7-day session frequency and core feature interaction count

*Explanation: We show the new users some premium features as a sample for the users to try out. If they keep coming back and using the features frequently in the 7 days, it means they like it and are finding it useful. Which can mean that the users can potentially pay for the subscription*  

**Driver 3:** Checkout completion  
**Sub-drivers:** Paywall views and payment method success rate.

*Explanation: We see how many users looked at the subscription prices. If they look further into the subscriptions, it means they are thinking of buying it. Or at least looking at what more we have to offer. Then we see how many actually buy a subscription and successfully complete the transaction.*  
__________
### 4. Experiment Result Summary
1. **Outliers in Revenue**  
    Average = Rs.53.13  
    Median = Rs.0  
    A median of 0 means that more than half of the users did not buy a subscription. But the average of Rs.53.13 means that the users who paid for a subscription paid enough to pull up the average.  

2. **Control vs Treatment Groups Count**  
    Control Group: 690 records  
    Treatment Group: 710 Records  
    The 2 groups are split almost equally (roughly 49% to 51%).  

3. **Landing Page Visit Rate**  
    Increased from 63.6% (Control) to 72.4% (Treatment), clearly showing that the new campaign shows more initial interest.  

4. **Trial Start Rate**  
    Increased from 25.1% (Control) to 29.0% (Treatment).  

5. **Onboarding Completion Rate**  
    Increased from 15.7% (Control) to 21.1% (Treatment). This means the new onboarding design is less confusing and helps users get through the setup.  

6. **Paid Conversion Rate**  
    Increased from 3.19% (Control) to 7.04% (Treatment), which is almost doubled. We are achieving the main goal, the North Star.    
_____________
### 5. Hypothesis Test Interpretation
The p value obtained is is about 0.1% (0.001026062), which is very less than $\alpha$ 5% (0.05). This means that there is only a 0.1% chance that this increase from 3.19% to 7.04% was a random fluke. It is 99.9% guaranteed that the new onboarding campaign is what caused the conversion rate to increase.
___________
### 6. Guardrail Analysis
1. **Support Ticket Rate**  
*The Data: Control = 14.78% | Treatment = 24.79%*  
The support ticket rate increased by almost 10%. This means nearly 1 out of every 4 users who goes through the new onboarding gets stuck, confused, or is experiencing a bug, forcing them to message customer service. Even if conversion rates have increased, a flood of support tickets creates operational chaos.

2. **Average Revenue Per Converted User**  
*The Data: Control = ₹1,630.10 | Treatment = ₹770.41*  
The amount of money spent per paying user dropped by more than half (52.7%). The new onboarding made it easier to subscribe and attracted budget plan users or caused premium users to choose cheaper options. While the total new users pulled the overall Average Revenue Per User up slightly (₹54.25 vs ₹51.97), it shifts the business model from "High-Value" to "Mass-Market."

3. **Segment-Level Performance**  
*The Data:  *North Region:* Control = ₹84.50 | Treatment = ₹80.97  
*South Region:* Control = ₹76.03 | Treatment = ₹47.26*  
In the East and West regions, the revenue increased. However, the North region revenue dropped by ₹3.53, and the South region decreased by ₹28.77 per user. The new onboarding campaign worked successfully in the East and West, but failed in the North and South regions.
_______________
### 7. Segment-level Insight
1. **Device Type**  
    The Treatment group performed well on Mobile (conversion increased from 2.58% to 7.41%) and Tablet (1.82% to 7.14%). This means the new onboarding is works better for mobile devices. The desktop users increased from 4.50% to 6.57%. 

2. **Region**  
    Average Revenue Per User increased significantly in the East (from Rs.18.23 to Rs.47.05) and West (from Rs.13.68 to Rs.41.24) regions, while remaining roughly steady or decreasing slightly in the North (from Rs.84.50 to Rs.80.97) and South(from Rs.76.03 to Rs.47.26).
_______________
### 8. Final Recommendation:
The new onboarding should be **launched only for selected segments.**  
- The new onboarding should be launched for Mobile and Tablet users in the East and West regions, since the campaign is successful here. This shows the new onboarding design is more responsive and optimized for mobile devices.
- For the North and South regions we should hold or exclude Launch. The campaign's messaging or pricing framework failed to resonate in here and would damage revenue if launched right away.
______________
### 9. Risks and Limitations
- **Operational Overload:** The support ticket rate increased by almost 10% (from 14.78% in Control to 24.79% in Treatment). This shows the new onboarding flow contains technical bugs, confusing UI elements, or problem points that are forcing nearly 1 in 4 users to contact customer support. This creates a risk of support team burnout and increased operational overhead.

- **Revenue Quality Dilution:** Average Revenue Per Converted User dropped by 52.7% (dropping from ₹1,630.10 to ₹770.41). By lowering the barrier to entry, we are shifting the company's business model from low-volume premium subscriptions to a high-volume, low-tier mass-market model. This increases server and data infrastructure costs.
_________________
### 10. Next Steps
- **Deploy Segmented Rollout:** Restrict the launch of the new onboarding campaign exclusively to Mobile and Tablet users in the East and West regions and hold North and South regions on the old onboarding for now.

- **Conduct an Audit to Fix Support Tickets:** Investigate why the support ticket rate increased to 24.79%. We must review the specific support tickets filed by Treatment users to identify and patch any specific bugs or confusing UI/UX designs causing confusion.

- **Optimize the Pricing:** Because the average value per customer dropped to ₹770.41, we to encourage these new users to upgrade to premium plans.

- **Investigate Regional Mismatch:** Run surveys specifically in the North and South regions to discover why the campaign backfired, allowing us to iterate on the onboarding for a future regional launch.
________