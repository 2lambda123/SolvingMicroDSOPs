# Make SolvingMicroDSOPs lecturenotes and cctwMoM paper

Most of the body of the existing cctwMoM paper comes word-for-word from the MoM section in the SolvingMicroDSOPs repo.
So editing of the paper should proceed mostly via editing SolvingMicroDSOPs.tex, which (when run), exports the relevant bits.  You can then run cctwMoM

SolvingMicroDSOPs.tex is a pretty messy document, with various true-false switches to generate various versions of the lecture notes.
I've disabled most of those switches by preceding them with ``%%%`` comment markers, but of course have left the switches that generate
content for cctwMoM intact (the relevant excerpts get put into the cctwMoM directory.

At the endpoint of this project, we will have achieved a divorce between the two projects; cctwMoM will be a standalone object thing.

But the first phase will be to make any desired edits that ought to be made anyway in SolvingMicroDSOPs; once we are satisfied with the revised MoM material in SolvingMicroDSOPs, that will be the time to have the amicable separation of the documents.  In particular, we will not divorce the two projects until all figures for the MoM part of the SolvingMicroDSOPs are generated by code in Econ-ARK.

Other notes:

1. A script to run the Mathematica code is `makeMath.sh`
   * I've just tested it on my Mac and it still works (!)
   * This script generates the figures in the ./Figures directory
   * There is a long document, `SolvingMicroDSOPs_Readme.tex` that explains the notation and operation of the Mathematica code
2. A contribution of this kind to [Econ-ARK](http://Econ-ARK.org) requires:
   * An eponymous replication python file: SolvingMicroDSOPs.py
      * It should do basically the what `makeMath.sh` does now
   * An eponymous [Jupyter Notebook](https://en.wikipedia.org/wiki/Project_Jupyter#Jupyter_Notebook) like the ones in [econ-ark.org/Notebooks](https://econ-ark.org/Notebooks) that interactively demonstrates some things that can be done "Live"
2. Whatever standalone tools can be built that make it easier to use the MoM to solve existing
3. If you need to add bibliographical entries, do NOT edit the SolvingMicroDSOPs.bib or cctwMoM.bib files because they are automatically generated and will be wiped out the next time I compile the document and push it.  Instead, edit the SolvingMicroDSOPs-Add.bib or cctwMoM-Add.bib files, and the next time I compile, I will add your new references (or updates to outdated references) to my master database of references, and then will regenerate the bib files in the repo.
# SolvingMicroDSOPs
