## Quality control and conduct of genome-wide association meta-analyses (GWAMAs)

The 33 steps to running a GWAMA as outlined in Natural Protocol Paper by [Winkler et al. (2014)](http://www.nature.com/nprot/journal/v9/n5/abs/nprot.2014.071.html?message-global=remove).

1. Identify GWAS partners and lay out rules of cooperation (memorandum of understanding). Form task groups and set up phone meetings.
2. Develop a GWAS analysis plan, including instructions on phenotype transformation, analysis models, covariate adjustment, stratifcation, use of reference panels for imputation and formatting of data submissions
3. Set up an sftp site that will be used to collect and securely store the data and to organize and label directories and subdirectories in a logical, self-explanatory manner
4. Send out the analysis plan and allow 2 months for the collaborators to provide the data.
5. In the meantime, prepare file cleaning instructions and a meta-analysis plan.
6. When all files are available (or at least fles from >80\% of studies), freeze the data (i.e., protect it from further changes and start conducting the file-level QC.
7. To check variable names and format in EasyQC, defne the requested columns and format by using the DEFINE and the EASYIN functions in the ecf header by using option A for imputed data or option B for genotyped Metabochip data.
8. If column names were incorrectly labeled (e.g., if the analyst used ‘Pvalue’ instead of ‘P’), change the column names centrally, as this is more time-effcient
9. Filter monomorphic SNPs. Exclude and count SNPs with allele frequency = 0 or = 1 - in EasyQC, this can be done by using the ‘CLEAN’ function.
10. Filter SNPs with missing values. Exclude and count all SNPs with missing alleles, P value, beta estimate, standard error, allele frequency or sample size. In EasyQC, this can be done by using the ‘CLEAN’ function:
11. Filter SNPs with nonsense values. Exclude and count all SNPs with alleles other than ‘A’, ‘C’, ‘G’ or ‘T’.
12. Filter SNPs on the basis of allele frequency and sample size. Exclude and count SNPs with a sample size less than 30. Add a column called MAC, defned as two times the sample size times MAF, and exclude and count all SNPs with MAC values ≤6.
13. Filter SNPs on the basis of genotype quality.
14. Filter and count SNPs on sex chromosomes. Keep the sex-chromosomal SNPs in a separate fle for optional subsequent analyses. 
15. Harmonize SNP identifers.
16. Filter duplicate SNPs.
17. Save cleaned fles.
18. To perform a fle-level QC check, prepare a summary for each study fle. Count and check the number of SNPs in the cleaned fle and the number of exclusions for each procedure step.
19. Identify analytical issues by the SE-N plot.
20. Check whether the points follow the identity line.
21. Identify analytical issues by using the P-Z scatter plot. 
22. Check whether the points follow the identity line.
23. Identify problems with allele frequencies or strand. To check for strand and allele frequency issues, plot the allele frequency of each SNP and for each fle against a reference allele frequency
24. The frequencies should be distributed along the identity line. Check whether there are patterns  that indicate problems with strand or allele frequencies.
25. Identify population stratifcation.
26. Examine the plot and check whether the inflation factor is above 1.1 in any of the individual studies.
27. Prepare scripts for an inverse variance–weighted meta-analysis by using a fxed-effects model with METAL (two analysts perform the meta-analysis independently).
28. Perform the inverse variance–weighted meta-analysis and create a METAL log file.
29. Compare results from two meta-analysts.
30. Examine the calculated values and the scatter plot to check for discrepancies between the two meta-analysis results.
31. Identify analytical issues by calculating the study-level inflation factor.
32. Consult the relevant study analyst in case of a study-level inflation factor greater than >1.1. If the study analyst then ﬂags analytical errors, then re-analysis is needed.
33. Finalize the meta-analysis. 
