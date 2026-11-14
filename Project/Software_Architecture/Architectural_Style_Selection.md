# Architectural Style Selection

## Selected architectural style
Layered architectural style (open architecture with partitions) under a presentation tier

## Main characteristics
- Components are grouped into horizontal layers; each layer offers services to the layers above it only through provided interfaces.
- A layer only depends on services from lower layers and has no knowledge of higher layers. ONE uses an open architecture: a layer may call any lower layer, not only the one directly below.
- Layers are divided into partitions (weakly coupled subsystems of the same layer). Partitions may provide services to each other. These dependencies point one way and contain no cycles.
- ONE has a presentation tier (web and mobile client) above three internal layers: L1 Application layer; L2 Business services layer; L3 Platform services layer.
- External systems (ERP, Attendance System) are reached only through adapters (PayrollAdapter, AttendanceAdapter) that specialize the shared IntegrationAdapter.

## Why it is appropriate for ONE
- ONE is a front end over enterprise services: almost every use case is a request/response chain from the client to a business service, which in turn uses identity, notification and integration services. Our sequence diagrams already show this top-down chain (e.g., UC-09: Employee → Payroll → PayrollAdapter → ERP).
- The Level-0 DFD processes map one-to-one or two-to-one onto components, and the three data stores D1–D3 stay owned by the components that use them.
- The Incremental Model delivers modules in increments; with layering, the platform layer is built first and each later increment adds a business component on top without changing lower layers.
- The team size and semester schedule suit one deployable application organized in layers better than separately deployed services.

## How it supports the design goals
| Design goal | Support provided by the layered style |
|---|---|
| DG-01 Maintainability | Classes are grouped by their associations, so most interaction stays inside a subsystem (high coherence). Subsystems meet only through narrow interfaces (low coupling, information hiding). Dependencies point only downward and contain no cycles, so a change in a business module cannot ripple into the platform layer. Directory, Announcements and Payroll are separate modules, as NFR-08 requires. |
| DG-02 Security | All access control lives in the lowest (platform) layer, and every business module must go through its access-control interface. No module can bypass authentication, session expiry or role permissions. |
| DG-03 Reliability | External systems are reached only through adapters that share one timeout and failure-handling base. An ERP outage is handled inside the payroll module, using the 24-hour cache, and never propagates to other layers. |
| DG-04 Performance | The open architecture lets the application layer read notifications, announcements and employee data directly from the platform layer, without pass-through calls. The dashboard is the only aggregation point. It calls independent lower-layer interfaces that can be queried in parallel. Attendance and payslip data come from imported records or the cache, not live external calls. |

## Advantages and potential limitations

### Advantages
- Clear separation of concerns that matches the team's existing module split and DFD processes.
- Lower layers (identity, notifications) are reused by every business module.
- Easy to test layer by layer and to replace an external system or adapter without touching business logic.
- Fits incremental delivery and the team's skills (single web/mobile application).

### Limitations
- Requests pass through several layers, adding call overhead; the dashboard depends on several lower-layer modules.
- Design trade-off: an open architecture favors runtime efficiency over the lower coupling of a closed one. The application layer calls the platform layer directly instead of passing through the business layer, so a change to platform interfaces can also affect the application layer.
- Partitions in the same layer must stay one-directional to avoid cycles.
