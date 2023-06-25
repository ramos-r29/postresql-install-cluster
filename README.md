# postresql-install-cluster
# Installation PostgreSQL on Linux 

<p>Step 1: Add repository to the list of package sources :</p>
<p>sudo sh -c 'echo "deb http://apt.postgresql.org/pub/repos/apt $(lsb_release -cs)-pgdg main" > /etc/apt/sources.list.d/pgdg.list'</p>

<p>Step 2 : Download the PostgreSQL repository's :</p>
<p>wget --quiet -O - https://www.postgresql.org/media/keys/ACCC4CF8.asc | sudo apt-key add - </p>

<p>Step 3: Update package repositories: </p> 
<p>sudo apt-get update </p>

<p>Step 4: Install PostgreSQL:  </p>
<p>sudo apt-get -y install postgresql v
       
# Cluster Creation and Server Startup 

<p>Step 5:  Create directory for data: </p>
<p>sudo mkdir -p /usr/local/pgsql/data </p>

<p>Step 6: Change Permission : </p>
<p>cd /usr/local </p>
<p>sudo chown -R postgres ./pgsql </p>

<p>Step 7: Initializing a new PostgreSQL database cluster :</p>
<p>su - postgres </p>
<p>cd /usr/lib/postgresql/15/bin </p>
<p>./initdb -D /usr/local/pgsql/data </p>

Step 8:  Start server
./pg_ctl start -D /usr/local/pgsql/data

<h2>References:</h2>
<p>https://www.postgresql.org/download/linux/ubuntu/ </p>
<p>https://www.postgresql.org/docs/current/app-initdb.html </p> 
<p>https://www.postgresql.org/docs/current/server-start.html </p>
