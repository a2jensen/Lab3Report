# Grep Command
The grep command is used in the searching and matching text files contained in the expression, where it filters text files based on your input. The command can search for exact matches, partial matches, or patterns using regular expressions. These 4 alternative ways of using the grep command below will show how you can specifically edit the outputs you desire.

# '-i' option 
This option tells 'grep' to perform a case-insensitive search. For example, inputting in "bye" will return 
ALL lines that contain bye, BYE, ByE, etc. This is useful for when you are searching for a pattern in a file, but your not sure if there is any capitlization or not. It pretty much broadens your answers.

Source: I used the help of chatgpt and asked it for alternative grep commands. 

ChatGPT prompt: What are alternative grep options?

ChatGPT output:
```
'grep' provides various options that allow you to customize the search behavior. Here are some alternative options commonly used with grep:

-i or --ignore-case: This option enables case-insensitive search. It will match patterns regardless of the letter case. For example, grep -i "example" file.txt will match lines containing "example", "Example", "EXAMPLE", and so on.

-v or --invert-match: This option inverts the match, causing grep to print lines that do not match the specified pattern. For example, grep -v "example" file.txt will print all lines in "file.txt" that do not contain the word "example".

-l or --files-with-matches: This option displays only the names of the files that contain the matching pattern, rather than printing the matching lines themselves. It is useful when you only want to know which files contain a specific pattern. For example, grep -l "example" *.txt will display the names of all text files in the current directory that contain the word "example".
```
   Example 1:
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
   
   
   Example 2:
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




# '-v' option 
This option tells 'grep' to show all lines in the text file that do not contain the expression. This alternative grep command is especially useful for excluding patterns/words you don't wanna see.

