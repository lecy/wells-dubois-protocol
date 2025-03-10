---
layout: home
title: The Protocol
---

## The Wells-Du Bois Protocol: Mitigating Biased Practices in Data Science

{:toc}

----

[*Monroe-White, T., Lecy, J. The Wells-Du Bois Protocol for Machine Learning Bias: Building Critical Quantitative Foundations for Third Sector Scholarship. Voluntas (2022). https://doi.org/10.1007/s11266-022-00479-2*](https://link.springer.com/article/10.1007/s11266-022-00479-2)

[[PDF](https://github.com/lecy/wells-dubois-protocol/raw/main/articles/wells-dubois-protocol.pdf)]

-----

Data science leverages approaches in statistics and computer science/information systems to create generalizable knowledge (Dhar, 2013). Myriad recent examples of bias in machine learning models or failed AI platforms have highlighted instances of public harms resulting from the unenlightened deployment of data science applications (O’Neil, 2016). Social scientists have a vested interest in these important considerations since they utilize data from, by, and about people, so algorithmic bias or failure can cause material harm to real people and impact lives.

The Wells-Du Bois protocol is an actionable approach to avoiding harms in data science application. It is a tool inspired by the simplicity and efficacy of similar parsimonious instruments such as the Bechdel test for gender bias (Kagan et al. 2020), the Apgar Score for newborn infant health (Gawande et al., 2007; Regenbogen et al., 2009), and several examples discussed in Gawande’s Checklist Manifesto (Gawande, 2011). The core insight is that heuristic decision rules cannot perfectly detect or measure latent constructs like health or gender bias, but they are approximately as accurate as more sophisticated instruments that require more information or data that is hard to collect.

Data science applications can cause harm when predictions are bad, model performance varies across groups, or engineers have failed to consider nefarious uses of the tools they are building. It is a challenge to determine whether complex machine learning models are likely to fail in these ways because it requires time and resources to “stress-test” models and validate them in the real world. Developing mathematical or algorithmic tests for bias requires advanced computational and statistical expertise and a sufficient understanding of algorithmic fairness (ethics for data scientists). Solutions require the calibration of model goals more than model parameters since algorithmic fairness requires trade-offs in performance between subgroups in the data, not optimization of a global model performance metric. These tasks require expertise beyond reach for most applied data science teams or social science collaborations.

The Wells-Du Bois (WDB) protocol is a stop-gap approach to the low-level of data science capacity in many social science disciplines or fields. It uses a simple protocol to identify common harmful practices instead of explicit tests by experts or an attempt to be exhaustive. It is designed as a checklist approach to harm reduction undertaken by scholars or system engineers before manuscript submission or model deployment.

**The goal of the protocol is to operationalize the least onerous process necessary to prevent the most serious instances of data science harm.** Users review the protocol before project deployment and assess whether there is a high likelihood of each type of data harm in their application, then decide whether they want to fix the issue or document and disclose the risk.

Whereas social science journals have developed nuanced ways to report regression models to avoid bias from omitted variables or misspecification, there is no equivalent reporting protocol for research generated with machine learning applications that are calibrated using predictive fit metrics. 

In the academic context, journals could also consider requiring authors to submit the protocol along with manuscripts that utilize machine learning algorithms as part of the peer-review process. In such a context, it would be near impossible for reviewers to detect harmful practices based on the type of information usually disclosed in a methodology section of most quantitative studies. In such circumstances check-lists have proved to be highly-effective in harm reduction (Gawande, 2011). 

Assumedly social science publishing practices will evolve as research methodologies evolve. As such, the WDB protocol is designed to seed discussions that will generate insights that move this conversation forward. There will ultimately be more durable solutions to these problems. In the meantime, it is an actionable step that requires a minimal amount of time and expertise to implement.

**The Protocol**

The Wells-Du Bois protocol is a process by which authors or engineers can assess a project to identify potential sources of harm. The protocol does not ask authors or engineers to verify that the application is free of any problems. Rather, it suggests mitigation strategies for each type of potential harm when possible and promotes transparency when mitigation is not possible. In this way, it is a good faith threshold for mitigating biased research practices.

**High Stakes**

Bias in research limits our understanding of social phenomenon and our ability to design effective policy. Over the long-run, though, science can be self-correcting through replication, new studies, better data, and impoved methods. Frameworks that help us understand machine learning bias are more consequential in the real-world, however, where stakes may be high. 

[Violations of hijab laws come with serious consequences but questionable due process regarding algorithm veracity](https://www.deseret.com/utah/2023/1/11/23550122/iran-using-facial-recognition-techology-enforce-hijab-law):

> Iran’s Headquarters for Promoting Virtue and Preventing Vice, Mohammad Saleh Hashemi Golpayegani, announced in an interview that the government was planning to use surveillance technology against women in public places following a new decree signed by the country’s hardline president, Ebrahim Raisi, on restricting women’s clothing.

> The country’s national identity database, built in 2015, includes biometric data like face scans and is used for national ID cards and to identify people considered dissidents by authorities.

> Mahsa Alimardani, who researches freedom of expression in Iran at the University of Oxford, has recently heard reports of women in Iran receiving citations in the mail for hijab law violations despite not having had an interaction with a law enforcement officer. 

_**Notably, in cases like this there is no record of training data, no disclosure of accuracy rates, and no recourse if you are misidentified by an algorithm.**_ 

Algorithms are increasingly deployed in these types of high stakes contexts with inadequate protections in place for instances in which the algorithms fail. As a result, we hope this framework and [similar tools](https://onlinelibrary.wiley.com/doi/10.1111/jiec.13509) will advance the development and use of generalizable protocols that can minimize technoharm in an increasingly digital world.   

------------



# Bad Data


## (1) Inadequate Data

Buolamwini and Gebru (2018) identified public harms caused by the deployment of facial recognition software that was calibrated with image databases that consisted of a larger number of light-skinned males than women and people with darker skin tones. As a result, the misclassification rate for darker-skinned female faces (34.7% error rate) was 43 times higher than lighter-skinned males (0.8% error rate). Poor performance that originates from lack of representation in training data disproportionately affects women of color.

**Inadequate Data Mitigation**: Harm can be mitigated by representative training data in most cases, but in some instances minoritized and marginalized groups may need to be over-represented to achieve sample sizes necessary for accurate within-group inferences, especially in data-intensive models like neutral networks. Authors that use predictive algorithms can demonstrate harm-reduction strategies by (1) reporting sample sizes and descriptive statistics in training datasets broken down by group identities like race or gender, and (2) reporting performance in a similar way to demonstrate the level of model consistency across subgroups. More nuanced treatments would also include considerations of intersectionality through interactions of subgroup status like race and gender.

**In the News**

[Eight Months Pregnant and Arrested After False Facial Recognition Match](https://www.nytimes.com/2023/08/06/business/facial-recognition-false-arrest.html)

> Porcha Woodruff is the first woman known to be wrongfully accused as a result of facial recognition technology.
> 
> She was getting her two daughters ready for school when six police officers showed up at her door in Detroit. They asked her to step outside because she was under arrest for robbery and carjacking. “Are you kidding?” she recalled saying to the officers, said she gestured at her stomach to indicate how ill-equipped she was to commit such a crime: She was eight months pregnant.
> 
> After being charged in court with robbery and carjacking, Ms. Woodruff was released that evening on a $100,000 personal bond. In an interview, she said she went straight to the hospital where she was diagnosed with dehydration and given two bags of intravenous fluids. A month later, the Wayne County prosecutor dismissed the case against her.


[Facial recognition mistake leads to wrong man being arrested and thrown in jail for SIX days - despite never visiting Louisiana](https://www.dailymail.co.uk/news/article-11593521/Facial-recognition-technology-blamed-mistaken-arrest-Louisiana-purse-snatching-case.html)

> In July, New Orleans City Council voted to allow police to use facial recognition after several people complained about privacy issues, NOLA reported. Police can use facial recognition to identify suspects of violent crimes after all other tactics failed.
> 
> Louisiana authorities' use of facial recognition technology led to the mistaken arrest of a Georgia man on a fugitive warrant, an attorney said in a case that renews attention to racial disparities in the use of the digital tool. 
> 
> Facial recognition systems have faced criticism because of their mass surveillance capabilities, which raise privacy concerns, and because some studies have shown that the technology is far more likely to misidentify Black and other people of color than white people, which has resulted in mistaken arrests.
> 
> A National Institute of Standards and Technology (NIST) study conducted in 2019 found two algorithms assigned the wrong gender to black females 35 percent of the time.


------------

## (2) Tendentious Data

Tendentious data are data generated by or accurately capturing human behavior in the real world. As a result, human tendencies of imperfect decision making and implicit or explicit bias are baked into the data. It will accurately reflect socially constructed realities and capture contours of human action with high fidelity. As a result, when it is used as training data for machine learning models it will generate predictions that mirror biases present in society.

For example, Amazon built an artificial intelligence system to automate the review of thousands of applications they receive annually for engineering positions. The system performed amazingly well at identifying highly qualified male engineers, but because it was trained using data from past hiring processes it had one huge blind spot. Historically Amazon had hired more male engineers than female engineers so the algorithm penalized women in the model and filtered out many highly qualified female candidates (Christian, 2020).

The problem was not in the construction of the training dataset nor was it an algorithm that performed poorly. Rather, the algorithm accurately reproduced human bias that was encoded in the real-world data that was used to train a system. The tendentious data predisposed the machine learning models toward unfair predictions of candidate fit. The crux of the problem is that the algorithm was accurately predicting how Amazon recruiters behaved in the past (which is what it was trained to do), not whether a candidate would do the job well if hired (which is the information Amazon actually wanted). Tendentious data produce models that are predisposed to the same cognitive inconsistencies or biases as the humans that generated the training data.

In a more subtle example, the over-policing of Black neighborhoods will result in higher arrest rates for Black citizens. As a result, predictive recidivism risk models will over-estimate the propensity of Black defendants to commit future crimes, deeming them as a higher risk than they are in reality (Dressel & Farid, 2018). In their study of more than more than 10,000 criminal defendants, ProPublica investigative journalists found that Black defendants were twice as likely to be misclassified as higher risk when compared to white defendants (Angwin et al., 2016).

The challenge is that arrest data accurately captures the number of arrests made by police, but it will over-represent the latent criminality of Black people because of the legacy of discrimination in the US criminal justice system. Thus, it both accurately represents the phenomenon of arrest but is biased in estimating the criminality of a Black defendant (their likelihood to commit a future crime or act of violence). Thus, tendentious data will generate predictive models that perform poorly when measured against objective reality.

**Tendentious Data Mitigation**: Disclose whether outcomes used in a training dataset are socially constructed latent constructs (i.e., intelligence, status, effectiveness, performance) that will reflect subjective human judgements or consist of administrative or archival data produced by human actors. For example, typing speed is a fairly objective and robust performance measure, but anything subjective like teacher evaluations will be prone to human bias.

It is usually not possible to fix the data. Once bias gets baked into the data, it reflects the realities of the world and models can only be fit to the subjective interpretations (human tendencies) that are present in the data. Awareness and disclosure of the issue is a starting point. Better, less subjective data is a more durable longer-term solution, but that requires time and resources needed to create calibrated outcomes (e.g., technical assessments for job candidates instead of only resumes).

Some bias-mitigation strategies might also be possible. In the policing case, for example, train the models using subsets of crimes that are more objective in nature like armed robberies. Compare those models to similar ones trained on crimes that are more subjective in nature, like traffic stops. That may help to quantify the amount of bias in the model. Predictions made from the models could then be corrected by reducing risk scores from that category of race by the level of bias estimated from the differences observed in risk associated with subjective versus objective outcomes. These techniques are commonly called “instrumental variables” in econometrics and are imperfect solutions. But beyond simply identifying and disclosing the problem while waiting for better data, they are one feasible approach to some level of bias mitigation.

**Examples:** 

['We're at risk of creating a generation of racist and sexist robots': Study shows artificial intelligence quickly becomes bigoted after learning 'toxic stereotypes' on the internet](https://www.dailymail.co.uk/sciencetech/article-10957023/Fears-AI-create-sexist-bigots-test-learns-toxic-stereotypes.html)

> The researchers said that those training artificial intelligence models to recognise humans often turn to vast datasets available for free on the internet. But because the web is filled with inaccurate and overtly biased content, they said any algorithm built with such datasets could be infused with the same issues.

[Inside the secret list of websites that make AI like ChatGPT sound smart](https://www.washingtonpost.com/technology/interactive/2023/ai-chatbot-learning/)

*AI chatbots have exploded in popularity over the past four months, stunning the public with their awesome abilities, from writing sophisticated term papers to holding unnervingly lucid conversations... They can mimic human speech because the artificial intelligence that powers them has ingested a gargantuan amount of text, mostly scraped from the internet.* 

*Tech companies have grown secretive about what they feed the AI. Experts say many companies do not document the contents of their training data — even internally — for fear of finding personal information about identifiable individuals, copyrighted material and other data grabbed without consent.*

*The Washington Post believes it is important to present the complete contents of the data fed into AI models, which promise to govern many aspects of modern life. So we set out to analyze one of these data sets to fully reveal the types of proprietary, personal, and often offensive websites that go into an AI’s training data.*

News sites 

> The News and Media category ranks third across categories. But half of the top 10 sites overall were news outlets: nytimes.com No. 4, latimes.com No. 6, theguardian.com No. 7, forbes.com No. 8, and huffpost.com No. 9. (Washingtonpost.com No. 11 was close behind.) Like artists and creators, some news organizations have criticized tech companies for using their content without authorization or compensation.
> 
> Meanwhile, we found several media outlets that rank low on NewsGuard’s independent scale for trustworthiness: RT.com No. 65, the Russian state-backed propaganda site; breitbart.com No. 159, a well-known source for far-right news and opinion; and vdare.com No. 993, an anti-immigration site that has been associated with white supremacy.

Religious sites reflect a Western perspective

> Sites devoted to community made up about 5 percent of categorized content, with religion dominating that category. Among the top 20 religious sites, 14 were Christian, two were Jewish and one was Muslim, one was Mormon, one was Jehovah’s Witness, and one celebrated all religions.
> 
> The top Christian site, Grace to You (gty.org No. 164), belongs to Grace Community Church, an evangelical megachurch in California. Christianity Today recently reported that the church counseled women to “continue to submit” to abusive fathers and husbands and to avoid reporting them to authorities.

Personal blogs

> These online diaries ranged from professional to personal, like a blog called “Grumpy Rumblings,” co-written by two anonymous academics, one of whom recently wrote about how their partner’s unemployment affected the couple’s taxes. One of the top blogs offered advice for live-action role-playing games. Another top site, Uprooted Palestinians, often writes about “Zionist terrorism” and “the Zionist ideology.”

What the filters missed

> Like most companies, Google heavily filtered the data before feeding it to the AI. (C4 stands for Colossal Clean Crawled Corpus.). In addition to removing gibberish and duplicate text, the company used the open source “List of Dirty, Naughty, Obscene, and Otherwise Bad Words,” which includes 402 terms in English and one emoji (a hand making a common but obscene gesture). Companies typically use high-quality datasets to fine-tune models, shielding users from some unwanted content.
> 
> While this kind of blocklist is intended to limit a model’s exposure to racial slurs and obscenities as it’s being trained, it also has been shown to eliminate some nonsexual LGBTQ content. 
> 
> Meanwhile, The Post found that the filters failed to remove some troubling content, including the white supremacist site stormfront.org No. 27,505, the anti-trans site kiwifarms.net No. 378,986, and 4chan.org No. 4,339,889, the anonymous message board known for organizing targeted harassment campaigns against individuals.

------------


# Bad Algorithms (Algorithmic Bias)

## (3) Harms of Identity Proxy

In many contexts where machine learning models enhance or replace human decision making, such as approval for a loan or credit card, laws forbid the explicit use of protected classes as a criterion for being denied a service (race, ethnicity, gender, language, and disability status). As a result, these variables are excluded from models to promote fairness and avoid lawsuits. However, they do not need to be explicit in models to be present. The role they serve in making algorithms biased or unfair can be fulfilled by identity proxies—composites of other variables in the model that predict the protected class with high accuracy.

The previous example of Amazon’s attempt to build an AI system to identify the best job candidates from the mountains of resumes they receive demonstrates the challenge of identity proxies as well. They trained their algorithms using resumes from past positions that were filled and calibrating the models based on who was actually hired from the candidate pools. Historic bias in hiring decisions led to algorithms that systematically excluded women from the list of top candidates in the current list of resumes. Once engineers recognized this problem they were horrified so they removed gender from variables considered by the model, expecting that to resolve the issue. What they quickly discovered, however, is that resumes are full of gender proxies.

The algorithms could predict the gender of candidates based on things like their first name, which sports they listed (softball vs baseball), hobbies or interests (anything that mentioned “women’s”), or which schools they attended (all-women’s colleges were penalized). These examples seem somewhat obvious and could be mitigated by editing the algorithm to remove known identity proxies. Gender was, however, deeply embedded in resumes in subtle ways that were hard to identify, such as the vocabulary used by candidates. The algorithms awarded points for the appearance of words like “executed” and “captured,” which are more prevalent on male resumes. After it became apparent that it was impossible to identify and neutralize all gender proxies Amazon scrapped the project (Christian, 2020). 

Race and other subgroup proxies manifest in similar ways in data. Recent studies have shown how powerful machine learning algorithms have become at identifying patterns that are imperceptible to humans but can serve as signatures of group membership. For example, Bansal et al. (2012) used a support vector machine to predict the gender of a patient from an image of the iris, a result that surprised medical professionals since male and female irises look the same to humans. Similarly, Banerjee et al. (2021) showed AI can predict a patient’s race from an X-ray despite the fact that physicians were unaware of any known correlations between features on medical images and race. They show that “detection is not due to trivial proxies or imaging-related surrogate covariates for race, such as underlying disease distribution” and that “performance persists over all anatomical regions and frequency spectrum of the images suggesting that mitigation efforts will be challenging.”

These examples demonstrate how much information is unintentionally encoded in data. Amazon did not anticipate that gender would permeate all aspects of a candidate’s resume. Bansal and Banerjee’s teams were not designing medical imaging techniques that optimize detection of gender or race. They simply used archives of eye images or X-rays to demonstrate how powerful machine learning algorithms have become at detecting patterns that are invisible to experts. The lesson they demonstrate is that it is an unrealistic assumption that algorithms are not making predictions based on protected classes simply because variables like race, gender, or disability status are not explicitly present in models. Identity proxies are ubiquitous.

**Identity Proxy Mitigation**: Instead of dropping a category like race from the model, assuming it solves the problem, test for the presence of identity proxies. Make race the dependent variable in the model while retaining the other covariates. If you can accurately predict race or another protected class with the remaining covariates in your model, identity proxies are present. Using predictive models when identity proxies are present violates the spirit of protections afforded to historically disadvantaged classes. When relevant to the research, report whether identity proxies can be detected in the data.

**Examples:** 

[Facebook’s Ad Algorithm Pushes Black Users to For-Profit Colleges](https://theintercept.com/2024/06/04/facebook-ads-algorithm-for-profit-colleges/)

> Ever since a 2016 ProPublica report found Facebook allowed advertisers to explicitly exclude users from advertising campaigns based on their race, the company’s advertising system has been subject to increased scrutiny and criticism. And while Facebook ultimately removed options that allowed marketers to target users by race, previous academic research has shown that the secret algorithm that decides who sees which ads is biased along race and gender lines, suggesting bias intrinsic to the company’s systems.
> 
> In order to put Facebook’s black-box advertising system to the test, academics from Princeton and the University of Southern California purchased Facebook ads and tracked their performance among real Facebook users, a method they say produced “evidence of racial discrimination in Meta’s algorithmic delivery of ads for education opportunities, posing legal and ethical concerns.”
> 
> The researchers say they focused on for-profit colleges because of their long, demonstrable history of deceiving prospective students — particularly students of color — with predatory marketing while delivering lackluster educational outcomes and diminished job prospects compared to other colleges.

> In a series of test marketing campaigns, the researchers purchased sets of two ads paired together: one for a public institution, like Colorado State University, and another marketing a for-profit company, like Strayer University (... they focused on for-profit colleges because of their long, demonstrable history of deceiving prospective students with predatory marketing while delivering lackluster educational outcomes and job prospects). 
> 
> Advertisers on Facebook can fine-tune their campaigns with a variety of targeting options, but race is no longer one of them. So the researchers found a clever proxy. Using North Carolina voter registration data that includes individuals’ races, the researchers built a sample audience that was 50 percent white and 50 percent Black. The Black users came from one region in North Carolina and white voters from another. Using Facebook’s “custom audiences” feature, they uploaded this roster of specific individuals to target with ads. Though Facebook’s ad performance metrics wouldn’t reveal the race of users who saw each ad, the data showed where each ad was viewed. “Whenever our ad is shown in Raleigh, we can infer it was shown to a Black person and, when it is shown in Charlotte — we can infer it was shown to a White person,” the paper explains.
> 
> Theoretically, an unbiased algorithm would serve each ads for each school to an equal number of Black and white users. The experiment was designed to see whether there was a statistically significant skew in which people ultimately saw which ads. With each pair of ads, Facebook’s delivery algorithm showed a bias, the researchers found. The company’s algorithm disproportionately showed Black users ads for colleges like DeVry and Grand Canyon University, for-profit schools that have been fined or sued by the Department of Education for advertising trickery, while more white users were steered toward state colleges, the academics concluded.

[Investigation Finds AI Algorithms Objectify Women’s Bodies](https://www.theguardian.com/technology/2023/feb/08/biased-ai-algorithms-racy-women-bodies)

> Journalists used AI tools to analyze hundreds of photos of men and women in underwear, working out, using medical tests with partial nudity and found evidence that the AI rate pictures of women as more “racy” or sexually suggestive than comparable pictures of men and tags photos of women in everyday situations as sexually suggestive.
> 
> Shadowbanning has been documented for years, but the journalists may have found a missing link to understand the phenomenon: biased AI algorithms. Social media platforms leverage algorithms to rate images and limit the reach of content that they consider too racy. AI algorithms seem to have a built-in gender bias, rating women more racy than images containing men.
> 
> **But what are these AI classifiers actually analyzing in the photos? When [a male subject was] photographed in long pants and with a bare chest, Microsoft’s algorithm had a confidence score lower than 22% for raciness. When he put on a bra the raciness score jumped to 97%. The algorithm gave a 99% score when the bra was held next to him**. (**_identity proxies_**)
> 
> Margaret Mitchell, chief ethics scientist at the AI firm Hugging Face and former co-head of Google’s Ethical AI research group, believes that the photos used to train these algorithms were probably labeled by straight men, who may associate men working out with fitness, but may consider an image of a woman working out as racy. It’s also possible that these ratings seem gender biased in the US and in Europe because the labelers may have been from a place with a more conservative culture.  (**_tendentious data_**) 
> 
> As a result, the social media companies that leverage these or similar algorithms suppress the reach of countless images featuring women’s bodies and potentially hurt female-led businesses, further amplifying societal disparities.

[AI Model Detects Mental Disorders Based on Web Posts](https://home.dartmouth.edu/news/2022/03/ai-model-detects-mental-disorders-based-web-posts)

> Dartmouth researchers have built an artificial intelligence model for detecting mental disorders using conversations on Reddit, part of an emerging wave of screening tools that use computers to analyze social media posts and gain an insight into people’s mental states.
> 
> They trained their model to label the emotions expressed in users’ posts and map the emotional transitions between different posts, so a post could be labeled ‘joy,’ ‘anger,’ ‘sadness,’ ‘ fear,’ ‘no emotion,’ or a combination of these... Different emotional disorders have their own signature patterns of emotional transitions. By creating an emotional “fingerprint” for a user and comparing it to established signatures of emotional disorders, the model can detect them.

In this example the researchers are explicitly trying to identify known emotional disorders in the study population. The important take-away is how the algorithms pick up on subtle changes in language to make predictions. 

An identity proxy harm might arise when machine learning is used by companies to support decisions like admissions into competitive programs, lending decisions by banks, or tenant applications reviewed by landlords. Similar to Amazon's resume screening program that inadvertently penalized female engineers, AI platforms could unknowingly be basing their decisions upon whether individuals have experienced depression or anxiety in the past, an extremely problematic practice in most contexts.

The algorithms detect patterns that are invisible to humans and correlate them with outcomes. Since the algorithms are often black boxes it is difficult to understand what the underlying patterns represent and whether the resulting decision heuristics produced by the machines are ethical or legal. For example, if a bank asked programmers to predict which of their clients suffered from depression and used the results to restrict access to credit they would be opening themselves up to lawsuits. If they use the same data to predict credit-worthiness while making no effort to understand the internal workings of the model they could end up with the exact same results but no understanding of the mechanisms and a diminished ability of humans using the algorithms to exercise discretion accordingly.  

> 'Models are built around scrutinizing and relying on the content of the text, and while the models show high performance, they can also be misleading. For instance, if a model learns to correlate “COVID” with “sadness” or “anxiety,” Vosoughi explains, it will naturally assume that a scientist studying and posting (quite dispassionately) about COVID-19 is suffering from depression or anxiety.'

For more examples of using social media data for psychological profiling see the excellent project [Apply Magic Sauce](https://applymagicsauce.com/demo).

------------


## (4) Harms of Subpopulation Difference

Harms of subpopulation difference arise when algorithm performance varies by subgroup within the data. For example, it is possible for a new drug to have a net positive population effect but when data are disaggregated, it can be shown to harm a subpopulation. While federal drug approval processes now account for subpopulation differences, there are no standards to hold corporations accountable for subpopulation harm resulting from algorithms.

The extent of this problem was only recently uncovered. In 2016 ProPublica conducted a high-profile review of the COMPAS algorithm that predicts the risk of an incarcerated criminal committing a future crime if released. They found that algorithm to be biased against Black prisoners, assigning risk scores that were higher than justified by their actual observed behavior once released (Angwin et al., 2016). Stated differently, if a white prisoner and a black prisoner were assigned the same risk score, the white prisoner was more likely to recidivate. Black prisoners were being refused parole at higher rates as a result.

ProPublica’s in-depth investigative reporting served as a lightning rod of sorts for machine learning scholars with expertise in algorithmic fairness, catalyzing a flurry of studies on the topic and an important breakthrough. The fact that the COMPAS algorithm was generating risk scores that were inconsistent across race was not a bug in their specific machine learning algorithm, but a feature of all machine learning models. Chouldechova (2017) and Pleiss et al. (2017) were able to prove that it is mathematically impossible to build machine learning models that perform consistently across subgroups in the data when baseline rates of the outcome differ by subgroup. In other words, the issue was not a poorly specified model in inadequate data inputs. Rather, it is a fundamental feature of machine learning models when baseline rates of the outcome vary by subgroups within the data. These examples of racialized bias are just one example of a larger conversation within the data science and ML ethics community surrounding persistent public value failures surrounding machine learning applications in the public domain (Monroe-White & Marshall, 2019).

**Subpopulation Difference Mitigation**: There is no easy fix to the problem of machine learning models that perform differently for each subpopulation within the data. Mathematical proofs have shown that it is impossible to fix the issue using a different model specification or better data. Mitigation is less about solving the issue and more about recognizing the issue before you build or deploy your algorithm.

COMPAS failed because the algorithm designers defined fairness by calibrating risk scores using false positives alone (Angwin, et al., 2016). The risk scores produced by the models did in fact accurately predict whether an individual was likely to be re-arrested after release, regardless of race. But performance varied wildly on the other criteria–false negatives, whether an individual remained locked up when they were unlikely to commit a future crime. The algorithm deemed blacks much riskier than was supported by the data, so risk scores were much higher than they should have been. This result in a scenario where if you put inmates into risk categories, within each category white inmates were given lower risk scores and were much more likely to receive parole than Black inmates that had a similar likelihood of recidivism.

Publications that use machine learning classifiers should examine outcomes across various protected subgroup classes in the data like race and gender to determine whether baseline rates differ by group. If so, recognize that it is impossible to build a model that will perform similarly for all subgroups. With just two subgroups like data that only includes individuals from White and Black race categories, the models can achieve balanced false positive rates but have disparate rates of false negatives, or achieve balanced false negative rates and have disparate rates of false positives. They cannot achieve balance in both (Kleinberg et al., 2016). The more subgroups there are present, the harder it is to achieve balance.

Mitigation starts with awareness or the issues that arise when subgroups have different baseline performances in the data and disclosure of baseline rates, as well as reporting model performance statistics separately for subgroups to quantify the extent of the difference. That would meet a minimal requirement of fairness operationalized as transparency.


------------


# Bad Models 


## (5) Harms of Misfit Models

Models become misfits when they are optimized by minimizing the wrong type of error or preferencing the wrong outcome. Minimizing model error instead of maximizing model benefit. One of the lessons from the field of machine learning is that less accurate models are generally more useful. This relationship arises because of two model features: (1) model accuracy can be improved by overfitting data and (2) the most powerful machine learning models (e.g., neural networks) generate highly accurate results that no one understands and consequently are harder to translate into practice.

The Harm of Misfit Models is a more specific case of the general issue regarding the trade-off of model accuracy and value. Specifically, model accuracy is measured as the rate of error produced by model predictions. It sounds simple enough, but it turns out that measuring accuracy is challenging as a result of different types of error and different costs associated with each. 
 
When social or economic costs of false positives and false negatives differ in the model, especially if one specific type of error is high-stakes, then attention to model fit is important. For example, if 1% of woman have breast cancer at age 45 then a test that concludes that no women have breast cancer is 99% accurate and 100% useless. 

A false positive in an initial screening (indications of cancer when the woman is healthy) will incur real costs such as invasive biopsies and expensive follow-up visits. But the costs are trivial compared to a false negative (failing to detect cancer that does exist) since it can result in death for the individual, extreme emotional and financial burden placed on her family, and loss of a member of society in their most productive years.

Another example to consider is parole for an incarcerated individual. A false positive in a parole risk model suggest that an individual is likely to recidivate if released when in reality they are unlikely to further engage in criminal activity. A false negative occurs when individuals are deemed to be low risk by the algorithm but in reality are prone to violence or criminality and likely to recidivate. Do these two types of error have equal value to society, or should one be weighted more heavily? 

Court systems must undertake the impossible task of balancing the social and economic costs of both types of errors. Incarcerating individuals longer than necessary violates civil liberties and increases the economic and social cost of incarceration. The cost of a false positive will disproportionately burden an incarcerated individual and their family. Conversely, freeing individuals that are likely to reoffend will impose the costs of crime and violence on communities. Parole risk models are typically calibrated on costs associated with the latter type of error rather than the former. 

**Misfit Models Mitigation**: The ML community has developed many practices like cross-fold validation to avoid over-fitting and has evolved an ethos that values simple models or assemblages of simpler models that over black-box oracles that might be more accurate but impossible to interpret.

Predictive algorithms that fail to account for differential costs of error types are potentially harmful. To mitigate harm authors should disclose the model fit criteria use for calibration. In the best case they would use an explicit link function that assigns different values to different types of error so that models can be calibrated to optimize economic or social benefits instead of minimizing a specific type of error. 

------------


# Bad Humans (Human Intent)


## (6) Do No Harm

Most data science failures are cases where models are biased in subtle ways or performance deviates from expectations. One must first ask, however, is the intent of the deployment to cause harm? For example, Cambridge Analytica used sophisticated data analytics to target marginalized and minoritized populations with misinformation to create a sense of frustration with the political process and make it less likely for the targeted individuals to vote (Schneble et al., 2018). Similarly, spatial analytics can be used to gerrymander voting districts to distort representation. In both cases, the goals are to suppress votes and undermine the democratic process, which one can argue are nefarious goals. These are not examples of algorithmic failure or bias. The models perform perfectly well, but their intent is to disadvantage or harm a subpopulation.

**Do No Harm Commitment**: Can you confirm that your true intent designing an algorithm matches the intent that is described in your manuscript or project documentation? Is the intent to benefit populations equally, or to advance objectives of fairness or justice?

**Example:** 

[Aims’: the software for hire that can control 30,000 fake online profiles](https://www.theguardian.com/world/2023/feb/15/aims-software-avatars-team-jorge-disinformation-fake-profiles?CMP=share_btn_tw)

> Canaelan is a non-human bot linked to a vast army of fake social media profiles controlled by a software designed to spread “propaganda”.
> 
> Advanced Impact Media Solutions, or Aims, which controls more than 30,000 fake social media profiles, can be used to spread disinformation at scale and at speed. It is sold by “Team Jorge”, a unit of disinformation operatives based in Israel.
> 
> Tal Hanan, who runs the covert group using the pseudonym “Jorge”, told undercover reporters that they sold access to their software to unnamed intelligence agencies, political parties and corporate clients. One appears to have been sold to a client who wanted to discredit the UK’s Information Commissioner’s Office (ICO), a statutory watchdog.

------------

## (7) Harms of Ignorance

In many cases, algorithms perform amazingly well on their intended tasks, but deployment does not consider potential harm, especially in sensitive racial or gender contexts. For example, Noble (2018) documents how Google’s keyword search algorithms returned pornographic and profane images as top results when “Black girls” or “Black women” were used as search terms. The search algorithm generally performed well in most contexts, but there was no proactive consideration for what might happen when deployed without safeguards in contexts where exploitation has been historically prevalent. The most pernicious examples of harmful practices are more likely unintended consequences that are difficult to anticipate when new technologies are deployed in unfamiliar or complex environments. Harms of ignorance are more aptly characterized as uncontemplated consequences—a sort of willful ignorance that results when scholars or engineers (groups often dominated by White and Asian males) have not considered possible harms to minoritized groups (i.e., Asian women, Black males, etc.). Unintended consequences are hard to anticipate, whereas uncontemplated consequences could have been anticipated through a reasonable level of rumination.

**Mitigating Harms of Ignorance**: Heath and Heath (2013) promote the use of pre-mortem analysis to avoid mistakes in business. These exercises occur prior to the launch of a new product or service, and require teams to sit down together and write a hypothetical obituary for the project. The exercise forces them ahead of time to determine the most likely reasons that a project will fail. This sort of brainstorming then allows the team to protect against the most likely threats to success as they begin to implement the project. 

Similarly, to mitigate harms of ignorance scholars or engineers should entertain the question, what’s the worst possible outcome that could result from this work? Are there specific groups that might be vulnerable to disproportionate harm by a failure of the algorithm? Scholars should ask, could the data collected for this research, or the tools developed through the work be used for nefarious purposes that are different from their original intent? It is impossible to anticipate every scenario or outcome, so mitigation would require a good faith effort to reduce willful ignorance of potential harms. 

**Example:** 

[Chatbots posing as therapists may encourage users to commit harmful acts, the nation’s largest psychological organization warned federal regulators.](https://www.nytimes.com/2025/02/24/health/ai-therapists-chatbots.html)

> The nation’s largest association of psychologists this month warned federal regulators that A.I. chatbots “masquerading” as therapists, but programmed to reinforce, rather than to challenge, a user’s thinking, could drive vulnerable people to harm themselves or others.
> 
> Dr. Evans said he was alarmed at the responses offered by the chatbots. The bots, he said, failed to challenge users’ beliefs even when they became dangerous; on the contrary, they encouraged them. If given by a human therapist, he added, those answers could have resulted in the loss of a license to practice, or civil or criminal liability.
> 
> In one case, a 14-year-old boy in Florida died by suicide after interacting with a character claiming to be a licensed therapist. In another, a 17-year-old boy with autism in Texas grew hostile and violent toward his parents during a period when he corresponded with a chatbot that claimed to be a psychologist. Both boys’ parents have filed lawsuits against the company.



----------------

## High Stakes Games

As an example of how these issues can impact citizens, a recent ProPublica story details the increasing reliance on tenant screening algorithms in rental markets. Considering that 65% of households in the under-35 age group are renters and almost everyone will be a renter at some point in their lives, the potential impact on housing markets is huge. 

The case study demonstrates the challenges of loosely-regulated, market-driven deployments of machine learning and artificial intelligence at scale. 



[**ProPublica: How Your Shadow Credit Score Could Decide Whether You Get an Apartment**](https://www.propublica.org/article/how-your-shadow-credit-score-could-decide-whether-you-get-an-apartment)

*The rapid rise of tenant screening is one of the seismic changes to hit the rental market since the Great Recession. As ProPublica has reported, private equity firms have poured into the multifamily apartment market, often driving up rents in search of greater profits than those typically sought by mom-and-pop landlords. Algorithms now often replace human judgment in deciding who qualifies for housing and how much rent costs.*

*Nearly 2,000 companies offered background screening in 2019, most for either employment or tenant purposes, an industry survey found. It estimated that tenant screening brought in roughly $1 billion in annual revenue.*

*A leading Texas-based property management tech firm, boasts that its algorithm uses artificial intelligence to “identify high-risk renters with greater accuracy.” The company says it uses a massive, proprietary database of 30 million lease outcomes, paired with consumer financial data, to evaluate rental applicants.*

*Tenant score algorithms try to predict how risky it is to rent to a potential tenant based on characteristics they share with other tenants, according to an attorney and former Federal Trade Commission official whose law firm represents tenant screening companies.*

*“A scoring model may find that certain characteristics help predict risk. They don’t predict it perfectly for every individual. Overall, they do a satisfactory job of predicting risk.”*

*A retired regional property manager said it was typical that several times a month he would need to override denial recommendations from the screening service his firm used. Often, it was because people had medical debt, foreclosures or student loans but otherwise looked like good candidates.*

*“If everything else looked clean to me, I would do an override,” said Withers, who oversaw thousands of apartments in Maryland and Virginia. Busy property managers may not realize that the screening service’s algorithm was set up in a way that would reject people who might be viable candidates.*

*Tenant advocates say the **consumer data used by screening companies too often results in negative recommendations for reasons that are not proven indicators of how good a tenant someone would be**. One tenant in Washington state who contacted ProPublica received a screening letter that listed “too many different phone numbers reported” as a risk factor that contributed to lowering her tenant score.*

---------------------

As a demonstration of the utuility of the Wells-DuBois protocol, one could identify potential sources of harms in tenant screening algorithms by considering whether companies have explicitly addressed any of the items in the protocol: 

**(1) Inadequate Data**: Since their data is proprietary it is impossible to tell whether data used to train algorithms are representative of the populations that are being screened with the algorithms. There are no current standards for data quality or representativeness used by commercial firms deploying algorithms at scale and no way for third parties to inspect proprietary data. In this context there were consistent complaints that data was often incomplete and inaccurate. If databases are built by linking lots of disparate data sources it is highly likely that data errors and data missingness are NOT random, which could lead to performance disparities across groups. 

**(2) Tendentious Data**: Eviction decisions can be biased in myriad ways (Desmond, 2016), so using past eviction data can bake bias into the models. If any subgroup in the training data was targetted for eviction by landlords in the past then those decisions will shape the algorithms. For example, if a candidate is employed and has paid bills reliably, but grew up poor and is thus considered high-risk, the algorithm is punishing a person for their circumstance, not their actual actions. It is a form of profiling that is all but inevitable with predictive algorithms.  

**(3) Identity Proxy**: Since the companies offering screening services build historic profiles of potentian tenants they will quickly acquire a rich set of composite variables that will serve as proxies for things like race or class, even if those indicators are excluded from the models explicitly. The presence of identity proxies can amplify the effects of tendentious data, especially if bias occurs in the dependent variable used to train models. Similar to how Amazon's resume screening program learned that it preferred male applicants and then became very good at identifying males even after every effort was made to scrub gender from the applications, many predictive algorithms could easily detect the race or socio-economic class of an applicant, which could then influence their score.  

**(4) Harms of Subpopulation Difference**: Baseline rates of eviction will vary by subgroups in the data like class and race. If the models are calibrated on past eviction data then their accuracy will vary by subgroup. For example, if they fit models to minimize false negatives (those that are approved as being low-risk but end up requiring eviction), then the rates of false positives will vary by subgroup (people being denied applications because they are considered high-risk when in reality they would be a reliable tenant). Unless firms are addressing this problem with clear and intentional strategies then mathmatically it is impossible for predictive algorithms to produce **fair** results (equal rates of false positive and false negatives across subgroups) as opposed to **accurate** results (recommendations that do a good job at identifying a group of individuals that will include the high-risk renters but have no concern for those incorrectly classified as high-risk). 

**(5) Harms of Misfit Models**: Related to the previous item, if rates of *balanced* accuracy (rates of both false positives and false negatives together) differ by subgroup then some subgroups will benefit from the algorithm and others will be burdened with higher search costs or prices. Screening algorithms are developed for landlords so they will primarily consider the **cost of false negatives** in the models since those will impact a landlord's bottom line. The **cost of false positives** are assumed by tenants through exclusion from residential opportunities in better neighborhoods (those more likely to promote economic mobility) or higher rents. There is virtually no recourse for an individual if their rental application is rejected for arbitrary or biased reasons. Thus the algorithm creates a type of zero-sum game between landlords and tenants since landlords are better off and tenants are worse off. 

**(7) Harms of Ignorance:** Although the algorithms are unlikely designed with ill-intent (iten 6 - Do No Harm) the incentives in a domain like this are aligned toward calibrating models to produce results that benefit landlords and not tenants. If 2,000 firms are competing for $1 billion in this marketplace then it is challenging for a firm to recalibrate their models to be more fair since there will be a trade-off between fairness and accuracy in predicting problematic tenants. Their landlord customers are paying for accuracy, not fairness. Harm is also extremely hard to establish because you need to be able to argue that an applicant *would have been reliable if they would have been approved*, which is a hard counterfactual to prove. How often are these firms reflecting upon the systematic harms that might occur as a result of these algorithms being scaled? Is their ignorance of potential harms willful? As a test of their willingness to expel ignorance, for example, are they willing to accept legal frameworks that would hold them accountable for damages if systematic harms were discovered? 

------------

The potential benefits of technological solutions to problems involving human discretion should not be ignored. Reductions in transaction costs benefit all actors in markets. Credit score algorithms allow banks to approve loans in real-time, benefitting banks and borrowers. Tenant screening algorithms allow for real-time decisions on applications, benefitting renters and landlords. Artificial discretion can also standardize decision criteria and deter bad actors from using arbitrary or intentionally discriminatory criteria, making markets more predictable (Young et al. 2019). 

The real concern is the potential impact of algorithms that operate at scale in domains like housing markets. Even if bias is at the margins, if it is systematic bias and algorithms are influencing entire markets then their impact will compound over time. O'Neil (2016) also notes that algorithms are being deployed more often to automate decisions that impact disadvantaged populations whereas those with resources and means are likely subject to human discretion. Those working with humans can scrutinize the process and advocate for themselves directly, whereas those in systems run by algorithms have fewer options without understanding what's inside the black box. In contexts where algorithms have a tangible impact on people's lives, tools like the Wells-DuBois protocol are important for training engineers that build the systems and regulators or consumer advocates that want to ensure they are fair. 






<br> 
------------

<br>

## References

Agarwal, P. K. (2018). Public administration challenges in the world of AI and Bots. Public Administration Review, 78(6), 917-921.

Angwin, J., Larson, J., Mattu, S., & Kirchner, L. (2016). Machine bias. ProPublica, May, 23(2016), 139-159.

Banerjee, I., Bhimireddy, A. R., Burns, J. L., Celi, L. A., Chen, L. C., Correa, R., Gichoya, J. W. (2021). Reading race: AI recognises patient’s racial identity in medical images. arXiv preprint https://arxiv.org/abs/2107.10356.

Bansal, A., Agarwal, R., & Sharma, R. K. (2012, November). SVM based gender classification using iris images. In: 2012 fourth
international conference on computational intelligence and communication networks (pp. 425–429). IEEE.

Buolamwini, J., & Gebru, T. (2018, January). Gender shades: Intersectional accuracy disparities in commercial gender classification. In Conference on fairness, accountability and transparency (pp. 77-91).

Chouldechova, A. (2017). Fair prediction with disparate impact: A study of bias in recidivism prediction instruments. Big Data, 5(2), 153–163.

Christian, B. (2020). The alignment problem: Machine learning and human values. WW Norton & Company

Desmond, M. (2016). Evicted: Poverty and profit in the American city. Crown.

Dhar, V. (2013). Data science and prediction. Communications of the ACM, 56(12), 64-73.

Dressel, J., & Farid, H. (2018). The accuracy, fairness, and limits of predicting recidivism. Science advances, 4(1), eaao5580.

Gawande A. (2011). The Checklist Manifesto: How to Get Things Right. Metropolitan Books, New York: Holt and Company.

Heath, C., & Heath, D. (2013). Decisive: How to make better choices in life and work. Random House.

Kagan, D., Chesney, T. & Fire, M. Using data science to understand the film industry’s gender gap. Palgrave Commun 6, 92 (2020). https://doi.org/10.1057/s41599-020-0436-1

Kleinberg, J., Mullainathan, S., & Raghavan, M. (2016). Inherent trade-offs in the fair determination of risk scores. arXiv preprint
https://arxiv.org/abs/1609.05807

Monroe-White, T. and Marshall, B. (2019). Data science intelligence: Mitigating public value failures using PAIR principles. Proceedings of the 2019 Pre-ICIS SIGDSA Symposium. 4._https://aisel.aisnet.org/sigdsa2019/4

Noble, S. U. (2018). Algorithms of oppression: How search engines reinforce racism. NYU Press.

O'Neil, C. (2016). Weapons of math destruction: How big data increases inequality and threatens democracy. Broadway Books.

Pleiss, G., Raghavan, M., Wu, F., Kleinberg, J., & Weinberger, K. Q. (2017). On fairness and calibration. arXiv preprint https://arxiv.org/abs/1709.02012

Regenbogen, S. E., Ehrenfeld, J. M., Lipsitz, S. R., Greenberg, C. C., Hutter, M. M., & Gawande, A. A. (2009). Utility of the surgical apgar score: validation in 4119 patients. Archives of Surgery, 144(1), 30-36.

Schneble, C. O., Elger, B. S., & Shaw, D. (2018). The cambridge analytica affair and Internet-mediated research. EMBO Reports, 19(8), e46579.

Young, M. M., Bullock, J. B., & Lecy, J. D. (2019). Artificial discretion as a tool of governance: a framework for understanding the impact of artificial intelligence on public administration. Perspectives on Public Management and Governance, 2(4), 301-313.
