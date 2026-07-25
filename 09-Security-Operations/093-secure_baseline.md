# Secure Configuration Baseline Standard

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Secure Configuration Baseline Standard
**Owner:** Infrastructure Manager
**Version:** 1.0



# 1. Purpose

This standard defines the minimum secure configuration expected for each asset type in WHT's digital estate. It is the primary evidence for CAF B4 System Security, currently rated **Partially Achieved** ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3): baselines exist and are applied to parts of the estate, but consistent, verified coverage across all asset types has not yet been demonstrated, which is why B4 is not rated Achieved.



# 2. Scope

This standard applies to all assets in the [master assets register](../02-Asset-Management/022-master_assets_register.xlsx). It does not apply to third-party-hosted systems where the supplier retains configuration responsibility under contract, which are instead addressed through supplier assurance ([../05-Governance/055-supplier_security_policy](../05-Governance/055-supplier_security_policy.md)).



# 3. Baseline Framework

Baselines are derived from CIS Benchmarks and vendor hardening guidance, adapted for WHT's environment. Where a CIS Benchmark does not exist for an asset type (notably medical devices), the manufacturer's security configuration guide is used instead.



# 4. Baseline Coverage by Asset Type

| Asset Type | Baseline Source | Coverage Status |
|---|---|---|
| Servers (Windows/Linux) | CIS Benchmarks | Applied to majority of estate; verification not yet continuous |
| Corporate endpoints | CIS Benchmarks, vendor endpoint hardening guidance | Applied via standard build image |
| Network devices | Vendor hardening guidance | Partial — dependent on accurate asset ownership records ([risk register](../04-Risk-Management/049-risk_register.md) CR-007) |
| Azure / cloud services | Microsoft cloud security benchmark | Not yet formally assessed — see [../12-Azure-Governance/](../12-Azure-Governance/) |
| Medical devices | Manufacturer configuration guidance | Constrained — see §6 and CR-003 |

This table should be read alongside §7: baseline application without a verification step is a documented control gap, not a claim of full coverage.



# 5. Deviation and Exception Process

Where an asset cannot meet the standard baseline — most commonly due to a clinical or operational dependency — the asset owner raises a documented exception with the Infrastructure Manager, recording the specific deviation, the reason, and any compensating control. Exceptions are time-bound and reviewed at the cadence in §8. This mirrors the exception process for unpatchable medical devices in [092-patch_management](092-patch_management.md) §5, since the two often arise from the same underlying constraint.



# 6. Medical Devices

Medical device configuration is constrained by the same factors as patching (§5 of [092-patch_management](092-patch_management.md)): manufacturers restrict configuration changes to preserve their regulatory approval and instructions for use. Where manufacturer guidance does not permit a control this standard would otherwise require, the deviation is logged as an exception (§5) rather than silently left unaddressed, consistent with the CR-003 treatment approach in [046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md).



# 7. Baseline Verification and Drift Detection

Baseline compliance is checked at build/deployment time for servers and endpoints. Ongoing drift detection — confirming a previously compliant asset has not since deviated from baseline — is not yet performed on a continuous, automated basis. This is consistent with, and contributes to, the CAF C2 Proactive Security Event Discovery rating of **Not Achieved** ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3, REC-005): closing that gap would also close the drift-detection gap recorded here.



# 8. Review and Maintenance

Baselines are reviewed annually, or sooner following a material change to a supported framework (e.g. a new CIS Benchmark release) or a finding from [091-vulnerability_register](091-vulnerability_register.md) that indicates a baseline is insufficient. Open exceptions are reviewed quarterly by the Infrastructure Manager and reported to the Cyber Security Governance Group per [051-security_strategy](../05-Governance/051-security_strategy.md) §6.
