/*
 * LED.c
 *
 * Created: 02/02/19 15:24:05
 *  Author: SHIV
 */ 


#include <avr/io.h>
#include <util/delay.h>
int main(void)
{	DDRB=0b00001111;
	DDRD=0b00000100;
    while(1)
    {
		PORTB=0b00001000;
		PORTD=0b00000100;
		
		_delay_ms(5000);
		PORTB=0b00000100;
		PORTD=0b00000000;
		
		_delay_ms(5000);
		PORTB=0b00000010;
		PORTD=0b00000100;
		
		_delay_ms(5000);
		PORTB=0b00000001;
		PORTD=0b00000000;
		_delay_ms(5000);
		PORTB=0b00000000;
		PORTD=0b00000100;
		
		_delay_ms(5000);
        //TODO:: Please write your application code 
    }
}