# localstack


# Check health in browser
http://localhost:4566/healthcheck

# Create AWS Profile for localstach
aws configure --profile localstack
test> test> eu-west-1

# Make/Create Buckets
aws  --endpoint-url http://localhost:4566 s3 mb s3://ho.leds.np.dts.recon.input
aws  --endpoint-url http://localhost:4566 s3 mb s3://ho.leds.np.dts.recon.output

# List Buckets
aws  --endpoint-url http://localhost:4566 s3 ls

# AWS Config. Windows
C:\Users\neera\.aws folder should have 2 files config & credentials



