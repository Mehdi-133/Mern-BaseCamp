# 📦 Controlled File Uploads with Multer

> 🟡 **In progress** — the Multer implementation is present and its first version is merged, but the upload flow has not been runtime-tested in this learning checkpoint and the understanding exercise is still open.

> 🧠 **Big idea:** Multer receives a `multipart/form-data` file, while the route and controller decide whether the user, file, module, and stored metadata are allowed.

## 🔄 How the upload works

![Workflow from authenticated trainer through upload validation and storage to a module-linked resource](../../brief-analysis/images/2026-10-14-upload-workflow.svg)

The picture shows the complete responsibility chain. The current LMS code follows this route:

1. Postman or a frontend sends `POST /api/modules/:id/resources/upload`.
2. The request uses `multipart/form-data` with a file field named `file` and a text field named `order`.
3. `authenticate` verifies the Bearer token.
4. `authorize(roles.TRAINER)` checks the general trainer role.
5. `upload.single("file")` asks Multer to receive exactly one file.
6. Multer checks the declared MIME type, rejects files larger than **5 MiB**, creates a UUID filename, and writes the file under `uploads/`.
7. The controller validates `order`, finds the module, and creates a MongoDB `Resource` containing the module ID, stored path, original name, size, type, and order.
8. If controller work fails after storage, `unlink()` removes the orphaned file.

## 🧱 Each layer has one job

| Layer | Responsibility |
| --- | --- |
| Express route | Defines the URL and middleware order |
| Authentication | Establishes the requester's identity |
| Authorization | Requires the trainer role |
| Multer middleware | Parses multipart data and creates `req.file` |
| Upload controller | Applies module, ownership, content, and metadata rules |
| Node.js filesystem | Stores the binary file and removes failed uploads |
| MongoDB `Resource` | Stores searchable metadata and the module relationship |

## 🛡️ Evidence from the LMS repository

| Evidence | Honest status |
| --- | --- |
| Basic Multer upload merged through commit `3aeba27` | ✅ Present on `main` |
| PDF, JPEG, and PNG declared MIME filter | ✅ Present on `main` |
| 5 MiB size limit and UUID stored filename | ✅ Present on `main` |
| Module-linked resource metadata and failure cleanup | ✅ Present on `main` |
| Course ownership and file-signature comparison | 🟡 Present in `883aa0e` on `feature/FAL-46-upload-module-file`; not confirmed on `main` |
| Upload-focused automated test | ⬜ Not found |
| Successful and rejected runtime requests | ⬜ Not rerun in this checkpoint |

## 📖 Eloquent JavaScript foundation

- **Chapter 18 — HTTP and Forms, printed pp. 317–319:** an HTTP request has a method, resource path, headers, and an optional body. A form packs its fields into the request body.
- **Chapter 20 — Node.js, printed pp. 361–363:** Node.js handles network and filesystem input/output asynchronously and organizes platform features through modules.
- **Boundary:** the book explains HTTP, Node.js I/O, and modules. It does not teach Multer, Mongoose, MIME sniffing, or Express middleware configuration.

## 🧩 MERN connection

- **MongoDB:** stores resource metadata and the reference to its module; the binary file is stored separately.
- **Express:** orders authentication, role authorization, Multer, and controller logic.
- **React or Postman:** sends multipart form data with the exact `file` field name.
- **Node.js:** writes, reads, and removes files through filesystem APIs.

## ⚠️ Common traps

- Sending JSON instead of `multipart/form-data` means Multer does not receive a file.
- Using a field name other than `file` does not match `upload.single("file")`.
- Trusting only `file.mimetype` trusts client-provided metadata. The branch hardening also compares the first file bytes with the declared type.
- A trainer role alone does not prove ownership of the module's course.
- Saving a file without saving its MongoDB metadata creates an orphan; saving metadata without a real file creates a broken resource.

## 🌐 Web culture

Production upload systems commonly use generated stored names, keep the original name only as metadata, limit size and type, authorize the target resource, and clean up partial failures. Signature checks reduce simple MIME spoofing, but they are not complete content validation or malware scanning.

## 🔗 Related learning

- [Short upload review note](../../notes/controlled-file-uploads.md)
- [Three-question understanding check](../../exercises/controlled-file-uploads.md)
- [14 October implementation-planning checkpoint](../../notes/2026-10-14-brief-checkpoint.md)

> ✅ **Remember:** Multer receives the file; your application still owns authentication, authorization, validation, metadata, and cleanup.
