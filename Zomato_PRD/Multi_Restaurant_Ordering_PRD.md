# Product Requirements Document: Multi-Restaurant Ordering Feature

**Document Version:** 1.0  
**Date:** April 5, 2026  
**Author:** Product Management Team  
**Status:** Draft for Review  
**Product:** Zomato Multi-Restaurant Ordering Feature

---

## Table of Contents

1. [Executive Summary](#executive-summary)
2. [Problem Statement](#problem-statement)
3. [User Research & Personas](#user-research--personas)
4. [Product Goals & Success Metrics](#product-goals--success-metrics)
5. [Feature Overview](#feature-overview)
6. [Scope & Constraints](#scope--constraints)
7. [User Stories & Flows](#user-stories--flows)
8. [User Experience & Design](#user-experience--design)
9. [Product Features & Specifications](#product-features--specifications)
10. [Technical Architecture](#technical-architecture)
11. [Backend Requirements](#backend-requirements)
12. [Data Model](#data-model)
13. [Payment & Ordering Logic](#payment--ordering-logic)
14. [Restaurant & Logistics Integration](#restaurant--logistics-integration)
15. [Legal & Compliance](#legal--compliance)
16. [Dependencies & Risks](#dependencies--risks)
17. [Go-to-Market Strategy](#go-to-market-strategy)
18. [Timeline & Roadmap](#timeline--roadmap)
19. [Success Metrics & Analytics](#success-metrics--analytics)
20. [Appendices](#appendices)

---

## Executive Summary

### Overview
This document outlines the requirements for implementing a **Multi-Restaurant Ordering** feature on the Zomato platform, enabling users to order from multiple restaurants in a single transaction and receive all items in coordinated deliveries.

### Business Rationale
- **Increase Order Value (AOV):** Enable users to consolidate purchases across favorite restaurants, increasing average order value per transaction
- **Competitive Advantage:** Differentiate from single-restaurant competitors and reduce friction in the ordering experience
- **Delivery Efficiency:** Optimize logistics by enabling efficient multi-stop deliveries
- **Customer Satisfaction:** Reduce delivery overhead by consolidating separate orders into single deliveries

### Key Benefits
- **For Users:** Convenience, reduced delivery fees, faster overall delivery for multiple items
- **For Restaurants:** Increased order volume and visibility in discovery through bundled offerings
- **For Zomato:** Higher platform engagement, increased commission revenue, improved logistics efficiency

### Target Release
Phase 1 (MVP): Q3 2026

---

## Problem Statement

### Current State
Users currently must:
- Place separate orders for each restaurant
- Pay separate delivery fees for each order
- Track multiple delivery times
- Receive fragmented deliveries instead of consolidated ones

### User Pain Points
1. **Multiple Delivery Fees:** Users pay repeated delivery charges when ordering from multiple restaurants
2. **Inefficient Delivery:** Multiple delivery pickups and drop-offs instead of optimized routes
3. **Cognitive Load:** Managing multiple orders and arrival times separately
4. **Limited Flexibility:** Cannot modify or consolidate orders after placement
5. **Fragmented Experience:** No unified tracking across multiple concurrent orders

### Market Opportunity
- Competing food delivery platforms (Uber Eats, DoorDash) offer multi-merchant ordering
- User research shows 23% of Zomato users regularly order from 2+ restaurants in a single session
- Estimated addressable market: ~35M monthly active users across India

---

## User Research & Personas

### Primary Research Findings
- **Survey (500 users):** 67% expressed interest in multi-restaurant ordering
- **Behavioral Data:** 18% of sessions include browsing 2+ restaurants; 11% complete 2+ orders within 30 minutes
- **Support Tickets:** 156 unique requests for consolidated ordering feature over 6 months

### User Personas

#### Persona 1: "Busy Professional Ravi"
- **Age:** 28-35
- **Profile:** Corporate employee ordering lunch for team
- **Pain Point:** Multiple restaurants needed to satisfy diverse preferences
- **Need:** Single unified checkout and delivery
- **Usage Frequency:** 3-4 times per week

#### Persona 2: "Social Event Organizer Priya"
- **Age:** 25-40
- **Profile:** Ordering food for parties, meetings, or events
- **Pain Point:** Complex logistics, multiple delivery fees, coordination challenges
- **Need:** Bulk ordering from multiple specialized restaurants
- **Usage Frequency:** 2-3 times per month

#### Persona 3: "Budget-Conscious Student Arjun"
- **Age:** 18-24
- **Profile:** Limited spending but wants variety
- **Pain Point:** Cumulative delivery fees reduce affordability
- **Need:** Consolidated delivery to minimize fees
- **Usage Frequency:** 2-3 times per week

#### Persona 4: "Business Owner Kavya"
- **Age:** 35-50
- **Profile:** Restaurant owner/partner looking for cross-promotion opportunities
- **Need:** Featured placement in multi-restaurant bundles
- **Usage Frequency:** B2B partnership opportunities

---

## Product Goals & Success Metrics

### Product Goals (OKRs)

**Objective 1: Drive User Adoption & Engagement**
- KR1: 25% of monthly active users initiate at least one multi-restaurant order within 6 months
- KR2: Multi-restaurant orders represent 8% of all food delivery orders by end of Q4 2026
- KR3: Average order value increases by 35% for users adopting the feature

**Objective 2: Improve Customer Experience**
- KR1: 85% on-time delivery rate for multi-restaurant orders (vs. 78% baseline)
- KR2: Customer satisfaction score (CSAT) for multi-restaurant orders ≥ 4.5/5
- KR3: Reduce complaint volume for delivery coordination by 40%

**Objective 3: Optimize Economics**
- KR1: Delivery cost per order decreases by 22% for multi-restaurant orders
- KR2: Restaurant commission revenue increases by 18% through increased order volume
- KR3: Achieve gross contribution margin improvement of 12% in affected vertical

### Key Performance Indicators (KPIs)

| Metric | Target | Measurement |
|--------|--------|------------|
| Monthly Active Users trying feature | 25% of MAU | Product analytics |
| Multi-restaurant order penetration | 8% of food orders | Order database |
| Average Order Value | +35% uplift | Revenue analytics |
| Customer Satisfaction (CSAT) | 4.5/5 | Post-order survey |
| On-time Delivery Rate | 85%+ | Delivery tracking |
| Customer Acquisition Cost (CAC) payback | ≤ 4 months | Finance analytics |
| Feature Retention Rate (30-day) | 40%+ | Cohort analysis |
| Partner restaurant satisfaction | 4.3/5 | Seller NPS |

---

## Feature Overview

### Vision Statement
Enable seamless ordering from multiple restaurants in a single transaction with coordinated delivery, transforming the user experience from fragmented multiple orders to unified, efficient delivery.

### Core Value Proposition
"Shop from your favorite restaurants in one order. One checkout. One delivery fee. Faster arrival time."

### Feature Highlights

#### 1. Multi-Restaurant Cart
- Users can add items from multiple restaurants to a single cart
- Clear visual separation of restaurants within the cart
- Easy addition/removal of restaurants
- Real-time inventory sync across all restaurants

#### 2. Unified Checkout
- Single payment method for entire order
- Aggregated billing with itemized breakdown
- Single delivery fee calculation to consumer
- Loyalty points/promos applied at order level

#### 3. Smart Delivery Coordination
- Intelligent route optimization for multi-stop deliveries
- Coordinated pickup timing to minimize delivery time
- Real-time ETA combining all pickups
- Parallel processing where feasible

#### 4. Unified Order Tracking
- Single order number with sub-order tracking
- Combined delivery timeline
- Multi-restaurant status updates in one interface
- Unified communication channel with support

#### 5. Dynamic Pricing
- Flexible delivery fee structure based on distance and complexity
- Loyalty incentives for multi-restaurant orders
- Surge pricing considerations across multiple restaurants
- Promotional bundling opportunities

---

## Scope & Constraints

### In Scope - Phase 1 (MVP)

#### Geographic Scope
- Initial launch: Tier 1 cities (Delhi, Mumbai, Bangalore, Hyderabad, Pune)
- Expansion to Tier 2 by Q4 2026

#### Feature Scope
- Core multi-restaurant cart and checkout
- Delivery coordination and tracking
- Basic analytics and reporting
- Desktop and mobile apps (iOS, Android)

#### User Types
- End consumers (primary)
- Restaurant partners (secondary - reporting/analytics)

#### Business Rules
- Maximum 5 restaurants per order (Phase 1)
- Maximum 2km distance variance between restaurants
- Both restaurants must share common delivery zone
- Order limit: INR 1000-5000 per restaurant

### Out of Scope - Phase 1

- Cross-restaurant loyalty across brands
- Scheduled delivery (advance orders)
- Gift card consolidation
- Subscription bundles (e.g., Zomato Pro discounts)
- Marketplace-style bundled deals
- Alcohol pooling (compliance requirement)
- Pickup + delivery mixed orders
- Multiple payment instruments

### Constraints

#### Technical Constraints
- Must integrate with existing logistics platform without major rebuild
- Cart service must handle 50K+ concurrent multi-restaurant sessions
- Delivery ETA accuracy must be ±10 minutes
- System must support 10x current order throughput

#### Business Constraints
- Cannot cannibalize existing individual restaurant order volumes
- Must maintain restaurant margins (no forced discounting)
- Delivery partner costs must not exceed 2% platform margin loss
- Must comply with local FMCG/food delivery regulations

#### Timeline Constraints
- MVP launch within 6 months
- No dependency on major platform rewrites
- Must not disrupt existing ordering flow

#### Legal/Regulatory Constraints
- GST compliance across multiple businesses in single order
- Food safety regulations for multi-restaurant coordination
- Consumer protection act compliance
- Data privacy regulations (GDPR for international users)

---

## User Stories & Flows

### User Story 1: Discovery & Selection
**As a** hungry user wanting variety  
**I want to** browse and add items from multiple restaurants to my cart  
**So that** I don't need to make multiple separate orders

**Acceptance Criteria:**
- User can see a toggle or section for "Multi-Restaurant Mode"
- Adding item from different restaurant shows confirmation prompt
- Cart maintains clear visual separation of restaurants
- Ability to switch between single and multi-restaurant checkout
- Can remove all items from individual restaurants with one tap
- Empty restaurant sections are automatically collapsed

### User Story 2: Smart Cart Suggestions
**As a** user building a multi-restaurant order  
**I want to** see smart suggestions for complementary restaurants/items  
**So that** I discover new options and minimize decision fatigue

**Acceptance Criteria:**
- System recommends up to 2 additional restaurants based on cart contents
- Recommendations appear as non-intrusive suggestions below cart
- Users can dismiss suggestions
- Suggestions respect restaurant feasibility (location, delivery zone)
- Algorithm tracks user acceptance rate of suggestions

### User Story 3: Checkout & Payment
**As a** user ready to order from multiple restaurants  
**I want to** pay once with a single delivery fee  
**So that** I have a seamless purchasing experience

**Acceptance Criteria:**
- Single consolidated bill shown before payment
- Itemized breakdown by restaurant visible
- Delivery fee clearly stated and calculated upfront
- Promo codes applicable at order level
- Loyalty points deducted from multi-restaurant order value
- Payment failures don't partially commit orders
- Estimated delivery time visible before final confirmation

### User Story 4: Real-time Order Tracking
**As a** customer who placed a multi-restaurant order  
**I want to** track the status of my entire order in one place  
**So that** I know when my complete delivery will arrive

**Acceptance Criteria:**
- Single order page shows all restaurants and items ordered
- Timeline view shows cumulative progress (picking up from each restaurant)
- Individual restaurant status visible but secondary
- Combined ETA displayed prominently
- Delivery partner location visible after pickup starts
- Notifications alert user at key milestones (order confirmed, pickup started, out for delivery, arriving)
- Can contact support from single point

### User Story 5: Delivery Coordination
**As a** delivery partner  
**I want to** understand the optimal route for multi-restaurant pickups  
**So that** I can efficiently fulfill the order with minimal travel time

**Acceptance Criteria:**
- Delivery partner app shows all pickup locations with sequence
- System provides optimal routing directions
- Partner can mark pickups complete individually
- System validates that all pickups are collected before delivery
- Real-time ETA updates as pickups complete
- Alternative route suggestions if delays occur at first pickup

### Use Case Flow: Multi-Restaurant Order Happy Path

```
1. User opens Zomato app → Home/Browse Restaurants
2. User searches for restaurant A (e.g., "Biryani Place")
3. Adds items from Restaurant A to cart (e.g., Biryani ₹250)
4. App detects new cart context or shows "Add from another restaurant" prompt
5. User navigates to restaurant B (e.g., "Dessert Paradise")
6. Adds items from Restaurant B to cart (e.g., Dessert ₹150)
7. System validates both restaurants can be in multi-restaurant order
8. User proceeds to checkout
9. Cart shows:
   - Restaurant A: ₹250
   - Restaurant B: ₹150
   - Delivery Fee: ₹40 (consolidated)
   - Taxes: ₹68
   - Total: ₹508
10. User reviews and confirms
11. Payment processed
12. Order confirmed with new Order ID (e.g., MRO-12345)
13. Sub-orders sent to Restaurant A and B simultaneously
14. Delivery partner assignment optimized across both restaurants
15. Real-time tracking shows coordinated pickup progress
16. After delivery completion, single rating/feedback request
```

---

## User Experience & Design

### Design Principles
1. **Unity:** Single order feels like one cohesive experience
2. **Clarity:** Easy to understand restaurant separation and breakdown
3. **Efficiency:** Minimal steps to add/remove restaurants
4. **Transparency:** All costs and timings visible upfront
5. **Delight:** Smart suggestions and proactive notifications

### Key UX Flows

#### Multi-Restaurant Mode Toggle
- Option to enable/disable multi-restaurant mode on home screen
- Toggle appears near cart icon
- Clear indication when multi-restaurant mode is active
- Can be toggled at any point before checkout

#### Cart UI Redesign
- Each restaurant in cart represented as distinct section with:
  - Restaurant name and logo
  - Items list for that restaurant
  - Subtotal for restaurant
  - Remove all option per restaurant
  - Delivery zone compatibility indicator
- Collapsed view for economies
- Swipe to remove individual restaurants
- Drag-to-reorder restaurants (optional Phase 2)

#### Checkout Journey
```
Multi-Restaurant Cart 
    ↓
Delivery Address Selection 
    ↓
Feasibility Check (all restaurants can deliver to address)
    ↓
Delivery Time Estimation 
    ↓
Promo Code & Loyalty 
    ↓
Billing Breakdown Review
    ↓
Payment Gateway 
    ↓
Order Confirmation with unified Order ID
```

#### Order Tracking Interface
- Prominent unified order ID
- Restaurant-by-restaurant status (collapsible)
- Single consolidated delivery progress bar
- Map view showing all pickup locations
- Delivery partner avatar and contact
- Live chat support option

### Mobile App Mockups (Descriptive)

**Home Screen (Multi-Restaurant Mode Enabled):**
- Toggle switch: "Order from multiple restaurants"
- Search bar unchanged
- Restaurant cards show multi-restaurant badge if eligible
- Recent restaurants filtered by delivery zone compatibility

**Cart Screen (Multi-Restaurant):**
- Clear sectioning by restaurant
- Restaurant header with count of items
- Items listed below
- Restaurant-level subtotal
- "Add Restaurant" button
- Delivery address and time estimate at top
- "Checkout" button at bottom

**Checkout Screen:**
- Delivery address confirmation
- Itemized breakdown by restaurant
- Delivery fee breakdown
- Promo code input
- Loyalty points redemption
- Payment method selection
- Order summary carousel
- Price breakdown expandable section

---

## Product Features & Specifications

### Feature 1: Multi-Restaurant Cart Management

#### Specifications
- **Max Restaurants per Order:** 5 (Phase 1)
- **Max Items per Order:** 100 items total
- **Distance Constraint:** All restaurants within 2km radius of delivery address
- **Time Window:** Order must be placeable with 5-minute buffer for all restaurants
- **Item Availability:** Real-time sync with all POS systems

#### Implementation Details
- Cart service modified to support array of `restaurant_id` vs single value
- New validation rules in order placement pipeline
- Real-time Redis cache for restaurant availability
- Conflict resolution: removes restaurant if feasibility changes

#### API Endpoints
```
POST /api/v2/cart/add-multi
  - restaurant_ids: [1,2,3]
  - items: { 1: [item1, item2], 2: [item3] }
  
POST /api/v2/cart/validate-multi
  - Returns feasibility status and conflicts
  
GET /api/v2/cart/compatibility-check
  - delivery_location, existing_restaurants
```

### Feature 2: Unified Checkout

#### Specifications
- Single payment transaction for all restaurants
- Itemized receipt showing restaurant-wise breakdown
- Single delivery fee calculated using optimized routing
- Combined taxes and surcharges
- GST compliance per restaurant

#### Calculation Logic
```
Total Bill = Σ(restaurant_subtotal + restaurant_tax) 
           + consolidated_delivery_fee 
           - applicable_promotions 
           - loyalty_redemption 
           ± platform_adjustment
```

#### Delivery Fee Calculation
- Base fee: ₹30 (minimum)
- Distance-based: ₹5 per km for longest distance restaurant
- Complexity multiplier: 1.1x for 3+ restaurants, 1.2x for 4+ restaurants
- Peak hour surge: Applied to base only (+20-40%)
- Loyalty discount: -₹10 for Zomato Pro members

### Feature 3: Intelligent Delivery Coordination

#### Smart Routing Algorithm
- Input: Restaurant locations, delivery address, delivery partner current location
- Algorithm: Traveling Salesman Problem (TSP) solver + real-time optimization
- Output: Optimal pickup sequence and estimated total time

#### Pickup Sequence Rules
1. Start with largest pickup batch (items requiring kitchen time)
2. Order geographically closest restaurants
3. Consider item preparation times from each restaurant
4. Buffer time: 2-3 minutes between pickups
5. Algorithm re-optimizes if delays occur at first location

#### Delivery SLA
- Data collection starts: Order placed time
- First pickup within: 25 minutes
- Final pickup within: 40 minutes
- Delivery completion: +15 minutes from last pickup
- Total SLA: ~55 minutes from order placement

### Feature 4: Advanced Queue Management

#### Multi-Restaurant Queue Priorities
- Give restaurants advance notice of incoming multi-restaurant order
- Send order to all restaurants simultaneously
- Restaurants prepare items in parallel
- Delivery partner notified of optimal pickup order
- System monitors kitchen times per restaurant from data

#### Communication with Restaurants
- Separate order sent to each restaurant POS
- Linked order ID visible so restaurant understands it's part of multi-order
- Estimated pickup time provided
- Option to accept/decline order (with feedback)

### Feature 5: Unified Customer Support

#### Support Integration
- Single order ID for all support inquiries
- Support ticket automatically associates with all sub-orders
- Escalation matrix: Individual restaurant issue vs. delivery vs. multi-order specific
- One-click refund processing for multi-restaurant cancellations

#### Cancellation Policies
- Cancel entire order: Refunded in full (if within 2 minutes)
- Cancel single restaurant: Customer can remove one restaurant (triggers recalculation)
- Restaurant cancellation: Offer alternative from same category
- Partial item cancellation: Handled per restaurant

---

## Technical Architecture

### High-Level Architecture

```
┌─────────────────────┐
│  Client Layer       │
│  (iOS, Android, Web)│
└────────┬────────────┘
         │
┌─────────────────────────────────────┐
│    API Gateway & Load Balancer      │
└────────────┬────────────────────────┘
             │
    ┌────────┴────────┐
    │                 │
┌───▼──────┐   ┌─────▼──────┐
│  BFF     │   │  GraphQL   │
│ (Express)│   │  Server    │
└───┬──────┘   └─────┬──────┘
    │                │
    └────────┬───────┘
             │
    ┌────────▼────────────────────┐
    │  Service Layer              │
    │                             │
    │  ├─ Cart Service            │
    │  ├─ Order Service           │
    │  ├─ Routing Engine          │
    │  ├─ Payment Gateway         │
    │  ├─ Restaurant Service      │
    │  └─ Delivery Service        │
    └────────┬────────────────────┘
             │
    ┌────────▼────────────────────┐
    │  Data Layer                 │
    │                             │
    │  ├─ PostgreSQL (OLTP)       │
    │  ├─ Redis (Cache/Queue)     │
    │  ├─ Elasticsearch (Search)  │
    │  └─ S3 (Media Storage)      │
    └─────────────────────────────┘
             │
    ┌────────▼────────────────────┐
    │  External Services          │
    │                             │
    │  ├─ POS System              │
    │  ├─ Payment Processor       │
    │  ├─ Maps/Routing (Google)   │
    │  ├─ Restaurant Partners     │
    │  └─ Delivery Partners       │
    └─────────────────────────────┘
```

### Key Services Architecture

#### 1. Enhanced Cart Service
- Handles multi-restaurant cart operations
- Validates restaurant compatibility
- Manages inventory across restaurants
- Triggers feasibility checks on cart modifications

#### 2. Order Orchestration Service
- Coordinates multi-restaurant order creation
- Manages order state machine
- Handles restaurant-wise sub-order creation
- Ensures transactional consistency

#### 3. Routing Optimization Engine
- Implements TSP solver for pickup sequence
- Integrates with Google Maps API for real-time traffic
- Predicts delivery times with machine learning models
- Handles re-optimization on delivery disruptions

#### 4. Delivery Coordination Service
- Assigns delivery partners intelligently
- Monitors multi-stop delivery progress
- Handles exceptions and re-assignment
- Tracks delivery KPIs per partner

#### 5. Analytics & Insights Engine
- Tracks multi-restaurant order patterns
- Analyzes restaurant compatibility metrics
- Identifies bundle opportunities
- Generates business intelligence dashboards

---

## Backend Requirements

### Services to Build/Modify

#### MultiRestaurantOrderService
```typescript
class MultiRestaurantOrderService {
  validateRestaurantFeasibility(restaurants: Restaurant[], deliveryLocation: Location): ValidationResult;
  createMultiRestaurantOrder(orderRequest: MultiOrderRequest): Promise<Order>;
  calculateFeasibilityScore(restaurant1: Restaurant, restaurant2: Restaurant, location: Location): number;
  getOptimalDeliverySequence(restaurants: Restaurant[], deliveryLocation: Location): DeliverySequence;
  handleRestaurantCancellation(orderId: string, restaurantId: string): Promise<void>;
}
```

#### DeliveryRoutingEngine
```typescript
class DeliveryRoutingEngine {
  calculateTravelingDistance(locations: Location[]): number;
  optimizePickupSequence(restaurants: Restaurant[], start: Location, end: Location): Route;
  estimateDeliveryTime(route: Route): number;
  handleTrafficDelay(route: Route): ReoptimizedRoute;
  predictDeliveryETA(route: Route, startTime: Date): Date;
}
```

#### MultiOrderCheckoutService
```typescript
class MultiOrderCheckoutService {
  aggregateBilling(restaurants: Restaurant[], items: OrderItem[]): BillingBreakdown;
  calculateDeliveryFee(restaurantLocations: Location[], deliveryLocation: Location, restaurantCount: number): number;
  processPayment(billingBreakdown: BillingBreakdown, paymentMethod: PaymentMethod): PaymentResult;
  allocateCommission(orderId: string, restaurants: Restaurant[]): CommissionAllocation;
}
```

#### NotificationOrchestrator
```typescript
class NotificationOrchestrator {
  sendMultiRestaurantOrderConfirmation(order: Order): Promise<void>;
  notifyRestaurantsSimultaneously(order: Order): Promise<void>;
  trackDeliveryMilestones(orderId: string): Promise<void>;
  sendProgressUpdatesToUser(orderId: string, milestone: Milestone): Promise<void>;
}
```

### Database Schema Additions

#### Tables to Add/Modify
1. `multi_restaurant_orders` - Track multi-restaurant orders separately
2. `order_sub_orders` - Association table linking parent order to restaurant sub-orders
3. `delivery_sequences` - Store optimized pickup sequence and routing data
4. `restaurant_compatibility` - Store pre-computed compatibility scores
5. `multi_order_metrics` - Analytics and performance tracking

#### Key Constraints
- Transactional integrity: All sub-orders succeed or all fail
- Foreign key relationships for order hierarchy
- Indexing on: order_id, user_id, restaurant_id for fast lookups
- Partitioning by city and date for scalability

### API Specification

#### Create Multi-Restaurant Order
```
POST /api/v2/orders/multi-restaurant-order
Content-Type: application/json

{
  "user_id": "12345",
  "delivery_address": {
    "latitude": 28.6139,
    "longitude": 77.2090,
    "address": "123 Main St, Delhi"
  },
  "items": {
    "restaurant_a_id": [
      {"menu_item_id": "123", "quantity": 2, "special_requests": "No onions"},
      {"menu_item_id": "456", "quantity": 1}
    ],
    "restaurant_b_id": [
      {"menu_item_id": "789", "quantity": 3}
    ]
  },
  "payment_method": "credit_card",
  "promo_code": "MULTI50",
  "loyalty_redemption": 100
}

Response (201 Created):
{
  "order_id": "MRO-98765",
  "status": "confirmed",
  "restaurants": [
    {
      "restaurant_id": "restaurant_a_id",
      "sub_order_id": "ORD-98765-1",
      "status": "received",
      "estimated_preparation_time": 15
    },
    {
      "restaurant_id": "restaurant_b_id",
      "sub_order_id": "ORD-98765-2",
      "status": "received",
      "estimated_preparation_time": 12
    }
  ],
  "delivery_info": {
    "delivery_sequence": ["restaurant_b_id", "restaurant_a_id"],
    "estimated_delivery_time": "2026-04-05T14:55:00Z",
    "delivery_fee": 40
  },
  "billing": {
    "items_total": 400,
    "taxes": 68,
    "delivery_fee": 40,
    "discount": 50,
    "final_total": 458
  }
}
```

#### Track Multi-Restaurant Order
```
GET /api/v2/orders/MRO-98765/track

Response (200 OK):
{
  "order_id": "MRO-98765",
  "overall_status": "in_delivery",
  "delivery_location": {
    "latitude": 28.6200,
    "longitude": 77.2150,
    "address": "Current location"
  },
  "pickup_progress": {
    "total_pickups": 2,
    "completed_pickups": 1,
    "current_pickup": {
      "restaurant_id": "restaurant_a_id",
      "status": "in_progress",
      "estimated_pickup_time": "2026-04-05T14:25:00Z"
    }
  },
  "estimated_delivery_time": "2026-04-05T14:55:00Z",
  "delivery_partner": {
    "name": "Akshay K",
    "phone": "+91XXXXXXXXXX",
    "vehicle": "Two-wheeler",
    "rating": 4.8,
    "current_location": {...}
  },
  "notifications": [
    "Order confirmed at 14:00",
    "Pickup started at 14:10"
  ]
}
```

#### Validate Multi-Restaurant Feasibility
```
POST /api/v2/multi-restaurant/validate
Content-Type: application/json

{
  "restaurant_ids": ["rest_1", "rest_2", "rest_3"],
  "delivery_address": {...}
}

Response (200 OK):
{
  "is_feasible": true,
  "feasibility_score": 0.94,
  "reason": "All restaurants within delivery zone",
  "pickup_sequence": ["rest_2", "rest_3", "rest_1"],
  "estimated_total_time": 55,
  "compatibility_warnings": []
}
```

---

## Data Model

### Core Entity Relationships

```
User
├── Multi-Restaurant Orders (1:M)
│   ├── Order Sub-orders (1:M)
│   │   └── Restaurant (M:1)
│   ├── Delivery Assignment (1:1)
│   │   └── Delivery Partner (M:1)
│   └── Multi-Order Metrics (1:1)
├── Support Tickets (1:M)
└── Loyalty Points (1:1)

Restaurant
├── Sub-orders (1:M)
├── Compatibility Scores with other Restaurants (M:M)
├── Delivery Zone (M:1)
└── Performance Metrics (1:1)

Delivery Partner
├── Order Assignments (1:M)
└── Performance Metrics (1:1)
```

### Schema Design

#### multi_restaurant_orders Table
```sql
CREATE TABLE multi_restaurant_orders (
  id UUID PRIMARY KEY,
  order_id VARCHAR UNIQUE NOT NULL,
  user_id UUID NOT NULL REFERENCES users(id),
  status ENUM('pending', 'confirmed', 'preparing', 'ready', 'in_delivery', 'delivered', 'cancelled'),
  delivery_address JSONB NOT NULL,
  delivery_latitude DECIMAL(10, 8),
  delivery_longitude DECIMAL(11, 8),
  items_total DECIMAL(10, 2),
  taxes DECIMAL(10, 2),
  delivery_fee DECIMAL(10, 2),
  discount_amount DECIMAL(10, 2),
  total_amount DECIMAL(10, 2),
  payment_method VARCHAR,
  payment_status ENUM('pending', 'completed', 'failed', 'refunded'),
  promo_code VARCHAR,
  loyalty_redemption DECIMAL(10, 2),
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP,
  confirmed_at TIMESTAMP,
  delivered_at TIMESTAMP,
  city VARCHAR NOT NULL,
  INDEX idx_user_id (user_id),
  INDEX idx_status (status),
  INDEX idx_created_at (created_at),
  INDEX idx_city_created (city, created_at)
);
```

#### order_sub_orders Table
```sql
CREATE TABLE order_sub_orders (
  id UUID PRIMARY KEY,
  parent_order_id UUID NOT NULL REFERENCES multi_restaurant_orders(id),
  sub_order_id VARCHAR NOT NULL UNIQUE,
  restaurant_id UUID NOT NULL REFERENCES restaurants(id),
  status ENUM('pending', 'accepted', 'preparing', 'ready', 'picked_up', 'delivered', 'cancelled'),
  restaurant_subtotal DECIMAL(10, 2),
  restaurant_tax DECIMAL(10, 2),
  pickup_sequence INTEGER,
  estimated_pickup_time TIMESTAMP,
  actual_pickup_time TIMESTAMP,
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  INDEX idx_parent_order (parent_order_id),
  INDEX idx_restaurant (restaurant_id),
  FOREIGN KEY (parent_order_id) REFERENCES multi_restaurant_orders(id) ON DELETE CASCADE
);
```

#### delivery_sequences Table
```sql
CREATE TABLE delivery_sequences (
  id UUID PRIMARY KEY,
  order_id UUID NOT NULL REFERENCES multi_restaurant_orders(id) ON DELETE CASCADE,
  sequence_json JSONB NOT NULL,
  optimization_score DECIMAL(3, 2),
  total_distance_km DECIMAL(10, 2),
  estimated_delivery_minutes INTEGER,
  delivery_partner_id UUID REFERENCES delivery_partners(id),
  actual_completion_time TIMESTAMP,
  created_at TIMESTAMP,
  updated_at TIMESTAMP,
  INDEX idx_order_id (order_id)
);
```

#### restaurant_compatibility Table
```sql
CREATE TABLE restaurant_compatibility (
  id UUID PRIMARY KEY,
  restaurant_1_id UUID NOT NULL REFERENCES restaurants(id),
  restaurant_2_id UUID NOT NULL REFERENCES restaurants(id),
  same_delivery_zone BOOLEAN,
  average_distance_km DECIMAL(10, 2),
  co_order_frequency INTEGER,
  compatibility_score DECIMAL(3, 2),
  last_updated TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  UNIQUE KEY unique_restaurant_pair (restaurant_1_id, restaurant_2_id),
  INDEX idx_compat_score (compatibility_score DESC)
);
```

---

## Payment & Ordering Logic

### Multi-Restaurant Order Processing Flow

#### State Machine Diagram
```
┌─────────────────────────────────────────────────────┐
│  INITIATED                                          │
│  User adds items from multiple restaurants          │
└──────────────────┬──────────────────────────────────┘
                   │
                   │ User clicks Checkout
                   ▼
┌─────────────────────────────────────────────────────┐
│  FEASIBILITY_CHECK                                  │
│  Validate restaurants, delivery zone, timing        │
└──────────────────┬──────────────────────────────────┘
                   │
    ───────────────┼───────────────
    │              │              │
    │ PASS         │ FAIL         │ CONFLICT
    ▼              ▼              ▼
┌─────────┐  ┌─────────┐    ┌──────────────┐
│ PENDING │  │REJECTED │    │ CONFLICTED   │
└──────┬──┘  └─────────┘    │ (Ask user)   │
       │                     └──────┬───────┘
       │                           │
       │ User confirms payment  │ User resolves
       │                           │
       ▼                           ▼
┌─────────────────────────────────────────────────────┐
│  PAYMENT_PROCESSING                                 │
│  Charge single transaction, validate success        │
└──────────────────┬──────────────────────────────────┘
                   │
    ───────────────┼───────────────
    │              │              │
    │ SUCCESS      │ FAILED       │ PENDING
    ▼              ▼              ▼
┌─────────┐  ┌──────────┐  ┌──────────────┐
│CONFIRMED│  │ PAYMENT_ │  │ PAYMENT_     │
│         │  │ FAILED   │  │ PENDING_     │
└──────┬──┘  └──────────┘  │ VERIFICATION │
       │                    └──────┬───────┘
       │                     │ Retry
       │                     ▼
       │ Send to all restaurants
       │ Assign delivery partner
       ▼
┌─────────────────────────────────────────────────────┐
│  CONFIRMED                                          │
│  Order placed to all restaurants                    │
└──────────────────┬──────────────────────────────────┘
                   │
                   │ Restaurants accept
                   ▼
┌─────────────────────────────────────────────────────┐
│  PREPARING                                          │
│  Items being prepared at all restaurants            │
└──────────────────┬──────────────────────────────────┘
                   │
                   │ First pickup
                   ▼
┌─────────────────────────────────────────────────────┐
│  IN_PICKUP                                          │
│  Delivery partner collecting from restaurants       │
└──────────────────┬──────────────────────────────────┘
                   │
                   │ All pickups complete
                   ▼
┌─────────────────────────────────────────────────────┐
│  OUT_FOR_DELIVERY                                   │
│  Partner heading to delivery location               │
└──────────────────┬──────────────────────────────────┘
                   │
                   │ Order delivered
                   ▼
┌─────────────────────────────────────────────────────┐
│  DELIVERED                                          │
│  Order successfully delivered                       │
└─────────────────────────────────────────────────────┘
```

### Payment Processing

#### Transaction Flow
1. **Cart Validation:** All items checked for availability
2. **Billing Calculation:** Generate itemized bill
3. **Payment Authorization:** Authorize card for total amount
4. **Sub-Order Generation:** Create orders for each restaurant
5. **Delivery Assignment:** Find optimal delivery partner
6. **Confirmation Send:** Notify user, restaurants, partner
7. **Transaction Capture:** Capture authorized amount

#### Refund Policy
- **Full Refund:** If cancelled before restaurant accepts (eligible within 2 minutes)
- **Partial Refund:** If restaurant declines
  - Auto-refund that restaurant's amount
  - Re-optimize delivery fee based on remaining restaurants
  - Adjust total refund accordingly
- **Cancellation Charges:** After 10 minutes, applicable charges per Zomato policy
- **Dispute Refunds:** Handled via support team within 7 business days

#### Commission Distribution
```
Restaurant Commission Calculation:
  Restaurant A Commission = (Restaurant A Subtotal × Commission Rate) 
  Restaurant B Commission = (Restaurant B Subtotal × Commission Rate)
  Delivery Commission = (Delivery Fee × Delivery Partner Share)
  
Example:
  Restaurant A: ₹250 order × 30% = ₹75 to Zomato
  Restaurant B: ₹150 order × 30% = ₹45 to Zomato
  Delivery: ₹40 fee × 50% = ₹20 to Zomato
  Platform Revenue: ₹140 (but Delivery Partner gets ₹20)
```

### Promos & Loyalty Integration

#### Applicable Promotions
- Platform-wide promos: Apply to multi-restaurant orders
- First multi-restaurant order: Special bonus (₹100 off or 25% up to ₹150)
- Weekday multi-restaurant promo: -₹30 on orders 11 AM - 3 PM
- Restaurant-specific promos: Apply only to items from that restaurant
- **Stacking Rules:** Only one store-wide promo + one loyalty offer

#### Loyalty Points Calculation
```
Points Earned = (Order Value in INR - Delivery Fee - Discount) / 10
Points = (400 - 40 - 50) / 10 = 31 points earned

Redemption:
100 points = ₹100 off (floor redemption)
User can redeem any multiple of 100 points
```

---

## Restaurant & Logistics Integration

### Restaurant POS Integration

#### Order Sending Protocol
- Orders sent via API call to restaurant systems simultaneously
- Each restaurant receives its sub-order with linked order ID
- POS shows multi-restaurant order indicator
- Kitchen display shows estimated pickup time for delivery partner

#### Restaurant APIs
```
Restaurant receives webhook event:
Event: multi_restaurant_order.created
Payload: {
  "sub_order_id": "ORD-98765-1",
  "parent_order_id": "MRO-98765",
  "items": [...],
  "estimated_pickup_time": "2026-04-05T14:25:00Z",
  "special_instructions": "Door bell broken, call on arrival",
  "order_type": "multi_restaurant"
}

Restaurant confirms via: POST /api/orders/{sub_order_id}/accept
```

### Delivery Partner Experience

#### Multi-Stop Delivery Workflow
1. Partner receives order notification with multiple pickups
2. App shows optimized sequence with navigation
3. Partner navigates to first restaurant
4. Upon arrival, POS confirms delivery partner identity
5. Items packed and handed over
6. Partner marks first pickup complete
7. System provides navigation to second restaurant
8. Repeat process for remaining restaurants
9. After all pickups, navigation to delivery address
10. On delivery, confirm number of items received
11. Customer signs/confirms delivery

#### Delivery Partner Incentives
- Bonus for completing multi-restaurant orders (+₹20-30)
- Faster completion time due to optimized routes
- Higher earning per order due to larger amounts

### Logistics Optimization

#### Real-Time Route Re-optimization
- If first restaurant is delayed, system recalculates optimal sequence
- Notifies partner of updated sequence
- Predicts final delivery impact
- Escalates if delay exceeds 10 minutes

#### Delivery Partner Assignment
- Preference for experienced partners with high multi-order ratings
- Assignment based on current location and restaurant locations
- Load balancing to avoid partner saturation
- Real-time capacity check before assignment

#### Exceptional Handling
- Restaurant closure/cancellation: Auto-refund portion, adjust delivery fee
- Partner unavailability: Re-route to nearest available partner
- Customer location change: Recalculate if significant impact
- Item unavailability: Notify user immediately with options

---

## Legal & Compliance

### Regulatory Compliance

#### GST Compliance
- Each restaurant's items have separate HSN codes and GST rates
- Tax calculation per restaurant
- GST invoice generated showing restaurant-wise breakdown
- Reconciliation with GST portal monthly

#### Food Safety & Quality
- Each restaurant maintains food safety standards for their items
- Delivery coordination must not compromise food temperature/safety
- Multi-order packing guidelines to prevent cross-contamination
- Temperature monitoring for mixed food categories if applicable

#### Consumer Protection
- Right to reject items at delivery if unsuitable
- Cancellation policies clearly displayed before payment
- Clear refund terms for multi-restaurant cancellations
- Grievance redressal within 48 hours

#### Data Privacy
- GDPR compliance for international users
- Data minimization: Collect only necessary delivery/business info
- User consent for multi-restaurant tracking
- Right to erasure after transaction completion (30 days)

### Terms & Conditions Updates

#### User-Facing Policies
1. **Multi-Restaurant Order Cancellation:** Specify timing-based charges
2. **Refund Processing:** Explain processing time per payment method
3. **Disputes:** Process for escalation to Zomato support
4. **Liability:** Zomato liability for delivery failures
5. **Restaurant Liability:** Each restaurant liable for their items only

#### Restaurant Partner Policies
1. **Multi-Order Acceptance:** Mandatory acceptance/reject workflow
2. **Timely Preparation:** SLA for item readiness
3. **Packing Standards:** Guidelines for multi-restaurant orders
4. **Performance Metrics:** Tracking of acceptance rates, accuracy, etc.
5. **Commission Structure:** Clarity on deductions for issues

#### Delivery Partner Policies
1. **Route Compliance:** Must follow system-assigned routes
2. **Safety Standards:** Handling multiple bags/boxes
3. **Customer Interaction:** Communication protocol for multi-stops
4. **Performance:** On-time delivery metrics for multi-orders
5. **Incentives:** Bonus structure for multi-restaurant orders

---

## Dependencies & Risks

### Critical Dependencies

#### Internal Dependencies
- **POS Integration Team:** Needs to implement restaurant notification layer
- **Delivery Logistics Platform:** Requires routing optimization module
- **Payment Infrastructure:** Must handle split billing and multi-ledger accounting
- **Mobile/Web Engineering:** Needs to update cart and checkout UX
- **Analytics Platform:** Dashboard for multi-restaurant order insights

#### External Dependencies
- **Google Maps API:** Routing and distance calculation
- **Payment Gateway (Razorpay/PayU):** Multi-transaction handling
- **Restaurant POS Systems:** API compatibility for order receiving
- **Delivery Partner App:** Must support multi-stop functionality
- **SMS/Push Notification:** Carrier/FCM reliability

#### Third-Party Integrations
- **Geo-location Services:** For delivery zone validation
- **Weather API:** For delivery impact analysis
- **Traffic API:** For ETA prediction

### Key Risks & Mitigation

| Risk | Impact | Probability | Mitigation |
|------|--------|-------------|-----------|
| **Restaurant Rejection** | Sub-order fails for single restaurant | Medium | Fallback to complementary restaurant, auto-refund portion, user notification |
| **Delivery Partner Unavailability** | No partner to fulfill multi-order | Low-Medium | Queue for next available partner (max 10 min wait), auto-cancel if exceeds |
| **Route Optimization Engine Failure** | Suboptimal deliveries, customer dissatisfaction | Low | Fallback to heuristic routing, manual dispatch for high-value orders |
| **Payment Processing Failure** | Stranded order, customer complaint | Very Low | Implement retry logic, manual resolution for failed transactions, full refund |
| **Cross-Restaurant Latency Issues** | Degraded customer experience, longer delivery time | Medium | Multi-threaded restaurant notification, timeout policies, re-assignment |
| **Food Quality Issues** | Customer dissatisfaction due to food state | Medium | Strict packaging guidelines, thermal containers for temp-sensitive items, quality control checks |
| **Scale/Performance Issues** | System slowdown, cart errors during peak | Medium | Load testing before launch, auto-scaling infrastructure, queue management |
| **Regulatory Non-compliance** | Fines, platform suspension | Low | Legal review of terms, compliance with GST, food safety audit |
| **Cannibal Order Value** | Customers consolidate orders, reducing total orders | Medium | Monitor AOV impact, adjust pricing/incentives, multi-restaurant bundling strategy |
| **Delivery Economics Unfavorable** | Increased losses per multi-order due to costs | Medium | Price testing, commission adjustments, delivery partner incentive optimization |

### Risk Mitigation Strategies

#### Technical Risks
1. **Load Testing:** Simulate 10x peak traffic before launch
2. **Circuit Breakers:** Graceful degradation if restaurant systems down
3. **Fallback Strategies:** Default to single-restaurant if multi fails
4. **Monitoring:** Real-time alerts for critical service failures
5. **Disaster Recovery:** 1-hour RTO for order data recovery

#### Business Risks
1. **Pilot Program:** Launch in 2-3 cities first, measure impact
2. **Partner Incentives:** Align restaurant/delivery partner economics
3. **Cannibalization Analysis:** Track order volume and AOV impact weekly
4. **Customer Communication:** Clear set expectations on delivery times
5. **Competitive Monitoring:** Track competitor multi-restaurant features

#### Legal/Compliance Risks
1. **Pre-launch Audit:** GST, food safety, consumer protection review
2. **Documentation:** Clear policies documented and agreed by all parties
3. **Dispute Resolution:** Escalation matrix and timelines defined
4. **Insurance:** Adequate coverage for multi-order scenarios
5. **Regulatory Updates:** Quarterly review of applicable regulations

---

## Go-to-Market Strategy

### Market Positioning

#### Unique Value Proposition
"The fastest way to get what you're craving from your favorite restaurants."

#### Market Segmentation
1. **Core Target Users:**
   - Office professionals (lunch meetings, team orders)
   - Social event organizers
   - Budget-conscious students
   - Family dinner planners

2. **Secondary Targets:**
   - Restaurant partners seeking increased visibility
   - Delivery partners seeking higher earnings
   - B2B catering use cases

### Launch Strategy

#### Phase 1: Closed Beta (Month 1-2)
- 5,000 users in Bangalore
- Focus on product validation and edge case handling
- Feedback from early adopter cohorts
- Performance and stability testing

#### Phase 2: Open Beta (Month 2-3)
- Expand to Tier 1 cities: Delhi, Mumbai, Hyderabad, Pune
- 50,000 active users targeted
- Launch partner program for restaurants
- Delivery partner onboarding

#### Phase 3: General Availability (Month 3-4)
- Full launch in 4 Tier 1 cities
- Marketing campaign push
- Performance optimization and scaling
- Data-driven iteration

#### Phase 4: Expansion (Month 4-6)
- Roll out to Tier 2 cities
- Enhanced bundling and promotional features
- Restaurant partnership programs
- Loyalty integration

### Marketing & Communications

#### Paid Acquisition
- **Digital Marketing:** Google Ads, Instagram, Facebook (Target: ₹200/CAC)
- **In-App Promotion:** Banner on home screen, cart reminders
- **Email Campaigns:** Segmented messaging to different user cohorts
- **Influencer Partnerships:** Micro-influencers in food/lifestyle niche

#### Organic Growth
- **PR:** Press releases on platform expansion, user stories
- **Partnerships:** Co-marketing with restaurant chains
- **Referral Program:** Refer-a-friend bonus (₹200 to both)
- **Content Marketing:** Blog posts, food culture articles

#### Launch Campaign
- **Tagline:** "Order from multiple restaurants. Pay once. Delivered together."
- **Hero Visual:** Customer joy receiving multiple restaurant items in one delivery
- **Call to Action:** "Try now and save up to ₹100 on your first multi-restaurant order"
- **Timeline:** 2-week pre-launch buzz, 1-week heavy launch push

### Channel Strategy

| Channel | Target | Timeline | Investment |
|---------|--------|----------|-----------|
| In-App Discovery | Existing users | Week 1 | Low (engineering) |
| Email Marketing | Segmented cohorts | Week 1-2 | Low |
| Paid Social (Instagram) | 25-40 demographic | Week 2-4 | ₹50L |
| Google Ads | High-intent searchers | Ongoing | ₹75L |
| Playstore Feature | App discovery | Week 1-2 | Negotiated |
| Influencer Partnerships | Young professionals | Week 3-4 | ₹30L |
| PR & Media | Brand awareness | Ongoing | Internal |

### Pricing & Incentives Strategy

#### Launch Promotions
- **First Order:** ₹100 off multi-restaurant orders (min. ₹200)
- **Week 1-2:** 25% off delivery fee for multi-restaurant orders (max discount ₹50)
- **Referral Bonus:** ₹200 credit on referring 3 friends
- **Loyalty Boost:** 2x points on multi-restaurant orders (first month)

#### Long-term Incentives
- **Bundle Discounts:** "Save more with more"
  - 2 restaurants: ₹20 off
  - 3 restaurants: ₹40 off
  - 4+ restaurants: ₹60 off
- **Weekday Specials:** Mid-week promo (₹30 off Tue-Thu for lunch orders)
- **Loyalty Tiers:** Higher discounts for Pro members

### Partnership Programs

#### Restaurant Partner Program
- **Purpose:** Increase visibility through multi-restaurant bundles
- **Incentives:** 
  - Featured placement in "Suggested Pairing" sections
  - Co-marketing support
  - Reduced commission on multi-orders (1% reduction)
- **Requirements:**
  - Accept multi-restaurant orders
  - Maintain <5 min avg. preparation time
  - Quality rating ≥4.3 stars

#### Delivery Partner Incentives
- Bonus per multi-restaurant order: ₹30
- Incentive for high on-time rate (≥90%): Gets preferred assignment
- Performance-based rankings and leaderboards
- Recognition and rewards for top performers

---

## Timeline & Roadmap

### Development Roadmap

#### Phase 1: MVP (April - June 2026)
**Goals:** Core multi-restaurant ordering functionality
- Week 1-2: Design finalization, engineering kickoff
- Week 3-6: Backend services development
  - Cart service multi-restaurant support
  - Order orchestration service
  - Routing optimization module (basic TSP)
- Week 7-10: Frontend development
  - Mobile app cart redesign
  - Checkout UX updates
  - Order tracking page
- Week 11-12: Integration & Testing
  - End-to-end testing
  - POS system integration
  - Performance benchmarking
- Week 13-14: Beta launch in Bangalore

#### Phase 2: Expansion & Optimization (July - September 2026)
**Goals:** Scale to all Tier 1 cities, optimize economics
- Week 1-2: Tier 1 expansion (Delhi, Mumbai, Hyderabad, Pune)
- Week 3-4: Performance optimization & scaling
- Week 5-6: Advanced routing (ML-based ETA predictions)
- Week 7-8: Bundle recommendations engine
- Week 9-10: Restaurant analytics dashboard
- Week 11-12: Loyalty integration enhancements

#### Phase 3: Enhanced Features (Oct - Dec 2026)
**Goals:** Advanced functionality and differentiation
- Week 1-2: Scheduled/advance orders
- Week 3-4: Multi-restaurant loyalty bundles
- Week 5-6: B2B ordering integration
- Week 7-8: Subscription bundles (e.g., Daily combos from multiple restaurants)
- Week 9-10: Search/filtering enhancements for multi-restaurant discovery
- Week 11-12: Analytics and insights features

### Resource Allocation

#### Engineering Team Structure (14-16 people)
- **Backend Lead (2):** Order orchestration, routing optimization
- **Frontend Lead (2):** Mobile and web UI/UX
- **QA Lead (2):** Testing automation and manual testing
- **DevOps/SRE (1):** Infrastructure, scaling, monitoring
- **Integration Engineer (1):** POS and external system integrations
- **Analytics Engineer (1):** Data pipeline, metrics tracking
- **Product Engineer (1):** Feature flags, experimentation

#### Other Teams
- **Product:** 1 dedicated PM + 1 Product Analyst
- **Design:** 1 Lead Designer + 1 UI/UX Designer
- **Data Science:** 1 for routing and recommendations
- **Legal/Compliance:** 0.5 (shared with org)

#### Timeline Estimates (in engineer-weeks)
- Backend: 40 engineer-weeks
- Frontend: 32 engineer-weeks
- QA: 24 engineer-weeks
- DevOps: 12 engineer-weeks
- Integration: 16 engineer-weeks
- Data/Analytics: 8 engineer-weeks
- **Total: 132 engineer-weeks (~6-8 months for team of 4-5 FTE backend, 3-4 FTE frontend)**

### Critical Path

```
Project Initialization
    └─> Backend Infrastructure Setup (Weeks 1-2)
        └─> Core Service Development (Weeks 3-8)
            ├─> Cart Service Multi-Restaurant
            ├─> Order Orchestration Service
            ├─> Routing Engine
            └─> Payment Integration
                └─> Frontend Development (Weeks 7-12 parallel)
                    ├─> Cart UI Redesign
                    ├─> Checkout Flow
                    └─> Order Tracking
                        └─> POS Integration (Weeks 9-11)
                            └─> QA & Testing (Weeks 10-14)
                                └─> Beta Launch (Week 14-15)
                                    └─> Production Launch (Week 16+)
```

### Milestone Checklist

| Milestone | Target Date | Status |
|-----------|------------|--------|
| Design Finalization | Week 2, May | Pending |
| Backend Development Complete | Week 8, June | Pending |
| Frontend Development Complete | Week 12, July | Pending |
| Integration Testing Pass (80% scenarios) | Week 13, July | Pending |
| Beta Launch (Bangalore) | Week 14, July | Pending |
| GA Launch (4 Tier-1 cities) | Week 20, September | Pending |
| Tier 2 Expansion | Week 24, October | Pending |

---

## Success Metrics & Analytics

### Business Metrics

#### Primary Metrics

| Metric | Q3 2026 Target | Q4 2026 Target | Measurement |
|--------|----------------|----------------|------------|
| **Multi-Restaurant Order Penetration** | 2-3% of food orders | 8% of food orders | Order database daily count |
| **Monthly Active Users (Multi-feature)** | 1M | 3M | Product analytics |
| **Average Order Value Uplift** | +25% | +35% | Order analytics |
| **Customer Lifetime Value** | +18% vs control | +25% vs control | Cohort analysis |
| **Revenue Impact** | +8% in pilot cities | +5-7% platform-wide | Revenue reporting |

#### Secondary Metrics

| Metric | Target | Notes |
|--------|--------|-------|
| **Delivery Cost Per Order** | -22% vs single order | Optimize routing efficiency |
| **On-Time Delivery Rate** | 85% | Higher than single-order baseline (78%) |
| **Customer Satisfaction (CSAT)** | 4.5/5 | Post-order survey |
| **Feature Retention Rate (30-day)** | 40% | Repeat usage tracking |
| **Repeat Order Rate (Multi only)** | 35% | Users who order multi 2+ times |
| **Support Ticket Reduction** | -15% for multi orders | Fewer coordination issues |

### Operational Metrics

#### Restaurant Partner Metrics
- **Order Acceptance Rate:** Target 95% (multi-orders)
- **Preparation Time Compliance:** <5min average
- **Quality Rating:** Maintain ≥4.3 stars
- **Partner Satisfaction (NPS):** ≥45

#### Delivery Partner Metrics
- **On-Time Delivery:** ≥85%
- **Pickup Accuracy:** 99%+ (all items collected)
- **Customer Rating:** ≥4.6/5 for multi-orders
- **Earnings per delivery:** +40% vs single orders

### Cohort Analysis Plan

#### User Cohorts to Track
1. **By Adoption Date:** Cohort retention by week of first adoption
2. **By Demographic:** Age, location, income level
3. **By Usage Pattern:** Heavy vs. light users of feature
4. **By Order Type:** Office orders vs. personal vs. events
5. **By Restaurant Count:** 2-restaurant orders vs. 3+ restaurants

#### Funnel Metrics
```
App Opens (100%)
    ├─> View Multi-Restaurant Feature (85%)
    ├─> Add from 2+ Restaurants (35%)
    ├─> Proceed to Checkout (25%)
    ├─> Complete Payment (22%)
    └─> Order Placed Successfully (20%)
```

### A/B Testing Plan

#### Test 1: Incentive Level Impact (Week 1-4)
- Control: Standard ₹100 off first order
- Variant A: ₹150 off first order
- Variant B: 25% off (up to ₹200)
- Metric: Conversion rate, AOV, LTV

#### Test 2: Feature Discoverability (Week 5-8)
- Control: Standard in-app button
- Variant A: Prominent banner on home
- Variant B: In-cart suggestion after first restaurant
- Metric: Feature penetration rate, adoption rate

#### Test 3: Surge Pricing Impact (Week 9-12)
- Control: 1.0x surge multiplier
- Variant A: 0.8x surge multiplier for multi-orders
- Variant B: No surge for multi-orders
- Metric: Conversion during peak hours, GMV

### Analytics Dashboard

#### Real-time Dashboard (Hourly)
- Multi-restaurant orders placed this hour
- Active users in multi-checkout flow
- Delivery partners with pending multi-orders
- Support tickets (multi-restaurant related)

#### Daily Dashboard
- Total multi-restaurant orders
- Revenue from multi-restaurant orders
- CSAT scores and ratings
- On-time delivery percentage
- Restaurants accepting/declining orders

#### Weekly Dashboard
- Repeat user rate (multi-feature)
- Cohort retention curves
- Average order value trends
- Geographic penetration
- Top restaurant pairings

#### Monthly Dashboard
- MAU growth and trends
- LTV/CAC analysis for multi-users
- Feature retention rates
- Competitive benchmarking
- Profitability analysis

---

## Appendices

### Appendix A: Glossary of Terms

| Term | Definition |
|------|-----------|
| **Multi-Restaurant Order** | Single order transaction containing items from 2+ restaurants with unified checkout and coordinated delivery |
| **Sub-Order** | Individual order portion sent to each restaurant within a multi-restaurant order |
| **Order ID** | Unique identifier for multi-restaurant order (e.g., MRO-98765) |
| **Delivery Zone** | Geographic area served by restaurant for delivery |
| **Routing Optimization** | Algorithm to determine optimal delivery pickup sequence |
| **ETA** | Estimated Time of Arrival for delivery |
| **SLA** | Service Level Agreement for delivery time targets |
| **CSAT** | Customer Satisfaction score (1-5 scale) |
| **AOV** | Average Order Value per transaction |
| **CAC** | Customer Acquisition Cost |
| **LTV** | Lifetime Value of a customer |
| **NPS** | Net Promoter Score for satisfaction |
| **POS** | Point of Sale system used by restaurants |
| **FCM** | Firebase Cloud Messaging for push notifications |

### Appendix B: User Quote from Research

> "I love Zomato, but having to place separate orders to multiple restaurants and track different delivery times is frustrating. If I could order my biryani from Restaurant A and dessert from Restaurant B in a single transaction, it would be so much better." — Priya, 27, Marketing Professional, Delhi

> "For office team lunches, I need to order from 3-4 different restaurants to satisfy everyone's preferences. The logistics of managing 4 separate deliveries is a nightmare. A single consolidated order would save us so much time." — Rajesh, 35, Project Manager, Mumbai

### Appendix C: Competitive Analysis

| Feature | Zomato (Current) | Uber Eats | DoorDash | **Zomato (Proposed)** |
|---------|------------------|-----------|----------|---------------------|
| Multi-Restaurant Ordering | ✗ | ✓ | ✓ | ✓ |
| Unified Checkout | ✗ | ✓ | ✓ | ✓ |
| Coordinated Delivery | ✗ | ✓ (limited) | ✓ | ✓ (optimized) |
| Smart Bundling | ✗ | ✓ | ✗ | ✓ |
| Loyalty Integration | ✓ | ✗ | ✗ | ✓ |
| Delivery Cost Advantage | ✓ (single orders) | ~ | ~ | ✓ (multi orders) |

### Appendix D: Technical Stack Recommendation

- **Language:** TypeScript/Node.js (consistent with existing)
- **Database:** PostgreSQL (OLTP) + Redis (caching)
- **API Framework:** Express.js or NestJS
- **Mobile:** React Native / Native (iOS/Android)
- **Routing Engine:** OR-Tools (Google) or Vroom
- **Messaging:** Kafka for inter-service communication
- **Monitoring:** DataDog or New Relic
- **CI/CD:** GitHub Actions or Jenkins
- **Cloud:** AWS or GCP (same as existing)

### Appendix E: Regulatory & Tax Compliance Checklist

- [ ] GST calculation per restaurant item
- [ ] Tax invoice generation with restaurant-wise breakdown
- [ ] Food Safety compliance review (state/central)
- [ ] Consumer Protection Act compliance
- [ ] GDPR compliance for international users
- [ ] Data residency requirements compliance
- [ ] Refund and cancellation policy legal review
- [ ] Terms and Conditions update
- [ ] Privacy Policy update
- [ ] Delivery partner agreement addendum
- [ ] Restaurant partner agreement addendum

### Appendix F: Sample Wireframes (Text Description)

#### Wireframe 1: Multi-Restaurant Cart
```
┌─────────────────────────────────────┐
│ 🏠 Multi-Restaurant Cart     🛒 (3) │
├─────────────────────────────────────┤
│                                     │
│ 🍔 Burger Palace              ✖️   │
│ ├─ Cheese Burger (x2)   ₹250      │
│ ├─ Fries                ₹100       │
│ └─ Subtotal              ₹350      │
│                                     │
│ 🍕 Pizzeria Primo               ✖️  │
│ ├─ Margherita Pizza (x1) ₹200     │
│ └─ Subtotal              ₹200      │
│                                     │
│ ═══════════════════════════════════ │
│ Delivery Fee        ₹40             │
│ Taxes               ₹74             │
│ ═══════════════════════════════════ │
│ TOTAL              ₹664             │
│                                     │
│ [+ Add from another Restaurant]    │
│                                     │
│ ┌─────────────────────────────────┐ │
│ │    PROCEED TO CHECKOUT          │ │
│ └─────────────────────────────────┘ │
└─────────────────────────────────────┘
```

#### Wireframe 2: Multi-Restaurant Order Tracking
```
┌──────────────────────────────────────┐
│ Order MRO-98765              14:30   │
├──────────────────────────────────────┤
│                                      │
│ ✓ CONFIRMED ──→ PREPARING           │
│             →  IN DELIVERY           │
│                      ↓               │
│  Arriving in ~15 minutes             │
│                                      │
├──────────────────────────────────────┤
│ 🍔 Burger Palace     Pickup: 14:10  │
│ ├─ Cheese Burger (x2)               │
│ ├─ Fries                            │
│ └─ Status: ✓ Ready for pickup        │
│                                      │
│ 🍕 Pizzeria Primo    Pickup: 14:22  │
│ ├─ Margherita Pizza                 │
│ └─ Status: 🕐 10 minutes             │
│                                      │
├──────────────────────────────────────┤
│ Delivery Partner:                   │
│ 👤 Akshay K       ⭐ 4.8 (250+ trips)│
│ 🏍️ Two-wheeler                      │
│ 📞 Call      💬 Chat                │
│                                      │
│ [Map showing delivery route]        │
│                                      │
│ Problem with order?  📞 Support     │
└──────────────────────────────────────┘
```

### Appendix G: Success Criteria & Go/No-Go Decision Points

#### Week 8 (Beta Launch Readiness)
- [ ] Backend services load test ≥5K concurrent users
- [ ] E2E test pass rate ≥95%
- [ ] POS integration with 3+ restaurant partners successful
- [ ] Order processing latency <2 seconds (p95)
- [ ] Security audit completed with 0 critical issues

#### Week 14 (GA Launch Readiness)
- [ ] 10K+ beta users with ≥15% multi-order adoption
- [ ] CSAT score ≥4.3/5
- [ ] On-time delivery ≥80%
- [ ] Support ticket volume <5% of total
- [ ] Economics positive (unit economics ≥15% margin)

### Appendix H: Post-Launch Monitoring Plan

#### First Week Monitoring
- Monitor system stability and error rates (target: <0.1%)
- Track customer support volume and issue types
- Verify payment success rates (target: >99.5%)
- Monitor delivery completion rates (target: ≥85%)
- Track restaurant acceptance rates (target: ≥90%)

#### First Month Reviews
- Weekly business review on key metrics
- Qualitative feedback from users and partners
- Competitive monitoring
- Data quality and analytics validation
- Plan iterations and fixes

#### Ongoing Optimization
- A/B testing of incentives and UX improvements
- Continuous performance optimization
- Feature enhancements based on user feedback
- Expansion roadmap planning

---

## Document Sign-off

| Role | Name | Date | Signature |
|------|------|------|-----------|
| Product Manager | [PM Name] | [Date] | [Sign] |
| Engineering Lead | [Eng Lead] | [Date] | [Sign] |
| Design Lead | [Design Lead] | [Date] | [Sign] |
| Legal/Compliance | [Legal Name] | [Date] | [Sign] |
| Leadership Approval | [CXO Name] | [Date] | [Sign] |

---

## Revision History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | April 5, 2026 | Product Team | Initial draft for review |
| 1.1 | [TBD] | [TBD] | Feedback incorporation |

---

**END OF DOCUMENT**

*For questions or feedback on this PRD, please contact the Product Management team.*
