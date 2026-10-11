COMPILADOR = g++
# -O1 como base para luego estudiar las mejoras de rendimiento con -O2 y -O3
OPCIONES = -O1 -std=c++17 -Wno-unused-result
PROGRAMA = simplemd.x
OBJETOS = Random.o Vector.o simplemd.o

# compilar el proyecto (make)
all: $(PROGRAMA)

$(PROGRAMA): $(OBJETOS)
	$(COMPILADOR) $(OPCIONES) -o $(PROGRAMA) $(OBJETOS)

%.o: %.cpp
	$(COMPILADOR) $(OPCIONES) -c $< -o $@

# ejecutar la aplicación con el caso de prueba (make run)
run: $(PROGRAMA)
	./$(PROGRAMA) < in

# eliminar los archivos generados durante la compilación (make clean)
clean:
	-rm -f $(OBJETOS) $(PROGRAMA) output.xyz trajectory.xyz energies.dat rdf_step_*.dat