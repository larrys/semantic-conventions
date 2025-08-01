
# z/OS software

This document defines z/OS software entity and documents how to populate other entities, such as `host` in the context of mainframes.

<!-- semconv entity.zos.software -->
<!-- NOTE: THIS TEXT IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/snippet.md.j2 -->
<!-- prettier-ignore-start -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->


**Status:** ![Development](https://img.shields.io/badge/-development-blue)

**type:** `zos.software`

**Description:** A software resource running on a z/OS system.
| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`zos.smf.id`](/docs/registry/attributes/zos.md) | string | The System Management Facility (SMF) Identifier uniquely identified a z/OS system within a SYSPLEX or mainframe environment and is used for system and performance analysis. | `SYS1` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`zos.sysplex.name`](/docs/registry/attributes/zos.md) | string | The name of the SYSPLEX to which the z/OS system belongs too. | `SYSPLEX1` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`mainframe.lpar.name`](/docs/registry/attributes/mainframe.md) | string | Name of the logical partition that hosts a systems with a mainframe operating system. | `LPAR01` | `Recommended` | ![Development](https://img.shields.io/badge/-development-blue) |

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->

## Host

The following table describes how to populate attributes on the `host` entity on mainframes.

<!-- semconv host.zos -->
<!-- NOTE: THIS TEXT IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/snippet.md.j2 -->
<!-- prettier-ignore-start -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->

| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`host.arch`](/docs/registry/attributes/host.md) | string | The CPU architecture the host system is running on. | `s390x` | `Recommended` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`host.name`](/docs/registry/attributes/host.md) | string | Name of the host. On z/OS, SHOULD be the full qualified hostname used to register the z/OS system in DNS. | `SYS1.DOMAIN.COM` | `Recommended` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`host.id`](/docs/registry/attributes/host.md) | string | Unique host ID. On z/OS, SHOULD be the concatenation of sysplex name and SMFID, separated by a dash | `SYSPLEX1-SYS1` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |

---

`host.arch` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `amd64` | AMD64 | ![Development](https://img.shields.io/badge/-development-blue) |
| `arm32` | ARM32 | ![Development](https://img.shields.io/badge/-development-blue) |
| `arm64` | ARM64 | ![Development](https://img.shields.io/badge/-development-blue) |
| `ia64` | Itanium | ![Development](https://img.shields.io/badge/-development-blue) |
| `ppc32` | 32-bit PowerPC | ![Development](https://img.shields.io/badge/-development-blue) |
| `ppc64` | 64-bit PowerPC | ![Development](https://img.shields.io/badge/-development-blue) |
| `s390x` | IBM z/Architecture | ![Development](https://img.shields.io/badge/-development-blue) |
| `x86` | 32-bit x86 | ![Development](https://img.shields.io/badge/-development-blue) |

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->

## Operating System

The following table describes how to populate the operating system attributes on mainframes.
<!-- semconv os.zos -->
<!-- NOTE: THIS TEXT IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/snippet.md.j2 -->
<!-- prettier-ignore-start -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->

| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`os.type`](/docs/registry/attributes/os.md) | string | The operating system type. | `zos` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`os.version`](/docs/registry/attributes/os.md) | string | The version string of the operating system. On z/OS, SHOULD be the release returned by the command `d iplinfo`. | `3.1.0` | `Recommended` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`os.description`](/docs/registry/attributes/os.md) | string | Human readable OS version information, e.g., as reported by command `d iplinfo`. | `IBM z/OS 3.1` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`os.name`](/docs/registry/attributes/os.md) | string | Human readable operating system name. | `z/OS` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |

---

`os.type` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `aix` | AIX (Advanced Interactive eXecutive) | ![Development](https://img.shields.io/badge/-development-blue) |
| `darwin` | Apple Darwin | ![Development](https://img.shields.io/badge/-development-blue) |
| `dragonflybsd` | DragonFly BSD | ![Development](https://img.shields.io/badge/-development-blue) |
| `freebsd` | FreeBSD | ![Development](https://img.shields.io/badge/-development-blue) |
| `hpux` | HP-UX (Hewlett Packard Unix) | ![Development](https://img.shields.io/badge/-development-blue) |
| `linux` | Linux | ![Development](https://img.shields.io/badge/-development-blue) |
| `netbsd` | NetBSD | ![Development](https://img.shields.io/badge/-development-blue) |
| `openbsd` | OpenBSD | ![Development](https://img.shields.io/badge/-development-blue) |
| `solaris` | SunOS, Oracle Solaris | ![Development](https://img.shields.io/badge/-development-blue) |
| `windows` | Microsoft Windows | ![Development](https://img.shields.io/badge/-development-blue) |
| `zos` | IBM z/OS | ![Development](https://img.shields.io/badge/-development-blue) |

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->

## Process

The following table describes how to populate attributes on the `process` entity on mainframes.
<!-- semconv process.zos -->
<!-- NOTE: THIS TEXT IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/snippet.md.j2 -->
<!-- prettier-ignore-start -->
<!-- markdownlint-capture -->
<!-- markdownlint-disable -->

| Attribute  | Type | Description  | Examples  | [Requirement Level](https://opentelemetry.io/docs/specs/semconv/general/attribute-requirement-level/) | Stability |
|---|---|---|---|---|---|
| [`process.command`](/docs/registry/attributes/process.md) | string | The command used to launch the process (i.e. the command name). On z/OS, SHOULD be set to the name of the job used to start the z/OS system software. | `CICSSTRT` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`process.pid`](/docs/registry/attributes/process.md) | int | Process identifier (PID). [1] | `008A` | `Required` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`process.owner`](/docs/registry/attributes/process.md) | string | The username of the user that owns the process. [2] | `CICSUSR` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`process.runtime.description`](/docs/registry/attributes/process.md) | string | An additional description about the runtime of the process, for example a specific vendor customization of the runtime environment. | `IBM Customer Information Control System (CICS) Transaction Server for z/OS Version 5.6` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`process.runtime.name`](/docs/registry/attributes/process.md) | string | The name of the runtime of this process. | `CICS Transaction Server z/OS Version 5.6` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |
| [`process.runtime.version`](/docs/registry/attributes/process.md) | string | The version of the runtime of this process, as returned by the runtime without modification. | `5.6` | `Opt-In` | ![Development](https://img.shields.io/badge/-development-blue) |

**[1] `process.pid`:** On z/OS, SHOULD be set to the Address Space Identifier.

**[2] `process.owner`:** On z/OS, SHOULD be set to the user under which the z/OS system software is executed.

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->

<!-- markdownlint-restore -->
<!-- prettier-ignore-end -->
<!-- END AUTOGENERATED TEXT -->
<!-- endsemconv -->
