# Grep Command
-The grep command is used in the searching and matching text files contained in the expression.

'-i' option: This option tells 'grep' to perform a case-insensitive search. For example, inputting in "bye" will return 
ALL lines that contain bye, BYE, ByE, etc.
   
   ex 1:
   The file we will be using for this example is "./pmed.0020191.txt"
   
   Our input line:
   ```
   grep -i "tHe" ./pmed.0020191.txt
   ```
   
   Our output line:
   ```
   The excellent article by Jordan Paradise, Lori B. Andrews, and colleagues, “Ethics.
        Constructing Ethical Guidelines for Biohistory” [1], neither advocates nor argues against
        taking place without guidelines—ethical, scientific, moral, or religious. The question
        permission? Who is to decide what is “historically significant”? Not to mention the
        meta-question: who is to decide who is to decide? I apologize to the authors if my brief
        comments [2] implied that they took a position on this issue.  
   ```
   The input in the command line "tHe", will still return all lines in the file that include "the", "tHe", "THE".
   
   
   ex 2:
   The file we will be using for this example is "rr74.txt" in biomed
   
   Our input line:
   ```
   grep -i "IDE" rr74.txt
   ```
   
   Our output line:
   ```
   methylsulfonyl fluoride was added. Samples were
          polyvinylidene difluoride membrane (Amersham Pharmacia
          lipopolysaccharide-treated mouse spleen protein and
          Hematocrit and nitric oxide metabolite
          chloride (Sigma-Aldrich) dissolved in 1 N HCl at 90°C to
          P < 0.05 is considered
          was lipopolysaccharide-treated mouse spleen) and using
          Nitric oxide metabolites
        exposure or exposure from neonatal life provided additional
        been identified in the eNOS promoter. Recently, altering
        lipopolysaccharide administration [ 24].
        In summary, we identified a unique pattern of NOS
        considering studies using NOS-deficient mice. The present
        eNOS = endothelial nitric oxide synthase; iNOS =
        inducible nitric oxide synthase; nNOS = neuronal nitric
        oxide synthase; NO = nitric oxide; NOS = nitric oxide
   ```
   The input in the command line "IDE", will still return all lines in the file that include "ide", "iDe", "IDE".
