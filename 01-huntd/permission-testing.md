# Permission Testing — Huntd

Matriz de permissões por módulo e tipo de usuário (deslogado, candidato, recrutador), usada para derivar os casos de teste de acesso.

| # | Module | Logged-out User | Candidate | Recruiter |
|---|---|---|---|---|
| 001 | Main Page | Allowed | Allowed | Allowed |
| 002 | For Companies | Allowed | Allowed | Allowed |
| 003 | For Engineers | Allowed | Allowed | Allowed |
| 004 | Authentication / Registration | Allowed | Allowed | Allowed |
| 005 | Candidates | Restricted | Allowed | Allowed |
| 006 | Candidate Profile | Restricted | Allowed | Allowed |
| 007 | Recruiter Profile | Restricted | Restricted | Allowed |
| 008 | Jobs | Restricted | Allowed | Allowed |
| 009 | Chats / Messages | Restricted | Allowed | Allowed |
| 010 | Bonus | Restricted | Restricted | Allowed |
| 011 | Footer | Allowed | Allowed | Allowed |
