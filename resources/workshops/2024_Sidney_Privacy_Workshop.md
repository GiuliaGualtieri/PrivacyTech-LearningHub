# Sindey Privacy Workshop

https://sites.google.com/view/sydney-privacy-workshop-2024/home

## Key takeaways
- The **epsilon privacy parameter**: "the smaller, the better". Thus, “is epsilon=10 good?” We don't have a definitive answer; it depends on the applications, environment, and the required trade-off between utility and privacy as determined by the client.
- **exp(eps)** represents the worst-case scenario. With the epsilon privacy parameter as the privacy budget, you preserve privacy up to the worst-case scenario, providing guarantees against potential adversaries who possess substantial knowledge beyond the sensitive data itself. The key idea we should have in mind is that this number represents the worst-case scenario.
- Some may criticize the differential privacy parameters, stating "**nothing is that bad in the world!**" Our response is: "Ok, but you never know! By applying differential privacy with that privacy parameter, you protect the data against the worst-case scenario."
- Example: **epsilon = 50**. One might exclaim, "WOW! That's a lot! The ratio between the two probabilities is less than or equal to exp(50)." Our response: "Yes, it's large, but only because it's the upper bound for now. Perhaps in the future, we can obtain a better estimate by delving deeper into our algorithm, thereby demonstrating that we preserve more privacy and end up with exp(2), discovering that we spent less privacy budget. However, at the moment, we don't know, as differential privacy is a mathematical framework still in development. We only have one formula and some mechanisms; that's it! The idea is that, so far, worse than exp(50), you could never get."
 
Please let me know, but in my opinion, these are key concepts that have helped me to gain more confidence in understanding the concept of the privacy parameter and the significance represented by its exponential value.
