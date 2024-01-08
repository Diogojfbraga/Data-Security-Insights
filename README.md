ABSTRACT
BACKGROUND: The background of this study orbits around analysing a dataset spanning four years from 2019 to 2022, which contains information on cybersecurity incidents and data breaches. The dataset provides insights into the types of incidents, affected data subjects, sectors targeted, and other relevant information.

OBJECTIVE: The objective of this study is to gain a comprehensive understanding of the cybersecurity landscape based on the provided dataset. The aim is to identify trends, patterns, and key insights related to incident types, data subjects affected, sectors targeted, and the response to these incidents.

METHOD: The analysis of the dataset involved web scraping to collect data from the pwned webpage and various data cleaning techniques to ensure data quality. The dataset was explored to understand its structure and variables. Different visualisation techniques, such as bar charts, line plots, and tables, were used to analyse and present the data effectively. Attention was given to accuracy and reliability through data cleaning and validation techniques. Overall, web scraping, data cleaning, and visualisation techniques were key components of the analysis.

RESULTS: The analysis of the dataset uncovered significant insights. Notably, 2019 emerged as the year with the highest number of data breaches, based on the pwned webpage. Over time, there was a gradual decrease in cyberattacks, with a noteworthy rise in incidents during the third quarter (Q3) of each year. Phishing incidents were found to be particularly prevalent among the various types of attacks investigated. The study identified basic personal identifiers as the most commonly compromised data type in the analysed breaches. Sectors such as education and childcare, retail and manufacturing, finance, insurance, credit, general business, and the legal sector experienced a higher frequency of cyberattacks.

On average, each incident impacted approximately 5,168 individuals. The analysis also considered the reporting time for breaches, revealing an average of 41.0 hours. It should be noted that a percentage of breaches exceeded the designated reporting timeframe. The findings underscored the significance of prompt decision-making and timely response in effectively addressing cybersecurity incidents. Taking swift action can help mitigate the repercussions of breaches and safeguard individuals and organisations from further harm.

CONCLUSION: In conclusion, this study provides valuable insights into the cybersecurity landscape based on the analysed dataset. The results emphasise how important it is to protect basic personal information by implementing strong security measures and raising awareness about phishing attacks within organisations. The findings also emphasise the need for prompt reporting, investigation, and appropriate action to mitigate the impact of cyber incidents. These insights can guide organisations and individuals towards strengthening their cybersecurity defences and responding effectively to potential threats.

Table of Contents
Introduction

Project background and aims

2.1 Background

2.2 Aims and Objectives

Data aquisition

3.1 Publicly Available Datasets

3.2 Data limitations

3.3 Data Cleaning and Preprocessing

Analysis

4.1 Explanatory Analysis

4.1.1 Univariate analysis

4.1.2 Bivariable analysis

4.2 Web Scraping

Conclusion and critical evaluation

Ethical Statement

References

Glossary

Introduction
For Parmar (2018), in today's interconnected world, where information flows freely across digital networks, the importance of cybersecurity cannot be overstated. Cybersecurity breaches, which embrace a wide range of malicious activities targeting computer systems, networks, and data, have become an ever-growing concern for individuals, organisations, and governments alike. These breaches not only compromise sensitive information but also have the potential to disrupt critical infrastructure, cause financial losses, and even threaten national security.

Craig et al. (2015), add that cybercriminals constantly evolve their tactics, exploiting sophisticated techniques to take advantage of vulnerabilities and infiltrate systems. From wide-ranging data breaches that compromise millions of user records to targeted attacks on specific companies or individuals, the impact of cybersecurity breaches can be extensive and devastating. For this reason, there is an urgent need for proactive defence measures and a deeper understanding of these breaches.

In Koike (2005) study, the author mentions that at that time, and for many years now, it has been possible to monitor and detect cyber threats. Using network sensors, incidents are logged, and details such as the time of attack, source of attack, and type of attack are statistically analysed so that the investigator can recognise and predict further threats.

Understanding and mitigating cybersecurity breaches requires a comprehensive approach that combines technical expertise, analytical understanding, and proactive measures. In this project, I will explore cybersecurity breaches using the power of Python programming and the interactive capabilities of Jupyter Notebooks.

Project background and aims
Background
Cybersecurity breaches have become an increasingly prevalent and critical issue in today's digital landscape. Due to the rapid advancement of technology and the widespread adoption of interconnected systems, cybercriminals have been provided with ample opportunities to exploit vulnerabilities. As a result, the increase in cyber threats worldwide, has also aroused interest and led to the exponential growth of skilled professionals in the field of cybersecurity.

My passion for technology and my deep-seated interest in safeguarding digital environments have motivated me to future specialise in this area and made me undertake this subject for the midterm project, delving into the intricate world of cybersecurity breaches. I am driven by a desire to understand the inner workings of cybercriminals and possibly contribute to the development of effective defence strategies.

