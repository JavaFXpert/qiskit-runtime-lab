## Qiskit Runtime Lab

Instructor: James L. Weaver

Email: james.weaver@ibm.com



### Introducing this hands-on lab

This hands-on lab is a gentle introduction to quantum computing with Qiskit. This lab leverages some the latest innovations from IBM Quantum, such as Qiskit Runtime, and will help you get up to speed on the following topics and skills:

- Creating quantum circuits:
  - Visually, using the IBM Quantum Composer
  - Procedurally, using Python and the Qiskit library
- Executing quantum circuits from the Composer, and by using Qiskit Runtime
- Leveraging Qiskit Runtime Sampler and Estimator primitives, an Runtime sessions
- Executing circuits in quantum simulators as well as on IBM Quantum computers

Along the way, we'll introduce you to the brand new IBM Quantum platform, which is continually being augmented and improved. There are links to specific resources on the platform in which you'll implement the instructions of this hands-on lab as well as gain information helpful in carrying out those steps. ***Note: You may find it helpful to open these links in separate tabs so that this syllabus remains open.***

You may access this lab at any time at [ibm.co/qiskit-runtime-lab](https://ibm.co/qiskit-runtime-lab) so don't be concerned about finishing in the allotted time. It is often better to spend time internalizing concepts than to rush through the learning process. We'll begin the journey with an overview of the [IBM Quantum ](https://quantum-computing.ibm.com/)platform. ➤



### Surveying the IBM Quantum platform

Go ahead and sign in to [IBM Quantum](https://quantum-computing.ibm.com/), creating an account if you don't already have one. Then take some time to get familiar with the IBM Quantum platform, beginning with clicking the "nine dot" icon in the upper right corner of its interface and visiting the **Platform**, **Documentation** and **Learning** options. Please review this [announcement](https://docs.quantum-computing.ibm.com/announcements/product-updates/2023-08-18-new-navigation-and-application-updates) that describes how to navigate the interface, and discusses recent innovations introduced to the platform.

Let's continue the journey by creating a quantum circuit in the IBM Quantum Composer. ➤



### Creating a quantum circuit in the IBM Quantum Composer

Go ahead and navigate to the IBM Quantum Composer from the [IBM Quantum](https://quantum-computing.ibm.com/) platform by selecting **Learning** from the “nine dot” icon, and then selecting **Composer** from the IBM Quantum Learning page options. When you are in the IBM Quantum Composer, perform the following steps:

1. Open the **Composer docs & tutorials** slide-out pane on the left
2. Select the **Create your first circuit walkthrough** option, clicking **Next** to visit each step in the process.
3. Select the **Explore the latest updates** option, clicking **Next** to learn about each new feature.
4. Now create your own circuit, but instead of the two-qubit ***ϕ*****+** Bell state shown in the walkthrough, create a two-qubit ***ψ*****−** Bell state, also called a *singlet Bell state*. You can find information about the four Bell states by searching the IBM Quantum Learning site. Hint: Strategically placed ***X*** and ***Z*** gates will turn the ***ϕ*****+** Bell state into a  ***ψ*****−** Bell state.
5. The resultant **Probabilities** histogram visualization should indicate 50% probabilities of the **01** and **10** *computational basis states* being the result of measuring the quantum state.
6. The resultant **Statevector** histogram and **Q-sphere** visualizations (after ***temporarily*** removing the measurement operations) should indicate that the amplitudes and probabilities of the **01** and **10** *computational basis states* are equal to each other, but in opposite *phases*.

Nice work! Let's move on to executing your quantum circuit from the IBM Quantum Composer. ➤



### Executing your quantum circuit from the IBM Quantum Composer

To execute your quantum circuit from the IBM Quantum Composer, perform the following steps:

1. Click the Setup and Run button located near the upper right corner of the interface.
2. A pane labeled **Setup and run your circuit** should slide out from the right. 
3. Choose a quantum system or simulator to run the circuit on. The **ibm_qasm_simulator** is a good choice if there aren't any systems available with low number of **Total pending jobs**.
4. Click the **Run on <chosen system or simulator>** button in the lower right corner of the interface.
5. Click on the circular **Composer jobs** icon on the left side of the interface. 
6. When the job is finished, the **Status timeline** should indicate that it has **Completed**.
7. Click the **Details**, **Results** and **See more details** controls to learn what information about the job is available.
8. Before you leave the IBM Quantum Composer, notice that the **OpenQASM** code that can create your circuit is shown in the rightmost pane. Clicking on the **OpenQASM** label and choosing **Qiskit** will reveal Python code that can create your circuit.

Awesome! Next we'll explore how to create and run quantum circuits using Python, Qiskit libraries, and Qiskit Runtime. ➤



### Understanding Qiskit Runtime, and accessing the IBM Quantum Lab

Before tackling the coding exercise coming up, go ahead and read the [Introduction to Qiskit Runtime](https://docs.quantum-computing.ibm.com/start/runtime) to get a feel for what it is and how it can make life easier for a quantum application developer. Then head over to the IBM Quantum Lab from the [IBM Quantum](https://quantum-computing.ibm.com/) platform by selecting **Learning** from the “nine dot” icon, and then selecting **Lab** from the IBM Quantum Learning page options. The IBM Quantum Lab is a cloud based environment in which you can develop Python programs that leverage Qiskit libraries as well as IBM Quantum systems and simulators.

When you're all set, let's walk through an IBM Quantum Lab-based tutorial about Qiskit Runtime and a *primitive* known as a Sampler. ➤



### Creating and running quantum circuits using Python, Qiskit libraries, and Qiskit Runtime

From the File Browser pane on the left side of the IBM Quantum Lab, navigate to the **tutorials** folder and double-click on the **how-to-getting-started-with-sampler.ipynb** file. A Jupyter notebook entitled **Get started with the Sampler primitive** should appear. Go ahead and learn from that tutorial by running each notebook cell using the triangular run icon ▷ at the top of the notebook. When you feel prepared, get ready to write to write some Python code in the IBM Quantum Lab that leverages Qiskit, Qiskit Runtime and the Sampler primitive. ➤



### Developing a program that leverages Qiskit, Qiskit Runtime and the Sampler primitive

***Subtitle: “Life is like a box of chocolates”***

Now it time to get your hands dirty with Python and Qiskit code. Your assignment, should you choose to accept it, will be to develop a program that samples one piece from a box that contains two chocolate candies. The circuit that chooses the piece of candy will be the singlet Bell state that you created earlier in this lab. *Note: If you want more than two pieces of candy in the box, create a* [*W-state*](https://en.wikipedia.org/wiki/W_state) *that contains one qubit for each piece of chocolate from which it may choose one piece.*

To get started on this assignment, perform the following steps:

1. Navigate to the **Lab files** folder and create a new folder (using the New Folder icon) named **qiskit-runtime-lab**
2. Create a Jupyter notebook in that folder by clicking the **New file +** button and selecting **Python 3 (ipykernel)** from the **Notebook** section of the **Launcher** pane.
3. In the Quantum Lab file browser, right-click on the **Untitled.ipynb** file and **Rename** it to something like **sampler-lab-exercise.ipynb**
4. Leverage the **Using Qiskit Runtime Sampler** section of the **how-to-getting-started-with-sampler.ipynb** notebook as a guide for coding this assignment. Adding a histogram visualization of the quasi-distribution would be a nice touch, so here's a code snippet you could add to the **4. Invoke the Sampler and get results section** if you'd like:

`from qiskit.visualization import plot_histogram`
`plot_histogram(job.result().quasi_dists[0].binary_probabilities())`

Good luck, and please ask for help at any time! When you've finished this exercise, compare it to the [class solution](https://github.com/JavaFXpert/qiskit-runtime-lab/blob/main/sampler_lab_exercise_solution.ipynb), realizing that it is one of many possible solutions. Here is the [W state version of the class solution](https://github.com/JavaFXpert/qiskit-runtime-lab/blob/main/sampler_lab_exercise_w_state.ipynb). ➤



### Leveraging the Qiskit Runtime Session and the Estimator Primitive

From the File Browser pane on the left side of the IBM Quantum Lab, navigate to the **tutorials** folder and double-click on the **how-to-getting-started-with-estimator.ipynb** file. A Jupyter notebook entitled **Get started with the Estimator primitive** should appear. Go ahead and learn from that tutorial by running each notebook cell using the triangular run icon ▷ at the top of the notebook. When you're ready, we'll look at an example program that leverages Session and Estimator to optimize a box of chocolates. ➤



### Examining a program that leverages Qiskit Runtime Session and the Estimator primitive

***Subtitle: “You never know what you're gonna get”***

Continuing with our box of chocolates theme, please examine [a simple program](https://github.com/JavaFXpert/qiskit-runtime-lab/blob/main/estimator_lab_exercise_solution.ipynb) that leverages Qiskit Runtime and the Variational Quantum Eigensolver (VQE) to assemble a box of chocolates that hopefully meets our expectations. 

This program draws upon code from an example that experimental physicist & IBM Quantum researcher Nick Bronn created for the [Coding with Qiskit Runtime video series](https://www.youtube.com/playlist?list=PLOFEBzvs-VvqAC8DnVoLOzg2bKE4C7ARM), specifically in [Episode 05 Primitives & Sessions](https://youtu.be/yxuH8eb4MS4?si=e3trSORNjooWlQXu). ➤



### Thanks for playing along!

We hope you enjoyed this gentle introduction to quantum computing with Qiskit. Please don't hesitate to reach out if you have any questions. ■
