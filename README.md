# localstack

# Starch localstack in dockers
CD to the directory where docker-cmpose file is
docker-compose up -d        -- Start services
localstack status services  -- Check status


# Check health in browser
http://localhost:4566/healthcheck

# AWS Config. Windows
C:\Users\neera\.aws folder should have 2 files config & credentials

Config file has two profiles as below:
[default]
region = eu-west-2
[profile localstack]
region = eu-west-1

Credentials file has two sets of credentials as below:
[default]
aws_access_key_id = XXXXX
aws_secret_access_key = YYYYY
[localstack]
aws_access_key_id = test
aws_secret_access_key = test

# Create AWS Profile for localstach
aws configure --profile localstack
test> test> eu-west-1 (This will add content to above two files)

# List configurations in the terminal
aws configure list

# Make/Create Buckets
aws  --endpoint-url http://localhost:4566 s3 mb s3://ho.leds.np.dts.recon.input
aws  --endpoint-url http://localhost:4566 s3 mb s3://ho.leds.np.dts.recon.output

# List Buckets
aws  --endpoint-url http://localhost:4566 s3 ls

# Maven Dependencies needed for spring S3

        <dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-java-sdk-s3</artifactId>
			<version>1.12.347</version>
		</dependency>

		<dependency>
			<groupId>com.amazonaws</groupId>
			<artifactId>aws-java-sdk-core</artifactId>
			<version>1.12.347</version>
		</dependency>





