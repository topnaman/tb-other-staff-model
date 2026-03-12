# TB Program Staffing Resource Calculator

A workforce planning tool for TB programs, estimating FTE requirements across support, site-based, centralized, and supervisory staff categories. Built for LA County Department of Public Health — TB Control Program.

## Features

- **Availability-adjusted FTEs**: Separate calculations for clinical (includes admin/meeting time) and non-clinical (time-off only) staff
- **Four staff categories**: Support staff, site-based, centralized, and supervisors
- **Configurable ratios**: Per-provider, per-site, and absolute headcounts
- **Real-time updates**: Results recalculate on every input change after first run
- **FTE bar visualization**: Relative proportion bars alongside each FTE figure
- **Span of control**: Supervisor requirements derived from subordinate FTE counts

## Parameters

### Basic
| Parameter | Default | Notes |
|-----------|---------|-------|
| TB Providers | 5 | Drives support staff ratios |
| Clinical Sites | 5 | Drives site-based staff ratios |
| Calendar Work Days | 260 | Pre-time-off baseline |

### Staff Availability
| Factor | Default |
|--------|---------|
| Scheduled Leave | 22 days/yr |
| Sick Leave | 8 days/yr |
| Training Time | 5 days/yr |
| Other Time Off | 12 days/yr |
| Admin Time | 4 hrs/week |
| Meeting Time | 4 hrs/week |

### Staffing Ratios (defaults)
- RN: 1 per provider
- MA/LVN: 1 per provider
- PHN: 2 per provider
- Supervising Clinic Nurse: 1 per site
- Clerk: 1 per site
- Rad Tech: 0.5 per site
- Nurse Visit: 1 per site

### Centralized Staff (default totals)
Pharmacists: 2 | DOT: 4 | Transport: 4 | Business Office: 4 | LTBI Providers: 2

### Supervisor Spans
Medical Director: 8 | Nurse Manager: 4 | PHNS: 8 | Rad Lead: 8 | Clerk Supervisor: 5

## How Availability Is Calculated

**Clinical staff** (RN, MA, PHN, Supervising Nurses, Nurse Visit, Pharmacists, DOT, LTBI Providers):

```
Clinical Availability = (Actual Work Days / Calendar Work Days) × (Direct Hours / 40hrs)
```

**Non-clinical staff** (Clerks, Rad Techs, Transport, Business Office):

```
Non-Clinical Availability = Actual Work Days / Calendar Work Days
```

The resulting FTE = Base Requirement ÷ Availability Factor.

## License

Provided as-is for TB program workforce planning purposes.

## Credits

Developed for LA County Department of Public Health — TB Control Program.
