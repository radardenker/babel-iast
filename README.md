# babel-iast
mapping for Sanskrit romanized in accordance with [IAST](https://en.wikipedia.org/wiki/International_Alphabet_of_Sanskrit_Transliteration) to Unicode-Devanagari

## Dependencies
babel>=3.44

## Usage
1. Include `\usepackage{babel-iast}` in the preamble of your LaTeX-file after loading babel,
2. specify a font for the `iast` language, for instance `\babelfont[iast]{rm}[Renderer=Harfbuzz]{DevanagariMT}`,
3. switch on the `iast` language in your document with `\selectlanguage{iast}` or `\begin{otherlanguage}{iast} … \end{otherlanguage}`.

## Special characters for encoding
- the hyphen character (-) can be used to separate words or morphems that should be written continuously in Devanagari, for instance `yoddhum-icchati`. Currently babel does not support [whitespace-replacement before hyphenation](https://github.com/latex3/babel/wiki/What's-new-in-babel-3.44#preliminary-code-for-babelprehyphenation), so this is rather a workaround that should at some point be replaced with a rule mapping the proper separation of words in the romanization to the usual separation of the Indian scripts.
