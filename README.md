# nova-shared-templates

NOVA - Shared CloudFormation Templates. A repository for re-useable CloudFormation
templates that can be used for NOVA service tools. Templates use parameters to be re-useable.

Built specifically to be used as [nested stack templates](https://blogs.aws.amazon.com/application-management/post/Tx1T9JYQOS8AB9I/Use-Nested-Stacks-to-Create-Reusable-Templates-and-Support-Role-Specialization).

## Auto-Scaling Templates

These templates include auto-scaling alarms with scale-up & scale-down by requests per minute. ELB, AutoScalingGroup, LaunchConfiguration & Healthcheck alarm.

## General Templates

These templates are general use-case. ELB, AutoScalingGroup, LaunchConfiguration & Healthcheck alarm.

## Live-Canary Templates

These templates are for live-canary instances. NO ELB is included and must be provided from another stack, AutoScalingGroup, LaunchConfiguration & Healthcheck alarm.

## External Templates

These templates are general use-case, except ELB & ASG subnets can be configured separately. ELB, AutoScalingGroup, LaunchConfiguration & Healthcheck alarm.

## Template Details

### 1.0/NovaAutoScalingStack.json

A simple auto-scaling stack.

### 1.0/NovaAutoScalingExternalHTTP_HTTPSStack.json

An auto-scaling stack with an internet-facing ELB and an extra parameter for separate ELB subnets
and both HTTP & HTTPS ELB listeners.

### 1.0/NovaAutoScalingExternalStack.json

An auto-scaling stack with an internet-facing ELB and an extra parameter for separate ELB subnets.

### 1.0/NovaGeneralStack.json

A simple non auto-scaling stack.

### 1.0/NovaGeneralExternalStack.json

A simple non auto-scaling stack with an internet-facing ELB and an extra parameter for separate ELB subnets.

### 1.0/NovaGeneralStack_NoDNS.json

A simple non auto-scaling stack, without a DNS record.

### 1.0/NovaLiveCanaryStack.json

A simple non auto-scaling stack with no ELB or DNS record, the ELB reference must be passed in as a parameter.
