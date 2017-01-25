# fractional-kapsack
###Algorithm for fractional knapsack is as following:
######Algorithm fractional_knapsack(W,n) 
######{
######&nbsp;&nbsp;&nbsp;&nbsp;//Let all arrays are sorted as per weight ratio of things
######&nbsp;&nbsp;&nbsp;&nbsp;//W is current maximum weight knapsack can hold
######&nbsp;&nbsp;&nbsp;&nbsp;//n is number of items
######&nbsp;&nbsp;&nbsp;&nbsp;//profit[i] is profit of i-th item where 1 <= i <= n
######&nbsp;&nbsp;&nbsp;&nbsp;//weight[i] is weight o
######&nbsp;&nbsp;&nbsp;&nbsp;//x[i] is the quantity of ith item
######&nbsp;&nbsp;&nbsp;&nbsp;set total_price = 0
######&nbsp;&nbsp;&nbsp;&nbsp;for i : 1 to n do
######&nbsp;&nbsp;&nbsp;&nbsp;{
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;if( weight[i] <= W ) then
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;{
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;x[i] = 1.0;
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;W = W – weight[i];
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;total_price = total_price + profit[i];
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;}
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;else
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;break;
######&nbsp;&nbsp;&nbsp;&nbsp;}
######&nbsp;&nbsp;&nbsp;&nbsp;if( i <= n )
######&nbsp;&nbsp;&nbsp;&nbsp;{
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;x[i] = W / weight[i];
######&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;total_price = total_price + ( profit[i] * x[i] );
######&nbsp;&nbsp;&nbsp;&nbsp;}
######}
