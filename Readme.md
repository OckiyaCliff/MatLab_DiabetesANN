## ANN on Diabetes Patient ##

- Run first the MPC controlle based on Hovorka Model.
- Then you can run the ANN controller
- The two main function are well commented.

## Abstract ##

An Artificial Pancreas was implemented using an Artificial Neural Network
that maintains the glucose levels of patients with type 1 diabetes. The neural network takes as input many parameters of the patient’s Glucose-Insulin
system and calculates the controller output (insulin flow rate) based only on
the current values of the Glucose-Insulin system. In other words, the neural network does not take into account the history of the parameters of the
patients. First an accurate representation of the Glucose - Insulin system
of human body is modelled. The mathematical used here is the Hovorka
model (insert reference here). Hovorka utilises a compartment model which
represents the glucoregulatory system and includes submodels representing
absorption of subcutaneously administered insulin and gut absorption. To
generate the data for training our neural network, an reference controller
was used. The reference controller employed was Model Predictive Control.
The controller samples the glucose system parameters every 15 minutes and
gives the insulin flow rate as output. A custom cost function is used that not
only minimises the controller effort but also the rate of change to provide a
smoother controller output. Moving target trajectory facilitates slow, controlled normalization of elevated glucose levels and faster normalization of low
glucose values. Data is then collected from this control scheme for different
initial values of glucose concentrations and different meal times and quantities so that the ANN controller can be effective under diverse conditions.
The neural network trained uses multilayer feed-forward back-propagation
that relates the output to the inputs by hyperbolic tangent sigmoid transfer
function and optimized by Levenberg-Marquardt, the training of the ANN
was successfull with R is approaching to 1 (R is a measure of the ANN performance. 1 is best possible result). The generated ANN was then used as
a controller and the Insulin - Glucose system was simulated, the ANN was
successfully able to maintain normoglycemia. In conclusion, ANN is viable
for use as an Artificial Pancreas and this methodology provides many advantages over direct implementation of MPC such as faster speed. (add more
reasons here).



#   M a t L a b _ D i a b e t e s A N N 
 
 
