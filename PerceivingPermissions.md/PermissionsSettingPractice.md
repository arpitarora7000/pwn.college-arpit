# Permissions Setting Practice
### Key points
1. In addition to adding and removing permissions, as in the previous level, chmod can also simply set permissions altogether, overwriting the old ones. This is done by using = instead of - or +. For example:

<img width="458" height="178" alt="Screenshot 2025-10-10 at 1 44 51 AM" src="https://github.com/user-attachments/assets/85ea7393-9692-4e54-b47c-6a736800f7ac" />

2. But what if you want to change user permissions in a different way as group permissions? Say, you want to set rw for the owning user, but only r for the owning group? You can achieve this by chaining multiple modes to chmod with ,!

<img width="489" height="350" alt="Screenshot 2025-10-10 at 1 46 06 AM" src="https://github.com/user-attachments/assets/05f268b7-19fe-478f-8b6d-adb8df98f558" />

3. This challenge --> `This level extends the previous level by requesting more radical permission changes, which you will need = and ,-chaining to achieve. Good luck!`

## My solve
**Flag :** `pwn.college{UHiyVqeora4dFX2dCI4T1Ored2q.QXzETO0wCOwIzNzEzW}`

<img width="621" height="749" alt="Screenshot 2025-10-10 at 1 56 03 AM" src="https://github.com/user-attachments/assets/47191f94-3e8b-445a-8fee-4ca884f76384" />

<img width="619" height="704" alt="Screenshot 2025-10-10 at 1 57 03 AM" src="https://github.com/user-attachments/assets/699cef54-2c5e-42df-93b8-4c911c5a59c2" />

<img width="605" height="694" alt="Screenshot 2025-10-10 at 1 57 17 AM" src="https://github.com/user-attachments/assets/726948a8-e46f-4846-8a5e-494d876cfe03" />

<img width="623" height="733" alt="Screenshot 2025-10-10 at 1 57 31 AM" src="https://github.com/user-attachments/assets/1556b394-c33d-4131-b8fc-15e1218a6e6d" />

<img width="566" height="195" alt="Screenshot 2025-10-10 at 1 57 41 AM" src="https://github.com/user-attachments/assets/46045f58-2e8e-4b64-bb08-036c0b69cf90" />

## What I Learned
- Learned new ways to use `chmod`, by using the `=` character, assigning particular permissions to user/group/others, and separating them by `,`.

### References
No external references.
