<!-- NOTE: THIS FILE IS AUTOGENERATED. DO NOT EDIT BY HAND. -->
<!-- see templates/registry/markdown/attribute_namespace.md.j2 -->

# Process

- [Process Attributes](#process-attributes)
- [Process Linux Attributes](#process-linux-attributes)
- [Deprecated Process Attributes](#deprecated-process-attributes)

## Process Attributes

An operating system process.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="process-args-count" href="#process-args-count">`process.args_count`</a> | int | Length of the process.command_args array [1] | `4` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-command" href="#process-command">`process.command`</a> | string | The command used to launch the process (i.e. the command name). On Linux based systems, can be set to the zeroth string in `proc/[pid]/cmdline`. On Windows, can be set to the first parameter extracted from `GetCommandLineW`. | `cmd/otelcol` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-command-args" href="#process-command-args">`process.command_args`</a> | string[] | All the command arguments (including the command/executable itself) as received by the process. On Linux-based systems (and some other Unixoid systems supporting procfs), can be set according to the list of null-delimited strings extracted from `proc/[pid]/cmdline`. For libc-based executables, this would be the full argv vector passed to `main`. SHOULD NOT be collected by default unless there is sanitization that excludes sensitive data. | `["cmd/otecol", "--config=config.yaml"]` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-command-line" href="#process-command-line">`process.command_line`</a> | string | The full command used to launch the process as a single string representing the full command. On Windows, can be set to the result of `GetCommandLineW`. Do not set this if you have to assemble it just for monitoring; use `process.command_args` instead. SHOULD NOT be collected by default unless there is sanitization that excludes sensitive data. | `C:\cmd\otecol --config="my directory\config.yaml"` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-context-switch-type" href="#process-context-switch-type">`process.context_switch_type`</a> | string | Specifies whether the context switches for this data point were voluntary or involuntary. | `voluntary`; `involuntary` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-creation-time" href="#process-creation-time">`process.creation.time`</a> | string | The date and time the process was created, in ISO 8601 format. | `2023-11-21T09:25:34.853Z` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-environment-variable" href="#process-environment-variable">`process.environment_variable.<key>`</a> | string | Process environment variables, `<key>` being the environment variable name, the value being the environment variable value. [2] | `ubuntu`; `/usr/local/bin:/usr/bin` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-executable-build-id-gnu" href="#process-executable-build-id-gnu">`process.executable.build_id.gnu`</a> | string | The GNU build ID as found in the `.note.gnu.build-id` ELF section (hex string). | `c89b11207f6479603b0d49bf291c092c2b719293` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-executable-build-id-go" href="#process-executable-build-id-go">`process.executable.build_id.go`</a> | string | The Go build ID as retrieved by `go tool buildid <go executable>`. | `foh3mEXu7BLZjsN9pOwG/kATcXlYVCDEFouRMQed_/WwRFB1hPo9LBkekthSPG/x8hMC8emW2cCjXD0_1aY` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-executable-build-id-htlhash" href="#process-executable-build-id-htlhash">`process.executable.build_id.htlhash`</a> | string | Profiling specific build ID for executables. See the OTel specification for Profiles for more information. | `600DCAFE4A110000F2BF38C493F5FB92` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-executable-name" href="#process-executable-name">`process.executable.name`</a> | string | The name of the process executable. On Linux based systems, this SHOULD be set to the base name of the target of `/proc/[pid]/exe`. On Windows, this SHOULD be set to the base name of `GetProcessImageFileNameW`. | `otelcol` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-executable-path" href="#process-executable-path">`process.executable.path`</a> | string | The full path to the process executable. On Linux based systems, can be set to the target of `proc/[pid]/exe`. On Windows, can be set to the result of `GetProcessImageFileNameW`. | `/usr/bin/cmd/otelcol` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-exit-code" href="#process-exit-code">`process.exit.code`</a> | int | The exit code of the process. | `127` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-exit-time" href="#process-exit-time">`process.exit.time`</a> | string | The date and time the process exited, in ISO 8601 format. | `2023-11-21T09:26:12.315Z` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-group-leader-pid" href="#process-group-leader-pid">`process.group_leader.pid`</a> | int | The PID of the process's group leader. This is also the process group ID (PGID) of the process. | `23` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-interactive" href="#process-interactive">`process.interactive`</a> | boolean | Whether the process is connected to an interactive shell. |  | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-owner" href="#process-owner">`process.owner`</a> | string | The username of the user that owns the process. | `root` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-paging-fault-type" href="#process-paging-fault-type">`process.paging.fault_type`</a> | string | The type of page fault for this data point. Type `major` is for major/hard page faults, and `minor` is for minor/soft page faults. | `major`; `minor` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-parent-pid" href="#process-parent-pid">`process.parent_pid`</a> | int | Parent Process identifier (PPID). | `111` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-pid" href="#process-pid">`process.pid`</a> | int | Process identifier (PID). | `1234` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-real-user-id" href="#process-real-user-id">`process.real_user.id`</a> | int | The real user ID (RUID) of the process. | `1000` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-real-user-name" href="#process-real-user-name">`process.real_user.name`</a> | string | The username of the real user of the process. | `operator` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-runtime-description" href="#process-runtime-description">`process.runtime.description`</a> | string | An additional description about the runtime of the process, for example a specific vendor customization of the runtime environment. | `Eclipse OpenJ9 Eclipse OpenJ9 VM openj9-0.21.0` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-runtime-name" href="#process-runtime-name">`process.runtime.name`</a> | string | The name of the runtime of this process. | `OpenJDK Runtime Environment` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-runtime-version" href="#process-runtime-version">`process.runtime.version`</a> | string | The version of the runtime of this process, as returned by the runtime without modification. | `14.0.2` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-saved-user-id" href="#process-saved-user-id">`process.saved_user.id`</a> | int | The saved user ID (SUID) of the process. | `1002` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-saved-user-name" href="#process-saved-user-name">`process.saved_user.name`</a> | string | The username of the saved user. | `operator` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-session-leader-pid" href="#process-session-leader-pid">`process.session_leader.pid`</a> | int | The PID of the process's session leader. This is also the session ID (SID) of the process. | `14` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-title" href="#process-title">`process.title`</a> | string | Process title (proctitle) [3] | `cat /etc/hostname`; `xfce4-session`; `bash` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-user-id" href="#process-user-id">`process.user.id`</a> | int | The effective user ID (EUID) of the process. | `1001` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-user-name" href="#process-user-name">`process.user.name`</a> | string | The username of the effective user of the process. | `root` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-vpid" href="#process-vpid">`process.vpid`</a> | int | Virtual process identifier. [4] | `12` | ![Development](https://img.shields.io/badge/-development-blue) |
| <a id="process-working-directory" href="#process-working-directory">`process.working_directory`</a> | string | The working directory of the process. | `/root` | ![Development](https://img.shields.io/badge/-development-blue) |

**[1] `process.args_count`:** This field can be useful for querying or performing bucket analysis on how many arguments were provided to start a process. More arguments may be an indication of suspicious activity.

**[2] `process.environment_variable.<key>`:** Examples:

- an environment variable `USER` with value `"ubuntu"` SHOULD be recorded
as the `process.environment_variable.USER` attribute with value `"ubuntu"`.

- an environment variable `PATH` with value `"/usr/local/bin:/usr/bin"`
SHOULD be recorded as the `process.environment_variable.PATH` attribute
with value `"/usr/local/bin:/usr/bin"`.

**[3] `process.title`:** In many Unix-like systems, process title (proctitle), is the string that represents the name or command line of a running process, displayed by system monitoring tools like ps, top, and htop.

**[4] `process.vpid`:** The process ID within a PID namespace. This is not necessarily unique across all processes on the host but it is unique within the process namespace that the process exists within.

---

`process.context_switch_type` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `involuntary` | involuntary | ![Development](https://img.shields.io/badge/-development-blue) |
| `voluntary` | voluntary | ![Development](https://img.shields.io/badge/-development-blue) |

---

`process.paging.fault_type` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `major` | major | ![Development](https://img.shields.io/badge/-development-blue) |
| `minor` | minor | ![Development](https://img.shields.io/badge/-development-blue) |

## Process Linux Attributes

Describes Linux Process attributes

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="process-linux-cgroup" href="#process-linux-cgroup">`process.linux.cgroup`</a> | string | The control group associated with the process. [5] | `1:name=systemd:/user.slice/user-1000.slice/session-3.scope`; `0::/user.slice/user-1000.slice/user@1000.service/tmux-spawn-0267755b-4639-4a27-90ed-f19f88e53748.scope` | ![Development](https://img.shields.io/badge/-development-blue) |

**[5] `process.linux.cgroup`:** Control groups (cgroups) are a kernel feature used to organize and manage process resources. This attribute provides the path(s) to the cgroup(s) associated with the process, which should match the contents of the [/proc/\[PID\]/cgroup](https://man7.org/linux/man-pages/man7/cgroups.7.html) file.

## Deprecated Process Attributes

Deprecated process attributes.

| Attribute | Type | Description | Examples | Stability |
|---|---|---|---|---|
| <a id="process-cpu-state" href="#process-cpu-state">`process.cpu.state`</a> | string | Deprecated, use `cpu.mode` instead. | `system`; `user`; `wait` | ![Deprecated](https://img.shields.io/badge/-deprecated-red)<br>Replaced by `cpu.mode`. |
| <a id="process-executable-build-id-profiling" href="#process-executable-build-id-profiling">`process.executable.build_id.profiling`</a> | string | "Deprecated, use `process.executable.build_id.htlhash` instead." | `600DCAFE4A110000F2BF38C493F5FB92` | ![Deprecated](https://img.shields.io/badge/-deprecated-red)<br>Replaced by `process.executable.build_id.htlhash`. |

---

`process.cpu.state` has the following list of well-known values. If one of them applies, then the respective value MUST be used; otherwise, a custom value MAY be used.

| Value  | Description | Stability |
|---|---|---|
| `system` | system | ![Development](https://img.shields.io/badge/-development-blue) |
| `user` | user | ![Development](https://img.shields.io/badge/-development-blue) |
| `wait` | wait | ![Development](https://img.shields.io/badge/-development-blue) |
