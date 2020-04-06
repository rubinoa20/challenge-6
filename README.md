// Created on Mon April 6 2020
int l_motor = 0; 
int r_motor = 2; 
int forward = 80;
int backward = -80;
int pause = 1500;

void forwards(){
    motor(l_motor,forward);
    motor(r_motor,forward);
	msleep(pause);
    ao();
}
void backwards(){
    motor(l_motor,backward);
    motor(r_motor,backward);
	msleep(pause);
    ao();
}

int main()
{
	int pig;
	
	for(pig=1; pig<=6; pig++){
		forwards();
		backwards();
		printf("pig is %d\n", pig);
	}
	
	
	printf("Hello, World!\n");
	return 0;
}
