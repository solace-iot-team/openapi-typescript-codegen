# Body vs. Headers and Body style

**Flag:**  `--exposeHeadersAndBody`

By default, the OpenAPI generator creates service functions that return the response body (or a single response header).

```typescript
public static createUser(
    requestBody?: User,
): CancelablePromise<User> {
    // ...
}
```

Alternatively, use the flag `--exposeHeadersAndBody` to generate service functions that return the response headers and
the response body. 

```typescript
public static createUser(
    requestBody?: User,
): CancelablePromise<{ headers: Record<string, string>; body: User; }> {
    // ...
}
```
