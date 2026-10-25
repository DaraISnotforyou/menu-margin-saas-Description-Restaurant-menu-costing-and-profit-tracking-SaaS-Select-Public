# Launch checklist

- [ ] Create hosted PostgreSQL database and run `db/schema.sql`.
- [ ] Deploy Node app and set `DATABASE_URL`, `JWT_SECRET`, `PGSSL`, `NODE_ENV` as host secrets.
- [ ] Confirm `/api/health` returns `{"ok":true}`.
- [ ] Test registration, duplicate-email handling, login, logout and account deletion.
- [ ] Test ingredient create/update/history/delete and recipe create/update/delete.
- [ ] Verify two accounts cannot see each other's data.
- [ ] Verify HTTPS, error handling, backup/restore and service monitoring.
- [ ] Add email verification and password reset.
- [ ] Complete privacy notice, terms, support contact, refund/cancellation policy.
- [ ] Configure payment provider plans and server-verified webhooks before advertising paid subscriptions.
- [ ] Add server-side paid-plan entitlements and test renewals, failed payments, cancellations and refunds.
- [ ] Test the app on multiple Android devices and slow networks.


## Billing connection checklist
- [ ] Create monthly and annual recurring plans in Paystack dashboard and confirm supported currency/prices for the merchant account.
- [ ] Set `PAYSTACK_SECRET_KEY`, `PAYSTACK_PLAN_MONTHLY_CODE`, `PAYSTACK_PLAN_YEARLY_CODE`, and `APP_URL` in server host secrets.
- [ ] Register `https://YOUR-APP-URL/api/paystack/webhook` in Paystack.
- [ ] Apply updated `db/schema.sql` so `billing_payments` exists.
- [ ] Test monthly and yearly checkout in test mode.
- [ ] Verify successful, failed, duplicate, renewal and cancellation webhooks.
- [ ] Complete subscription entitlements, refunds, invoice emails and cancellation UI before public paid launch.
