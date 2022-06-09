# Black Lives Matter twitter corpus (BLMtwitter) --- datasheet

By: [A. Maurits van der Veen](http://www.maurits.net/) `<maurits@wm.edu>`

As part of a research project investigating the spread of social movements online and across national borders, I collected a dataset of all explicit references in tweets to Black Lives Matter, All Lives Matter, and Blue Lives Matter (either in the form of the full phrase or as a condensed hashtag or acronym). Most of the dataset was collected directly; some was supplied from a comparable dataset, collected by Giorgi et al. (2020, 2022). Below is the datasheet describing the corpus, following the guidelines set out in [Gebru et al. (2022)](url) on datasheets, and the specific format adopted by [Cao and Daom (2020)](https://github.com/TristaCao/into_inclusivecoref/blob/master/MAP/datasheet-map.md) for their dataset.

If you use the BLM twitter corpus, please cite the associated paper:

 
```
@inproceedings{cao2019toward,
  title={BLMtwitter: The Black Lives Matter (BLM) Twitter Corpus},
  author={van der Veen, A. Maurits}},
  year={2022},
  note={osf.io/preprints/socarxiv/kna9s}
}
```



## Motivation


1. **For what purpose was the dataset created?** *(Was there a specific task in mind? Was there a specific gap that needed to be filled? Please provide a description.)*
    
    This dataset was created to study the discourse surrounding Black Lives Matter on social media (specifically, Twitter). While other BLM twitter datasets exist, they are not generally publicly available, they often cover only a limited period, and they frequently include tweets that, while about issues relating to BLM, do not explicitly reference the movement by name, hashtag, or acronym.

1. **Who created this dataset (e.g., which team, research group) and on behalf of which entity (e.g., company, institution, organization)?**
    
    This dataset was created by A. Maurits van der Veen, Associate Professor of Government at William & Mary, but not on behalf of that institution. 

1. **Who funded the creation of the dataset?** *(If there is an associated grant, please provide the name of the grantor and the grant name and number.)*
    
    No funding was received for the creation of the dataset.


1. **Any other comments?**
    
    None





## Composition


1. **What do the instances that comprise the dataset represent (e.g., documents, photos, people, countries)?** *(Are there multiple types of instances (e.g., movies, users, and ratings; people and interactions between them; nodes and edges)? Please provide a description.)*
    
    The dataset is constructed of tweet ids, along with information about which of Black Lives Matter, All Lives Matter, or Blue Lives Matter are explicitly referenced in the tweet (either as a full phrase or in some abbreviated form). In accordance with Twitter rules, only the tweet ids are shared; users can "hydrate" the corpus to get the additional components of each tweet, including tweet text.


1. **How many instances are there in total (of each type, if appropriate)?**
    
    The dataset consists of *** Black Lives Matter tweets, *** All Lives Matter tweets, and *** Blue Lives Matter tweets.


1. **Does the dataset contain all possible instances or is it a sample (not necessarily random) of instances from a larger set?** *(If the dataset is a sample, then what is the larger set? Is the sample representative of the larger set (e.g., geographic coverage)? If so, please describe how this representativeness was validated/verified. If it is not representative of the larger set, please describe why not (e.g., to cover a more diverse range of instances, because instances were withheld or unavailable).]* 
    
    The dataset represents the most complete collection of tweets explicitly referencing Black, All, or Blue Lives Matter. However, it is not complete. Specifically, many such tweets have been deleted, either by the Twitter users themselves or by Twitter. Moreover, tweet collection appears to be non-deterministic: the same search query will not always return the same set of tweets, and thus it appears certain that some tweets that meet the criteria are not included. Tweets that are deleted, either by users or by Twitter, are not a random subset of all tweets (for one, they are more likely to contain language violating Twitter norms); as such, the remaining tweets are not fully representative of the complete set. 

 
1. **What data does each instance consist of?** *(''Raw'' data (e.g., unprocessed text or images)or features? In either case, please provide a description.)*
    
    Each instance consists of 10 features: a tweet id, and 9 columns representing different search strings, containing a 1 if the search string appears in the tweet and a 0 otherwise. The strings are: black lives matter, blacklivesmatter, blklivesmatter, blm, all lives matter,	alllivesmatter, allivesmatter, blue lives matter, and bluelivesmatter. For the multi-word search terms, the words can be separated by any alphanumeric characters (spaces, underscores, etc.)

1. **Is there a label or target associated with each instance? If so, please provide a description.**
    
    See preceding item. 


1. **Is any information missing from individual instances?** *(If so, please provide a description, explaining why this information is missing (e.g., because it was unavailable). This does not include intentionally removed information, but might include, e.g., redacted text.)*
    
    No.


1. **Are relationships between individual instances made explicit (e.g., users' movie ratings, social network links)?** *( If so, please describe how these relationships are made explicit.)*
    
    No; since only tweet ids are provided, any relationships between tweets (replies, retweets, etc.) will only become visible after hydration.


1. **Are there recommended data splits (e.g., training, development/validation, testing)?** *(If so, please provide a description of these splits, explaining the rationale behind them.)*
    
    No.  


1. **Are there any errors, sources of noise, or redundancies in the dataset?** *(If so, please provide a description.)*
    
    Some tweets mention more than one of Black, All, or Blue Lives Matter. Such tweets are included once each in each of the respective sub-corpora.


1. **Is the dataset self-contained, or does it link to or otherwise rely on external resources (e.g., websites, tweets, other datasets)?** *(If it links to or relies on external resources, a) are there guarantees that they will exist, and remain constant, over time; b) are there official archival versions of the complete dataset (i.e., including the external resources as they existed at the time the dataset was created); c) are there any restrictions (e.g., licenses, fees) associated with any of the external resources that might apply to a future user? Please provide descriptions of all external resources and any restrictions associated with them, as well as links or other access points, as appropriate.)*
    
    The dataset is self-contained.


