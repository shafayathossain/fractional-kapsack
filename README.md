### What is Knapsack Problem?

Knapsack problem is a problem of combinatorial optimization. Which means within a set of cmombination, you have to choose a combination which results best. In knapsack problem you have given a values and weight of some item. You have to choose item/s so that weight is less than or equal to the given limit of weight but value as large as possible.

### What is fractional knapsack problem?

We can choose item in seperate ways. If you are allowed to take any part of an item or fractional part of an item, them fractional knapsack problem raises. 


# Fractional Knapsack

### Algorithm for fractional knapsack

	Algorithm fractionalKnapsack(W,n)
	{
		//Let all arrays are sorted as per weight ratio of things
		//W is current maximum weight knapsack can hold
		//n is number of items
		//profit[i] is profit of i-th item where 1 <= i <= n
		//weight[i] is weight o
		//x[i] is the quantity of ith item
		
		set total_price = 0
		for i : 1 to n do
		{
			if( weight[i] <= W ) then
			{
				x[i] = 1.0;
				W = W – weight[i];
				total_price = total_price + profit[i];
			}
			else
				break;
		}
		if( i <= n )
		{
			x[i] = W / weight[i];
			total_price = total_price + ( profit[i] * x[i] );
		}
	}
