# Lyft Data Science Assignment
Rider Cancellations create bad experiences for both Drivers and Riders on the Lyft platform and impact Lyft financially. This analysis aims to explore and analyze the rider cancellation data and randomized experiment data to help develop Lyft Cancellation Fee policy.

The attached notebook uses basic Exploratory Data Analysis technics and focuses on demonstrating the application of [Bootstrap](https://en.wikipedia.org/wiki/Bootstrapping_(statistics)) and [Delta Method](https://dl.acm.org/doi/10.1145/3219819.3219919) for A/B testing, as well as proper use of [Logistic Regression](https://en.wikipedia.org/wiki/Logistic_regression) for factor analysis.

**Ride Data**
1. `ride_id` - Unique identifier for the ride request.
2. `rider_id` - Unique identifier for the rider who requested the ride.
3. `driver_id` - Unique identifier for the driver.
4. `ride_type` - Type of ride requested (shared, normal).
5. `upfront_fare` - Final fare quote provided to the Rider before the request was made. This is
surfaced to the rider after they enter both an origin and destination in the Lyft app..
6. `rider_paid_amount` - Total amount of money the rider paid to Lyft.
7. `eta_to_rider_pre_match` - ETA (estimated time to arrival) shown to the rider immediately
before the ride request was made.
8. `eta_to_rider_post_match` - ETA shown to the rider immediately after the ride request was matched to a specific driver driver.
9. `requested_at_local` - Time when ride was requested.
10. `accepted_at_local` - Time when the driver accepted the ride request.
11. `arrived_at_local` - Time when the driver arrived at the pickup location.
12. `picked_up_at_local` - Time when the rider was picked up from the pickup location.
13. `dropped_off_at_local` - Time when the rider was dropped off.
14. `actual_time_to_arrival` - Time (in seconds) for the driver to reach the designated pickup
location after being matched with the ride request.
15. `cancellation_flag` - Boolean flag for whether the ride was cancelled.
16. `rider_request_number` - Sequential count of ride requests for each rider.

**Experiment Data**
1. `rider_id` - unique identifier for a Rider.
2. `variant` - experiment group the Rider was in.
3. `cancel_penalty` - cancellation penalty fee for the variant.

**Additional references:**
* https://medium.com/@vktech/practitioners-guide-to-statistical-tests-ed2d580ef04f
* https://github.com/marnikitta/stattests
