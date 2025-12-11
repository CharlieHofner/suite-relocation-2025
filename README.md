# suite-relocation-2025
2025 server room relocation &amp; full refresh: Suite A → Suite B (30% larger). New 48U rack, stacked 9200Ls, Arctic Wolf, cabling, ISP drama, zero critical downtime. Complete timeline + lessons learned.

# Server Rack & Network Relocation Project Documentation

**Project:** Physical Relocation & Infrastructure Refresh – Suite A → Suite B  
**Location:** Texas, USA  
**Author:** Charlie Hofner  
**LinkedIn**: [LinkedIn](https://www.linkedin.com/in/charlie-hofner/)  
**Date:** December 10, 2025  

## 📋 Executive Summary

This document details the complete relocation and infrastructure refresh of our primary server rack and network infrastructure from Suite A to the newly acquired Suite B (30% larger footprint). What began as a simple "move next door" became a full swing migration with significant hardware upgrades due to leasing delays and strategic planning.

**Key Challenges:**
- 2.5-month lease execution delay by landlord
- Only 2.5 weeks total move window (March 10 - April 1, 2025)
- AT&T ISP demarcation delays (4 weeks late despite simultaneous notification with Verizon)

**Major Wins:**
- Complete infrastructure refresh during the move
- Proactive cabling completed in 4 business days
- Verizon MPLS carried all critical ERP traffic flawlessly
- Large wall cut enabled efficient warehouse relocation

## 🛠️ Infrastructure Upgrades

| Component | Old | New | Benefit |
|-----------|-----|-----|---------|
| **Server Rack** | 42U | 48U full-depth | 14% more capacity |
| **MDF UPS** | Aging APC units | 2× APC Smart-UPS (≥3000VA) | True N+1 redundancy |
| **IDF UPS** | Weak 1kW APC | 1× APC Smart-UPS 1000W | Replaced end-of-life |
| **MDF Switching** | 1× Cisco 2960X 48-port | **2× Cisco 9200L 48-port PoE+** | Stacked redundancy |
| **IDF Switching** | 1× Cisco 2960X 48-port | **2× Cisco 9200L 24-port PoE+** | Redundancy + growth |
| **Security** | None | 2× Arctic Wolf AWN202 | First-time MDR deployment |

## 📊 Timeline

| Date | Milestone |
|------|-----------|
| **Late 2024** | Previous tenant vacates Suite B |
| **Jan 2025** | Move first anticipated |
| **Mid-Mar 2025** | Lease finally executed (2.5mo delay) |
| **Mar 10-14** | Cabling contractor completes all low-voltage work |
| **Mar 10** | ISP notifications sent (Verizon + AT&T) |
| **Mar 11** | Verizon MPLS cutover completed |
| **Late Mar** | Server rack swing weekend |
| **Apr 1** | **HARD DEADLINE** - Suite A fully vacated |
| **Apr 8-12** | AT&T finally completes demarc (4 weeks late) |

## 🌐 ISP Performance

| Provider | Service | Performance | Notes |
|----------|---------|-------------|-------|
| **Verizon** | MPLS + DIA | ⭐⭐⭐⭐⭐ Flawless | Completed same week; carried ERP/file shares |
| **AT&T** | DIA (Internet) | ⭐⭐ No-show for 4 weeks | Required payment threats + churn warning |

**Traffic during AT&T outage:**
- ✅ **Verizon MPLS:** ERP, file shares (100% uptime)
- 📱 **Cellular failover:** O365, web, Teams (50/50 circuit → ~25/20 Mbps real-world)

## 🔧 Structured Cabling (Pre-Move)
- **8× Wi-Fi APs** (PoE)
- **6× IP cameras** (PoE) - requested 12-14, budget approved 6
- **4× workstations** + **4× Zebra label printers** + **4× HP printers**
- **2× fiber runs** demarc → server room
- All Cat6A, plenum-rated, 10G tested

## ⚠️ Lessons Learned

1. **Start cabling DAY 1** of lease signing - saved weeks of schedule
2. **Verizon Business = gold standard** for enterprise moves
3. **AT&T Business = avoid if possible** - prepare escalation paths immediately
4. **Negotiate wall openings** in lease exhibits for warehouse moves
5. **Cellular failover works** but expect ~50% of rated speeds
6. **Turn delays into upgrades** - this "simple move" became a full refresh

## 📁 Files

- [`suite-relocation-2025.pdf`](./suite-relocation-2025.pdf) - Official project documentation
- [`README.md`](./README.md) - This file

## 🏆 Project Outcome

Despite landlord delays, aggressive timelines, and ISP failures, the project was completed on time (April 1 deadline met) with:
- ✅ Zero downtime to critical ERP/file share systems
- ✅ Complete infrastructure refresh at no additional schedule cost
- ✅ Future-proofed network for 2+ years of growth
- ✅ First-time MDR security deployment

---

*Documented by Charlie Hofner - December 2025*
