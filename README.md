# laravel-api-passport
Starter Kit for Laravel api and passport

Fork and Clone the Repository

    Click "Fork" on GitHub, then clone your forked repository locally:

    bash

    git clone https://github.com/your-username/your-repo.git
    cd your-repo

Install Dependencies

    Run Composer and NPM to install PHP and frontend dependencies:

    bash

    composer install
    npm install

Environment Setup

    Copy .env.example to .env and set up your environment variables:

    bash

cp .env.example .env

Generate an application key:

bash

    php artisan key:generate

Database Setup

    Create a database and update the .env file with your database credentials.
    Run migrations to create the necessary tables:

    bash

    php artisan migrate

Install Passport

    Run the Passport install command to create encryption keys and clients:

    bash

    php artisan passport:install

Run the Application

    Start the development server:

    bash

    #Incase you are having issue to generate personal token on production server 
    If the list doesn’t show a personal access client, create one by running:
    php artisan passport:client --personal
This will prompt you to fill in details for creating a personal access client and should generate the necessary id and secret.

    php artisan serve

Using the API

    Obtain an access token by hitting the /oauth/token endpoint with the required client credentials.
    Use the token in your requests with an Authorization: Bearer {access_token} header.
