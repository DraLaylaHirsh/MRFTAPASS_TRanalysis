
THRESHOLD RULES for TAPASS prediction types in Tandem Repeats regions
=====================================================================
Transmembrane region
--------------------
For each of the identified lines for the protein In TAPASS file:  Calculate the total number of amino acids of the TAPASS prediction (Ntaa) and the number of amino acids that are overlapping with the MRF prediction (Naao)  of the Tandem repeat region (TR region). 

TAPASS variables:  first_residue_involved , last_residue_involved
MRF variables: start , end 

If the threshold is achived (coverage>=50)the processed output line should be saved in TAPASS annotation file and the protein repeat region should be saved to the transmembrane list (external file).
(External file: ID, first, last)

The coverage is calculated by:
Coverage=(Naao /  Ntaa) * 100 >= 50
In the example: 
A (2/4)x100 = 50 >= 50 ,  threshold achived
B  (3/3)x100 = 100  >=50 , threshold achived
C (2/5)x100 = 40 < 50, threshold not achived


.. image:: /images/transmembrane.png
