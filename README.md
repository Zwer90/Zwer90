- /*
project for Introduction to Programming (COMP 209)
                             team members:
                             Zainab Almubarak
                             Zainab Alnahab
                             Zainab alrashed
                             Hawra Algrash
*/
#include<iostream>
#include<cmath> 
using namespace std;
const float G = 9.8f;
float getPotential(float weight,float height){
return weight*height*G ;
}
float getKinetic(float weight,float speed){
return weight*pow(speed,2)/2 ; 
}
float getTotal(float weight,float speed,float height){
return getPotential(weight,height)+getKinetic(weight,speed);
}
float getWork(float force,float distance){
return force*distance ;
}
int main(){
cout<<"Welcome To The Physics Program"<<endl<<endl;

int choice ;

 do{
	    cout<<"Please Choose A Physical Law From The Menu Below:"<<endl<<"1.Potential Energy"<<endl<<"2.Kinetic Energy"<<endl<<"3.Total Energy"
<<endl<<"4.Work"<<endl<<"5.Exit"<<endl<<"Your Choice : ";

      

    cin>>choice ;
     float weight,speed,height,distance,result=0 ;
     switch(choice){
         case 1:
           cout<<"Enter The Weight (kg) : ";
          cin>>weight;
         cout<<"Enter The Height (m) : ";
         cin>>height;
        result = getPotential(weight,height);
           cout<<"Potential Energy = "<<result<<" J"<<endl;
                break;
        case 2:
             cout<<"Enter The Weight (kg) : ";
            cin>>weight;
            cout<<"Enter The Speed (m/s) : ";
            cin>>speed;
         result = getKinetic(weight,speed);
            cout<<"Kinetic Energy = "<<result<<" J"<<endl;
            break;
        case 3:
                cout<<"Enter The Weight (kg) : ";
             cin>>weight;
            cout<<"Enter The Height (m) : ";
             cin>>height;
             cout<<"Enter The Speed (m/s) : ";
             cin>>speed;
             result = getTotal(weight,speed,height);
             cout<<"Total Energy = "<<result<<" J"<<endl;
              break;
        case 4:
            cout<<"Enter The Force (N) : ";
            cin>>weight;
            cout<<"Enter The Distance (m) : ";
           cin>>distance;
          result = getWork(weight,distance);
           cout<<"Work = "<<result<<" J"<<endl;
              break; 
        case 5: 
                cout << "Exiting program" << endl;
                break;
        default:
                cout << "Invalid choice" << endl;   
       }
           } while (choice <=4); 

    return 0;
}


