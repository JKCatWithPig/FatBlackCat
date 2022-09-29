# Arduino RGB Final #CODE

// RGB light programmed by JK FatBlackCat

#define RED 11
#define YELLOW 12
#define GREEN 13

// the setup function runs once when you press reset or power the board
void setup() {

  // initialize digital pin LED_BUILTIN as an output.
  pinMode(RED, OUTPUT) ;
  pinMode(YELLOW, OUTPUT) ;
  pinMode(GREEN, OUTPUT) ;

}

void blink( int light, int duration, int times ) 
{
  for( int i=0 ; i<times ; i++ )
  {
    digitalWrite(light, HIGH) ;
    delay(duration) ;
  }
}

void UnBlink( int light, int duration, int times ) 
{
  for( int i=0 ; i<times ; i++ )
  {
    digitalWrite(light, LOW) ;
    delay(duration) ;
  }
}
// the loop function runs over and over again forever
void loop() {

  blink( RED, 1000, 1 ) ;
  UnBlink( RED, 250, 1 ) ;

  for( int j=1 ; j<=3 ; j++ ) {
    blink( YELLOW, 250, 1) ;
    UnBlink( YELLOW, 250, 1 ) ;
  }

  blink( GREEN, 1000, 1) ;
  UnBlink( GREEN, 250, 1) ;

  for( int j=1 ; j<=3 ; j++ ) {
    blink( YELLOW, 250, 1) ;
    UnBlink( YELLOW, 250, 1 ) ;
  }

}