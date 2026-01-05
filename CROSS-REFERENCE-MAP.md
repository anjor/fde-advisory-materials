# Cross-Reference Map

This document maps all dependencies and relationships between the 17 FDE practice areas to help maintain link integrity and understand how topics connect.

---

## How to Use This Map

- **Prerequisites**: Must be addressed before this practice area
- **Complementary**: Work better when addressed together
- **Downstream**: Enabled or improved by this practice area
- **Referenced by**: Other practice areas that link to this one

---

## People & Organization

### Organizational Design & Structure
**File**: `people/organizational-design.md`

**Prerequisites**: None (typically first)

**Complementary**:
- Operating Model & Metrics - Metrics follow from org structure
- Hiring & Talent Strategy - Role definitions inform hiring
- Commercial Model & GTM - Commercial structure aligns with org

**Downstream**:
- Product-FDE Interface - Clear boundaries enable interfaces
- Change Management - Org changes require change management

**Referenced by**: Hiring, Commercial Model, Operating Model, Product-FDE Interface, Change Management

---

### Hiring & Talent Strategy
**File**: `people/hiring-talent-strategy.md`

**Prerequisites**:
- Organizational Design - Define roles before hiring

**Complementary**:
- Training & Career Development - Hiring and development work together

**Downstream**:
- Scaling the Organization - Strong hiring enables scaling

**Referenced by**: Training, Scaling, Competitive Positioning

---

### Training, Onboarding & Career Development
**File**: `people/training-career-development.md`

**Prerequisites**:
- Hiring & Talent Strategy - Hire before onboarding

**Complementary**:
- Technical Enablement - Technical infrastructure supports training
- Operating Model & Metrics - Performance management aligns with career development

**Downstream**:
- Community & Knowledge Management - Trained FDEs contribute to knowledge sharing
- Scaling the Organization - Strong development programs enable scaling

**Referenced by**: Operating Model, Scaling, Community & Knowledge, Domain Expertise

---

### Change Management & Organizational Adoption
**File**: `people/change-management.md`

**Prerequisites**:
- Organizational Design - Define target state before driving change

**Complementary**:
- Product-FDE Interface - Clear interfaces reduce friction
- Commercial Model & GTM - Sales enablement is part of change management

**Downstream**:
- Scaling the Organization - Successful adoption enables scaling

**Referenced by**: Scaling

---

### Geographic Distribution & Remote Models
**File**: `people/geographic-distribution.md`

**Prerequisites**: None

**Complementary**:
- Hiring & Talent Strategy - Location strategy affects sourcing
- Customer Deployment & Success - Geographic decisions impact deployment models

**Downstream**:
- Scaling the Organization - Geographic expansion is part of scaling

**Referenced by**: None explicitly, but relevant to hiring and scaling

---

### FDE Community & Knowledge Management
**File**: `people/community-knowledge-management.md`

**Prerequisites**: None (but critical during scaling)

**Complementary**:
- Training & Career Development - Learning and knowledge sharing are intertwined
- Technical Enablement - Documentation standards support knowledge capture
- Scaling the Organization - Knowledge management essential for scaling

**Downstream**: None (often last to fully mature)

**Referenced by**: Scaling, Technical Enablement

---

## Product & Technical

### Product-FDE Interface
**File**: `product/product-fde-interface.md`

**Prerequisites**:
- Organizational Design - Clear org boundaries enable interface agreements

**Complementary**:
- Technical Enablement - Technical standards support collaboration
- Operating Model & Metrics - Governance and prioritization frameworks

**Downstream**:
- Customer Deployment & Success - Smooth interface enables faster deployments

**Referenced by**: Change Management, Operating Model, Competitive Positioning

---

### Technical Enablement & Standards
**File**: `product/technical-enablement.md`

**Prerequisites**: None

**Complementary**:
- Product-FDE Interface - Technical standards support collaboration
- Training & Career Development - Good documentation accelerates onboarding

**Downstream**:
- Community & Knowledge Management - Standards enable knowledge sharing

**Referenced by**: Training

---

### Domain Expertise & Industry Specialization
**File**: `product/domain-expertise.md`

**Prerequisites**: None

**Complementary**:
- Training & Career Development - Domain learning is part of FDE development
- Product-FDE Interface - Domain insights inform product direction

**Downstream**: None

**Referenced by**: None explicitly

---

### Failure Recovery & Risk Management
**File**: `product/failure-recovery-risk.md`

**Prerequisites**: None

**Complementary**:
- Customer Deployment & Success - Deployment practices affect failure risk
- Operating Model & Metrics - Early warning signals come from metrics

