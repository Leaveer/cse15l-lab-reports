grep is an interesting tool. And I'm going to do 4 orders with it.

## 1. “grep” can be use to find all subdirectories by add "-r" behind the grep,

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:168$ grep -r LICR ./technical
./technical/plos/journal.pbio.0020214.txt:        Cancer Research (LICR) based jointly in Zurich, New York, and London, and the Belozersky
./technical/plos/journal.pbio.0020214.txt:        moving toward integration of a research program in Moscow with other LICR projects, and
./technical/plos/journal.pbio.0020214.txt:        real collaboration between Moscow groups and LICR labs elsewhere.
./technical/plos/journal.pbio.0020214.txt:        University [Moscow, Russia] cycle on oncology and immunology sponsored by LICR;
```

This code searched all documents under the technical that match "LICR".

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:170$ grep -r Hopkins ./technical
./technical/biomed/1471-2091-3-4.txt:          Chemistry at Johns Hopkins University. After confirmation
./technical/biomed/1471-2229-3-3.txt:        Compared to the previous report of Hopkins et al. on
./technical/biomed/1471-2261-3-5.txt:        Dr. Hopkins and Dr. Polukoff have been retained as
./technical/biomed/1471-2334-2-27.txt:          Hopkins University. The mouse monoclonal antibody (mAb),
./technical/biomed/1471-2407-2-33.txt:          Hopkins Transgenic Core Facility. Human β-catenin exon 3
./technical/biomed/1475-2875-1-5.txt:          was a generous gift from N. Kumar (Johns Hopkins
./technical/biomed/1475-925X-2-1.txt:        • Prof. Piotr Franaszczuk, Johns Hopkins Medical
./technical/government/Env_Prot_Agen/tech_adden.txt:by investigators at Johns Hopkins University and others that have
./technical/government/Env_Prot_Agen/tech_adden.txt:Health. Johns Hopkins Univeristy Press, Baltimore.
./technical/government/Env_Prot_Agen/tech_adden.txt:Environmental Threats. Johns Hopkins School of Public Health,
./technical/government/Media/Legal_Aid_looks_to_legislators.txt:Green is in the process of closing its Hopkinsville office and
./technical/government/Media/Marylands_Legal_Aid.txt:several come to mind: the Terps, the Johns Hopkins University and
./technical/plos/journal.pbio.0020148.txt:        but another set of mutants has recently been isolated by Nancy Hopkins, Amgen Professor of
./technical/plos/journal.pbio.0020148.txt:        States). About ten years ago, Hopkins started to develop insertional mutagenesis in
./technical/plos/journal.pbio.0020148.txt:        screens. Hopkins has isolated 550 mutants in her screen, representing around 400 different
./technical/plos/journal.pbio.0020148.txt:        project are published in this issue of PLoS Biology. Hopkins's group is now collaborating
./technical/plos/journal.pbio.0020148.txt:        says Hopkins, noting that the days of small groups working in isolation are long gone. This
./technical/plos/journal.pbio.0020148.txt:        zebrafish researchers. ‘Fish really are just little people with fins’, says Hopkins. ‘Of
./technical/plos/journal.pbio.0020148.txt:        potential targets for therapeutic interventions. Hopkins provides the following
./technical/plos/journal.pbio.0020148.txt:        somewhere, but we had no idea what the other genes were’. Hopkins and Sun have since
./technical/plos/journal.pbio.0030032.txt:        Bioinformatics at Johns Hopkins. And while most PSM-style programs are currently in the US,
./technical/plos/pmed.0020210.txt:        Washington, Johns Hopkins University, Harvard University, and the University of Dundee. In
```

This code searched all documents under the technical that match "Hopkins"

## 2. “grep” can be use to only show lines that exactly match the search string by add "-x" behind the grep,

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:183$ grep -rx LICR ./technical
```

This code searched all documents under the technical that exatcly match the "LICR". Unfortunaly, there are none, so no output.

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:182$ grep -r -x "What If?" ./technical
./technical/911report/chapter-1.txt:What If?
```

This code searched all documents under the technical that exatcly match the "What If?". there is only one.

## 3. “grep” can be use to only show the name of the matched files by add "-l" behind the grep,

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:184$ grep -rl LICR ./technical
./technical/plos/journal.pbio.0020214.txt
```

This code searched all documents under the technical that  match the "LICR", but only shows the file's name. And there is only one matched file.

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:186$ grep -r -l Hopkins ./technical
./technical/biomed/1471-2091-3-4.txt
./technical/biomed/1471-2229-3-3.txt
./technical/biomed/1471-2261-3-5.txt
./technical/biomed/1471-2334-2-27.txt
./technical/biomed/1471-2407-2-33.txt
./technical/biomed/1475-2875-1-5.txt
./technical/biomed/1475-925X-2-1.txt
./technical/government/Env_Prot_Agen/tech_adden.txt
./technical/government/Media/Legal_Aid_looks_to_legislators.txt
./technical/government/Media/Marylands_Legal_Aid.txt
./technical/plos/journal.pbio.0020148.txt
./technical/plos/journal.pbio.0030032.txt
./technical/plos/pmed.0020210.txt
```
This code searched all documents under the technical that  match the "Hopkins", but only shows the file's name. And there are few matched files.

