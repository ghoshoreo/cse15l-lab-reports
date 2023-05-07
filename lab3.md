Lab Report 3
============
Welcome to my third lab report for CSE 15L ! This lab report will explore the interesting command-line options for the command `grep`.


A little about `grep`
---------------------

The `grep` command is a powerful and versatile Unix/Linux utility tool used to search for specific patterns of text in files. This can be incredibly helpful when you need to find specific information in a large text file or locate all occurences of a particular string in a directory full of files. Additionally, `grep` supports regular expressions, which allows for complex pattern matching and seamless data extraction. Indeed, the `grep` command is a highly useful tool hat can save you a lot of time and effort when working with text files on Unix/Linux systems.

The basic syntax is as follows:

`grep [options] pattern [file...]`


`grep -w`
---------

The `-w` option matches the pattern only as a whole word. 

**Example 1**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:468$ grep -w  on ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`        on health than on mortality. If so, then behavior change
        they were evaluated on improved health, rather than on
        analyses based on years of life (YOL) or on YHL would
          or active life expectancy [ 14 ] . We based YHL on
          incomplete covariate data, leaving 4,878 persons on whom
          follows. We regressed YOL and YHL first on age, age
          second on all of the covariates listed above. We
        significantly on BMI, BMI>30, weight loss since age 50,
        YOL for women (the uppermost curve on Figure 1) averaged
          Based on these findings, trials to address obesity in
          would probably not have a direct effect on either YOL or
          EVGFP, on which YHL was based, might have missed some
          effects of obesity on risk factors for future health. A
          pain would surely have worse EVGFP than others, based on
          were based on such measures, the superiority of YHL to`
          
**Example 2**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:469$ grep -w most  ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`        most robust health as we age. It has been suggested that
        men were most likely to have unintentionally lost more than
        lost to death (7 minus YOL). White women had the most YHL
        and black men the fewest; black women had the most years of
        the most years to death (1.3 out of 7) while white women `

In summary, the `-w` option in the `grep` command is a useful tool when you need to match a pattern as a whole word and exclude partial matches. It can be particularly helpful when you need to search for specific words or patterns in log files or code files.

`grep-i`
--------

The `-i` option performs a case-insensitive search.

**Example 1**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:471$ grep -i THIS ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`        events [ 10 ] . In this paper we study whether BMI at
          For this analysis we defined YHL as the number of
          drawback of this simple definition of 'healthy' is that
          this analysis is based.
          plus the grand mean. The mean of this new variable, for a
          required to detect an effect of this magnitude is
        with 20-24.9 in all comparisons. For this reason, and to
        YOL, but this group was not significantly different from
          people's YHL. This suggests that the development of
          adults are the subjects. This is particularly important
          significant in this patient group.
          10% of the sample, but results with and without this
          persons, but we think this is unlikely given the absence
        'overweight' by the NHLBI guidelines. This suggests using`

**Example 2**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:472$ grep -i analysis ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:
`
          For this analysis we defined YHL as the number of
          primary analysis we used observed 7-year YOL and YHL why
          this analysis is based.
          Analysis
          intervals or analysis of variance. Finally we calculated
          group were similar. Analysis of mean YOL instead of the
          more traditional survival analysis survival analysis was
        present in the mortality analysis, suggesting that YHL may`
        
Overall, the `-i` option in the `grep` command is particularly useful in ensuring that we locate all the occurences of a given string, regardless of the status of their case. 

`grep -n`
---------

The `-n` option displays the matching lines along with their respective line numbers.

**Example 1**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:473$ grep -n  analysis ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`
94:          For this analysis we defined YHL as the number of

117:          primary analysis we used observed 7-year YOL and YHL when

146:          this analysis is based.

168:          intervals or analysis of variance. Finally we calculated

372:          more traditional survival analysis survival analysis was

404:        present in the mortality analysis, suggesting that YHL may`


**Example 2**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:473$ grep -n  obsese ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`
184:        percent obese (BMI ≥ 30) than the other three groups. Black

259:        classified as normal, overweight or obese all had about the

263:        about 4.9 YHL. The YHL for underweight or obese women was

269:        the sexes had similar YHL in the underweight and obese

294:        would be needed. For comparing obese to normal, only YHL

299:        make obese women comparable to normal women could be

303:        overweight (for men or women) or obese (for men) affects

322:          overweight (as opposed to the obese) are no different

336:          being obese to being normal would likely show changes in

412:        obese or underweight older adults, and discouraging trials`

The `-n` is handy when you need to search the line numbers associated with a given string. It can be particularly helpful when you need to locate specific lines in a file or when you need to extract data from log files or other types of text files.

`grep -c`
----------

The `-c` option displays the number of matching lines.

**Example 1**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:473$ grep -n  obsese ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`10`

**Example 2**

*Input*:

`[cs15lsp23rg@ieng6-203]:stringsearch:479$ grep -c analysis ./stringsearch-data/technical/biomed/1468-6708-3-1.txt`

*Output*:

`6`

In summary, the `-c` option of the `grep` command is particularly useful when you only need to count the total number of occurences of a given string. This can come in clutch when you are searching for common words like "in" or "the" and want to avoid seeing all the lines in which the word appears.


Citations
---------

This lab report was made possible with the help of the `man grep` command and information listed by ChatGPT!


*This brings us to the end of my lab report 3 for CSE15L. Thanks for reading through! :)*












