# Analysis of Linked GitHub and Wikidata

Ekaterina Levitskaya<sup>1</sup>, Gizem Korkmaz<sup>2</sup>, Daniel Mietchen<sup>3</sup>, Lane Rasberry<sup>4</sup>

1. Coleridge Initiative, ekaterina.levitskaya@coleridgeinitiative.org
2. Coleridge Initiative, gizem.korkmaz@coleridgeinitiative.org
3. Leibniz-Institute of Freshwater Ecology and Inland Fisheries, daniel.mietchen@googlemail.com
4. University of Virginia, School of Data Science, lr2ua@virginia.edu 

We aim to study the features of GitHub developers that have corresponding Wikidata entries. In this report, we focus on GitHub developers that are associated with academic institutions. First, we explore the countries of these developers to understand major countries that contribute to open source software (OSS). Second, we explore whether there are gender differences with respect to OSS contributions. We analyze number of repositories owned and contributes to, number of commits and code additions. Finally we generate a collaboration network, and study the degree centrality of the users.

About the sample: As noted above, this report explores a sample of OSS contributors. The sample is obtained by extracting GitHub user logins that are associated with academic institutions. This information is obtained from their profile information as well as email domains using the tidyorgs package [cite]. We obtained 109,752 number of users. We used the query below to identify users that are in Wikidata. We obtained 1,481 number of individuals. This notebook provides the code as well as the output of the analyses.

