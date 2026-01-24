# Compilation Guide / 编译指南 / Kompilierungsanleitung

## Requirements / 要求 / Anforderungen

This LaTeX document requires **XeLaTeX** to compile properly due to Chinese character support.

由于需要支持中文字符，此 LaTeX 文档需要使用 **XeLaTeX** 编译。

Dieses LaTeX-Dokument erfordert **XeLaTeX** zur Kompilierung aufgrund der chinesischen Zeichenunterstützung.

## Compilation Command / 编译命令 / Kompilierungsbefehl

### Using XeLaTeX / 使用 XeLaTeX / Mit XeLaTeX

```bash
xelatex potsdam_fusion_egg_recipe.tex
```

You may need to run it twice for proper cross-references:

```bash
xelatex potsdam_fusion_egg_recipe.tex
xelatex potsdam_fusion_egg_recipe.tex
```

### Using Overleaf / 使用 Overleaf / Mit Overleaf

1. Upload the `.tex` file to Overleaf
2. Change the compiler to **XeLaTeX** in the menu (Menu → Compiler → XeLaTeX)
3. Click "Recompile"

### Required Packages / 所需包 / Erforderliche Pakete

- `tikz` - For diagrams
- `xeCJK` - For Chinese character support
- `babel` - For multilingual support
- `geometry` - For page layout
- `enumitem` - For itemized lists
- `xcolor` - For colors
- `fontspec` - For font management

### Font Note / 字体说明 / Schriftarten-Hinweis

The document will automatically use a suitable Chinese font from your system. If you want to specify a particular font, uncomment one of the font settings in the document (around line 15).

If you get font errors, you can:

1. **Let xeCJK auto-detect** (default - no action needed), or
2. **Specify a font** by uncommenting one of these lines in the `.tex` file:
   ```latex
   \setCJKmainfont{SimSun}              % Windows
   \setCJKmainfont{Microsoft YaHei}     % Windows
   \setCJKmainfont{STSong}               % Mac
   \setCJKmainfont{PingFang SC}          % Mac
   \setCJKmainfont{AR PL UMing CN}      % Linux
   \setCJKmainfont{Noto Sans CJK SC}    % Cross-platform
   ```

Common font names by system:
- **Windows**: `SimSun`, `Microsoft YaHei`, `KaiTi`
- **Mac**: `STSong`, `PingFang SC`, `STHeiti`
- **Linux**: Install Chinese fonts package (`fonts-noto-cjk` or `wqy-microhei`)

## Output / 输出 / Ausgabe

The compilation will produce:
- `potsdam_fusion_egg_recipe.pdf` - The final document

Die Kompilierung erzeugt:
- `potsdam_fusion_egg_recipe.pdf` - Das finale Dokument

编译将生成：
- `potsdam_fusion_egg_recipe.pdf` - 最终文档
