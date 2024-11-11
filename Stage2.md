# Specification Stage
The purpose of the Specification Stage is to assemble the necessary details so that an experiment is ready to go live on the platform. The following elements are needed:

## TO-DO 

- Human subjects protocol approval

- Specification of manipulations (mostly through implementation of an appropriate endpoint)

- Specification of measurements (mostly though specification of questionnaire and survey questions)

- Specification of user population (not yet supported)

## Human Subjects
A protocol outline document is provided in each experiment’s GitHub repository. This provides a starting point for researchers to develop a protocol for their specific experiment. Each institution’s Institutional Review Board (IRB) will have slightly different requirements for how human subjects research should be handled. Key things to know about POPROX experiments:

- All user data is anonymized by the platform. Researchers do not have access to personally-identifiable information (PII) for any user.

- There is an umbrella protocol covering the POPROX platform as a whole. Most experiments are already pre-approved under this protocol and only need approval by the researcher(s) local IRB(s).

- Some types of studies are not covered under the umbrella protocol and would need additional approval by POPROX’s external IRB even if approved by a local IRB. See [Outside of protocol experiments](https://docs.poprox.ai/guide/stages/specification.html#Outside-of-protocol-experiment) below.

- Some types of studies are not allowed on the platform at all. See [Disallowed experiments](https://docs.poprox.ai/guide/stages/specification.html#disallowed-experiments) below.

## Within-protocol experimental designs
This type of experiment fits within the basic human study design criteria that can be covered by the basic protocol approved by the POPROX Institutional Review Board (IRB). It should not require separate user consent nor additional reviews by POPROX IRB. Researchers need to follow their institutions’ IRB review process. If no local IRB is available, researchers are required to get an external approval. Examples of such type of experiments are provided below:

- Placing headers and slugs of news in various locations or layouts;

- Presenting explanations for or annotations of article stubs;

- Presenting new machine-generated summarization of news;

- New machine learning algorithm efficiency test by replacing top-recommended personalized news with more objective and unbiased news.

## Disallowed experiments
- Researchers may not introduce inappropriate content, significant deception, or use interventions we believe would be harmful to retaining our user base. For example:

    - Use of pornography or graphic violence in news display;

- We reserve the right to disallow experiments if, in consultation with our advisory board, we believe that they will be harmful to the long-term viability of POPROX as a platform. For example:

    - New interface experiment by inserting advertisements into different locations on the newsletter and testing user click-through rates on different treatments.

## Outside of protocol experiments
This type of experiment does not fall within the bounds of the POPROX guidelines and POPROX IRB protocol. It needs researchers’ local or external IRB review, and will then require a modification of the POPROX protocol to be submitted (by the POPROX team) for POPROX IRB review. Outside-protocol experiments will be first reviewed by the POPROX advisory board to determine whether to proceed to IRB review, implementation, and deployment. Examples of such type of experiments are provided below:

- New interface or content experiment with manipulated or deceptive news headers, slugs, or media on different geo-located user groups;

- News natural-language processing (NLP) study by training users’ historic text feedback to further exploit their recommendation preferences;

- New pop-up windows containing questions for users’ personal opinions on political news that are included within daily newsletters;

- New human-AI interaction study by manipulating the original content of news articles with generative AI algorithms and testing users’ engagement patterns;

## Key points for human subjects
- Researchers do not have to get consent. All POPROX participants have already given consent in order to be on the platform.

- Researcher do not have access to an personnally-identifiable information (PII). POPROX handles all of this information including participants email addresses.

- Reseachers do not have to manage experimental data coming from human subjects except the finalized data sets that POPROX delivers.

## Manipulations
By manipulations, we mean steps that researchers take to alter the experience of one or more group of users with the aim of measuring a change in their response. A POPROX experiment may not require manipulations: for example, a researcher might wish to study trends in response the newsletter as a function of what stories are delivered without changing the recommendation algorithm.

## Algorithmic manipulation
One major type of experiment that POPROX supports is the ability to change or substitute for the default recommendation algorithm that drives the personalized newsletters that users receive. That algorithm is described and its code is provided [at our GitHub repo](https://github.com/CCRI-POPROX/poprox-recommender). Researchers are free to implement recommendation algorithms of their own, with or without this code as a base. Key requirements are that the algorithm takes the documented JSON input and returns a list of recommendations per the specification.

Note that the API is subject to enhancement, amd we are interested in hearing from researchers about use cases for algorithmic experimentation that are not covered by this version of the API.

## Display manipulation
We do not currently support the ability to modify the manner in which recommendations are displayed within the POPROX email.

We are interested in hearing from researchers about experiments that would explore presentation and explanation aspects of POPROX recommendations.

## Manifest
A key output of the specification phase is an experiment manifest, the formal description of the experiment that will be compiled and used by the POPROX platform to execute the experiment in the Testing and Operational phases. See [Manifest documentation](https://docs.poprox.ai/reference/experiments/manifest.html) for additional details.

## Measurements
By measurements, we means the information we gain about subjects who are using the system. POPROX currently supports three kinds of input from users:

- On-boarding questionnaire: Users who are joining POPROX fill out a questionnaire including demographic information and news reading preferences. This information can be used by experimenters, for example, to customize news to different demographic groups.

- Click-throughs: When a user clicks on a story to read it, they are directed to the original article on the AP website through a POPROX server. We keep a log of all stories clicked by the user and these are supplied to the recommender as part of the recommendation request.

- Surveys: Every other week, POPROX users are sent a survey about their news reading experiences. T

Document final survey structure and contents.

For technical and contractual reasons, we are not able to obtain additional behavioral data such as user scrolling behavior, read time, etc.

## Custom surveys
It is possible for researchers to add their own questions to surveys. Right now, it is only possible add survey questions to be sent to the entire experimental population.

In future versions of POPROX, we will support:

- Survey questions based on treatment

- Survey questions based on user characteristics

- (eventually) Survey questions based on user behavior over the course of the study

As above, we are interested in hearing from researchers about experiments that would explore a variety of survey designs as part of their POPROX studies.