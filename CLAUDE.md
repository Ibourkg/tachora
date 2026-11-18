# Istruzioni per Claude

## Lettura dei PDF: usa sempre MarkItDown

Per leggere **qualsiasi file PDF** (e in generale DOCX, PPTX, XLSX, ecc.) usa **sempre**
il server MCP `markitdown` configurato in `.mcp.json`, non il tool `Read` né altri estrattori.

- Tool: `mcp__markitdown__convert_to_markdown`
- Argomento: `uri` con un URI `file://` assoluto, ad esempio
  `file:///home/user/tachora/docs/manuale.pdf` (supporta anche `http:`, `https:` e `data:`).

Se il server MCP non è disponibile, usa la CLI come fallback:

```bash
uvx --from 'markitdown[pdf]' markitdown percorso/del/file.pdf
```
