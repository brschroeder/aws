# Amazon Web Services

## Getting Started

need access key id

install aws bundle if not using amazon linux

need to run "aws configure" before using any aws cli tool

for yr in 2005 2006; do aws s3 cp $yr.csv.bz2 s3://brs-analytics/airline/$yr.csv.bz2; done
