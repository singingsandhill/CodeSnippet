### NBSP 일반 공백으로 치환
```
docker exec -i ksox-ai-be-local python - <<'PY'
from pathlib import Path
root = Path("/app")
cnt_files = 0
cnt_repl = 0

for p in root.rglob("*.py"):
    b = p.read_bytes()
    if b"\xc2\xa0" in b:
        text = b.decode("utf-8", errors="surrogateescape")
        n = text.count("\u00a0")
        text = text.replace("\u00a0", " ")
        p.write_text(text, encoding="utf-8")
        cnt_files += 1
        cnt_repl += n

print("fixed files:", cnt_files, "total replacements:", cnt_repl)
PY

```
