# 📊 Multi-Factor Pricing Optimization Framework  
## E-Commerce Catalog Strategy Case Study  

---

## 👤 Author

**Ritesh Yadav**  
Data Analyst | Business & Pricing Strategy  

- GitHub: https://github.com/Ritesh01010  
- LinkedIn: https://www.linkedin.com/in/ritesh-yadav-406331240  

---

# 1. Executive Summary

This project presents a structured pricing optimization framework for an e-commerce catalog containing multiple SKUs with varying cost structures, demand patterns, inventory levels, and competitive pressures.

The objective was to design a scalable, data-driven pricing system that:

- Protects profitability  
- Responds to demand signals  
- Adjusts for inventory risk  
- Aligns with competitive market conditions  

Instead of reactive pricing, a rule-based analytical framework was implemented to generate SKU-level recommended prices while maintaining margin discipline.

---

# 2. Business Problem

The catalog exhibited inconsistent pricing decisions due to:

- Rapid stock-outs in high-demand SKUs  
- Overstock accumulation in slow-moving products  
- Misalignment with competitor price bands  
- Margin erosion in high-competition segments  

The company required a repeatable pricing logic that balances:

- Growth  
- Profitability  
- Operational stability  

---

# 3. Data Sources & Signals Used

The pricing model integrates multiple business signals.

## 3.1 Cost Structure

- Product Cost  
- FBA Fee  
- Storage Fee  
- Handling Cost  
- Minimum Acceptable Margin %  
- Target Gross Margin %  

---

## 3.2 Demand Metrics

- Sessions  
- Units Ordered  
- Conversion Rate

**Conversion Rate Formula:**
- Conversion Rate = Units Ordered / Sessions

Demand classification:

- STRONG → Above-average conversion rate  
- WEAK → Below-average conversion rate  

---

## 3.3 Inventory Health

- Days of Supply  
- Sell-through metrics  

Inventory classification:

- LOW_STOCK → Days of Supply < 30  
- HEALTHY → 30–90  
- OVERSTOCK → > 90  

---

## 3.4 Competitive Positioning

- Average Competitor Price  
- Lowest Competitor Price  
- Highest Competitor Price  
- Competitor Count  

These define the market pricing envelope.

---

# 4. Pricing Framework Logic

The pricing engine follows a structured sequence.

---

## 4.1 Step 1: Profitability Floor

**Total Unit Cost =**
- Product Cost + FBA Fee + Storage Fee + Handling Cost

**Minimum Price =**
Total Unit Cost / (1 − Minimum Margin)

This ensures no SKU is sold below profitability threshold.

---

## 4.2 Step 2: Target Margin Price

Target Price = Total Unit Cost / (1 − Target Margin)


Establishes the strategic profitability objective.

---

## 4.3 Step 3: Inventory-Based Adjustment

- LOW_STOCK → Increase price by 10%  
- OVERSTOCK → Decrease price by 10%  
- HEALTHY → No adjustment  

Purpose: Balance stock pressure and capital efficiency.

---

## 4.4 Step 4: Demand-Based Adjustment

- STRONG demand → Increase price by 5%  
- WEAK demand → Reduce price by 5%  

Purpose: Capture willingness to pay while supporting slow-moving SKUs.

---

## 4.5 Step 5: Competitive Alignment

If adjusted price:

- Exceeds 110% of lowest competitor → Reposition to 105%  
- Falls below 90% of average competitor → Reposition to 95%  
- Otherwise → Maintain adjusted price  

Purpose: Avoid price wars while staying market-relevant.

---

## 4.6 Step 6: Margin Protection Rule

Final Recommended Price = MAX(Competition_Adjusted_Price, Minimum_Price)

Guarantees profitability protection across all SKUs.

---

# 5. Analytical Findings

## 5.1 Inventory Impact on Pricing

Low-stock SKUs supported price increases without harming competitiveness.  
Overstocked SKUs required margin sacrifice to improve inventory velocity.

---

## 5.2 Demand Signal Effectiveness

Conversion rate effectively differentiated pricing power across SKUs.  
High-demand products tolerated moderate price increases.

---

## 5.3 Competitive Pressure Analysis

High competitor density constrained upward pricing flexibility.  
Low competition SKUs allowed improved margin capture.

---

## 5.4 Margin Discipline Evaluation

No SKU was recommended below minimum viable pricing threshold.  
Profit integrity was preserved across the catalog.

---

# 6. Business Impact Simulation

Using historical sales volumes, the framework supports:

- Improved margin capture in strong-demand SKUs  
- Reduced capital lock-in in overstocked items  
- Controlled competitive price drift  
- Standardized pricing governance  

The model enables consistent, repeatable pricing decisions instead of manual adjustments.

---

# 7. Strategic Insights

- Pricing must integrate operational signals, not just cost  
- Inventory risk and demand elasticity are interconnected  
- Competitive benchmarking must be guided, not blindly followed  
- Structured pricing improves scalability in growing catalogs  

---

# 8. Limitations & Future Enhancements

Future improvements may include:

- Demand elasticity modeling  
- Predictive demand forecasting  
- Weighted multi-factor scoring models  
- Dynamic ad-performance integration  
- Scenario simulation dashboards  

---

# 9. Conclusion

This project demonstrates the development of a multi-signal pricing optimization framework combining financial discipline with operational intelligence.

The model is:

- Scalable  
- Transparent  
- Data-driven  
- Business-aligned  

It provides a structured foundation for evolving toward more advanced predictive pricing systems.

---



