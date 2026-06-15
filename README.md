# Football Ticket Booking System

A PostgreSQL assignment where I built a football ticket booking database from scratch.

## What I Did

### Schema Design
Created 3 tables with proper constraints:
- `Users` — stores fans and ticket managers, with a role check and unique email enforcement
- `Matches` — holds fixture info, tournament category, pricing, and availability status
- `Bookings` — links users to matches with seat numbers, payment status, and total cost

### Sample Data
Seeded realistic data — 4 users, 5 matches across different leagues, and 5 bookings with varied payment statuses (including a NULL case to test edge handling).

### Queries
Wrote 7 queries covering real-world scenarios:
1. Filter available Champions League matches
2. Search users by name using `ILIKE`
3. Find bookings with missing payment status, replacing `NULL` with `'Action Required'` via `COALESCE`
4. Join all 3 tables to show full booking details
5. `LEFT JOIN` to list all users including those with no bookings
6. Subquery to find above-average cost bookings
7. Pagination with `LIMIT` and `OFFSET` to get the 2nd and 3rd most expensive matches
