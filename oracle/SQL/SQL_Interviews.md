# 1. What is the difference between `VARCHAR` and `VARCHAR2` data types?

## Current Behavior

- In modern Oracle versions, `VARCHAR` and `VARCHAR2` are effectively the same internally when used in table columns.
- Oracle recommends using `VARCHAR2` because `VARCHAR` is reserved for potential future changes (e.g., distinguishing between empty strings and `NULL`).

## Storage Limits

- **`VARCHAR2`:**
  - Can store up to 4000 bytes by default.
  - Can store up to 32767 bytes if `max_string_size` is set to `extended`.
- **`VARCHAR` (when used as an external type in Oracle Call Interface, OCI):**
  - Has a maximum size of up to 65533 bytes (including length bytes).

## Space Usage for NULL

- Neither `VARCHAR` nor `VARCHAR2` consumes storage space for a `NULL` value in a column.

## Recommendation

- Always use `VARCHAR2` in Oracle databases to ensure consistent and supported behavior.

---

# 2. What is the `RAW` datatype?

- **Purpose:**  
  `RAW` is a datatype for storing variable-length binary data (data not interpreted by Oracle).

- **Usage:**  
  Commonly used for data that must remain unaltered, such as encrypted values or other binary formats.

- **Size Limit:**
  - **Default (`max_string_size = STANDARD`):** Up to 2000 bytes.
  - **Extended (`max_string_size = EXTENDED`):** Up to 32767 bytes.
