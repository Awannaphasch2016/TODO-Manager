# Terraform
*) terminology 
    * Hashicorm Cofniguration Laungauge
        * Identifiers
        * Argument 
            * assign a value to a name
        * block
            * a container for other content
                * https://www.terraform.io/docs/language/syntax/configuration.html
* FAQs
    * what is modulee?
* todo
    * list the thigns that I want to create
        * try to create kniesis and run program that only have kinesis see if it works?
            * how to create terraform to connect kinesis stream to kinesis firehorse
        * here> how to move data from kinesis to s3 using firehorse 
            * here> terraform
                * add lambda with kinesis trigger
                    * dynamoDB
                * change value of service in lambda to match what i have  
                    * lambda function
                        * what is the lambda 
                    * dynamodb
                    * s3?
        * components
            1. kinesis
                * raw input stream
                    * twitter -> faucovidstream_input
                    * reddit -> faucovidstream_input_from_reddit
            2. firehose
                * twitter -> faucovidstream_from_kinesis_to_s3
                * reddit -> faucovidstream_from_reddit_input_kinesis_to_s3
            3. s3
                * twitter -> faucovidstream
                * reddit ->  faucovidstreamreddit
            4. lambda
                * twitter -> faucovidstream
                * reddit -> faucovidstream_reddit
            5. kinesis
                * modified input stream (with sentiment)
                    * twitter -> faucovidstreamsentiment
                    * reddit -> faucovidstreamsentiment_reddit
            6. dynamoDB
                * twitter -> faucovidstream_twitter_with_sentiment 
                * reddit -> faucovidstream_reddit_with_sentiment

