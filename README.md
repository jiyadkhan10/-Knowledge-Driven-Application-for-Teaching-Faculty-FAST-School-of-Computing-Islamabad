# Knowledge Driven Application for Teaching Faculty FAST School of Computing Islamabad

# Course

CS4102 Introduction to Knowledge Graphs and Linked Data <br />

# Description

# Data Set Link
https://docs.google.com/spreadsheets/d/1z4w8Y6v5mwOeyAsztaLcoPqtQOqJJT7jtivVWUcdehQ/edit#gid=0 <br />
# Domain Description
The selected domain of the project is Knowledge driven application for Teaching Faculty FAST School of computing Islamabad for Fall 2022. For this purpose, we’ll be using the FAST NUCES "Courses Allocation, Fall-2022 Semester" data set, communicated to the students via email. The dataset contains all the information regarding all the courses offered in the semester, course code, and Teacher allocated to each course. The data will be discussed in detail later on. Our end Product will be a knowledge-driven application for our university that can answer the mentioned competency questions. Our goal is to create an ontology that could help in the analysis of any type of faculty allocation to any course. <br />

# Dataset Description

The dataset contains the following attributes mentioned as follows: <br />

Code: Course Code for each course. <br />
Course: Course Name <br />
CHS: Number of Credit Hours for each Course. <br />
Section: Sections in which that particular course is being offered.<br />
Course Instructor: Instructor assigned to the particular section and course. <br />
Course Coordinator: Coordinator name assigned to any course. <br />
Batch Allocation: The data set is further divided into sections according to the batch in which those courses are offered. <br />

# Competency Questions

Following are the competency questions that are we aiming to query from the final version of our application: <br />

1. User should be able to query the names of all the teaching faculty. <br />
2. User should be able to query the names of all the courses being offered in Fall 2022. <br />
3. User should be able to query the names of all the elective courses. <br />
4. User should be able to query the names of all the core courses. <br />
5. User should be able to query the credit hours of any courses. <br />
6. User should be able to query the type of any courses. <br />
7. User should be able to query the coordinator of any course. <br />
8. User should be able to query the section-wise allocation of courses. <br />
9. User should be able to query the section-wise allocation of coordinators. <br />
10. User should be able to query the designation of all the teachers. <br />
11. User should be able to query the courses being taught by any teacher. <br />
12. User should be able to query the number of courses any teacher teaches. <br />
13. User should be able to query the max number of courses any teacher teaches. <br />
14. User should be able to query the min number of courses any teacher teaches. <br />
15. User should be able to query the section-wise allocation of any teacher. <br />
16. User should be able to query the number of courses any teacher teaches. <br />

# External Data Set Link

For faculty designation, we have used an external link http://isb.nu.edu.pk/Faculty/allfaculty. <br />

# Modeling Decisions

1. Mapped all the classes and subclasses as present in the conceptual model. <br />
2. Made teacher and course class disjoint <br />
3. Made visiting subclass disjoint with all sibling classes <br />
4. Object property Restriction on visiting for teaches have max cardinality 4 <br />
5. Object property Restriction on visiting for teaches have min cardinality 1 <br />
6. Mad coordinator class disjoint only with visiting class <br />
7. Made the professor’s class disjoint with the lecturer and visiting <br />
8. Object property Restriction professor on teaches have max cardinality 4 <br />
9. Object property Restriction professor on teaches have min cardinality 1 <br />
10. Made assistant professor class disjoint with the professor, lecturer, and visiting <br />
11. Object property Restriction assistant professor on teaches have max cardinality 4 <br />
12. Object property Restriction assistant professor on teaches have min cardinality 1 <br />
13. Made lecturer class disjoint with the professor, assistant professor, and visiting <br />
14. Object property Restriction Lecturer on teaches have max cardinality 4 <br />
15. Object property Restriction Lecturer on teaches have min cardinality 1 <br />
16. Made object property HasNumCRs and IsOfNumCRs transitive as well inverse <br />
17. Made teacher a named class <br />
18. Made the object property section a functional class <br />
19. Made. the object property Teaches functional <br />
20. Object property Teaches has domain teacher and range Course <br />
21. Object restriction property on Courses, i-e course HasCoordinator Some Coordinator <br />
22. Object restriction property on Teacher i-e teaches some course <br />
23. Made the Course an enumerated class i-e covering of core or elective <br />
24. Data property Course ID have domain Course and range rdfs: Literal <br />
25. Data property Num Crs (No. of CRs) have domain Course and range xsd:int <br />
26. Data property HasCoord have domain Course and range rdfs: Literal <br />
27. Data property CourseName have domain Course and range rdfs: Literal <br />
28. Data property SectionName have domain Course and range rdfs: Literal <br />
29. Data property Restriction on NumCRs have max cardinality 4 <br />
