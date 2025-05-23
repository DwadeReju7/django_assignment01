(DJANGO Assignment 01)
My application domain was meant to capture necessary data for an e-commerce website. For this site I wanted to capture the necessary information and created 5 tables. These tables included Categories, Customers, Order_Items, Orders and Products. 

In  order to set up the project I had to first start a virtual environment. To do that i typed python3 -m venv venv. After that I typed in source venv/bin/activate. After that I pip installed django so it would be available in our virtual environment. It was very important to include all the information including " pip install django~=5.2 "psycopg[binary]" django-environ " this caused an issue for us later. In regards to installing requirements I didn't do this until the end but I had to run "pip freeze > requirements.txt ". 

To create an .env file to include in my overall folder. In regards to the credntials before testing this on my local environment I had my actual credentials. For the purpose of submitted this assignment as directed at the end, I replaced it with example data. 

Running migrations took me the longest time because I kept running into errors. This included making edits on my settings.py and ensuring that myapp was in the correct directory. After creating the migration using " PS > python3 manage.py makemigrations myapp " I then ran " PS> python manage.py migrate ". Afterwards we ran python3 manage.py createsuperuser where we were prompted to create a username and password. After confirming that we would run the server using " PS> $ python manage.py runserver` "

(DJANGO Assignment 02)
I choose to implement CRUD from my 'Products Model'. This is inclusive of name, price and category.

Myapp url was used for creating url patterns that would assist me with switching from one html document to another. 

In regards to implementing CRUD operations. C stands for Create, this is the process of creating new products to add to our e-commerce site. This is implemented directly into the browser with the information presented in urls.py. R stands for Read which is meant to view existing data that we already have set. Read can be connected to both our detail view as well as our list view to look at certain information that is already available. U stands for update which gives us a way of updating information directly to adding a new product to the table. For this we would put the integer thats tied to the product and then update. D stands for delete which gives us a way of deleting current information. 

(DJANGO Assignment 03)
With adding Google Authentication to the project. The firsts step was to go to the Gogle Cloud Console and create a new project. Through navigating those steps we were given the proper credentials to add to our .env file to store them securely. This information included a 'Client ID' as well as a 'Client Secret'. Afterwards we had to alter our settings.py with adding a dictionary entitled SOCIALACCOUNT_PROVIDERS. We would have to do this for every Auth based provider. 

In order to test login we ran our command "python3 manage.py runserver" upon getting our http link the first thing we did was add '/accounts/' to the link which took us to the sign in page. The immediate difference I noticed was the additional "Or use a third party" option that appeared with Google hyperlinked. I first focused on logging in locally to ensure I had the proper credentials. Funny enough I forgot my password but was able to login to my admin account and change my password directly there. I used the link for the Google Auth and was amazed how this looked the exact same as the process with well established sites. 

Permission restrictions on update/delete views were completed by adding UserPassesTextMixin so while I am logged in, every product I view in my inventory has update and delete options. 
