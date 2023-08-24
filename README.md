# DBS211GroupProjectSummer2023
MEMBERS:                                                                                                                         
SAKSHI SAKSHI
NIYATIBEN PATEL

Database Design for Travel Management System

Introduction

The tourism industry is a rapidly growing sector nowadays. It mostly relates to creating a seamless travel experience for people. We chose this industry because as travel enthusiasts, we know the importance of efficient trip planning and organization. That’s why, we have chosen this industry for our project.

Problem Statement: 

When it comes to trip planning, the main problem faced by most travelers is to find both economical and memorable trips. Also, some travelers face challenges in organizing their itineraries, obtaining trustworthy facts about destinations, and organizing a stay. A dedicated trip planner database is needed to address these issues and provide a holistic solution for travelers. Solution: A database is essential for trip planning as it streamlines the process, enables collaboration between travel agents and customers, and ensures accurate and up-to-date information. Thus, this database centralizes trip details, making it easily access and reference them for future trips.• Provide options for users to add, remove, and organize their favorites easier to track and manage all aspects of the trip, resulting in a smoother and more efficient planning and execution experience for all travellers. 

Requirements: 
1.	User Registration and Authentication:
• Allow users to create accounts and securely log in to the trip planningapplication.• Store user information such as username, password, and contact details in the database.• Enable authentication mechanisms to ensure secure access to user-specific trip data.

2.	Favorites:
• Implement a feature that allows users to save favorite destinations, accommodations, or activities.• Store the user's favorite choices in the database, enabling them to within the application.

3.	Trip Budget and Expense Tracking:
• Enable users to set budgets for their trips and track expenses within the application.• Store budget details and track actual expenses in the database for each trip.• Generate reports or visualizations based on budget allocations and actual spending for better financial management. 

4.	Trip Creation and Management:
• Ability to create and manage multiple trips with details such as destination, dates, and budget.• Itinerary builder to add activities, attractions, restaurants, and accommodations to the trip schedule.

5.	Destination Information:
• Comprehensive database of destinations with details on points of interest, attractions, local customs, and safety guidelines.• Real-time weather information for selected destinations.• User-generated reviews and ratings for destinations, accommodations, restaurants, and activities.
6.	Reporting and Decision-making (Data reports to provide information for informed business decisions):
• Revenue generated from bookings.• Inventory levels for accommodations and transportation.• User feedback and satisfaction ratings.

The Travel Management System is a database designed to facilitate travel-related activities, including managing traveler information, hotel bookings, destinations, and accounts. The database schema has undergone several updates and changes based on feedback and iterative improvements.

Tables and Entities

The database consists of the following tables and their corresponding entities:
Travellors: This table stores information about travelers, including their passport number, first name, last name, age, phone number, email, and address.
Account: The Account table contains details of user accounts, such as account number, user ID, password, account balance, account type, and the associated traveler's passport number.
Country: The Country table holds information about countries, including a unique country ID, country name, country code, country location, and the passport number of a traveler associated with the country.
City: This table stores details about cities, such as city ID, city name, and the corresponding country ID where the city is located.
Hotel: The Hotel table contains information about hotels, including hotel ID, city ID, hotel address, details, hotel name, email, active status, and the associated country ID.
Room: This table stores data about hotel rooms, including room number, room type, city ID, service price, active status, and the traveler's passport number associated with the room.
Destination: The Destination table contains details of travel destinations, including destination ID, destination name, description, a flag indicating if it's a favorite destination, traveler's passport number, and the corresponding country ID.
TravellorDestinations: This bridge table establishes a many-to-many relationship between travelers and destinations, storing the traveler's passport number and destination ID.
CountryCities: The CountryCities bridge table establishes a many-to-many relationship between countries and cities, storing the country ID and city ID.

Constraints

Throughout the design process, constraints have been added and updated to ensure data integrity:
The Travellors table now includes a CHECK constraint on the Age column to ensure the age is between 1 and 200.
The Account table has a CHECK constraint on the AccountType column to limit it to specific values ('B', 'S', 'G').
The Country table includes a CHECK constraint on the CountryID column to ensure it falls within a valid range (1 to 50).
The Hotel table now includes a CHECK constraint on the Active column to limit it to 'YES' = 1 or 'NO' = 0.

Views Added

Based on the feedback and requirements, we have added the following views:
TravellorAccounts: This view lists traveler account details, including first name, last name, account number, and account type.
TravellorsByCountry: This view provides a count of travelers in each country.
TravellorDestinationView: This view combines information from the 
TravellorDestinations and Travellors tables to show travelers and their associated destinations.
FavouriteDestinations: This view displays favorite destinations along with the travelers' first and last names.

Conclusion

The Travel Management System database design has undergone several improvements based on feedback and iterative enhancements. The database now incorporates essential constraints and updated views to support travel-related operations effectively.