Source:
[JavaRevisited](https://javarevisited.blogspot.com/2011/06/10-examples-of-grep-command-in-unix-and.html#axzz80oUFELM8)
   
   Example 1:
   The file we will be using for this example is "rr74.txt"
   
   Our input line:
   ```
   grep -v "a" rr74.txt
   ```
   
   Our output line:
   ```
          Introduction
          immunohistochemistry.
          Mice
          Exposure environments
          Western blotting
          with A 
          260 /A 
          diluted in depC H 
          determined using 18 S rRNA primers/probes (Applied
          RNA.
          Immunohistochemistry  
          2 -, NO 
          (Ionics Instrument Business Group, Boulder, CO, USA).
          P < 0.05 is considered
          Results
          respectively; 
          P < 0.001).
          Western blotting
          As shown in Fig. 2, lung eNOS protein levels were
          3.5-fold (Fig. 3).
          Immunohistochemistry
          shown).
   ```
   The input in the command line returns all lines in the file that do not contain the letter "a".
   
   
   Example 2:
   The file we will be using for this example is "rr74.txt" in biomed
   
   Our input line:
   ```
   grep -v "i" rr74.txt
   ```
   
   Our output line:
   ```
   25-gauge needles, and 10 μl/ml RIPA 10 mg/ml phenyl
          Total RNA was extracted from 100 mg of frozen lung
          260 /A 
          280 >1.8 were used. Samples were
          RNA.
          methyl carnoys (60% methanol, 30% chloroform and 10%
          measurements
          2 -, NO 
          Data are expressed as mean ± standard error of the
        Results
          P < 0.001).
          shown), and nNOS was unchanged among the three
          shown).
        development.
        21].
        reports [ 13, 14, 18]. LeCras 
        et al . [ 13] found that the amount
        et al. [ 15], who found that eNOS
        et al. [ 38] reported 
        et al. [ 42] found that plasma NO
        and decreased O 
        et al. [ 38], then the lack of
        warrants further study.
   ```
   The input in the command line will return all lines in the file that include "i".
   
# '-e' option
This option enables the use of extended regular expressions when using the grep command. This option is useful in a variety of ways, such as using the or "|" command to find two words/patterns.
 
Source: I also used chatgpt where it provided the -e option as an alternative way of using the grep method.


ChatGPT prompt: Any other grep options?

ChatGPT output:
```
The -e option in the grep command allows you to specify multiple patterns to search for. It is particularly useful when you want to search for lines that match any of the specified patterns.

Here's an example usage:

perl
Copy code
grep -e pattern1 -e pattern2 file.txt
In the above command, grep will search for lines in "file.txt" that contain either "pattern1" or "pattern2" and display the matching lines.
```

   Example 1:
   The file we will be using for this example is "cc4.txt"
   
   Our input line:
   ```
   grep -E 'PaO2/FiO2|\bMPAP\b' cc4.txt
   ```
   
   Our output line:
   ```
         decrease in MPAP of at least 2 mmHg and an increase in
          patients responding to NO by a decrease in MPAP and an
          dose-dependent decrease in MPAP, SPAP, DPAP, PVRI,RVSWI
          4.5 ppm for MPAP, PVRI, Q 
          dose-dependent decrease in SPAP, DPAP, MPAP, PVRI, RVSWI,
          inhaled NO for MPAP, PVRI, RVSWI, PaCO 
          patients without septic shock, the decrease in MPAP
          decrease in MPAP (Fig 4c), whereas MPAP continued to
          effect in MPAP at NO concentrations of 4.5 ppm suggesting
          shock (Fig 5), the decrease in MPAP varied from 8 to 32%
          dose-response curve of MPAP (Fig cc) whereas it continued
          concurrent dose-dependent decrease in MPAP and an
          in each group) a plateau effect for MPAP could be
          4.5 ppm. In six patients (three in each group) MPAP
          on MPAP have been found to be in the range of 1-100 ppm [
          in agreement: a decrease in MPAP > 20% of the control
          9) inhaled NO-induced changes in MPAP and PaO 
          decrease in MPAP, his PaO 
   ```
   With inputs of extended expressions, the output are the lines in the file that contain 'MPAP'.
   
   
   Example 2:
   The file we will be using for this example is "cc4.txt" in biomed
   
   Our input line:
   ```
   grep -E 'inhal|exhal' cc4.txt
   ```
   
   Our output line:
   ```
   inhaled NO has been shown to selectively dilate pulmonary
        injury receiving inhaled NO, a dose-dependent increase in
        the optimal dose of inhaled NO in humans is of critical
        responsiveness to inhaled NO [ 14]: among 25 patients with
        ARDS and septic shock, only 40% responded to inhaled NO
        responding to inhaled NO by an increase in PaO 
        could modify the dose-response to inhaled NO. We wanted to
          4. positive response to inhaled NO, defined as a
          inhalation at an inspiratory concentration of 15 ppm.
          evaluation of dose-response to inhaled NO would have been
          and tracheal concentrations of inhaled NO. After
          inhaled NO.
          2 was maintained during NO inhalation,
          control values after the cessation of inhaled NO.
          inhalation.
          inhaled NO for MPAP, PVRI, RVSWI, PaCO 
          2, 3). As shown in Fig 2, the effect of inhaled NO on PaO
          inhaled NO increased PaO 
          In patients without septic shock, inhaled NO increased
          inhaled NO.
          inhaled NO
          Although the mean pulmonary vascular effect of inhaled
          hypothesized that the same degree of inhaled NO-induced
          interferences between these agents, inhaled NO and
          membrane oxygenation, dose-response curves of inhaled NO
          inhaled NO: (1) the anatomical remodeling of the
          less and less sensitive to inhaled NO. If the alveolar
          responsiveness to inhaled NO [ 14]. However, due to the
          dose-response of inhaled NO on pulmonary artery pressure
          9) inhaled NO-induced changes in MPAP and PaO 
          does not modify the inhaled NO-induced pulmonary artery
   ```
   The input in the command line will return all lines in the file that include 'inhal' OR 'exhal'.


# '-c' option
This option will print the number of lines that includes the expression given. This is specifically useful for seeing the amount of file lines in a alternative way, where instead of printing out all the possible lines it just gives the number of lines making your answer shorter.

Source: [JavaRevisted](https://javarevisited.blogspot.com/2011/06/10-examples-of-grep-command-in-unix-and.html#axzz80oUFELM8)
   
   Example 1:
   The file we will be using for this example is "rr74.txt"
   
   Our input line:
   ```
   grep -c "a" rr74.txt
   ```
   
   Our output line:
   ```
         351
   ```
   With inputs of 'a', this returns the number of lines which include a in the file which is 351.
   
   
   Example 2:
   The file we will be using for this example is "cc4.txt" in biomed
   
   Our input line:
   ```
   grep -c "experimental" cc4.txt
   ```
   
   Our output line:
   ```
   2
   ```
   The input in the command line will return that 2 lines in the file include the word experimental.

