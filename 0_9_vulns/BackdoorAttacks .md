Vulnerability Name

backdoor attacks on LLM

Author(s):
Shanyang Fu

Description:
The backdoor attack mentioned here is completely different from the backdoor in traditional attack. The traditional backdoor is a code written and implanted into a computer. In the case of backdoor attacks in large language models, the attack is achieved by modifying the training data. After the data training is completed, the backdoor is implanted inside the model. When facing samples with triggers, the backdoor attack is triggered.
Backdoor attacks are somewhat similar to data poisoning, but they differ in that data poisoning attacks affect the overall accuracy and significantly degrade the performance of the model. In contrast, backdoor attacks maintain the inference accuracy for benign samples (i.e., without triggers), and only when facing samples with triggers, the inference will produce the attacker's desired results.

Labels/Tags:

•	 Label: "backdoor attacks "

•	 Label: " Backdooring Attacks on Deep Neural Networks "

•	 Label: " backdoor poisons"

•	 Label: “Trigger”

Common Examples of Vulnerability:

Example 1: The attacker implants a pre-selected backdoor data into the model training data. After the training is completed, the backdoor is embedded within the model. When the model is deployed, if it encounters input samples with triggers, the backdoor attack is triggered, causing inference errors and achieving the desired effect for the attacker.

Example 2: Many data annotation tasks are outsourced to external companies. The attacker bribes an employee from the outsourcing company to inject pre-prepared backdoor data into the training data. After the training is completed, the backdoor is implanted within the model. When the model is deployed, if it encounters input samples with triggers, the backdoor attack is triggered.

How to Prevent:

Prevention Step 1: Verify legitimacy of data sources and data within，Verify supply chain of the Training Data if sourced externally as well as maintaining attestations, similar to SBOM (Software Bill of Materials) methodology.

Prevention Step 2: Ensure the security and integrity of the data processing environment and the data handling processes, minimizing the risk of introducing backdoor data.

Prevention Step 3: Employ white-box or black-box mechanisms to detect the presence of backdoors in the model.

Prevention Step 4: Enhance the robustness of the model and improve its resistance to backdoor attacks.

Example Attack Scenarios:
Scenario #1: Training the model with unverified data sources creates a vulnerability where an attacker can embed backdoor data within these datasets. Once the model is trained, the backdoor is implanted in the model weights. When trigger samples are inputted, the attack is triggered.

Scenario #2: Outsourcing the model training process to a vendor team introduces a risk where an attacker can infiltrate the outsourcing team and inject backdoor data into the training data. After the model is trained, the backdoor is implanted in the model weights. When trigger samples are inputted, the attack is triggered.

Reference Links:
1.	https://arxiv.org/abs/2007.10760   Backdoor Attacks and Countermeasures on Deep Learning: A Comprehensive Review
2.	https://arxiv.org/abs/1902.06531   STRIP: A Defence Against Trojan Attacks on Deep Neural Networks
3.	https://people.cs.rutgers.edu/~sm2283/papers/NDSS18.TNN.pdf  Trojaning Attack on Neural Networks 
