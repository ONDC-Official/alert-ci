# alert-ci

Reusable Google Chat notification action for CI/CD workflows across `ONDC-Official` repositories.

## Usage

Add this step at the end of any job in `.github/workflows/*.yml`:

```yaml
- name: Notify Google Chat
  if: always()
  uses: ONDC-Official/alert-ci@main
  with:
    gchat_webhook: ${{ secrets.GCHAT_WEBHOOK_URL }}
    job_status: ${{ job.status }}
```
