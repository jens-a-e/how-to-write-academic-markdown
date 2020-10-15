# How to write academic things with Markdown

In this repository I document my attempt to use plain text Markdown files for my academic writing.

This is a **work in progress** as I have not yet found a setup which works to my liking.

The aim is to write a whole PhD thesis in design research with it.

Currently I followed the instructions in this tutorial: https://www.youtube.com/watch?v=J86Pm62XM_Q
It assumes the use of VSCodium (or VSCode) as the editor, however. It is good to see how to install pandoc toolchain and how the text looks like.

More topics to cover in this README:

- why is this good?
- what tools do I need?
- What do I need to install?
  - pandoc
  - TODO: list all the other things; it is more than one thing
  - VSCodium as an editor allows you to install an extension which helps to preview and stictch together the Markdown files

## Things I want to try out

- Check out further automation
-- How to use this package https://www.npmjs.com/package/@shd101wyy/mume which powers the VSCode extension in a build task with e.g. npm

## Configuring how the Word document looks

To influence the style of the Word document a reference file must be created. This can be done by running this command in the project directory:

```
pandoc --print-default-data-file reference.docx > custom-reference.docx
```

It will copy a docx file into the porject folder which you can edit to your liking. For example make sure the style 'Abstract' has a page break before it. **It is important to note that only the style definitions in the document, the margins, and some other template related settings are used!** Inserting a page break before the word 'Abstract' in the document does not have the desired effect.

## Notes on doing things just with pandoc on the commandline

### Compiling a .docx file

Given your main Markdown file is `index.md`:

```
pandoc -F pandoc-crossref -F pandoc-citeproc index.md -o test.docx --reference-doc=custom-reference.docx --toc
```

or 

```
pandoc index.md --from=markdown-raw_tex+tex_math_single_backslash --katex --filter pandoc-crossref --filter pandoc-citeproc -o test.docx --toc --reference-doc=custom-reference.docx
```