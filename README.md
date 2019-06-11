## Home
This package comes under **View** and it contains all the inner pages once an user is done with registration. 
We're following **package-by-component** way of structuring. So, you can find packages inside packages in the 
same way as you can travel through the application.

### Each package contains following sub-packages excluding the packages specificifically in need to that package :

* **analytics**: It contains java class that defines all the methods neeeded for analytics purpose for that particular 
                 package.
* **di**: Dependency providing classes using Dagger2 specific to that package.
* **viewmodel**: This has ViewModel for View of that package to maintain MVVM design pattern.
* **model**: This containes model classes.
* **adapter** : This containes adapter in case it's needed.

**HomeActivity is the initial start point to reach all other parts of the application.**

Typical structure of the HomeActivity goes as follows:


![image](https://i.imgur.com/F2XTZky.png)



Now let's start with individual parts.

## HomeFragment

HomeFrag is the place where you can get latest Tests, Results etc. It's also the connecting point of 
**cumulative analysis** and **nLeanCorner**. 

Below is the screens, you can navigate to from HomeFragment.

![image](https://i.imgur.com/dvLIm1r.png)

## TestFragment

TestFrag is the place where you can get all the **scheduled tests** available and then you can travel through 
and take a particular test, submit and see the result.

## PerformanceFragment

PerformanceFrag is the place where an user can get result of all the tests that S/he has taken.

## Dependency Injection (di) For PerformanceFragment


Below is the **dependency injection graph for any fragment** throughout:-


![image](https://i.imgur.com/IhE7lJ6.png)

Below is the **dependency injection graph for any Activity** throughout:-

![image](https://i.imgur.com/HfkNnZl.png)

Now, the hierachy of Performance is as follows, it shows how you can go from one screen to another inside performance.

![image](https://i.imgur.com/XwCFRjj.png)

