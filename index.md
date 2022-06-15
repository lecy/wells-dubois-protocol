---
layout: home
title: The Protocol
---

## The Wells-Du Bois Protocol: Mitigating Biased Practices in Data Science

----

[*Monroe-White, T., Lecy, J. The Wells-Du Bois Protocol for Machine Learning Bias: Building Critical Quantitative Foundations for Third Sector Scholarship. Voluntas (2022). https://doi.org/10.1007/s11266-022-00479-2*](https://link.springer.com/article/10.1007/s11266-022-00479-2)

-----

Data science leverages approaches in statistics and computer science/information systems to create generalizable knowledge (Dhar, 2013). Myriad recent examples of bias in machine learning models or failed AI platforms have highlighted instances of public harms resulting from the unenlightened deployment of data science applications (O’Neil, 2016). Social scientists have a vested interest in these important considerations since they utilize data from, by, and about people, so algorithmic bias or failure can cause material harm to real people and impact lives.

The Wells-Du Bois protocol is an actionable approach to avoiding harms in data science application. It is a tool inspired by the simplicity and efficacy of similar parsimonious instruments such as the Bechdel test for gender bias (Agarwal, 2018), the Apgar Score for newborn infant health (Gawande et al., 2007; Regenbogen et al., 2009), and myriad examples presented in Gawande’s Checklist Manifesto (Gawande, 2011). The core insight is that these heuristics are not perfect measures of subtle latent constructs like gender bias or health, but they are approximately as accurate as more sophisticated instruments using only a couple of questions that are simple to apply.

Data science applications can cause harm when predictions are bad, model performance varies across groups, or engineers have failed to consider nefarious uses of the tools they are building. It is a challenge to determine whether complex machine learning models are likely to fail in these ways because it requires time and resources to “stress-test” models and validate them in the real world. Developing mathematical or algorithmic tests for bias requires advanced computational and statistical expertise and a sufficient understanding of algorithmic fairness (ethics for data scientists). Solutions require the calibration of model goals more than model parameters since algorithmic fairness requires trade-offs in performance between subgroups in the data, not optimization of a global model performance metric. These tasks require expertise beyond reach for most applied data science teams or social science collaborations.

The Wells-Du Bois (WDB) protocol is a stop-gap approach to a lack of broad data science capacity in a discipline or field. It uses a simple protocol to identify common harmful practices instead of explicit tests by experts or an attempt to be exhaustive. It is designed as a checklist approach to harm reduction undertaken by scholars or system engineers before manuscript submission or model deployment.

The goal is to capture the least onerous process that will prevent the most serious instances of data science harm. Users review the protocol before project deployment and assess whether there is a high likelihood of each type of data harm in their application, then decide whether they want to fix the issue or document and disclose the risk.

Whereas social science journals have developed nuanced ways to report regression results to avoid bias from omitted variables or under-specified models, there is no equivalent reporting protocol for research generated with a large class of machine learning applications that are calibrated using predictive fit metrics. In the academic context, journals could also consider requiring authors to submit the protocol along with manuscripts that utilize machine learning algorithms as part of the peer-review process. In such a context, it would be near impossible for reviewers to detect harmful practices based on the type of information usually disclosed in a methodology section in quantitative studies.

Assumedly social science publishing practices will evolve as research methodologies evolve. As such, the WDB protocol is designed to seed discussions that will generate insights that move this conversation forward. There will ultimately be more durable solutions to these problems. In the meantime, it is an actionable step that requires a minimal amount of time and expertise to implement.

The Protocol
The Wells-Du Bois protocol is a process by which authors or engineers can assess a project to identify potential sources of harm. The protocol does not ask authors or engineers to verify that the application is free of any problems. Rather, it suggests mitigation strategies for each type of potential harm when possible and promotes transparency when mitigation is not possible. In this way, it is a good faith threshold for mitigating biased research practices.

------------


## Bad Data


### (1) Inadequate Data

Buolamwini and Gebru (2018) identified public harms caused by the deployment of facial recognition software that was calibrated with image databases that consisted of a larger number of light-skinned males than women and people with darker skin tones. As a result, the misclassification rate for darker-skinned female faces (34.7% error rate) was 43 times higher than lighter-skinned males (0.8% error rate). Poor performance that originates from lack of representation in training data disproportionately affects women of color.

**Inadequate Data Mitigation**: Representative data in most cases, but minoritized and marginalized groups, might need to be over-represented in some instances to achieve necessary sample sizes for neutral algorithms. Authors that use predictive algorithms can demonstrate harm-reduction strategies by (1) reporting sample sizes and descriptive statistics in training datasets separated out by socially constructed group identities like race or gender, and (2) reporting performance by  in this way will help to demonstrate that algorithm performance is consistent across groups. More nuanced treatments would also include considerations of intersectionality—interactions of subgroup status like race and gender—since the lived experiences of individuals in these populations are shaped by the combined effects of these and other socially constructed identities.

------------

### (2) Tendentious Data

Tendentious data are data generated by or accurately capturing human behavior in the real world. As a result, human tendencies of imperfect decision making and implicit or explicit bias are baked into the data. It will accurately reflect socially constructed realities and capture contours of human action with high fidelity. As a result, when it is used as training data for machine learning models it will generate predictions that mirror biases present in society.

For example, Amazon built an artificial intelligence system to automate the review of thousands of applications they get for engineering positions. The system performed amazingly well at identifying highly qualified male engineers, but because it was trained using resumes from previous hiring processes and they had historically hired more male engineers than female engineers the algorithm penalized women and filtered out many highly qualified female candidates (Christian, 2020).

The problem was not in the construction of a training dataset, and it was not an algorithm that performs poorly. It is that real-world data were used to train a system and the algorithm accurately reproduced human bias that was encoded in the data. The tendentious data predisposed the machine learning models toward unfair predictions. The crux of the problem is that the algorithm is accurately predicting how Amazon recruiters behaved in the past (which is what it was trained to do), not whether a candidate can do the job well (which is what we want). Tendentious data produce models that are predisposed to the same cognitive inconsistencies or biases as the humans that generated the training data.

In a more subtle example, the over-policing of Black neighborhoods will result in higher arrest rates for Black citizens. As a result, predictive recidivism risk models will over-estimate their propensity of Black defendants to commit future crimes, deeming them as a higher risk than they are in reality (Dressel & Farid, 2018). In their study of more than more than 10,000 criminal defendants, ProPublica investigative journalists found that Black defendants were twice as likely to be misclassified as higher risk when compared to white defendants (Angwin et al., 2016).

The challenge is that arrest data accurately captures the number of arrests made by police, but it will over-represent the latent criminality of Black people because of the legacy of discrimination in the US criminal justice system. Thus, it both accurately represents the phenomenon of arrest but is biased in estimating the likelihood a Black defendant will commit a future crime or act of violence. Thus, it will generate tendentious predictive models that perform poorly when measured against objective reality.

**Tendentious Data Mitigation**: Disclose whether outcomes used in a training dataset are socially constructed latent constructs (i.e., intelligence, status, effectiveness, performance) that will reflect subjective human judgements or consist of administrative or archival data produced by human actors. For example, typing speed is a fairly objective and robust performance measure, but anything subjective like teacher evaluations will be prone to human bias.

It is usually not possible to fix the data. Once bias gets baked into the data, it reflects the realities of the world and models can only be fit to the subjective interpretations (human tendencies) that are present in the data. Awareness and disclosure of the issue is a starting point. Better, less subjective data is a more durable longer-term solution, but that requires time and resources needed to create calibrated outcomes (e.g., technical assessments for job candidates instead of only resumes).

Some bias-mitigation strategies might also be possible. In the policing case, for example, train the models using subsets of crimes that are more objective in nature like armed robberies. Compare those models to similar ones trained on crimes that are more subjective in nature, like traffic stops. That may help to quantify the amount of bias in the model. Predictions made from the models could then be corrected by reducing risk scores from that category of race by the level of bias estimated from the differences observed in risk associated with subjective versus objective outcomes. These techniques are commonly called “instrumental variables” in econometrics and are imperfect solutions. But beyond simply identifying and disclosing the problem while waiting for better data, they are one feasible approach to some level of bias mitigation.

------------


## Bad Algorithms (Algorithmic Bias)

### (3) Harms of Identity Proxy

In many contexts where machine learning models enhance or replace human decision making, such as approval for a loan or credit card, laws forbid the explicit use of protected classes as a criterion for being denied a service (race, ethnicity, gender, language, and disability status). As a result, these variables are excluded from models to promote fairness and avoid lawsuits. However, they do not need to be explicit in models to be present. The role they serve in making algorithms biased or unfair can be fulfilled by identity proxies—composites of other variables in the model that predict the protected class with high accuracy.

The previous example of Amazon’s attempt to build an AI system to identify the best job candidates from the mountains of resumes they receive demonstrates the challenge of identity proxies as well. They trained their algorithms using resumes from past positions that were filled and calibrating the models based on who was actually hired from the candidate pools. Historic bias in hiring decisions led to algorithms that systematically excluded women from the list of top candidates in the current list of resumes. Once engineers recognized this problem they were horrified so they removed gender from variables considered by the model, expecting that to resolve the issue. What they quickly discovered, however, is that resumes are full of gender proxies.

The algorithms could predict the gender of candidates based on things like their first name, which sports they listed (softball vs baseball), hobbies or interests (anything that mentioned “women’s”), or which schools they attended (all-women’s colleges were penalized). These examples seem somewhat obvious and could be mitigated by editing the algorithm once identified. The problem was that gender was deeply embedded in resumes in subtle ways that are hard to identify, such as the vocabulary used by candidates. The algorithms awarded points for the appearance of words like “executed” and “captured,” which are more prevalent on male resumes. It proved to be impossible to identify and neutralize all gender proxies, so Amazon scrapped the project (Christian, 2020). Race and other subgroup proxies manifest in similar ways in data.

How pernicious is the problem? Some recent studies have shown how powerful machine learning algorithms have become at identifying patterns that are imperceptible to humans but can serve as signatures of group membership. For example, Bansal et al. (2012) used a support vector machine to predict the gender of a patient from an image of the iris, a result that surprised medical professionals since male and female irises look the same to humans. Similarly, Banerjee et al. (2021) showed AI can predict a patient’s race from an X-ray despite the fact that physicians were unaware of any known correlations between features on medical images and race. They show that “detection is not due to trivial proxies or imaging-related surrogate covariates for race, such as underlying disease distribution” and that “performance persists over all anatomical regions and frequency spectrum of the images suggesting that mitigation efforts will be challenging.”

These examples demonstrate how much information is unintentionally encoded in data. Amazon did not anticipate that gender would permeate all aspects of a candidate’s resume. Bansal and Banerjee’s teams were not designing medical imaging techniques that optimize detection of gender or race. They simply used archives of eye images or X-rays to demonstrate how powerful machine learning algorithms have become at detecting patterns that are invisible to experts. The lesson they demonstrate is that it is an unrealistic assumption that algorithms are not making predictions based on protected classes simply because variables like race, gender, or disability status are not explicitly present in models. Identity proxies are ubiquitous.

**Identity Proxy Mitigation**: Instead of dropping a category like race from the model, assuming it solves the problem, test for the presence of identity proxies. Make race the dependent variable in the model while retaining the other covariates. If you can accurately predict race or another protected class with the remaining covariates in your model, identity proxies are present. Using predictive models when identity proxies are present violates the spirit of protections afforded to historically disadvantaged classes. When relevant to the research, report whether identity proxies can be detected in the data.

------------


### (4) Harms of Subpopulation Difference

Harms of subpopulation difference arise when algorithm performance varies by subgroup within the data. For example, it is possible for a new drug to have a net positive population effect but when data are disaggregated, it can be shown to harm a subpopulation. While federal drug approval processes now account for subpopulation differences, there are no standards to hold corporations accountable for subpopulation harm resulting from algorithms.

The extent of this problem was only recently uncovered. In 2016 ProPublica conducted a high-profile review of the COMPAS algorithm that predicts the risk of an incarcerated criminal committing a future crime if released. They found that algorithm to be biased against Black prisoners, assigning risk scores that were higher than justified by their actual observed behavior once released (Angwin et al., 2016). Stated differently, if a white prisoner and a black prisoner were assigned the same risk score, the white prisoner was more likely to recidivate. Black prisoners were being refused parole at higher rates as a result.

ProPublica’s in-depth investigative reporting served as a lightning rod of sorts for machine learning scholars with expertise in algorithmic fairness, catalyzing a flurry of studies on the topic and an important breakthrough. The fact that the COMPAS algorithm was generating risk scores that were inconsistent across race was not a bug in their specific machine learning algorithm, but a feature of all machine learning models. Chouldechova (2017) and Pleiss et al. (2017) were able to prove that it is mathematically impossible to build machine learning models that perform consistently across subgroups in the data when baseline rates of the outcome differ by subgroup. In other words, the issue was not a poorly specified model in inadequate data inputs. Rather, it is a fundamental feature of machine learning models when baseline rates of the outcome vary by subgroups within the data. These examples of racialized bias are just one example of a larger conversation within the data science and ML ethics community surrounding persistent public value failures surrounding machine learning applications in the public domain (Monroe-White & Marshall, 2019).

**Subpopulation Difference Mitigation**: There is no easy fix to the problem of machine learning models that perform differently for each subpopulation within the data. Mathematical proofs have shown that it is impossible to fix the issue using a different model specification or better data. Mitigation is less about solving the issue and more about recognizing the issue before you build or deploy your algorithm.

COMPAS failed because the algorithm designers defined fairness by calibrating risk scores using false positives alone (Angwin, et al., 2016). The risk scores produced by the models did in fact accurately predict whether an individual was likely to be re-arrested after release, regardless of race. But performance varied wildly on the other criteria–false negatives, whether an individual remained locked up when they were unlikely to commit a future crime. The algorithm deemed blacks much riskier than was supported by the data, so risk scores were much higher than they should have been. This result in a scenario where if you put inmates into risk categories, within each category white inmates were given lower risk scores and were much more likely to receive parole than Black inmates that had a similar likelihood of recidivism.

Publications that use machine learning classifiers should examine outcomes across various protected subgroup classes in the data like race and gender to determine whether baseline rates differ by group. If so, recognize that it is impossible to build a model that will perform similarly for all subgroups. With just two subgroups like data that only includes individuals from White and Black race categories, the models can achieve balanced false positive rates but have disparate rates of false negatives, or achieve balanced false negative rates and have disparate rates of false positives. They cannot achieve balance in both (Kleinberg et al., 2016). The more subgroups there are present, the harder it is to achieve balance.

Mitigation starts with awareness or the issues that arise when subgroups have different baseline performances in the data and disclosure of baseline rates, as well as reporting model performance statistics separately for subgroups to quantify the extent of the difference. That would meet a minimal requirement of fairness operationalized as transparency.


------------


## Bad Models 


### (5) Harms of Misfit Models

Models become misfits when they are optimized by minimizing the wrong type of error or preferencing the wrong outcome. Minimizing model error instead of maximizing model benefit. One of the lessons from the field of machine learning is that less accurate models are generally more useful. This relationship arises because of two model features: (1) model accuracy can be improved by overfitting data and (2) the most powerful machine learning models (e.g., neural networks) generate highly accurate results that no one understands and consequently are harder to translate into practice.

**Misfit Models Mitigation**: The ML community has developed many practices like cross-fold validation to avoid over-fitting and has evolved an ethos of valuing simple models or assemblages of simpler models that offer insights to experts and decision-makers over black-box oracles.


------------


## Bad Humans (Human Intent)


### (6) Do No Harm

Most data science failures are cases where models are biased in subtle ways or performance deviates from expectations. The first item in the checklist asks, however, is the intent of the deployment to cause harm? For example, Cambridge Analytica used sophisticated data analytics to target marginalized and minoritized populations with misinformation to create a sense of frustration with the political process and make it less likely for the targeted individuals to vote (Schneble et al., 2018). Similarly, spatial analytics can be used to gerrymander voting districts to distort representation. In both cases, the goals are to suppress votes and undermine the democratic process, which one can argue are nefarious goals. In these examples there are no algorithmic failures or undetected bias. The models perform perfectly well, but their intent is to disadvantage or harm a subpopulation.

**Do No Harm Commitment**: Can you confirm that your true intent matches the intent that is described in your manuscript or project documentation? Is the intent to benefit populations equally, or to advance objectives of fairness or justice?

------------

### (7) Harms of Ignorance

In many cases, algorithms perform amazingly well on their intended tasks, but deployment does not consider potential harm, especially in sensitive racial or gender contexts. For example, Noble (2018) documents how Google’s keyword search algorithms returned pornographic and profane images as top results when “Black girls” or “Black women” were used as search terms. The search algorithm generally performed well in most contexts, but there was no proactive consideration for what might happen when deployed without safeguards in contexts where exploitation has been historically prevalent. The most pernicious examples of harmful practices are more likely unintended consequences that are difficult to anticipate when new technologies are deployed in unfamiliar or complex environments. Harms of ignorance are more aptly characterized as uncontemplated consequences—a sort of willful ignorance that results when scholars or engineers (composed primarily of While and Asian males) have not considered possible harms to minoritized groups (i.e., Asian women, Black males, etc.). Unintended consequences are hard to anticipate, whereas uncontemplated consequences could have been anticipated through a reasonable level of rumination.

**Mitigating Harms of Ignorance**: Heath and Heath (2013) promote the use of pre-mortem analysis to avoid mistakes in business. These exercises occur prior to the launch of a new product or service, and require teams to sit down together and write a hypothetical obituary for the project. The exercise forces them ahead of time to determine the most likely reasons that a project will fail. This sort of brainstorming then allows the team to protect against the most likely threats to success as they begin to implement the project. Similarly, to mitigate harms of ignorance scholars or engineers should entertain the question, what’s the worst possible outcome that could result from this work? Are there specific groups that might be vulnerable to disproportionate harm by a failure of the algorithm? In the domain of research scholars should ask, could the data collected for this research, or the tools developed through the work be used for nefarious purposes that are different from their original intent?



