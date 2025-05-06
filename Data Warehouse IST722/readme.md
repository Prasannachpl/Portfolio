# FEC Campaign Finance Data Warehouse

## Project Overview
This project implements a comprehensive data warehouse for Federal Election Commission (FEC) campaign finance data. It leverages dbt (data build tool) to transform raw FEC data into structured, analytics-ready tables that can be used for campaign finance analysis and reporting.

## Data Architecture

### Dimensional Model
This project follows a star schema dimensional model with:

- *Fact Tables*:
  - fact_individual_contributions - Contains contribution transactions from individuals to committees

- *Dimension Tables*:
  - dim_candidate - Candidate information
  - dim_committie - Committee details
  - dim_contributors - Individual contributor information
  - dim_transactiontypes - Transaction type classifications
  - dim_state - State reference data
  - ref_reporttypes - Report type reference data

### Analytics Layer
The individual_contributions model serves as a denormalized view that combines fact and dimension data into a comprehensive table optimized for analytics and dashboarding.

## Key Components

### Dashboard View
The individual_contributions model joins relevant dimension tables to the fact table to provide a complete view of campaign contributions including:

- Contribution details (amount, transaction ID)
- Committee information (name, party, designation)
- Candidate details (name, office, district)
- Contributor information (name, location, employer, occupation)
- Transaction metadata (report type, transaction type)

### Implementation Details

1. *dbt Models*: Written in SQL and configured with dbt-specific parameters
2. *YAML Definitions*: Document table schemas, column descriptions, and relationships
3. *Materialization Strategy*: Implemented as a table for optimized query performance

## Usage

### Querying the Data
Analysts can query the individual_contributions model to answer questions such as:

- What is the distribution of contribution amounts by party?
- Which states contribute the most to specific candidates?
- How do contribution patterns change across election cycles?
- What occupations or employers are most represented in campaign financing?

### Technical Components

- *Database*: Snowflake
- *Schema*: DBT_AYUSHSASEENDRAN_FEC
- *Framework*: dbt (data build tool)

## Project Structure


Data Warehouse IST722/
├── dashboard_view.sql      # SQL model for the analytics layer
├── dashboard_view.yml      # YAML definitions for the model
└── README.md               # Project documentation


## Development

The models are developed using dbt, which allows for:

- Version control of SQL transformations
- Testing and documentation of data models
- Dependency management between tables
- Incremental loading patterns
- Environment-specific configurations

## Contributors
- Prasanna Lakshmi Chelliboyina
- Ayush Thoniparambil Saseendran
- Vedant Kadam
- Akshay D
