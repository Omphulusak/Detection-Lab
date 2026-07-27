# Custom KQL Detection Rules

## Detect Apollo Payload Execution

```kql
event.code:1 and (
process.name:"svchost-mydfir.exe"
or
winlog.event_data.OriginalFileName:"Apollo.exe"
)
```

---

## Detect RDP Authentication

```kql
event.code:4624
and
winlog.event_data.LogonType:10
```

---

## Detect PowerShell Execution

```kql
event.code:1
and process.name:powershell.exe
```

---

## Detect Suspicious Network Connections

```kql
event.code:3
```

---

## Detect Discovery Commands

```kql
process.command_line:
(
*whoami*
or
*hostname*
or
*ipconfig*
or
*net user*
or
*net group*
)
```

---

# Investigation Fields

- host.name
- user.name
- process.name
- process.parent.name
- process.command_line
- process.hash.sha256
- destination.ip
