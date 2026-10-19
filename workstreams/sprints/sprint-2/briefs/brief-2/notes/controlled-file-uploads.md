# 📦 Multer Upload — Quick Review

> 🟡 **In progress** — implementation evidence is saved; runtime checks and Mehdi's explanation are still pending.

> 🧠 **Big idea:** Multer converts one multipart file into `req.file`; the controller then applies the LMS rules and creates the MongoDB resource record.

## 🔑 Five points

1. The client sends `multipart/form-data`, not JSON.
2. The field name must match `upload.single("file")`.
3. Multer limits declared types and size, generates a safe stored filename, and writes the file.
4. The controller connects the stored file to the module through a `Resource` document.
5. Failed controller work removes the stored file so it does not become an orphan.

## 📖 Eloquent JavaScript foundation

- **Chapter 18, printed pp. 317–319:** method, path, headers, and request body explain what Postman sends.
- **Chapter 20, printed pp. 361–363:** Node.js provides asynchronous network and filesystem I/O through modules.
- Multer and Mongoose are project libraries, not book topics.

## 🧩 MERN connection

- **Express/Node.js:** parse and store the incoming file.
- **MongoDB:** store its metadata and module relationship.
- **React/Postman:** construct the multipart request.

## ⚠️ Common trap

`req.file` is not automatic Express behavior. It exists only after the request passes through the matching Multer middleware.

## 🌐 Web culture

Developers separate binary storage from database metadata and treat file type, ownership, cleanup, and public access as separate security decisions.

## 🔗 Full lesson

Open [Controlled File Uploads with Multer](../concepts/controlled-file-uploads/) for the complete flow and evidence table.

> ✅ **Remember:** the file and its database record are two connected pieces that must stay consistent.
