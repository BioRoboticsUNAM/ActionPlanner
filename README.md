#Action Planner

Los archivos donde programar�n sus m�quinas de estados est�n en la ruta *ActionPlanner/Tests/StateMachines*

Ah�Eencontrar�n un archivo de clase por cada una de las m�quinas de estados correspondientes a las pruebas de Robocup:

* AudioTest.cs - para Speech Recognition & Audio Detection Test
* GPSR.cs - para GPSR
* ManipulationTest.cs - para Manipulation And Object Recognition
* NavigationTest.cs - para Navigation Test
* OpenChallenge.cs - para Open Challenge
* PersonRecognition.cs - para Person Recognition Test
* Restaurant.cs - para Restaurant
* RoboNurse.cs - para Robo-Nurse
* RoboZoo.cs - para Robo-Zoo
* WakeMeUp.cs - para Wake me up test

Cada archivo cuenta con lo m��imo necesario que debe tener una m�quina de estados. Modifiquen los archivos que correspondan a las pruebas que tienen asignadas.

En la ruta *ActionPlanner/Tests/ConfigurationFiles* encontrar�n archivos de clase para la configuraci�n de cada una de las m�quinas de estados:

* AudioTest_WORLD.cs corresponde a AudioTest.cs
* GPSR_WORLD.cs corresponde a GPSR.cs
* ManipulationTest_WORLD.cs corresponde a ManipulationTest.cs
* NavigationTest_WORLD.cs corresponde a NavigationTest.cs
* OpenChallenge_WORLD.cs corresponde a OpenChallenge.cs
* PersonRecognition_WORLD.cs corresponde a PersonRecognition.cs
* Restaurant_WORLD.cs corresponde a Restaurant.cs
* RoboNurse_WORLD.cs corresponde a RoboNurse.cs
* RoboZoo_WORLD.cs corresponde a RoboZoo.cs
* WakeMeUp_WORLD.cs corresponde a WakeMeUp.cs

En estas clases pueden configurar todo lo correspondiente al estado del robot (posiciones de brazos, locations del motion planner, mensajes para el spgen, etc.). Pueden usarlos si gustan o pueden configurar todo en la m�quina de estados, como se sientan m�s c�modos.

En la ruta *ActionPlanner/ComplexActions*
encontrar�n m�quinas de estado de "uso com�n" (entrar a la arena, tomar objetos, etc). A estas las pueden mandar a llamar desde otra m�quina de estados.

En el archivo DefaultStateMachineSM.cs encontrar�n un ejemplo de una m�quina de estados simple (entrar a la arena->tomar un objeto de una mesa->dejar el objeto en otra mesa->salir de la arena) y en el archivo DefaultStateMachine_WORLD.cs la clase de configuraci�n correspondiente a la m�quina de estados. Pueden usar esto como ejemplo base (el c�digo est�Ecomentado).

As�Emismo, se separ�Ela clase Command Manager en varios archivos (uno por cada m�dulo del robot):

* HAL9000CmdMan.ARMS.cs - contiene todos los comandos para ARMS
* HAL9000CmdMan.BLK.cs - contiene todos los comandos para blackboard
* HAL9000CmdMan.OBJ_FNDT.cs - contiene todos los comandos de visi�n
* etc...

Por �ltimo, cada una de las m�quinas de estado ya tiene un bot�n de la interfaz gr�fica asociado, por lo que s�lo deber�n preocuparse de modificar la clase correspondiente a la prueba que est�n programando.