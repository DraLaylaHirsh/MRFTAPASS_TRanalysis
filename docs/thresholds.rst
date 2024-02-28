
THRESHOLD RULES for TAPASS prediction types in Tandem Repeats regions
=====================================================================
Transmembrane region
--------------------
For each of the identified lines for the protein In TAPASS file:  Calculate the total number of amino acids of the TAPASS prediction (Ntaa) and the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region). 

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achieved (coverage>=50)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the transmembrane list (external file).
(External file: ID, first, last)

The coverage is calculated by:
Coverage=(Naao /  Ntaa) * 100 >= 50
In the example: 
A (2/4)x100 = 50 >= 50 ,  threshold achieved
B  (3/3)x100 = 100  >=50 , threshold achieved
C (2/5)x100 = 40 < 50, threshold not achieved


.. image:: /images/transmembrane.png

Consensus disordered region
---------------------------

For each of the identified lines for the protein In TAPASS file:  Calculate the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region),  and add all the resulting values to obtain a total number of overlapped amino acids(TNaao). Calculate the total number of amino acids(MRFaa) in the MRF Tandem repeat region (TR region). 

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achieved (coverage >= 50)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the disorder list (external file). 
(External file: ID, first, last)
The coverage is calculated by:
TNaao = \Sigma (Naao of each disorder region)
Coverage = (TNaao /  MRFaa) * 100 >= 50
In the example: 
TNaao = A + B + C = 2 + 3 + 2 = 6
MRFaa = 23
Coverage = (6 / 23)*100 = 26.09, threshold not achieved

.. image:: /images/disorder.png

Functional domain
-----------------
For each of the identified lines for the protein In TAPASS file:  Calculate the total number of amino acids of the TAPASS prediction (Ntaa) and the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region). 

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start, end 

If the threshold is achieved (coverage>=60)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the functional domain list (external file).
(External file: ID, first, last, accession)

The coverage is calculated by:
coverage = (Naao /  Ntaa) * 100 >= 60
In the example: 
A (3/5)x100 = 60 >= 60 ,  threshold achieved
B (3/3)x100 = 100  >=60 , threshold achieved
C (2/5)x100 = 40 < 60, threshold not achieved

.. image:: /images/functional.png

SLIMs
-----
For each of the identified lines for the protein In TAPASS file:  Calculate the total number of amino acids of the TAPASS prediction (Ntaa) and the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region). 

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achieved (coverage>=50)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the SLIM list (external file).
(External file: ID, first, last, accession)

The coverage is calculated by:
coverage = (Naao /  Ntaa) * 100 >= 50
In the example: 
A (2/4)x100 = 50 >= 50 ,  threshold achieved
B (3/3)x100 = 100  >=50 , threshold achieved
C (2/5)x100 = 40 < 50, threshold not achieved

.. image:: /images/slim.png

Structured domain
-----------------
For each of the identified lines for the protein In TAPASS file:  Calculate the total number of amino acids of the TAPASS prediction (Ntaa) and the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region). 

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achieved (coverage>=50)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the structural domain list (external file).
(External file: ID, prediction tool, first, last, accession)

The coverage is calculated by:
coverage = (Naao /  Ntaa) * 100 >= 50
In the example: 
A (3/4)x100 = 60 >= 50 ,  threshold achieved
B (3/3)x100 = 100  >=50 , threshold achieved
C (3/6)x100 = 50 >= 50, threshold achieved

.. image:: /images/structured.png

Amyloidogenicity_AR
--------------------
For each of the identified lines for the protein: Calculate the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region).

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achieved (Naao>=15)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the amyloidogenicity_AR list (external file).
(External file: ID, prediction type, prediction tool,first, last)

The coverage is calculated by:
(Ntaa) >= 15
In the example: 
15 >= 15 ,  threshold achieved
6  < 15 , threshold not achieved


.. image:: /images/AR.png

Amyloidogenicity_EAR
--------------------
For each of the identified lines for the protein: Calculate the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region).

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achieved (Naao>=15)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the amyloidogenicity_EAR list (external file).
(External file: ID, prediction type, prediction tool,first, last)

The coverage is calculated by:
(Ntaa) >= 15
In the example: 
15 >= 15 ,  threshold achieved
6  < 15 , threshold not achieved

.. image:: /images/EAR.png
