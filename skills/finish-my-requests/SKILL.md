---
name: finish-my-requests
description: Use this when a client wants to get through everything their accounting firm has asked of them, such as "help me finish my tax stuff" or "what do I still owe my accountant".
---

# Finish what the firm asked for

Work through the client's open items one at a time, soonest due first.

1. Call `pocketfirm_client_home` (or `pocketfirm_list_my_work`) and tell the client, in a short
   list, what is open and when each is due.
2. Ask which one to start with. For each item:
   - **Form or questionnaire**: open it, ask the questions in plain words a few at a time, save a
     draft as you go, then show all answers and submit only when the client says go ahead. A file
     question takes `pocketfirm_upload_file` with the form's `assignmentId`; put the returned
     `uploadId` in that question's answer.
   - **Document request**: read what the firm needs. Ask the client to attach the file or give a
     link, confirm which request it is for, then upload it with `pocketfirm_upload_file`. If the
     client does not have it, offer `pocketfirm_mark_document_request_not_applicable` with a short
     note they approve.
   - **Signature or proposal**: give the PocketFirm link; the client signs or accepts there.
   - **Invoice**: give the PocketFirm link; the client pays there.
   - **Message waiting**: read the thread and help the client reply.
3. After each item, say what was done and what is next. Finish with what is still open.

Never guess an answer the client did not give. When a question is unclear, suggest messaging the
firm instead.
