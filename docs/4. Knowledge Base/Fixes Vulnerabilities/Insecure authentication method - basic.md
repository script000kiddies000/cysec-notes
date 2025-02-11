
## Description

The server uses Basic authentication over an insecure channel.  

## Impact

Gather base 64 coded credentials.

## Recommendation

Use stronger authentication mechanisms like Bearer and OAuth.  

## Threat

Unauthorized attacker from adjacent network performing a Sniffing attack.

## Score

Default score using [CVSS 3.1](https://www.first.org/cvss/calculator/3.1). It may change depending on the context of the src.

### Base

- Attack vector: **A**
- Attack complexity: **L**
- Privileges required: **N**
- User interaction: **N**
- Scope: **U**
- Confidentiality: **L**
- Integrity: **N**
- Availability: **N**

### Result

- Vector string: **CVSS:3.1/AV:A/AC:L/PR:N/UI:N/S:U/C:L/I:N/A:N/E:P/RL:O/RC:C**
-  Score:
	- Base: **4.3**
	- Temporal: **3.9**
- Severity:
	- Base: **Medium**

## Requirements

- [030.Avoid object reutilization](https://help.fluidattacks.com/portal/en/kb/articles/criteria-requirements-030)
- [228.Authenticate using standard protocols](https://help.fluidattacks.com/portal/en/kb/articles/criteria-requirements-228)
- [319.Make authentication options equally secure](https://help.fluidattacks.com/portal/en/kb/articles/criteria-requirements-319)

## Fixes

- [Swift](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-swift-015)
- [Java](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-java-015)
- [Elixir](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-elixir-015)
- [C-Sharp](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-csharp-015)
- [Go](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-go-015)
- [Ruby](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-ruby-015)
- [PHP](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-php-015)
- [Scala](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-scala-015)
- [Python](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-python-015)
- [TypeScript](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-typescript-015)
- [Azure](https://help.fluidattacks.com/portal/en/kb/articles/criteria-fixes-azure-015)