# 🚨 Runbook: Incident Response

## Scope

Use this runbook for a broken public page, unexpected content change, exposed repository secret, compromised dependency, or suspected website compromise. It is not a substitute for the hosting provider's emergency procedures.

## 1. Triage

- Record the time, affected URL, symptoms, and first known occurrence.
- Identify whether the issue affects all visitors or a specific browser/device.
- Check recent commits, workflow runs, and hosting deployment records.
- Preserve relevant logs and evidence without collecting unnecessary visitor data.

## 2. Broken page or assets

1. Compare the deployed commit with the last known-good commit.
2. Check stylesheet, JavaScript, image, and font requests.
3. Confirm path casing and deployment base path.
4. Roll back if the issue materially affects visitors.
5. Verify the restored page before closing the incident.

## 3. Exposed secret

1. Treat the secret as compromised.
2. Revoke or rotate it at the issuing provider immediately.
3. Review audit logs for unauthorized use.
4. Remove the secret from active code and move it to an appropriate secret store.
5. Follow GitHub's guidance for sensitive data in repository history when needed.
6. Do not paste the secret into an issue or incident report.

Deleting a secret from the latest commit does not invalidate it and does not erase all copies from Git history.

## 4. Suspected malicious change

- Restrict or pause affected deployment workflows if safe and authorized.
- Review recent commits and dependency changes.
- Restore a known-good artifact.
- Rotate credentials that may have been exposed.
- Coordinate with repository and hosting owners.

## 5. Communication and closure

Communicate confirmed impact and mitigation without speculation. Record root cause, timeline, corrective actions, and follow-up owner. Avoid publishing exploit details while remediation is underway.
