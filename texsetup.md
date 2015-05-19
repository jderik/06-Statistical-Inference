##### Process for the tex setup

1. Installed MikTEX from  http://miktex.org/2.9/setup
2. Go to MikTEX setup from programs menu. Use admin setup.
3. Go to packages -> Format -> LaTeX -> LaTeX Contrib -> select fancyvrb package as this one not being selected  will cause 
KNITPDF to not work.
4. Apply
5. Under General clikc both -> Update **Formats** and then **Refresh FNDB** 


THis is based on multiple inputs read online. 
The following also should work from console.

*render("file.md", output_format="pdf_document")*   -- This is from console --
