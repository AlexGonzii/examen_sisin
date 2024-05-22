Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.hostname = "server-alexis-gonzalez"

  config.vm.provision "shell", inline: <<-SHELL
 
  echo "-- Insertar datos de ejemplo en la tabla 'Pacientes'" > /home/vagrant/datos_pacientes.sql
  echo "INSERT INTO gestion_clinica_veterinaria.pacientes (nombre,especie,raza,edad,dueño)VALUES" >> /home/vagrant/datos_pacientes.sql
  echo "('Miguel','Gato','Felino',7,'Paco')," >> /home/vagrant/datos_pacientes.sql
  echo "('Manolo','Perro','Canino',12,'Juan')," >> /home/vagrant/datos_pacientes.sql
  echo "('Raquel','Puma','Felino',13,'David')," >> /home/vagrant/datos_pacientes.sql
  echo "('Teresa','Gato','Felino',3,'Alexis')," >> /home/vagrant/datos_pacientes.sql
  echo "('Pepe','Perro','Canino',5,'Diego')" >> /home/vagrant/datos_pacientes.sql


  SHELL
end
