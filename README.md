# Submission of QOSF Mentorship Screening Task
## Task-4: Find the lowest eigenvalue of the given matrix
- First I tried to find out eigenvalues and the one which is lowest among them for Hamiltonian classically
- I first tried to simulate VQE without noise 
  - For that I have first decomposed the hamiltonian in terms of linear combination of the tensor products of Pauli operators.
  - Then I have applied the Variational method to get the minimum energy
  - Created a function so that we can measure in all three basis  
  - I calculated the expectation values in Z basis and calculated summation of them. This function I designed it such that it will work for both Noiseless and Noise cases.
  - Applied minimize function to find the opimal parameter with method as **COBYLA**.
  - Plotted a graph to get better understanding by first getting expectation values for different parameters ranging from *-π* to *π*.
  - Doing this, I was able to obtain the eigenvalue ≈ *-0.9995*. 
- Next I have tried to simulate VQE with noise.
  - First I tried to understand the Noise Model which constructs an approximate noise model, then passing the basis gates and coupling map. Also I tried to understand the qubit properties for device_backend I used.
  - Created a similar function to summation with some minor changes
  - Repeating the penulltimate step used in Noiseless simulation with again some minor changes
  - Again simulated graph but now the graph was looking different and the eigenvalue obtained was ≈ *-0.7751*.
  - I tried to overlay the graphs where I got good intuition of the effect of noise on the circuit created along with intuition of what would be the outcome achieved, if we run this on a real quantum computer.
