# 🔐 Wi‑Fi Authentication Flow (Open System Authentication)

802.11 uses "Open System" authentication for nearly all modern Wi‑Fi networks.

---

# 🧩 Steps

## 1. Authentication Frame (SEQ #1)
STA → AP

Fields:
- Authentication Algorithm: 0 (Open System)
- Transaction Seq #: 1

---

## 2. Authentication Response (SEQ #2)
AP → STA

Fields:
- Status Code (0 = Success)

---

# 🔑 Note
This is *not* security.  
It only establishes that the STA is allowed to proceed to association.