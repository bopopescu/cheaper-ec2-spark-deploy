# Cheaper Spark AWS deployment script

Author: San-Chuan Hung (2015)

## Description

This script is extended from "spark_ec2.py" in Spark 1.5.1. I added the
configuration to support master node running as spot-instance. Please
see "--master-spot-price" setting.

## Example

spark-ec2 --key-pair=$KEY_PAIR --identity-file=$PEM_FILE --region=us-east-1 --zone=$ZONE --master-spot-price=$MASTER_SPOT_PRICE --spot-price=$SPOT_PRICE -s $SLAVES --instance-type=$INSTANCE_TYPE --hadoop-major-version=yarn launch $EXPERIMENT_NAME