**Downstream**: None

**Referenced by**: Customer Deployment

---

## Commercial & Market

### Commercial Model & Go-to-Market
**File**: `commercial/commercial-model-gtm.md`

**Prerequisites**:
- Organizational Design - Commercial model must align with org structure

**Complementary**:
- Customer Deployment & Success - Delivery model affects commercial structure
- Legal, Contracts & IP - Legal frameworks support commercial terms
- Change Management - Sales team enablement is critical

**Downstream**:
- Competitive Positioning - Commercial model is key differentiator

**Referenced by**: Organizational Design, Customer Deployment, Legal, Competitive Positioning

---

### Customer Deployment & Success
**File**: `commercial/customer-deployment-success.md`

**Prerequisites**: None

**Complementary**:
- Commercial Model & GTM - Commercial terms affect deployment approaches
- Product-FDE Interface - Technical collaboration enables successful deployments
- Failure Recovery & Risk - Deployment challenges require recovery plans

**Referenced by**: Commercial Model, Operating Model, Geographic Distribution, Partner Ecosystem

---

### Legal, Contracts & IP Considerations
**File**: `commercial/legal-contracts-ip.md`

**Prerequisites**: None

**Complementary**:
- Commercial Model & GTM - Legal terms support commercial structure
- Customer Deployment & Success - Contracts govern deployment work
- Partner & Ecosystem - Legal frameworks for partner relationships

**Referenced by**: Commercial Model

---

### Partner & Ecosystem Coexistence
**File**: `commercial/partner-ecosystem.md`

**Prerequisites**: None

**Complementary**:
- Customer Deployment & Success - Partner collaboration affects delivery
- Competitive Positioning - Positioning relative to partners
- Legal, Contracts & IP - Legal frameworks for partnerships

**Downstream**: None

**Referenced by**: None explicitly

---

### Competitive Positioning & Differentiation
**File**: `commercial/competitive-positioning.md`

**Prerequisites**: None

**Complementary**:
- Commercial Model & GTM - Commercial structure affects positioning
- Organizational Design - Org design reflects positioning
- Hiring & Talent Strategy - Talent quality supports positioning
- Product-FDE Interface - Product collaboration is differentiator

**Downstream**: None

**Referenced by**: Commercial Model

---

## Operations & Scaling

### Operating Model & Metrics
**File**: `operations/operating-model-metrics.md`

**Prerequisites**:
- Organizational Design - Metrics follow from org structure

**Complementary**:
- Training & Career Development - Performance management links to career development
- Product-FDE Interface - Backlog governance requires interface clarity
- Customer Deployment & Success - Deployment metrics inform operating model

**Downstream**:
- Scaling the Organization - Operating metrics enable informed scaling decisions

**Referenced by**: Organizational Design, Product-FDE Interface, Failure Recovery

---

### Scaling the FDE Organization
**File**: `operations/scaling-organization.md`

**Prerequisites**:
- Operating Model & Metrics - Metrics inform scaling decisions

**Complementary**:
- Training & Career Development - Career paths support scaling
- Change Management - Scaling requires organizational change
- Community & Knowledge Management - Knowledge management prevents silos

**Downstream**: None (often culmination of FDE maturity)

**Referenced by**: Hiring, Training, Change Management, Geographic Distribution, Community & Knowledge

---

## Dependency Visualization

### Most Referenced (Central to Framework)
1. **Organizational Design** (6 references) - Foundation for many practices
2. **Operating Model & Metrics** (5 references) - Measurement drives decisions
3. **Scaling the Organization** (5 references) - Goal for many practices
4. **Training & Career Development** (4 references) - People development is key

### Prerequisites (Start Here)
1. **Organizational Design** - No prerequisites, enables many others
2. **Hiring & Talent Strategy** - Requires org design
3. **Training & Career Development** - Requires hiring

### Terminal Nodes (Later Stage)
1. **Competitive Positioning** - No downstream dependencies
2. **Partner & Ecosystem** - Situational, no dependencies
3. **Community & Knowledge Management** - Often last to mature

---

## Link Integrity Checklist

When updating practice area documents, verify:

- [ ] All "Prerequisites" links in frontmatter point to correct files
- [ ] All "Complementary" links in frontmatter point to correct files
- [ ] All "Downstream" links in frontmatter point to correct files
- [ ] "Related Practices" section has correct relative paths
- [ ] Cross-reference arrow (→) links use correct relative paths
- [ ] Framework.md links to practice area are accurate
- [ ] Template links in practice areas point to correct template files

---

*Last Updated: 2026-01-05*
*Version: 3.0*
