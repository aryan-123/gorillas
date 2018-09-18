# gorillas
//
//  Gorillas.cpp
//  Gorillas
//
//  Created by ARYAN  PILLAI on 15/09/18.
//  Copyright © 2018 ARYAN  PILLAI. All rights reserved.
//

#include <iostream>
#include <cmath>

#define G 9.80665

#ifndef MARMOSET_TESTING
int main();
#endif

double horizontal_velocity(double launch_velocity, double launch_angle);
double vertical_velocity(double launch_velocity, double launch_angle);
double gravity();
double computed_range(double launch_velocity, double launch_angle, double height);


double horizontal_velocity(double launch_velocity, double launch_angle)
{
return launch_velocity*cos(launch_angle*M_PI/180);
}

double vertical_velocity(double launch_velocity, double launch_angle)
{
return launch_velocity*sin(launch_angle*M_PI/180);
}

double gravity()
{
return G;
}

double computed_range(double launch_velocity, double launch_angle, double height)
{

return ((horizontal_velocity(launch_velocity,launch_angle)*vertical_velocity(launch_velocity,launch_angle))/gravity()) + horizontal_velocity(launch_velocity,launch_angle)*sqrt((vertical_velocity(launch_velocity,launch_angle)*vertical_velocity(launch_velocity,launch_angle))+2*height*gravity())/gravity() ;


}


#ifndef MARMOSET_TESTING
int main()
{   //part A
std::cout<<"The range the banana reaches for the launch angle of 10 degrees is "
<< computed_range(600, 10, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 20 degrees is "
<< computed_range(600, 20, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 25.5 degrees is "
<< computed_range(600, 25.5, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 30 degrees is "
<< computed_range(600, 30, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 40 degrees is "
<< computed_range(600, 40, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 50 degrees is "
<< computed_range(600, 50, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 55.5 degrees is "
<< computed_range(600, 55.5, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 60 degrees is "
<< computed_range(600, 60, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 70 degrees is "
<< computed_range(600, 70, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 75.5 degrees is "
<< computed_range(600, 75.5, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 80 degrees is "
<< computed_range(600, 80, 10)<<std::endl;

std::cout<<"The range the banana reaches for the launch angle of 90 degrees is "
<< computed_range(600, 90, 10)<<std::endl;

return 0;
}
#endif

