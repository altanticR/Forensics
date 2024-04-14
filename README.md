# Forensics
To Detect the Hacking Tools Used Based on the PCPAP files

## Description
This program discusses the development of a machine learning (ML) program designed to identify specific hacking activities using forensic evidence from PCAP files, which are data files created by network analyzers like Wireshark. These files capture packet data across various layers of the Open Systems Interconnection (OSI) model, providing a rich source of data that, once converted to a human-readable format, can help forensic investigators identify suspicious activities like DDoS attacks and port scanning. However, manually analyzing these files is inefficient and challenging, especially given their potentially vast size and the static nature of human expertise in recognizing novel network threats. Thus, this program employs supervised ML to automatically learn from and identify patterns indicative of three types of network scans: port scanning, OS scanning, and host scanning.

To effectively train the ML models, the program leverages a variety of network traffic data encapsulated in the PCAP files. Specific features extracted for the ML process include different types of network scans—port, OS, and host scans, which are differentiated by aspects such as TCP flags, TTL, Packet Size, Window Size, and Maximum Segment Size. These scans vary in their methodologies; for example, port scanning involves sending packets to various ports to determine their status, while OS scanning, or fingerprinting, identifies a host's operating system based on characteristics of the packets it emits. For each scan type, the program considers a range of protocols and TCP flags to enrich the dataset used for ML.

The ML methodology follows a structured process involving data preparation, algorithm testing, and model improvement to enhance predictive accuracy. The ML framework utilized includes decision trees, random forests, k-nearest neighbors (KNN), and support vector classification (SVC). These models are trained on labeled datasets that are meticulously prepared and encoded, ensuring a balanced representation of different network scans. Cross-validation methods are employed to validate the models’ effectiveness and minimize overfitting, helping establish robust predictions of hacking activities.

Finally, the paper underscores the program’s capacity to automate the detection of network scans, thereby significantly aiding forensic investigators. The use of ML not only expedites the analysis of complex and large datasets but also enhances the detection capabilities beyond the limitations of manual analysis. Future work will focus on improving data processing automation, exploring advanced feature engineering techniques, and possibly integrating deep learning algorithms to broaden the scope of detectable activities and improve overall model performance. This progression aims to refine the program’s accuracy and utility in real-world applications, making it a powerful tool in the ongoing effort to secure networks against a variety of cyber threats.

## Contributing
We welcome any and all contributions! Here are some ways you can get started:
1. Report bugs: If you encounter any bugs, please let us know. Open up an issue and let us know the problem.
2. Contribute code: If you are a developer and want to contribute, follow the instructions below to get started!
3. Suggestions: If you don't want to code but have some awesome ideas, open up an issue explaining some updates or imporvements you would like to see!
4. Documentation: If you see the need for some additional documentation, feel free to add some!

## Instructions
1. Fork this repository
2. Clone the forked repository
3. Ensure that Sklearn, Matplotlib and Fast_ml packages are installed. If you require any of the packages, 
3a. Install Fast-ml package by running "pip install fast-ml" in your python terminal.
3b. Install Scikit-learn package by running "pip install scikit-learn" in your python terminal.
3c. Install Matplotlib package by running "pip install matplotlib" in your python terminal.
4. Commit and push
5. Wait for pull request to be merged
