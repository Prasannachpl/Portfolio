# Travel Management Database System

## Overview
This project implements a comprehensive database system for a travel management application. The system is designed to handle various aspects of travel management including customer information, destinations, accommodations, flights, activities, packages, bookings, reviews, and payments.

## Project Structure
The project consists of the following components:

1. *Conceptual Model*: A visual representation of the database entities and their relationships.
2. *Logical ERD*: A detailed entity-relationship diagram showing tables, attributes, and relationships.
3. *Up-Down Script*: A SQL script that handles both the creation (up) and deletion (down) of the database structure.

## Database Design

### Key Entities
- *Customers*: Stores information about customers including contact details and address information.
- *Destinations*: Contains data about travel destinations with descriptions and locations.
- *Places in Destination*: Records notable places within each destination.
- *Accommodations*: Tracks lodging options at various destinations.
- *Flights*: Stores flight information including schedules and pricing.
- *Activities*: Contains information about activities available at destinations.
- *Packages*: Pre-configured combinations of destinations, accommodations, flights, and activities.
- *Bookings*: Records customer reservations for travel services.
- *Reviews*: Stores customer feedback on different aspects of their travel experience.
- *Payments*: Tracks payment transactions related to bookings.

### Relationships
The database is designed with various relationships between entities:
- Customers can book multiple destinations and leave multiple reviews
- Destinations contain multiple places of interest, accommodations, flights, and activities
- Packages combine destinations with specific accommodations, flights, and activities
- Bookings link customers with destinations and optionally with specific services
- Reviews are associated with customers and can reference specific travel components

## Implementation

### Technologies Used
- Microsoft SQL Server
- T-SQL

### Database Creation Script
The script supports both the creation and deletion of the database structure, including:
- Tables with appropriate data types and constraints
- Primary and foreign key relationships
- Check constraints for data validation
- Indexes for performance optimization
- Sample data insertion for testing

### Example Queries
The database supports various types of queries such as:
- Finding available accommodations at a destination
- Retrieving package details with all included components
- Listing customer bookings and their status
- Analyzing customer reviews for specific services
- Tracking payment information for bookings

## Testing
The database implementation includes sample data insertion statements to test the functionality of the database structure and relationships.

## Usage
To use this database system:

1. Execute the up-down script to create the database structure
2. Insert your data or use the provided sample data
3. Create appropriate views, stored procedures, or application connections to interact with the data

## Future Improvements
Potential enhancements include:
- Additional views for common reporting needs
- Stored procedures for complex operations
- Triggers for data integrity and event logging
- Performance optimizations for large datasets

## Contributors
- Prasanna Lakshmi Chelliboyina
- Ayush Thoniparambil Saseendran
- Apoorva M