1. **Does the dataset contain data that might be considered confidential (e.g., data that is protected by legal privilege or by doctor-patient confidentiality, data that includes the content of individuals' non-public communications)?** *(If so, please provide a description.)*
    
    No; tweet ids are not confidential, and any hydrated tweets will contain only publicly available information.


1. **Does the dataset contain data that, if viewed directly, might be offensive, insulting, threatening, or might otherwise cause anxiety?** *(If so, please describe why.)*
    
    Yes. Some tweets may be offensive. 


1. **Does the dataset relate to people?** *(If not, you may skip the remaining questions in this section.)*
    
    Yes. Tweets are usually by people (not always: bots also tweets) and are often about people.


1. **Does the dataset identify any subpopulations (e.g., by age, gender)?** *(If so, please describe how these subpopulations are identified and provide a description of their respective distributions within the dataset.)*
    
    No. 


1. **Is it possible to identify individuals (i.e., one or more natural persons), either directly or indirectly (i.e., in combination with other data) from the dataset?** *(If so, please describe how.)*
    
    Yes. Hydrated tweets include twitter user information. If a person is identifiable from their twitter user data, as is often the case, then it is possible to identify them from the hydrated tweets.


1. **Does the dataset contain data that might be considered sensitive in any way (e.g., data that reveals racial or ethnic origins, sexual orientations, religious beliefs, political opinions or union memberships, or locations; financial or health data; biometric or genetic data; forms of government identification, such as social security numbers; criminal history)?** *(If so, please provide a description.)*
    
    Not the twitter ids themselves, but hydrated tweets potentially do, but only if such data is shared by twitter users.


1. **Any other comments?**
    
    No.





## Collection Process


1. **How was the data associated with each instance acquired?** *(Was the data directly observable (e.g., raw text, movie ratings), reported by subjects (e.g., survey responses), or indirectly inferred/derived from other data (e.g., part-of-speech tags, model-based guesses for age or language)? If data was reported by subjects or indirectly inferred/derived from other data, was the data validated/verified? If so, please describe how.)*
    
    The majority of the data was collected retrospectively from Twitter. The resulting dataset was supplemented from the comparable corpus by Giorgi et al. (2020, 2022), which was collected contemporaneously through Twitter's API. The flags for explicit references to Black, All, or Blue Lives Matter were generated using straightforward string matching.


1. **What mechanisms or procedures were used to collect the data (e.g., hardware apparatus or sensor, manual human curation, software program, software API)?** *(How were these mechanisms or procedures validated?)*
    
    The retrospective collection used the python module 'twint'. Supplementing from the Giorgi et al. corpus was done by hydrating the tweet ids in that corpus using the application Hydrator, created at the University of Maryland.


1. **If the dataset is a sample from a larger set, what was the sampling strategy (e.g., deterministic, probabilistic with specific sampling probabilities)?**
    
    The dataset is as complete as possible.


1. **Who was involved in the data collection process (e.g., students, crowdworkers, contractors) and how were they compensated (e.g., how much were crowdworkers paid)?**
    
    Data collection was done by the author.


1. **Over what timeframe was the data collected?** *( Does this timeframe match the creation timeframe of the data associated with the instances (e.g., recent crawl of old news articles)?  If not, please describe the timeframe in which the data associated with the instances was created.)*
    
    The dataset was collected starting in the Spring of 2021; collection is ongoing.


1. **Were any ethical review processes conducted (e.g., by an institutional review board)?** *(If so, please provide a description of these review processes, including the outcomes, as well as a link or other access point to any supporting documentation.)*
    
    No review processes were conducted since Twitter data is public.


1. **Does the dataset relate to people?** *(If not, you may skip the remaining questions in this section.)*
    
    Yes. Tweets are usually by people (not always: bots also tweets) and are often about people.


1. **Did you collect the data from the individuals in question directly, or obtain it via third parties or other sources (e.g., websites)?**
    
    Other sources: Twitter.


1. **Were the individuals in question notified about the data collection?** *(If so, please describe (or show with screenshots or other information) how notice was provided, and provide a link or other access point to, or otherwise reproduce, the exact language of the notification itself.)*
    
    No, they were not notified.


1. **Did the individuals in question consent to the collection and use of their data?** *(If so, please describe (or show with screenshots or other information) how consent was requested and provided, and provide a link or other access point to, or otherwise reproduce, the exact language to which the individuals consented.)*
    
    Not explicitly. All tweets are public.


1. **If consent was obtained, were the consenting individuals provided with a mechanism to revoke their consent in the future or for certain uses?** *(If so, please provide a description, as well as a link or other access point to the mechanism (if appropriate).)*
    
    N/A.


1. **Has an analysis of the potential impact of the dataset and its use on data subjects (e.g., a data protection impact analysis)been conducted?** *(If so, please provide a description of this analysis, including the outcomes, as well as a link or other access point to any supporting documentation.)*
    
    No.


1. **Any other comments?**
    
    None.





## Preprocessing/cleaning/labeling


1. **Was any preprocessing/cleaning/labeling of the data done (e.g., discretization or bucketing, tokenization, part-of-speech tagging, SIFT feature extraction, removal of instances, processing of missing values)?** *(If so, please provide a description. If not, you may skip the remainder of the questions in this section.)*
    
    Data was labeled to indicate the presence of explicit references to Black, All, or Blue Lives Matter


1. **Was the "raw" data saved in addition to the preprocessed/cleaned/labeled data (e.g., to support unanticipated future uses)?** *(If so, please provide a link or other access point to the "raw" data.)*
    
    Tweet texts were saved for local research use. Twitter rules prohibit the sharing of these data.


1. **Is the software used to preprocess/clean/label the instances available?** *(If so, please provide a link or other access point.)*
    
    The labeling was done using straightforward text searches (using python's re package). The script is available from the author upon request.


1. **Any other comments?**
    
    None.





## Uses


1. **Has the dataset been used for any tasks already?** *(If so, please provide a description.)*
    
    The dataset has been used to investigate the degree to which BLM has become a truly international movement. Further research regarding the nature of the BLM discourse across different geographic and linguistic areas is ongoing.


1. **Is there a repository that links to any or all papers or systems that use the dataset?** *(If so, please provide a link or other access point.)*
    
    No. When available, working papers will be posted at the author's website, www.maurits.net.


1. **What (other) tasks could the dataset be used for?**
    
    The dataset could be used for a range of studies into the national and international discourse about BLM, including tweet contents, sharing networks, etc.


1. **Is there anything about the composition of the dataset or the way it was collected and preprocessed/cleaned/labeled that might impact future uses?** *(For example, is there anything that a future user might need to know to avoid uses that could result in unfair treatment of individuals or groups (e.g., stereotyping, quality of service issues) or other undesirable harms (e.g., financial harms, legal risks)  If so, please provide a description. Is there anything a future user could do to mitigate these undesirable harms?)*
    
    No.


1. **Are there tasks for which the dataset should not be used?** *(If so, please provide a description.)*
    
    No.



1. **Any other comments?**
    
    None.




## Distribution


1. **Will the dataset be distributed to third parties outside of the entity (e.g., company, institution, organization) on behalf of which the dataset was created?** *(If so, please provide a description.)*
    
    Yes, the dataset is freely available.


1. **How will the dataset will be distributed (e.g., tarball  on website, API, GitHub)?** *(Does the dataset have a digital object identifier (DOI)?)*
    
    The dataset is free for download at Zenodo


1. **When will the dataset be distributed?**
    
    The dataset is distributed as of June 2022 in its first version.


1. **Will the dataset be distributed under a copyright or other intellectual property (IP) license, and/or under applicable terms of use (ToU)?** *(If so, please describe this license and/or ToU, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms or ToU, as well as any fees associated with these restrictions.)*
    
    The dataset is licensed under a ?? license.


1. **Have any third parties imposed IP-based or other restrictions on the data associated with the instances?** *(If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any relevant licensing terms, as well as any fees associated with these restrictions.)*
    
    Not on the tweet ids, which are the only part of a tweet included in the dataset.


1. **Do any export controls or other regulatory restrictions apply to the dataset or to individual instances?** *(If so, please describe these restrictions, and provide a link or other access point to, or otherwise reproduce, any supporting documentation.)*
    
    Not to my knowledge.


1. **Any other comments?**
    
    None.





## Maintenance


1. **Who is supporting/hosting/maintaining the dataset?**
    
    The dataset is maintained by the author, A. Maurits van der Veen


1. **How can the owner/curator/manager of the dataset be contacted (e.g., email address)?**
    
    The contact e-mail address is at the top of this document.


1. **Is there an erratum?** *(If so, please provide a link or other access point.)*
    
    Currently, no. If errors are found (e.g. tweet ids are included that should not be, or the tagging of explicit references to Black, Blue, or All Lives Matter is incorrect, versioned updates will be posted.


1. **Will the dataset be updated (e.g., to correct labeling errors, add new instances, delete instances')?** *(If so, please describe how often, by whom, and how updates will be communicated to users (e.g., mailing list, GitHub)?)*
    
    The dataset will be extended monthly. Updates for the sake of correction will be posted as the need arises.


1. **If the dataset relates to people, are there applicable limits on the retention of the data associated with the instances (e.g., were individuals in question told that their data would be retained for a fixed period of time and then deleted)?** *(If so, please describe these limits and explain how they will be enforced.)*
    
    Not regarding the tweet ids.


1. **Will older versions of the dataset continue to be supported/hosted/maintained?** *(If so, please describe how. If not, please describe how its obsolescence will be communicated to users.)*
    
    Yes; the data will be versioned.


1. **If others want to extend/augment/build on/contribute to the dataset, is there a mechanism for them to do so?** *(If so, please provide a description. Will these contributions be validated/verified? If so, please describe how. If not, why not? Is there a process for communicating/distributing these contributions to other users? If so, please provide a description.)*
    
    Errors may be submitted via email. Supplements of ids not included that do fit the inclusion criterion can also be submitted via email to the author, and will be added in new versioned releases.


1. **Any other comments?**
    
    None.
