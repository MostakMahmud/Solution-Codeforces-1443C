# Solution-Codeforces-1443C
Here our target is to get all the foods within minimum amount of time. As it is clear in case of getting delivary from the resturants it's all about the maximum time taken from the ones we want to get delivary from as they work in prallel. For an example let time taken by them is 4,9,6 so as described before within 9 min we will get all the food. So here our task is to minimize this time. First we have to sort these time. So initially the maximum possible result is the largest one. Now let's run a loop starting from the back and check upitl which point if petya goes to the resturant time is less than courier time. This way we can minimize the max value. And in the end we just have to find the maximum value betweem courier and petya's time.
