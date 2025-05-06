# Online Recipe Sharing Platform Database

## Project Overview
This SQL project implements a database system for an Online Recipe Sharing Platform. The database is designed to store and manage recipes, ingredients, cooking steps, user reviews, and cuisine categories.

## Database Structure
The database consists of the following tables:

- *Ingredients*: Stores ingredient information
- *Recipes*: Contains recipe details including name, preparation time, and difficulty level
- *Cuisines*: Holds different cuisine types
- *RecipeCuisines*: Junction table linking recipes to cuisines
- *Users*: Stores user information
- *Reviews*: Contains user reviews and ratings for recipes
- *CookingSteps*: Details the step-by-step cooking instructions for recipes

## Key Views
- *RecipeDetails*: Combines recipe information with ingredients and cooking steps
- *TopRatedRecipes*: Shows recipes with their average ratings and review counts

## Stored Procedures
1. *RecipesWithHighestRating*
   - Returns the top N recipes by average rating
   - Parameters: @TopN (number of recipes to return)

2. *AverageRating*
   - Calculates the running average rating for a specific recipe over time
   - Parameters: @recipeID (the recipe to analyze)
   - Returns: Review details and the running average rating ordered by review time

## Sample Queries
sql
-- Get top 10 highest-rated recipes
EXEC RecipesWithHighestRating @TopN = 10;

-- Get the running average rating for a specific recipe
EXEC AverageRating @recipeID = 1;


## Data Sample
The database includes sample data for:
- 65 ingredients
- 14 cuisine types
- 50 recipes
- 50 users
- Multiple cooking steps per recipe
- 50 reviews with ratings and timestamps

## Setup Instructions
1. Run the script to create the database and its objects
2. The script handles cleanup of existing objects before creating new ones
3. Sample data is automatically loaded into all tables
4. Views and stored procedures are ready to use immediately after running the script

## Contributors
- Prasanna Lakshmi Chelliboyina
- Ayush Thoniparambil Saseendran
- Greeshma Pothineni
