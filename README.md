# Infisical (CloudShift self-hosted)

Openship deploy config for [Infisical](https://github.com/Infisical/infisical) at
https://infisical.app.cloudshiftsolutions.in, running on the HP Mini Elite
(Openship project `infisical`).

- Image pinned to `infisical/infisical:v0.167.4`. To upgrade, change the tag, push, and redeploy in Openship.
- `ENCRYPTION_KEY` and `AUTH_SECRET` are set on the Openship service. **Losing `ENCRYPTION_KEY` makes every stored secret unreadable**; it is backed up outside Infisical.
- Public sign-up is disabled after the first admin is created.
- Backups: the `pg_data` volume holds everything; back it up together with `ENCRYPTION_KEY`.
