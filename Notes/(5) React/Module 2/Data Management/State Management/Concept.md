Often, while building full-fledged React apps, some components need to access and use other components’ state. 

As an example, say, a React app consists of two components `Drives` and `FuelTank`. 


![[Pasted image 20231118123154.png|450]]


Each `drive` costs $10\%$ of the `fuelLeft`. In other words, 

	1 drive = 10 fuelLeft


So, `drivesLeft` is *a function of* `fuelLeft`. Or simply, `drivesLeft` needs to access `fuelLeft` for the calculations.

This is not possible as `fuelLeft` and `drivesLeft` are State variables and cannot be accessed by other components.

### The Solution
There are multiple solutions for this problem.

* #### [[Prop-Drilling]]
* #### [[Lift the State Up]]
* #### [[Context API]]

