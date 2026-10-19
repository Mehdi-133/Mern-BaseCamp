# 🧪 Controlled Upload Check

> ⬜ **Not started** — answer from your understanding before reopening the implementation.

Estimated effort: **5–10 minutes**.

## Questions

1. What happens if Postman sends the file with the field name `document` while the route uses `upload.single("file")`?
2. Why do we store the file on disk but store `module`, `url`, `originalName`, `size`, and `order` in MongoDB?
3. Which upload protections are merged on `main`, and which protections are still visible only in commit `883aa0e` on the feature branch?

## ✅ Completion check

The exercise is complete when Mehdi explains the complete path from multipart request to `req.file` to the `Resource` document, and clearly separates merged behavior from branch-only hardening.

Do not mark runtime behavior verified until one accepted upload and the important rejected cases are actually run.
