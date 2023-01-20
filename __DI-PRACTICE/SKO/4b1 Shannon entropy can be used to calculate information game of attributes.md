https://learning.oreilly.com/library/view/data-science-for/9781449374273/ch03.html#threedot2dot2_extended_example_attribute
![[Pasted image 20230112154233.png]]
*Figure 3-3. Entropy of a two-class set as a function of p(+).*

![[Pasted image 20230112154259.png]]
![[Pasted image 20230112154313.png]]

Parent has 30 instances (16 dots, 14 stars)
![[Pasted image 20230112154339.png]]
Entropy of *left child*
![[Pasted image 20230112154359.png]]
Entropy of *right* child
![[Pasted image 20230112154416.png]]
Calculating *information gain*
![[Pasted image 20230112154425.png]]

![[Pasted image 20230112151509.png]]
*Figure 3-4. Splitting the “write-off” sample into two segments, based on splitting the Balance attribute (account balance) at 50K.*

![[Pasted image 20230112154638.png]]
![[Pasted image 20230112151541.png]]
*Figure 3-5. A classification tree split on the three-valued Residence attribute.*

Table 3-1. The attributes of the Mushroom dataset^[ [[Foster, Fawcett-Data Science for Business]] pg 49 -62]
| Attribute name           | Possible values                                                                      |
| ------------------------ | ------------------------------------------------------------------------------------ |
| CAP-SHAPE                | bell, conical, convex, flat, knobbed, sunken                                         |
| CAP-SURFACE              | fibrous, grooves, scaly, smooth                                                      |
| CAP-COLOR                | brown, buff, cinnamon, gray, green, pink, purple, red, white, yellow                 |
| BRUISES?                 | yes, no                                                                              |
| ODOR                     | almond, anise, creosote, fishy, foul, musty, none, pungent, spicy                    |
| GILL-ATTACHMENT          | attached, descending, free, notched                                                  |
| GILL-SPACING             | close, crowded, distant                                                              |
| GILL-SIZE                | broad, narrow                                                                        |
| GILL-COLOR               | black, brown, buff, chocolate, gray, green, orange, pink, purple, red, white, yellow |
| STALK-SHAPE              | enlarging, tapering                                                                  |
| STALK-ROOT               | bulbous, club, cup, equal, rhizomorphs, rooted, missing                              |
| STALK-SURFACE-ABOVE-RING | fibrous, scaly, silky, smooth                                                        |
| STALK-SURFACE-BELOW-RING | fibrous, scaly, silky, smooth                                                        |
| STALK-COLOR-ABOVE-RING   | brown, buff, cinnamon, gray, orange, pink, red, white,     yellow                                                                                     |
| STALK-COLOR-BELOW-RING   |brown, buff, cinnamon, gray, orange, pink, red, white,     yellow                                                                                      |                                                                    
| VEIL-TYPE                     |partial, universal                                                                                      |
| VEIL-COLOR                    |brown, orange, white, yellow                                                                                      |
| RING-NUMBER                   |none, one, two                                                                                      |
| RING-TYPE                     |cobwebby, evanescent, flaring, large, none, pendant, sheathing, zone                                                                                      |
| SPORE-PRINT-COLOR             |black, brown, buff, chocolate, green, orange, purple, white, yellow                                                                                      |
| POPULATION                    |abundant, clustered, numerous, scattered, several, solitary                                                                                      |
| HABITAT                       |grasses, leaves, meadows, paths, urban, waste, woods                                                                                      |
| EDIBLE? (**Target variable**) |   yes, no                                                                                   |


![[Pasted image 20230112153803.png]]
*Figure 3-6. Entropy chart for the entire Mushroom dataset. The entropy for the entire dataset is 0.96, so 96% of the area is shaded.*

![[Pasted image 20230112153827.png]]
*Figure 3-7. Entropy chart for the Mushroom dataset as split by GILL-COLOR. The amount of shading corresponds to the total (weighted sum) entropy, with each bar corresponding to the entropy of one of the attribute’s values, and the width of the bar corresponding to the prevalence of that value in the data.*

![[Pasted image 20230112153851.png]]
*Figure 3-8. Entropy chart for the Mushroom dataset as split by SPORE-PRINT-COLOR. The amount of shading corresponds to the total (weighted sum) entropy, with each bar corresponding to the entropy of one of the attribute’s values, and the width of the bar corresponding to the prevalence of that value in the data.*

![[Pasted image 20230112153929.png]]
*Figure 3-9. Entropy chart for the Mushroom dataset as split by ODOR. The amount of shading corresponds to the total (weighted sum) entropy, with each bar corresponding to the entropy of one of the attribute’s values, and the width of the bar corresponding to the prevalence of that value in the data.*