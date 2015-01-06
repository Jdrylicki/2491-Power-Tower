#include <WPILib.h>
#include <math.h>

class TestRobot : public SimpleRobot
{
    Joystick *Rjoystick, *Ljoystick;
    Talon *Rmotor, *Lmotor, *lifterO, *lifterT, *loaderO, *loaderT
    Timer *timer
    
public:
      TestRobot()
      {
      
        	Lmotor = new Talon(1);
		      Rmotor = new Talon(2);
		
	    	  lifterO = new Talon(5);
		      lifterT = new Talon(6);
		    
	     	  loaderO = new Talon(7);
		      loaderT = new Talon(8);
		
		      Rjoystick = new Joystick(1);
		      Ljoystick = new Joystick(2);
		      
		      timer = new Timer;
		      timer->Start();
		      timer->Reset();
		  }    
		   void OperatorControl()
	      {	
	        motorLeft->Set(joystickLeft->GetY() * fabs(joystickLeft->GetY()));
		    	motorRight->Set(joystickRight->GetY() * fabs(joystickRight->GetY()) * -1.0);
		    	int totecount = 0
		    	if(Rjoystick->GetRawButton(4){
		      
		      	Wait(2);
		    	
		    	  while(totecount < 7);
		    	  { 
		    	    totecount++
		    	    Wait (1);
		    	    
		    	    loaderO->Set(0.5);
		    	    loaderT->Set(-0.5);
		    	    
		    	    Wait(1.5);
		    	    
		    	    loaderO->Set(0.0);
		    	    loaderT->Set(0.0);
		    	    
		    	    Wait(0.1);
		    	    
		    	    lifterO->Set(0.5);
		    	    lifterT->Set(-0.5);
		    	    
		    	    Wait(1);
		    	    
		    	    lifterO->Set(0.0);
		    	    lifterT->Set(0.0);
		    	    
		    	    Wait(10);
		    	    }
		    	  
