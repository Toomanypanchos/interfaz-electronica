# interfaz-electronica
sesiones Arduino 

// primer codigo 
//Agregar comentarios en el codigo para tu yo futuro y diveros lectores
//Pancho
//24 marzo 2023
int tiempoActual = 0;

int tiempoRojo = 5;
int tiempoAmarillo= 3;
int tiempoVerde = 7;

color rojo = color(255, 0 , 0);
color amarillo = color(255, 255, 0);
color verde = color (0, 255, 0);


void setup () {
  //size (800, 1000);
  fullScreen ();
  background (255, 70, 0);
  noCursor();
}


void draw() {
  tiempoActual = millis();
  tiempoActual = tiempoActual /1000;
  println(tiempoActual);
  
  if (tiempoActual < tiempoRojo) {
    
    background(rojo);
  }
  else if (tiempoActual < tiempoRojo + tiempoAmarillo) {
    
    background(amarillo);
  }
   else if (tiempoActual < tiempoRojo + tiempoAmarillo + tiempoVerde) {
    
    background(verde);
  }
    else if (tiempoActual > tiempoRojo + tiempoAmarillo + tiempoVerde) {
    
    background(55, 80 ,150);
  }
    ellipse(mouseX, mouseY, 40, 40);

}
