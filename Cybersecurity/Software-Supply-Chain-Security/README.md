# Software Supply Chain Security

## Overview

This research examines software supply-chain security and the risks created when vulnerabilities or malicious changes are introduced upstream in the software development and distribution process.

Modern software depends on interconnected components, repositories, build systems, CI/CD pipelines, package registries, and third-party dependencies. A compromise at one point in this chain can potentially affect organisations further downstream.

The research evaluates three complementary security approaches:

- Software Bill of Materials (SBOM)
- SLSA-style provenance and build assurance
- NIST Secure Software Development Framework (SSDF)

## Research Question

**How can organisations improve visibility, provenance, and security assurance across the software supply chain?**

## Research Focus

The research examines:

- Software supply-chain attacks
- Third-party dependencies
- Open-source software
- Source-code compromise
- Build-system compromise
- CI/CD security
- Artifact integrity
- Software provenance
- Software Bill of Materials (SBOM)
- SLSA-style provenance
- Secure Software Development Framework (SSDF)
- Vulnerability management
- Software assurance

## Threat Landscape

The research identifies several areas where software supply chains can be compromised.

### Upstream Dependency Compromise

A malicious or vulnerable dependency can introduce risk into applications that consume it.

### Source-Code Tampering

Attackers may attempt to modify source code before it reaches the build process.

### Build and CI/CD Compromise

Compromise of build infrastructure can allow attackers to influence software artifacts without necessarily modifying the original source code.

### Distribution Compromise

Even if source code and build processes are secure, weaknesses in artifact distribution can create additional risks.

## Security Controls Examined

### Software Bill of Materials

An SBOM provides visibility into the components and relationships that make up a software product.

This can support:

- Dependency visibility
- Vulnerability identification
- Component tracking
- Software inventory
- Faster vulnerability response

### SLSA-Style Provenance

SLSA-style approaches are examined as a method of increasing confidence in where and how software artifacts were produced.

The focus is on build integrity, provenance, and the ability to establish evidence about the software production process.

### NIST SSDF

The NIST Secure Software Development Framework is examined as a structured approach to incorporating security practices throughout the software development lifecycle.

The research considers how secure development practices can complement technical supply-chain controls.

## Case Studies

### SolarWinds Orion

The research examines the SolarWinds Orion compromise as an example of how malicious changes introduced into a software vendor's development and distribution process can reach downstream customers through trusted software updates.

The case is used to discuss:

- Build integrity
- Software provenance
- Trust in vendor updates
- Detection challenges
- Evidence and assurance
- Secure software-development controls

### Log4Shell

The research also considers the Log4j vulnerability as an example of the visibility challenges created by widely distributed software dependencies.

The case highlights the importance of understanding which components exist within an organisation's software environment and how quickly affected components can be identified.

## Layered Security Model

The research considers SBOMs, provenance, and secure development practices as complementary controls.

```text
              SOFTWARE SUPPLY CHAIN
                       |
        +--------------+--------------+
        |              |              |
       SBOM        Provenance         SSDF
        |              |              |
  Component        Build /        Secure
  Visibility       Artifact       Development
                   Assurance       Practices
        |              |              |
        +--------------+--------------+
                       |
              Supply-Chain Assurance
```

The three approaches address different aspects of the problem:

| Control | Primary Security Goal |
|---|---|
| SBOM | Visibility into software components and dependencies |
| SLSA-style provenance | Evidence about software origin and build integrity |
| SSDF | Secure development practices throughout the SDLC |

## Key Findings

The research concludes that software supply-chain security requires visibility, assurance, and secure development practices working together.

An organisation may know which components are present without knowing whether an artifact was produced through a trustworthy build process. Similarly, strong development practices do not automatically provide complete visibility into every dependency used by a software product.

A layered approach can therefore provide broader assurance than relying on a single control.

## Key Learning Outcomes

This research developed my understanding of:

- Software supply-chain attack surfaces
- Dependency management
- SBOMs
- Software provenance
- Build integrity
- CI/CD security
- Secure software development
- Software assurance
- Supply-chain risk management
- The relationship between development security and operational security

## Limitations

This research is primarily a literature and case-study analysis.

It does not present:

- A production software supply-chain implementation
- A formal security proof
- Independent penetration testing of the case-study organisations
- A complete implementation of SLSA or SSDF
- A guarantee that the discussed controls eliminate supply-chain risk

## Academic Context

This work was completed as academic cybersecurity research.

It is intended to demonstrate research, analysis, and understanding of software supply-chain security rather than claim professional implementation experience.

## Files

- `report.pdf` — Full academic research report
- `README.md` — Portfolio summary of the research
