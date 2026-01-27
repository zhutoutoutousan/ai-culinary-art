# Compilation Notes for Trilingual Book

## Compilation Method

This book is designed to be compiled with **XeLaTeX** to support Chinese, English, and German languages.

### Recommended Compilation Command

```bash
xelatex main.tex
xelatex main.tex  # Run twice for proper cross-references
```

### Alternative: pdfLaTeX (Limited Chinese Support)

If XeLaTeX is not available, you can use pdfLaTeX with CJKutf8 package, but Chinese rendering may be limited:

1. Comment out the XeLaTeX-specific packages in main.tex
2. Uncomment the pdfLaTeX fallback section
3. Compile with: `pdflatex main.tex`

## Font Requirements

### Chinese Fonts

The document uses the following Chinese fonts (adjust in main.tex based on your system):

**Windows:**
- SimSun (宋体) - Main font
- SimHei (黑体) - Sans serif
- FangSong (仿宋) - Monospace

**Linux:**
- Noto Sans CJK
- Source Han Sans

**Mac:**
- STSong
- STHeiti
- PingFang SC

### German Fonts

Standard LaTeX fonts work fine for German. For better typography, consider:
- Latin Modern
- Computer Modern
- Times New Roman

## Language Structure

The book uses a trilingual format where:
- Chapter titles include all three languages
- Section headings include all three languages  
- Content is presented in parallel format: English | Chinese | German

## Notes

- Ensure all three languages are properly installed on your system
- Chinese fonts must be available for proper rendering
- Some LaTeX editors may require special configuration for XeLaTeX
- The document uses UTF-8 encoding throughout
