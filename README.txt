Il faut que tu installes sur ta machine le package joint_state_publisher_gui :
sudo apt-get install ros-melodic-joint-state-gui

Pour que tu puisses simuler ton modèle dans gazebo, il te manque tous les controleurs et les actuateurs. J'ai indiqué quelques exemples, mais il faudrait vraiment reprendre ton code pour le passer en XACRO, sinon, cela va vraiment être peinible.
Le mieux, serait donc que tu viennes à Jade, pour que l'on puisse te guider pas à pas.
Le problème ne vient donc pas de ton fichier launch, c'est clair.

Par ailleurs, je te conseille de renommer ton chassis en "base_link" et d'ajouter un corps "base_footprint" qui sera le parent de base_link. Il sera exactement a la meme position en liaison "fixed". Si tu ne le fais pas, il y aura une singularité numérique lors de la simulation.
