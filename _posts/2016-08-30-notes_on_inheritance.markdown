---
layout: post
title:  "Notes on Inheritance"
date:   2016-08-30 20:32:20 +0000
---



When learning about inheritance we first learned that it is useful to reuse instance and class methods so as not to replicate code and we saw that this was good. The subclass will inherit from the superclass and is shown by using the “<” symbol to denote the relationship between the two:

**class Car < Vehicle
end**

With the above code telling us that the Car class (superclass) is inherited from the Vehicle class (the subclass) so it may use methods common to all cars. However, there is another means of denoting inheritance that uses the “::” or name-space. This form of inheritance is used for instance when inheritance is used in nested modules. For instance:

**	class Dancer
	   extend FancyDance::ClassMethods
	end**
	
The above code tells us that the ClassMethods module will inherit the methods within the FancyDance module as class methods (denoted by the “extend” keyword). So what is the difference? In the case of the Car/Vehicle relationship, the “<” shows that BMW is a type of Car AND will inherit all instance methods. On the other hand, in the Dancer class, the ClassMethods module will inherit from FancyDance modules and be will provide the class methods and constants to the Dancer class without showing a specific relationship as in the BMW is a Car scenario. 

In summary, the two notations “<” and “::” are different in that the “<” will show  that the subclass is a type of the superclass whereas the “::” notation does not and will only imply access to whatever instance or class methods (or modules) to be inherited.

