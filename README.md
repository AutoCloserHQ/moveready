# MoveReady deployment

MoveReady is a self-contained 12-question moving-readiness assessment.

## Files to upload

Create a new public GitHub repository named `moveready` under the `AutoCloserHQ` account and add these files to the repository root:

- `index.html`
- `CNAME`

The `README.md` file is optional and is only an instruction sheet.

## Turn on GitHub Pages

1. Open the new repository's **Settings**.
2. Select **Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Select the `main` branch and the `/ (root)` folder.
5. Click **Save**.
6. In **Custom domain**, enter `moveready.modelmoving.com` and save.
7. When GitHub finishes the certificate, enable **Enforce HTTPS**.

## DNS

In GoDaddy, the expected DNS record is:

- Type: `CNAME`
- Name: `moveready`
- Value: `autocloserhq.github.io`
- TTL: default

Do not change the existing `routes` record.

## Links

Default ModelMoving link:

`https://moveready.modelmoving.com`

Route-aware link:

`https://moveready.modelmoving.com/?route=New%20Jersey%20to%20Florida`

The page can also be linked from another moving website with optional URL parameters:

- `company`: displayed company name
- `home`: website URL used by the back link
- `quote`: quote-form URL used by the result button
- `route`: route displayed on the result
- `logo`: absolute HTTPS logo URL
- `primary`: six-digit hex primary color, including `#`
- `accent`: six-digit hex accent color, including `#`

Encode parameter values when building a link. Example:

`https://moveready.modelmoving.com/?company=A%20Plus%20Moving&home=https%3A%2F%2Fexample.com&quote=https%3A%2F%2Fexample.com%2Fquote&route=Hawaii%20to%20California`

The assessment does not collect or transmit answers. The quote button sends only the readiness score, route (when provided), and `source=moveready` to the configured quote URL.
