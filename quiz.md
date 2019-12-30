# Optimization with Genetic Algorithm
___
**Instructions**

Hello, congratulations and thank you for taking part in this Internal Training on Genetic Algorithm. To test your abilities, let's do the quiz.
___
 
1. Which one is not an optimization problem?
   - [ ] Finding the shortest path
   - [ ] Forecasting future demand
   - [ ] Maximize profit



2. Which statement is **WRONG** about Genetic Algorithm
   - [ ] Genetic Algorithm is inspired by biological evolution
   - [ ] Genetic Algorithm can only has one optimal solution
   - [ ] Genetic Algorithm can only has one optimal fitness value



3. A pool of solutions in Genetic Algorithm is called:
   - [ ] Population
   - [ ] Chromosomes
   - [ ] Genes

 

___
**Instructions for number 4-10**

You are going to spend a month in the wilderness. You're taking a backpack with you, however, the maximum weight it can carry is 20 kilograms. You have a number of survival items available, each with its own number of survival points. The bigger survival points you have, the higher your chance to survive. But don't forget about your backpack weight limit.

Use `survival.csv` in your data to answer the questions. 
___

4. What is the objective on the problem above?
   - [ ] Minimize survival points
   - [ ] Maximize total weight 
   - [ ] Maximize survival points constrained by total weight



5. What is the constraint for the problem?
   - [ ] Weight limit > 20
   - [ ] Surival point <= 20
   - [ ] Weight limit <= 20



```
weightlimit <- 20

evalFunc <- function(x) {
  df <- df[x == 1, ]
  total_weight <- sum(df$weight)
  total_survival <- sum(df$survivalpoints)
  
  # Put the constraint
  total_survival <- ...
  
  return(total_survival)
}
```

6. Complete the function above to create the fitness function

   - [ ] ifelse(total_weight >= weightlimit , 0 , total_survival )
   - [ ] ifelse(total_weight <= weightlimit , 0 , total_survival )
   - [ ] ifelse(total_weight >= weightlimit , total_survival , 0 )



7. What is the type of encoding we will use?
   - [ ] binary
   - [ ] real-valued
   - [ ] permutation



```
library(GA)

ga_survive <- ga(type = ...., fitness = ...., nBits = ..., popSize = 100, maxiter = 100, run = 20, seed = 123)
```


8. The algorithm will stop on the following condition, EXCEPT ...
   - [ ] Reach iteration 123
   - [ ] No improvement on the best solution after 20 iteration
   - [ ] Reach iteration 100



9. What is the optimal survival points?
   - [ ] 20
   - [ ] 102
   - [ ] 67.38



10. What item we should not bring based on the optimal solution?
    - [ ] potatoes
    - [ ] pocketknife
    - [ ] rope