## 4. “grep” can be use to show the line number of the matched files by add "-n" behind the grep,

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:189$ grep -rn LICR ./technical
./technical/plos/journal.pbio.0020214.txt:166:        Cancer Research (LICR) based jointly in Zurich, New York, and London, and the Belozersky
./technical/plos/journal.pbio.0020214.txt:169:        moving toward integration of a research program in Moscow with other LICR projects, and
./technical/plos/journal.pbio.0020214.txt:170:        real collaboration between Moscow groups and LICR labs elsewhere.
./technical/plos/journal.pbio.0020214.txt:174:        University [Moscow, Russia] cycle on oncology and immunology sponsored by LICR;
```

This code searched all documents under the technical that  match the "LICR", and shows the files include the match string with the line number of the match string of each result and files. There are only one file matches the string but there are few results in that files. we can see the line number of each result after ':'.

```
[cs15lsp23bo@ieng6-202]:stringsearch-data:190$ grep -r -n Hopkins ./technical
./technical/biomed/1471-2091-3-4.txt:873:          Chemistry at Johns Hopkins University. After confirmation
./technical/biomed/1471-2229-3-3.txt:129:        Compared to the previous report of Hopkins et al. on
./technical/biomed/1471-2261-3-5.txt:481:        Dr. Hopkins and Dr. Polukoff have been retained as
./technical/biomed/1471-2334-2-27.txt:85:          Hopkins University. The mouse monoclonal antibody (mAb),
./technical/biomed/1471-2407-2-33.txt:140:          Hopkins Transgenic Core Facility. Human β-catenin exon 3
./technical/biomed/1475-2875-1-5.txt:451:          was a generous gift from N. Kumar (Johns Hopkins
./technical/biomed/1475-925X-2-1.txt:441:        • Prof. Piotr Franaszczuk, Johns Hopkins Medical
./technical/government/Env_Prot_Agen/tech_adden.txt:1053:by investigators at Johns Hopkins University and others that have
./technical/government/Env_Prot_Agen/tech_adden.txt:3049:Health. Johns Hopkins Univeristy Press, Baltimore.
./technical/government/Env_Prot_Agen/tech_adden.txt:3091:Environmental Threats. Johns Hopkins School of Public Health,
./technical/government/Media/Legal_Aid_looks_to_legislators.txt:39:Green is in the process of closing its Hopkinsville office and
./technical/government/Media/Marylands_Legal_Aid.txt:8:several come to mind: the Terps, the Johns Hopkins University and
./technical/plos/journal.pbio.0020148.txt:59:        but another set of mutants has recently been isolated by Nancy Hopkins, Amgen Professor of
./technical/plos/journal.pbio.0020148.txt:61:        States). About ten years ago, Hopkins started to develop insertional mutagenesis in
./technical/plos/journal.pbio.0020148.txt:66:        screens. Hopkins has isolated 550 mutants in her screen, representing around 400 different
./technical/plos/journal.pbio.0020148.txt:68:        project are published in this issue of PLoS Biology. Hopkins's group is now collaborating
./technical/plos/journal.pbio.0020148.txt:149:        says Hopkins, noting that the days of small groups working in isolation are long gone. This
./technical/plos/journal.pbio.0020148.txt:154:        zebrafish researchers. ‘Fish really are just little people with fins’, says Hopkins. ‘Of
./technical/plos/journal.pbio.0020148.txt:158:        potential targets for therapeutic interventions. Hopkins provides the following
./technical/plos/journal.pbio.0020148.txt:164:        somewhere, but we had no idea what the other genes were’. Hopkins and Sun have since
./technical/plos/journal.pbio.0030032.txt:53:        Bioinformatics at Johns Hopkins. And while most PSM-style programs are currently in the US,
./technical/plos/pmed.0020210.txt:121:        Washington, Johns Hopkins University, Harvard University, and the University of Dundee. In
```

This code searched all documents under the technical that  match the "Hopkins", and shows the files include the match string with the line number of the match string of each result of their files.

I find all of my option/mode from this article: [How To Use grep Command In Linux/UNIX](https://phoenixnap.com/kb/grep-command-linux-unix-examples) This is a great website with lots of useful information!!
 
