# DamnVUlnerableAnsible



## CHECKOV- Ansible Security Check Groups

### 1. Validation of Certificates

These checks ensure that certificate validation is not disabled when using different Ansible modules.

- **Module `uri`:**
  - `CKV_ANSIBLE_1` (Tasks involving `uri` and `ansible.builtin.uri`)
- **Module `get_url`:**
  - `CKV_ANSIBLE_2` (Tasks involving `get_url` and `ansible.builtin.get_url`)
- **Module `yum`:**
  - `CKV_ANSIBLE_3` (Tasks involving `yum` and `ansible.builtin.yum`)
  - `CKV_ANSIBLE_4` (SSL Validation for `yum`)
- **Module `dnf`:**
  - `CKV2_ANSIBLE_5` (SSL Validation for `dnf`)
  - `CKV2_ANSIBLE_6` (Certificate validation for `dnf`)

### 2. HTTPS Usage in URLs

These checks ensure that HTTPS URLs are used with certain modules.

- **Module `uri`:**
  - `CKV2_ANSIBLE_1`
- **Module `get_url`:**
  - `CKV2_ANSIBLE_2`

### 3. GPG Signature and Authenticity Control

These checks verify that package signatures are not disabled.

- **Module `yum`:**
  - `CKV_ANSIBLE_5` (Signature verification for `yum`)
- **Module `dnf`:**
  - `CKV2_ANSIBLE_4`

### 4. Insecure Parameters Usage

Checks related to the use of insecure parameters in modules.

- **Module `apt`:**
  - `CKV_ANSIBLE_6` (Avoid the `force` parameter)

### 5. Error Handling in Blocks (`block`)

Checks that ensure proper error handling in task blocks.

- `CKV2_ANSIBLE_3`
