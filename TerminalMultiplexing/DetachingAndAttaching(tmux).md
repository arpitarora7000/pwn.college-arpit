# Detaching And Attaching (tmux)
### Key points
1. `tmux` (terminal multiplexer) is screen's younger, more modern cousin. It does all the same things but with some different key bindings. The biggest difference? Instead of Ctrl-A, tmux uses Ctrl-B as its command prefix.
2. `ctrl-b` instead of `a`, commands also differ, `tmux ls` - List sessions, `tmux attach` or `tmux a` - Reattach to session.

 <img width="502" height="205" alt="Screenshot 2025-10-10 at 11 29 43 PM" src="https://github.com/user-attachments/assets/ea17e935-d721-4be1-be5d-f83558bdfad7" />

## My solve
**Flag :** `pwn.college{wp70PEKCIrBtHca-rBLRYWpuVAw.0VO4IDOxwCOwIzNzEzW}`

Just launched tmux, detached from it then reattached to it, to find the flag.

<img width="631" height="124" alt="Screenshot 2025-10-10 at 11 31 11 PM" src="https://github.com/user-attachments/assets/45689304-52ae-458a-8103-3bfde91e8640" />

<img width="624" height="295" alt="Screenshot 2025-10-10 at 11 31 25 PM" src="https://github.com/user-attachments/assets/0d901900-407e-40ec-a771-2467b2ba75be" />

## What I Learned
- Learned about the new thing `tmux`, which is quiet similar to a screen has different command prefix and also commands differ, which is all written above.

### Referencs
None.