By focusing on data analysis and visualisation using Python and Jupyter Notebooks, I aim to leverage the power of programming and interactive tools to gain valuable insights into cybersecurity breaches.

Through this project, I seek to not only enhance my own understanding, but also contribute to the broader community of cybersecurity professionals and enthusiasts. By sharing my findings, recommendations, and best practises, I aspire to inspire others and raise awareness about the critical importance of cybersecurity.

Note: It is important to remember that this project is purely for educational and analytical purposes. Any analysis performed adheres to ethical guidelines, and there is respect for privacy considerations. Therefore, the use of the data in this dataset was handled responsibly, obtained legally, and used in compliance with applicable laws and regulations. [Please refer to the Ethical Statement section for more details.] (##Ethical-statement). This data set can be found at https://ico.org.uk/ and https://haveibeenpwned.com/PwnedWebsites.

Aims and Objectives
The main objective of this project will be to explore and analyse cybersecurity breaches from the perspective of data treatment, data analysis, and visualisation techniques using Jupyter Notebook and the Python programming language. To achieve this, I will use libraries and Jupyter Notebooks Python techniques, aiming to obtain an understanding of the various aspects of cybersecurity breaches, such as the type of attacks, the impact of these attacks, the relation between the period during which they took place, and the mitigation strategies used to contain or prevent them. My discoveries will hopefully contribute to raise awareness about the importance of security practices and enabling individuals and organizations to safeguard their digital assets.

Finally, by sharing the knowledge gained from this project, I hope to facilitate informed decision-making, enhance cooperation, and improve overall cybersecurity preparedness.

Data aquisition
To conduct a comprehensive analysis of cybersecurity breaches, it is fundamental to collect reliable and relevant datasets that capture everyday incidents. In this project, I will employ various methods to obtain and analyse the necessary data.

Publicly Available Datasets:
I explore publicly available cybersecurity breach datasets that have been made accessible by reliable sources. These datasets were taken from ico's webpage. The Information Commissioner's Office (ICO) is an independent authority operating in the United Kingdom that promotes and enforces information rights, including data protection and privacy laws. It is also responsible for safeguarding information rights and ensuring that individuals' personal data is treated and processed appropriately by organisations. The ICO acts as an independent regulator, only accountable directly to the UK Parliament, and its functions extend beyond data protection to include overseeing freedom of information legislation and ensuring individuals' rights to access public information are protected. It strives to balance the rights of individuals with the rightful needs of organisations to process personal data, promoting transparency, accountability, and trust in the technological era.

In addition to the Information Commissioner's Office (ICO), this project uses another valuable dataset that collects cybersecurity breach datasets and was retrieved from the website "Have I Been Pwned" (https://haveibeenpwned.com/PwnedWebsites). This website provides information about known data breaches and compromised websites. It allows individuals to check if their email addresses or usernames have been involved in any publicly disclosed breaches.

"Have I Been Pwned" aggregates data from various sources, including public databases, security researchers, and disclosed breaches. The website's creator, Troy Hunt, has dedicated significant efforts to compile and maintain this dataset, making it a reliable resource for understanding the extent of data breaches and compromised websites.

By scraping the "Pwned Websites" section of the website, anyone can access a list of websites that have suffered data breaches and had user account information exposed. This information can help researchers, cybersecurity professionals, and individuals stay informed about potential risks and take appropriate actions, such as changing passwords or monitoring their accounts for suspicious activities.

Data limitations
The ICO's dataset has a few limitations:

The data starts in Q2 2019, as incidents were recorded differently prior to this period.
There was a substantial drop in reporting in Q2 2020, which is likely a result of the first national UK coronavirus lockdown in 2020 (March 2020 to June 2020).
There are unknown Data types, Other cyber incidents, and an unknown No. of Data Subjects affected that cannot be properly measurable.
There are data ranges, for example, No. Data subjects affected or 'Time Taken to Report', that when tried to calculate the average might not reflect the real value.
The Pawned dataset:

There is no information in regard to the sector to which the companies belongs.
The "Compromised accounts" depend on the size of the attacked institution. This means that a Year can have the lowest number of breaches but the highest number of Compromised accounts.
Data Cleaning and Preprocessing:
Once the datasets were acquired, I performed the necessary data cleaning and preprocessing steps to ensure data integrity and consistency. On the ICO dataset, this involved removing duplicate entries, handling missing values, standardising data formats, and transforming the data into a suitable format for analysis.

On the Pwned Websites, I utilised BeautifulSoup to parse HTML content and extract relevant information from web pages. The strip() method was employed to remove leading and trailing whitespace characters from strings, ensuring clean and formatted data. The datetime module was used to convert breach dates from string format to datetime objects, facilitating manipulation and formatting of the dates (e.g., extracting the year).

These tools and techniques collectively contribute to data cleaning and preprocessing, ensuring that the extracted data is appropriately formatted for subsequent analysis or storage.
