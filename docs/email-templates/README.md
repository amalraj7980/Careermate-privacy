# CareerMate AI — Firebase Auth Email Templates

Paste these into **Firebase Console → Authentication → Templates**. Do not replace `%LINK%`.

## Files

| Template | File |
| --- | --- |
| Password reset | `password-reset.html` |
| Email verification | `verify-email.html` |

## Logo

Both emails use the live GitHub Pages asset (no Firebase Hosting required for the icon):

`https://amalraj7980.github.io/Careermate-privacy/favicon.png`

This reuses the existing `@Careermate-privacy/favicon.png`. Existing privacy / delete-account pages were not modified.

## Firebase Console steps

1. **Project settings → General → Public-facing name** = `CareerMate AI`  
   (removes `project-640629751815` from emails)
2. **Authentication → Templates → Password reset**
   - Subject: `Reset your CareerMate AI password`
   - From name: `CareerMate AI`
   - Body: paste contents of `password-reset.html`
3. **Authentication → Templates → Email address verification**
   - Subject: `Verify your CareerMate AI email`
   - From name: `CareerMate AI`
   - Body: paste contents of `verify-email.html`
4. Save and send a test email

## Important

- Keep `%LINK%` unchanged — Firebase injects the real action URL.
- Do not use `%APP_NAME%` in the body (hardcode **CareerMate AI** instead).
- Do not change app authentication / reset / verification code for this email UI.
- Post-reset Continue “Site Not Found” is handled by Firebase Hosting in the CareerMate AI app repo (`yarn deploy:hosting`), not by these templates.
