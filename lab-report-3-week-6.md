# Lab report3

**Find -name**
-why useful? because we can directly searche for files by their name.
- Using find from command line to locate files by name, search for *.txt files in the technical/911report directory and all sub-directories.
```
$ find technical/911report -name "*.txt"

technical/911report/chapter-13.4.txt
technical/911report/chapter-13.5.txt
technical/911report/chapter-13.1.txt
technical/911report/chapter-13.2.txt
technical/911report/chapter-13.3.txt
technical/911report/chapter-3.txt
technical/911report/chapter-2.txt
technical/911report/chapter-1.txt
technical/911report/chapter-5.txt
technical/911report/chapter-6.txt
technical/911report/chapter-7.txt
technical/911report/chapter-9.txt
technical/911report/chapter-8.txt
technical/911report/preface.txt
technical/911report/chapter-12.txt
technical/911report/chapter-10.txt
technical/911report/chapter-11.txt
```
- Find files called chapter-*.txt means files name contains 'chapter-' and 'txt' in current technical directories and all sub-directories
```
technical wangwenshuang$ find . -name "chapter-*.txt"
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-3.txt
./911report/chapter-2.txt
./911report/chapter-1.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-9.txt
./911report/chapter-8.txt
./911report/chapter-12.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
```

- Find files called *.txt means files name contains '.txt' in current technical/government/Post_Rate_Comm directories and all sub-directories.
```
technical wangwenshuang$ find government/Post_Rate_Comm -name "*.txt"
government/Post_Rate_Comm/Gleiman_EMASpeech.txt
government/Post_Rate_Comm/Mitchell_spyros-first-class.txt
government/Post_Rate_Comm/Cohenetal_CreamSkimming.txt
government/Post_Rate_Comm/Cohenetal_DeliveryCost.txt
government/Post_Rate_Comm/Mitchell_RMVancouver.txt
government/Post_Rate_Comm/Gleiman_gca2000.txt
government/Post_Rate_Comm/Cohenetal_Cost_Function.txt
government/Post_Rate_Comm/Redacted_Study.txt
government/Post_Rate_Comm/Mitchell_6-17-Mit.txt
government/Post_Rate_Comm/Cohenetal_comparison.txt
government/Post_Rate_Comm/Cohenetal_Scale.txt
government/Post_Rate_Comm/Cohenetal_RuralDelivery.txt
government/Post_Rate_Comm/ReportToCongress2002WEB.txt
government/Post_Rate_Comm/WolakSpeech_usps.txt
```
**find -type**
-why useful? Because it can directly and easily find all files or directories of the directory.
- Find only files in technical/911report directories.
```
technical wangwenshuang$ find ./911report -type f -print
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-3.txt
./911report/chapter-2.txt
./911report/chapter-1.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-9.txt
./911report/chapter-8.txt
./911report/preface.txt
./911report/chapter-12.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
```
- Find only directories in current technical directories and all sub-directories.
```
technical wangwenshuang$ find . -type d
.
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
./plos
./biomed
./911report
```
- Find only directories in current technical/government directories and all sub-directories.
```
technical wangwenshuang$ find ./government -type d -name "*"
./government
./government/About_LSC
./government/Env_Prot_Agen
./government/Alcohol_Problems
./government/Gen_Account_Office
./government/Post_Rate_Comm
./government/Media
```

**find -maxdepth**
-why useful? It takes less time than searching the entire directory becasue we only need to do a limited search only in the current ditectory.
-  Do a limited search only in the current directory technical and go 1 level deep to find files contains 'txt'.
```
technical wangwenshuang$ find ./911report -maxdepth 1 -name "*.txt" 
./911report/chapter-13.4.txt
./911report/chapter-13.5.txt
./911report/chapter-13.1.txt
./911report/chapter-13.2.txt
./911report/chapter-13.3.txt
./911report/chapter-3.txt
./911report/chapter-2.txt
./911report/chapter-1.txt
./911report/chapter-5.txt
./911report/chapter-6.txt
./911report/chapter-7.txt
./911report/chapter-9.txt
./911report/chapter-8.txt
./911report/preface.txt
./911report/chapter-12.txt
./911report/chapter-10.txt
./911report/chapter-11.txt
```
- Do a limited search only in the current directory technical and go 2 level deep to find files contains 'Session' and 'txt'.
```
technical wangwenshuang$ find ./government -maxdepth 2 -name "Session*.txt" 
./government/Alcohol_Problems/Session2-PDF.txt
./government/Alcohol_Problems/Session3-PDF.txt
./government/Alcohol_Problems/Session4-PDF.txt
```
- Do a limited search only in the current directory technical and go 1 level deep to find files contains 'txt' and no such files exit.
```
technical wangwenshuang$ find . -maxdepth 1 -name "*.txt"
```