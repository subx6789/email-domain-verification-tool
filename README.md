# Domain Email Verification Tool

This is a Go-based tool to check for essential email-related DNS records for a given domain. The tool verifies the presence of the following:

- **MX records:** Used for mail delivery.
- **SPF (Sender Policy Framework) record:** A TXT record that defines which mail servers are allowed to send emails on behalf of the domain.
- **DMARC (Domain-based Message Authentication, Reporting & Conformance) record:** A TXT record used for email authentication and policy enforcement.

## Features

- **Check for MX records:** Verifies if a domain has MX (Mail Exchange) records.
- **Check for SPF records:** Scans TXT records to identify if the domain has a valid SPF policy.
- **Check for DMARC records:** Scans for the DMARC record in the \_dmarc subdomain.

## Installation

Install Go on your machine if it is not already installed. You can download it [here](https://go.dev/).

### Clone this repository:

```bash
 git clone https://github.com/subx6789/email-domain-verification-tool.git
 cd email-domain-verification-tool
```

### Build the program:

```bash
 go build -o app
```

### Usage:

- Run the program:

  ```bash
   ./app
  ```

- Enter the domain names you want to check, one per line:

  ```bash
   gmail.com
  ```

- exit

Type exit to terminate the program.

## Error Handling

The program logs errors if there are issues fetching DNS records, but it continues running. For example, if a DMARC record is not found, the program will log the error but proceed with the next domain.

## License

This project is licensed under the MIT License - see the [LICENSE](./LICENSE) file for details.
