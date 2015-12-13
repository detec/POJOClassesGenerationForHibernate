# POJO classes generation for Hibernate ORM in 1C 8.3 #

This is a mirror of my 1C 8.3 project, originally published at Infostart <http://infostart.ru/public/359102/>

## Description ##

This tool is a 1C:Enterprise implementation of Hibernate Reverse Engineering for Netbeans, Hibernate Reverse Engineering standalone and other IDE or standalone tools that generate classes for Hibernate based on existing database schema. It generates entity classes with Hibernate annotations from 1C 8.3 database where this tool is launched. Additionally it generates mapping class strings for hibernate.cfg.xml.

## Target audience ##

This small open-source tool will be of a great assistance to you in following cases:

- you are familiar with 1C:Enterprise RAD platform  <http://1c-dn.com/> ;
- you want to create a new Java enterprise project with Hibernate ORM framework;
- you don't have a designed database schema in Oracle, MS SQL, Postgres etc.;
- you want to create business entities, stored in database tables, quickly, without spending much time on consistency tasks such as primary keys and so on;
- you have a specification in your native language and you want to translate the entity fields' names automatically into English or other language.


## Features and limitations of current version ##

- Hard-coded Russian-to-English translation direction (string "from=ru&to=en" in the source code). Therefore, after consulting to Bing Translator API site, you can replace the languages used up to your needs in the source code in 1C Designer. Also you can use English names in fields that will be processed by Bing without translation.
- You can convert  entities in following 1C:Enterprise metadata types: references, enumerations, periodic and non-periodic tables. References with pre-defined elements are treated as enumerations.
- Documents and composite type fields are not supported.
- Object codes, 1C built-in readable identifiers, are converted to Hibernate Id-fields with primitive type long.
- There is an option to include Jackson annotations to fields for JSON serialization: @JsonProperty, @JsonManagedReference, @JsonBackReference.


## System requirements ##

- 1C:Enterprise full client installation from version 8.3.6 or higher. You can use a free Trainee version to design database structure <https://1c-dn.com/user/updates/1c_enterprise_platform_training_version/>.
- Hibernate ORM framework version 4.3.x dependency in your Java project. Other versions were not tested.
- Bing Translator API key, it is subscription fee free up to 2 mln. of translated symbols per month per key. 