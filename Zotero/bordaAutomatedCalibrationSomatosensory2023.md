---
category: literaturenote
tags: 
citekey: bordaAutomatedCalibrationSomatosensory2023
status: read
---

> [!Cite]
> Borda, Luigi, Noemi Gozzi, Greta Preatoni, Giacomo Valle, and Stanisa Raspopovic. “Automated Calibration of Somatosensory Stimulation Using Reinforcement Learning.” _Journal of NeuroEngineering and Rehabilitation_ 20, no. 1 (September 26, 2023): 131. [https://doi.org/10.1186/s12984-023-01246-0](https://doi.org/10.1186/s12984-023-01246-0).

>[!Synth]
>**Contribution**:: 
>
>**Related**:: 
>

>[!md]
> **FirstAuthor**:: Borda, Luigi  
> **Author**:: Gozzi, Noemi  
> **Author**:: Preatoni, Greta  
> **Author**:: Valle, Giacomo  
> **Author**:: Raspopovic, Stanisa  
~    
> **Title**:: Automated calibration of somatosensory stimulation using reinforcement learning  
> **Year**:: 2023   
> **Citekey**:: bordaAutomatedCalibrationSomatosensory2023  
> **itemType**:: journalArticle  
> **Journal**:: *Journal of NeuroEngineering and Rehabilitation*  
> **Volume**:: 20  
> **Issue**:: 1   
> **Pages**:: 131  
> **DOI**:: 10.1186/s12984-023-01246-0    

> [!LINK] 
>
>  [Borda et al. - 2023 - Automated calibration of somatosensory stimulation.pdf](file://C:\Users\emzpe\Zotero\storage\9HDE746I\Borda%20et%20al.%20-%202023%20-%20Automated%20calibration%20of%20somatosensory%20stimulation.pdf).

> [!Abstract]
>
> Background  The identification of the electrical stimulation parameters for neuromodulation is a subject-specific and time-consuming procedure that presently mostly relies on the expertise of the user (e.g., clinician, experimenter, bioengineer). Since the parameters of stimulation change over time (due to displacement of electrodes, skin status, etc.), patients undergo recurrent, long calibration sessions, along with visits to the clinics, which are inefficient and expensive. To address this issue, we developed an automatized calibration system based on reinforcement learning (RL) allowing for accurate and efficient identification of the peripheral nerve stimulation parameters for somatosensory neuroprostheses.
Methods  We developed an RL algorithm to automatically select neurostimulation parameters for restoring sensory feedback with transcutaneous electrical nerve stimulation (TENS). First, the algorithm was trained offline on a dataset comprising 49 subjects. Then, the neurostimulation was then integrated with a graphical user interface (GUI) to create an intuitive AI-based mapping platform enabling the user to autonomously perform the sensation characterization procedure. We assessed the algorithm against the performance of both experienced and naïve and of a brute force algorithm (BFA), on 15 nerves from five subjects. Then, we validated the AI-based platform on six neuropathic nerves affected by distal sensory loss.
Results  Our automatized approach demonstrated the ability to find the optimal values of neurostimulation achieving reliable and comfortable elicited sensations. When compared to alternatives, RL outperformed the naïve and BFA, significantly decreasing the time for mapping and the number of delivered stimulation trains, while improving the overall quality. Furthermore, the RL algorithm showed performance comparable to trained experimenters. Finally, we exploited it successfully for eliciting sensory feedback in neuropathic patients.
Conclusions  Our findings demonstrated that the AI-based platform based on a RL algorithm can automatically and efficiently calibrate parameters for somatosensory nerve stimulation. This holds promise to avoid experts’ employment in similar scenarios, thanks to the merging between AI and neurotech. Our RL algorithm has the potential to be used in other neuromodulation fields requiring a mapping process of the stimulation parameters. Trial registration: ClinicalTrial.gov (Identifier: NCT04217005)
>.
> 
# Notes
>.


# Annotations%% begin annotations %%


### Imported: 2023-10-25 4:18 pm



<mark style="background-color: #2ea8e5">Quote</mark>
> When compared to alternatives, RL outperformed the naïve and BFA, significantly decreasing the time for mapping and the number of delivered stimulation trains, while improving the overall quality. Furthermore, the RL algorithm showed performance comparable to trained experimenters. Finally, we exploited it successfully for eliciting sensory feedback in neuropathic patients.

<mark style="background-color: #2ea8e5">Quote</mark>
> The technique exploiting invasive neural interfaces (i.e., implantable electrodes) [11–14] and non-invasive transcutaneous stimulation (i.e., TENS) [15–18] has been successfully tested in upper and lower limb amputees

<mark style="background-color: #2ea8e5">Quote</mark>
> The calibration procedure of a sensory neuroprostheses consists of a trial-and-error process, where the neurostimulation parameters are manually changed by a user (e.g., therapist, clinicians, or technicians) according to the produced outcome (e.g., in case of sensory restoration the patient’s answer), with the help of custom-made platforms [21].

<mark style="background-color: #2ea8e5">Quote</mark>
> Furthermore, the neurostimulation parameters may vary over time due to adaptation to stimulation [26

<mark style="background-color: #2ea8e5">Quote</mark>
> In RL, a software agent makes observations and takes actions within an environment receiving rewards in return. The agent learns, thanks to a positive or negative reward, which are the best actions to undertake in order to achieve a specific goal [32].

<mark style="background-color: #2ea8e5">Quote</mark>
> ndeed, in somatosensory prosthetics, the subject is required to report in detail the electrically-evoked sensation [21, 34, 35]. The resulting quality of the perceived sensation can be captured in a reward that the RL agent can use to optimize the neurostimulation parameters based on the subjects’ feedback in order to evoke a more effective and reliable artificial sensation.

<mark style="background-color: #2ea8e5">Quote</mark>
> The RL algorithm was firstly tested offline using a dataset collecting 888 trials from 49 independent subjects with TENS neurostimulation parameters

<mark style="background-color: #2ea8e5">Quote</mark>
> Typically, the pulse amplitude and pulse width values are modulated keeping the frequency value fixed at 50 Hz

<mark style="background-color: #5fb236">Quote</mark>
> The user selects a reasonable pulse width, and a pulse amplitude ramp is performed until the minimum value that makes the sensation somatotopic is identified.

<mark style="background-color: #2ea8e5">Quote</mark>
> Once the pulse amplitude value is defined, a pulse width ramp is performed to find the minimum and maximum non-painful perceived sensation.

<mark style="background-color: #2ea8e5">Quote</mark>
> 0.5mA amplitude resolution in PA and 1us width resolution in pulse width. Therefore, changing first PA provides bigger steps for faster convergence, while the following PW ramp allows a finer and resolute modulation.

<mark style="background-color: #e56eee">Quote</mark>
> VR, with purposely-designed scenarios and highly-controlled environments, is a widely used tool for neurotechnologies applications [18, 36–39]

<mark style="background-color: #2ea8e5">Quote</mark>
> The initial low-level parameters, indeed, were chosen from the dataset (Table 1), based on the subject’s gender and targeted nerve, to ensure higher safety and less discomfort.

<mark style="background-color: #2ea8e5">Quote</mark>
> This algorithm is formalized through a Markov’s decision-making process (MDP) (S, A, p, r). The state transition function p: S × A × S → [0, ∞) gives the distribution of the next state, St+1 based on the current state St and action At [42].

<mark style="background-color: #2ea8e5">Quote</mark>
> Deep Q-Network (DQN) method, a combination of Q-learning, a popular reinforcement learning algorithm, and artificial neural network (ANN)

<mark style="background-color: #2ea8e5">Quote</mark>
> The Q-function estimates the expected cumulative rewards for taking a specific action in a given state. It is a model-free, online, off-policy reinforcement learning method. A DQN agent is a value-based reinforcement learning agent that trains a critic to estimate the return or future reward

<mark style="background-color: #2ea8e5">Quote</mark>
> agent explores the action space using an ε-greedy policy to balance exploration (it chooses random actions with probability ε) and exploitation (selects the action with the highest estimated reward with probability 1 - ε)

<mark style="background-color: #2ea8e5">Quote</mark>
> agent learns by minimizing the difference between its predicted rewards and the actual rewards it receives. It does this by updating the neural network’s parameters using a technique called batch updating.

<mark style="background-color: #2ea8e5">Quote</mark>
> The perceived threshold is indeed proportional to the injected charge, which follows Q = PA * PW. However, as described by the strengthduration curve, it is important to take into account the rheobase (i.e., the threshold current required to excite a neural tissue when the pulse width tends to infinity) and the chronaxie  (i.e., the minimum time required for an  electric current  two times the  rheobase  to stimulate the neural tissue).

<mark style="background-color: #2ea8e5">Quote</mark>
> rheobase currents and the chronaxie change with the diameter of the sensory fibers [44], distance from the nerve, age [45], and pathological conditions (e.g., significant higher rheobase for polyneuropathy with respect to healthy [46]) among others, making impossible to fix a-priori stimulus current for all tested subjects and pathologies.

<mark style="background-color: #2ea8e5">Quote</mark>
> For this purpose, we created a data-driven machine learning environment that learned this relationship from a dataset built from previous neurostimulation experiments carried out on 49 subjects (Table 1). After receiving specific neurostimulation parameters (PW and PA) as inputs, our simulated environment returns as outputs the level of perceived intensity, the type and the location of the elicited sensation similarly to a real subject.

<mark style="background-color: #5fb236">Quote</mark>
> Specifically, the environment comprised three different models (Fig. 2B) trained using the MATLAB Classification and Regression Learner toolboxes (See Additional file 1: Sec 1.3):

<mark style="background-color: #2ea8e5">Quote</mark>
> In the online implementation, the environment has been replaced by the recruited subject

<mark style="background-color: #2ea8e5">Quote</mark>
> state is represented by three components which include the information about the perceived intensity, type and location of the electrically-evoked sensation

<mark style="background-color: #2ea8e5">Quote</mark>
> However, the perceived intensity level not perceived was considered as a single state because the patient would not be able to describe the type and location of a not-perceived sensation.

<mark style="background-color: #2ea8e5">Quote</mark>
> we attributed an increasing negative reward for the uncomfortable states and increasing positive reward for the desired ones. A zero reward was instead assigned to the not perceived state.

<mark style="background-color: #2ea8e5">Quote</mark>
> B During the offline training the environment is simulated through three different machine learning models trained on a dataset of neurostimulation experiments mimicking answers of subjects, for intensity, type and location elicited.

<mark style="background-color: #2ea8e5">Quote</mark>
> PA and PW. Two arrays have been defined: a PA array made of 16 values ranging from 1 to 16 mA; a PW array made of 54 values ranging from 70 μs to 600 μs. The resolution of each array was 1 mA and 10 μs, respectively.

<mark style="background-color: #2ea8e5">Quote</mark>
> Modulating either one or both simultaneously allows the RL to perform larger or smaller steps towards the optimal state, according to the distance from it.

<mark style="background-color: #2ea8e5">Quote</mark>
> An episode could end in two ways: (1) the agent reached a state where the perceived intensity level was classified as too high which implied the failure of that episode; (2) the maximum number of iterations was reached which implied the success of the characterization.

<mark style="background-color: #2ea8e5">Quote</mark>
> The BFA algorithm performed monotonic increasing ramps of PA and PW until the optimal parameters were found

<mark style="background-color: #5fb236">Quote</mark>
> The four conditions (i.e., expert user, naïve experimenter, RL-algorithm, BFA) were randomly presented to the subjects.

<mark style="background-color: #2ea8e5">Quote</mark>
> The quality index is a measure defined to evaluate the quality of the mapping during characterization.

<mark style="background-color: #2ea8e5">Quote</mark>
> The value of the quality index ranged from 0 to 1, as follows:

<mark style="background-color: #2ea8e5">Quote</mark>
> The normality of the distributions has been checked using the Kolmogorov-Smirnov test. A nonparametric Friedman’s test to compare the experimental condition on outcome measures was used.

<mark style="background-color: #2ea8e5">Quote</mark>
> post-hoc analysis with Wilcoxon signed-rank tests was conducted with a Bonferroni correction applied, resulting in a significance level set at p < 0.0083.

<mark style="background-color: #2ea8e5">Quote</mark>
> The offline environment was fitted using previously collected data (888 trials from 49 subjects, Table 1).

<mark style="background-color: #2ea8e5">Quote</mark>
> Convergence was considered achieved when the parameters did not change for five consecutive iterations. A state was considered correct if the desired level of perceived intensity was reached

<mark style="background-color: #2ea8e5">Quote</mark>
> The low-level agent showed an accuracy of 88.51% (

<mark style="background-color: #2ea8e5">Quote</mark>
> the high-level agent showed an accuracy of 98.64%

<mark style="background-color: #5fb236">Quote</mark>
> RL algorithm was the fastest to perform the sensation mapping

<mark style="background-color: #2ea8e5">Quote</mark>
> RL: 4.6 ± 2.7 min; Exp: 7.3 ± 3.0 min; Wilcoxon p > 0.0083)

<mark style="background-color: #5fb236">Quote</mark>
> Among the three conditions of which performance was evaluated with respect to the Expert (i.e., RL, Naive and BFA) the RL was the only one that on average presented a decrease in time

<mark style="background-color: #2ea8e5">Quote</mark>
> n 74% of cases the RL took less time than the Expert

<mark style="background-color: #2ea8e5">Quote</mark>
> RL was higher than the expert, reporting in 53% of the characterizations performed a sensation quality index higher than the latter. On the second day of testing, the RL algorithm showed

<mark style="background-color: #2ea8e5">Quote</mark>
> The results are reported in terms of injected charge values for the low- and high-level, sensation location elicited over the foot and type of evoked sensation.

<mark style="background-color: #2ea8e5">Quote</mark>
> Overall, the high-level agent showed better performance than the low-level agent, likely due to the different type of initialization of the stimulation parameters for the two agents.

<mark style="background-color: #2ea8e5">Quote</mark>
> the high-level agent started from the parameters previously found by the lowlevel agent.

<mark style="background-color: #5fb236">Quote</mark>
> The RL algorithm required comparable time to an expert experimenter, released a comparable quantity of charge but with a substantially lower number of stimulations.

<mark style="background-color: #2ea8e5">Quote</mark>
> RL outperformed BFA for all evaluation metrics

<mark style="background-color: #2ea8e5">Quote</mark>
> two neuropathic individuals with reduced nerve integrity. Although the algorithm was trained on healthy data, it was able to successfully complete the calibration with high sensation quality

<mark style="background-color: #2ea8e5">Quote</mark>
> . Therefore, our results support the potential of the RL algorithm in other neuroprosthetics applications [66

<mark style="background-color: #2ea8e5">Quote</mark>
> Finding the placement of the TENS electrodes in order to obtain a somatotopic sensation remains a timeconsuming procedure, particularly when sensory deficits are present.

<mark style="background-color: #2ea8e5">Quote</mark>
> peripheral neuropathy which has been tested. The number of subjects should drastically increase to evaluate the performance of the RL algorithm considering also different degrees of lesion.

<mark style="background-color: #2ea8e5">Quote</mark>
> Indeed, a personalized RL would allow specific state transition probability for each subject (also depending on the degree of lesion), possibly improving the time and number of steps required to calibrate.


%% end annotations %%

%% Import Date: 2023-10-25T16:18:35.490-04:00 %%

# Journal Club
Can an RL algo characterize stim params faster + w/ better quality than human experimenters 

9 actions of AI to modulate PW + PA

RehaMove3 stimulator: CE approved 

Not compared with a "smarter" algo like binary search algo
- Why ML used here 

Why VR???

Time includes subj response time

Fig 3: some data points where Quality for RL is high and expert is not

**Discussion**
Location placement not included!
Apply to homegoing to reduce time for system tuning 
More useful if parameters were changing over time and could predict that
Take home users will become expert users

Not addressing source of problem: cuff location, contact, participant variability
- Healthy subjs, same location, no skin variation considered


Train a network on different stim patterns: what pattern will make sensationus more natural 