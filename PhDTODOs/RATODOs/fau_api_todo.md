#=====================
#==NOTE
#=====================
from 2020-9-1, until 11-1-2020, there are 27197 subreddit.

how to choose what operational database to use?
    1. structured data.
    2. volum -> I think i need in the gigabyte range. (account for twitter
        crawler)
        what much data is 1 million per day in term of bytes?
            megabyte, gigabyte, terabyte, and petabytes scales.
    3. performance issues via unpredictable queries -> I don't know what
    mine belong to.
        find example that is similar to my case.
            what app both write/read data real time?
                ?online store?
    4. noSQL
        MongoDB vs Apache vs Cassandra vs Redis

What will data be used for?  (data usecase)
    1. data will be provided through api (in a real-time fashion)
    2. data will be use to construct graph.
    3. data will e use to do analytics.

database dsign option
    database design option 1
        json (easy to write and hard to read )
        -> Document database (noSQL) (easy to read and hard to write.)
        -> APi
            ?what is the property of API that have access to database?

    database design option 2: using SQL datbase that support columns for
        JSON format (and also allow you to make special operations over them)
        Note: one of the SQL database option is PostgreSQL
        json
        -> stored it in PostgresSQL

    database design option 3: using both SQL and noSQL
        NOTE: consider prices for each solution that can be done using this
            option.

        NOTE: the reason for this option is because I am not sure whether or
             not when having or data from other source, I will need to use
             SQL operation. (the purpose of SQL operatio is just making it
                 easy to access, read, write, combine data )

         1. using SQL as a single source of truth ( act like data warehouse)
         2. using noSQL as a data lake

         we need microservice that ca do the following.
            ? how can each component be combined?

            > stream processos/message broker
                producer -> stream processor -> cosumer
                eg.
                    Apache Kafka and Amazon Kinesis Data Streams
            > ETL tools for straming data.
                eg.
                    data lake ETL
            > serverless query egine.
                eg.
                    lambda?
            > streaming data storage.
                database or data warehouse
                    PostgresQL or Amzaon Reditshift
                message broker

        AWS services stack option 1
            AWS CloudFormation Template  (stake things together)
                [
                    json output from api ->
                     Kenesis ->
                     [
                      Amazon S3 (data warehouse) ->
#                       Amazon DynamoB (noSQL database) ->
                      AWS lambda (create function that response to api request.
                           to query) ->
        #               AWS GLUE (data transfomration: this is ETL, so I need to
        #                   use it with data warehouse ) ->
        #               AWS Athena (sql engine)
                     ] (both things can be access with data lake command line)->
                      provide API

                    what is the ETL technology that I am looking for?
                ]
        <selected> AWS services stack option 2
            Kinesis data stream->
                1. Kinesis firehorse
                    can I apply sentiment analysis in this process? if not
                    selected the following option
                        1.1 use DynamoDB Stream -> trigger lambda -> S3
                        1.2 How to apply sentiment analysis to Kinesis
                                see Real-Time Reddit Streaming Solution: Self-Guided Tutorial

                   S3 ->
                   query "aspect" straight from S3 (in batch)

                   If query from s3 is not possilbe, add to DynamoDB and
                   query from it instread
                   DynamoDB
                    given primary key&sorted kyes
                        option1
                            sorted keys = subreddit
                            primary key = comment/submission
                        <selected >option2
                            primary key = subreddit
                            sorted_key = date time

     database design option 4: use Amazon microservice
        ?what are microservices that I will need?
            microservice for ETL? or real-time (like kafka)
     database design option 5: using Docker Container


    using EC2 with lambda
    using docker with lambda

    read worign with AWS Lambda and Lambda Layers in AWS SAm
        what is Lambda Lyaer

    here> hwo to import Custon Python pKacges on AW Lambda Funciton
        https://www.youtube.com/watch?v=yyBSeGkuPqk&ab_channel
        =Tekashi6ix9ineTekashi6ix9ineOfficialArtistChannelk:w

    SEt up locla lambda Developement Envionrment Using SAM _
        https://www.youtube.com/watch?v=bih5b3C1nqc&ab_channel=Hip-HopUniverseHip-HopUniverseVerified

    read Workgin with AWS Lambda and Lambda Layers in AWS SAM
       read https://aws.amazon.com/blogs/compute/working-with-aws-lambda-and-lambda-layers-in-aws-sam/

        how to create docker container for Amazon Linux?
            Configuring a function to use layers
            Managing layers
            Inlcuidng library dependencies in a layer
            layer permissions
            AWS CloudFormation and AWS SAM
            SAmple application

    Develope AWS Lambda with AWS EC2 (or Docker)
        read hwo to use AWS Lambda service with EC2-an Example
            https://learnfromsanthosh.com/how-to-use-aws-lambda-service/



    read Buildig application
        https://docs.aws.amazon.com/serverless-application-model/latest/developerguide/serverless-sam-cli-using-build.html

    ? if you are creating a deployment package used in a layer.
        read including library dependencies in a layer
           https://docs.aws.amazon.com/lambda/latest/dg/configuration-layers.html#configuration-layers-path

    with a virtual environment
        https://docs.aws.amazon.com/lambda/latest/dg/python-package.html


#=====================
#==REQUIREMENT
#=====================

system requirement
    store data before modified.
    store data after modified.
    store missing data when client side fail
    store missing data when server side fail
    stream data as well as stored data can be accessed via url endpoint
    system add sentiment to the stream data

user requirment
    user can get streaming data from URL endpoint
    user can specified date range, crawler_type, aspect,
    user can use the same url paramters .


#=====================
#==QUESTION
#=====================

#=====================
#==WAITING
#=====================

how to deploy twitter kinesis with serverless (lambda)?
    ref: https://aws.amazon.com/blogs/opensource/data-processing-pipeline-kinesis-kubeless/ 
        I don't think kubeless is related to serverless.

    sol1: how to make kinesis stream more data? 
        already asked questions:
            how to auto scale kinesis?
            kinesis with tweepy? what are ways that people do things? what are code they put in on_success?
                look at article that use spark with kinesis.
                    why is spark needed?  where does processing happen?
                        processing in side on_sucess?
        change config?
        are there althernative ways to deploy it?
        need more shard?
    sol3: try other solution that could cause error.
        https://stackoverflow.com/questions/53326879/twitter-streaming-api-urllib3-exceptions-protocolerror-connection-broken-i
            Erorr: urllib3.exceptions.ProtocolError: ('Connection broken: IncompleteRead(0 bytes read)', IncompleteRead(0 bytes read))
            what are other options?
            search for errror in tweepy github
        https://github.com/tweepy/tweepy/issues/237

        here> https://stackoverflow.com/questions/28717249/error-while-fetching-tweets-with-tweepy
            Error: urllib3.exceptions.ProtocolError: ('Connection broken: IncompleteRead(0 bytes read)', IncompleteRead(0 bytes read))
            I guess you could try to distinguish between those two cases by keeping track of the delay between the tweet being posted and received. If it's greater than a couple seconds, you're probably falling behind and it's a disconnect. If it's real time, you're probably ok and should just continue. Alternatively, try reading again, and disconnect/reconnect if it happens again or you get some other error (socket closed?). Any better solutions?
                I've ran Tweepy - streaming the sample API - 4 times and every time I receive a Tweet I display the time it was received and the created_at value provided by the Twitter API indicating the time the Tweet was tweeted. I've come back with the following results:
            here> Well, the solution is easy: stop falling behind. This can either be achieved by listening to fewer or less popular words, or by processing them faster
                lets figure out how to 
                    here> how do I know if I catch the wrong error
                        here> try to validate that error is due to stalling 
                            here> 10 sec between on_data
                            why can't I get 406 error?  what is this error?

implement architecture as code
    using cdk with api
        CDK for serverless.
            here> running lambda on EC2
                how to load lambda into EC2 using python?
                    solution attempt

                    using web server (how?)
                        " Python-based web server on the EC2 box itself (e.g. Flask). "
                    using ssh (how?)

            here> create path for dynamoDB stream
                figure how to create path and method
                figure how to connect to kinesis
                figure how to connect to dynamoDB
                figure how to connect to s3

        Note:
            api invoke url
                 https://om3ozpzn1e.execute-api.us-east-2.amazonaws.com/test
            example
                 curl -v -X POST 'https://om3ozpzn1e.execute-api.us-east-2.amazonaws.com/test/helloworld?name=John&city=Seattle' -H 'content-type: application/json' -H 'day: Thursday' -d '{ "time": "evening" }'
                 curl -v -X GET 'https://om3ozpzn1e.execute-api.us-east-2.amazonaws.com/test/helloworld?name=John&city=Seattle' -H 'content-type: application/json' -H 'day: Thursday' -d '{ "time": "evening" }'
                 curl -v -X PUT 'https://om3ozpzn1e.execute-api.us-east-2.amazonaws.com/test/helloworld?name=John&city=Seattle' -H 'content-type: application/json' -H 'day: Thursday' -d '{ "time": "evening" }'

    Goal: AWS CDK Tutorial Python | Create Dynamodb, Kinesis, S3, Lambda, API gateway - Demo
        here> use code to do api gate way similar to what I did in console.
            here> what is paginate operation?
            implement twitter stream in kinesis and with apigateway

            Boto3 and cloudformation vs cli and couformation
                reference: https://www.bing.com/search?q=python+apigateway+kinesis&go=Search&qs=ds&form=QBRE
                here> test the existing api gateway that I have .
                    here> GET + /stream-name/

            select tutorial that match my case.
                (kinesis + api gateway + lambda + s3 + dynamoDB)
                    here> kinesis + apigateway
                    s3 + api gateway
                    dyamoDB + api gateway

            select template that I will need.
            how to create template from AWS CLI?
            use cloudfront to create gateway + kinesis.
                look at cloudfront tutorial.
        use code to do api gate way focus on query string

    here> how to use existing api in SAM
        here> how to use existing resource clouformation
            note api resource:
                https://docs.aws.amazon.com/apigateway/latest/developerguide/arn-format-reference.html
                https://stackoverflow.com/questions/48514180/how-can-i-find-the-arn-of-an-api-gateway-stage
                    eg arn:aws:apigateway:{region}::/restapis/{rest_api_id}/stages/{stage_name}
                    arn:aws:apigateway:us-east-2::/restapis/77ue66yk77/stages/dev/dynamodb
            can I create SAMAPIDynamodb manually?
                hwo to add DynamoDB to stack mnaully?
                    useful ref
                        https://www.youtube.com/watch?v=GgoQWOU6BDc&ab_channel=BasantRawat
            here> create with sam
                here> do I need to create tags for my resources?
                    when to use tags?
                        what is the benefit of doing so? 

        cdk shit

            https://GUID.execute-api-REGION.amazonaws.com/prod/
            https://810414031677.execute-api-us-east-2.amazonaws.com/prod/
            curl -X GET 'https://GUID.execute-api.REGION.amazonaws.com/prod'
            curl -X GET 'https://810414031677.execute-api-us-east-2.amazonaws.com/prod/'

            where do I specify my srucirty token in cdK?
                do I need to provide access token to cdk when using it?
                    icluding the following
                        arn
                        url
                        access
                        UID
            do I have to have bucket before that using s3.Bucket?
            how do I debug CDK?
                are there log?
                    if yes, where is it?
            before trying to make MyWidgetService work
                I have to implement AWS API by itself.

            here> Goal: implement CDK as a base template for crawler
                here> CDK
                    find free template for lambda, s3, kinesis.
                        ?is the following option what I want?
                            option1: cdk for serverless
                                here> https://docs.aws.amazon.com/cdk/latest/guide/serverless_example.html
                                    bootstrapping?
                                    assets?
                                    CDK pipelines

                            option2: SAM CLI with CDK
                                https://docs.aws.amazon.com/cdk/latest/guide/sam.html

implement system monitoring 
    how to deal with when code throw exception and stop running.
    figure out how to re-run when code throw exception
        Code Pipline vs DataPipelin vs Airflow
            if use Code Pipeline use CDK
                see the following
                    https://docs.aws.amazon.com/cdk/latest/guide/cdk_pipeline.html
                    https://docs.aws.amazon.com/cdk/latest/guide/codepipeline_example.html

migrate from cloud to local
    what do you need to use MinIO?
        read about MinIO
            https://docs.min.io/docs/minio-docker-quickstart-guide
            https://docs.minio.io/docs/deploy-minio-on-docker-compose
            https://hub.docker.com/u/minio/
            https://registry.hub.docker.com/r/minio/minio/
        see docker-compose.yml in TestBeyondJupyter

    FreeNAS in Window using virtual machine?

    how to setup storage serve in my labtop

    MinIO vs s3
        what is the difference?

Add unittest to AWS 
    ref:
        types of test 
            type of test in software testing
                https://www.atlassian.com/continuous-delivery/software-testing/types-of-software-testing
            what are the types of testing in CD/CI?
                Continuous integration vs. continuous delivery vs. continuous deployment
                    https://www.atlassian.com/continuous-delivery/principles/continuous-integration-vs-delivery-vs-deployment
                Automated Unit Testing in DevOps Pipeline | AWS Lambda Unit Testing using AWS CodeBuild
                    https://www.youtube.com/watch?v=wUvYTmTvmko&ab_channel=AgentofChange
                AWS re:Invent 2019: Continuous delivery to AWS with GitHub Actions (DOP322-S)
                    https://www.youtube.com/watch?v=KJNj37ZXPqE&ab_channel=AWSEvents

        begin implementing API gateway + test (using TCR) (possible?)

    better Python testing: how to mock AWS
        https://www.youtube.com/watch?v=11Fr0wqcxRc&ab_channel=JeffreyNess

    here> how to test AWS service in python?
        read this https://towardsdatascience.com/how-i-write-meaningful-tests-for-aws-lambda-functions-f009f0a9c587
        implement the following + add to cacher
            https://roamresearch.com/#/app/AdaptiveGraphStucture/page/lKMbKrTRO

here> lets show sentiment of covid19 on Kibana?
    finish the article

waiting reply from Skyler    
    ref: https://mail.google.com/mail/u/0/#search/rresnick%40fau.edu/QgrcJHsTnPnDxKNvCVqkksqnsVHCTCRNpbG
    is it possible to upgrade form vim 7.4 to vim 8?

learn about reddis cache

disable ding sound on the CESTONS 7 
    ref: 
        here> https://mail.google.com/mail/u/0/#search/rresnick%40fau.edu/QgrcJHsTnPnDxKNvCVqkksqnsVHCTCRNpbG
            This sound can be disabled with the following command:
            echo 'set bell-style none' >> ~/.inputrc
            Once completed open a new terminal and the sound should be gone.

            For the port forwarding through ssh do the following:
            ssh koko-login.hpc.fau.edu
            From here I request a node to be allocated to me
            salloc -c 64 -p longq7 --exclusive # 64 cpu cores for 7 days with x11 and make sure I am the only one on the node
            Notice the output
            salloc:Granted job allocation ###### (some job id)
            salloc:Waiting for resource configuration
            salloc: Nodes nodeamd009 (note this name, yours maybe different) some node name are ready for the job

            run this command:
            ssh nodeamd009 (use your node name seen in the output )
            launch jupyter notebooks

            then from your computer do the following 
            ssh -L 8888:localhost:8111 spaulus2017@koko-login.hpc.fau.edu "ssh -L 8111:localhost:8888 -N nodeamd009"

            You will have to find a port that no one else is using, for example 8111 in the above ssh may need to change if someone has already opened it for their application. 


#=====================
#==OPTIMIZATION
#Note: no need to be done right now, but if it is done it will be better.
#=====================
add query word for aspects that can be use with dynamodb (or if needed elasticsearch).

how to manage cost using  AWS service?

fnigure out a way to make tweepy process faster:
    note: you can do more than 1 of the following solution 
    sol1: distributed computing
        put on slurm cluter. 
    sol2: parallel computing 
    sol3: multithreahd computing  ( not sure if it is already included form the first 2 solution) 

use openapi as standard for my api documentation
update documentation to the clodu version

* use the following to optimize the architecutre
    * here> step function
        * here> temrporal
            * note
                * similar to step function but more generalized

* here> try to destroy and recreate
    * terraform registry
        * https://registry.terraform.io/browse/modules
    * here> how does module works in terraform?
        * ref 
            * here> how to use terraform registry?
                * https://learn.hashicorp.com/tutorials/terraform/module-use 
            * read the following
                * https://www.terraform.io/docs/language/modules/develop/index.html
            * how to start building terraform from scratch?
                * ref 
                    * terraform best practices
                        * https://www.terraform-best-practices.com/examples/terraform/medium-size-infrastructure
                    * https://medium.com/@simon.so/7-tips-to-start-your-terraform-project-the-right-way-93d9b890721a
                    * module in terraform 
                        * https://medium.com/@mitesh_shamra/module-in-terraform-920257136228
                    * hands-on 
                        * https://www.youtube.com/watch?v=Ql8RqTH8gOA&list=PLMxDdjhmPw7L5kpguJxVuMoEfoqmygOiW&ab_channel=HMInformative
                        * https://www.youtube.com/watch?v=e_rcdTGTnt0&ab_channel=HMInformative
        * fix terrform error 
        * change kinesis to be autoscaled or increase sharding.
        * fix provider key error 
            * here> add iam-policy to dynamodb table  
                * find iam_policy  
                * how to attach policy to a resource? 
        * here> configure the following services
            * here> read policy 
                * policy
                    * here> https://learn.hashicorp.com/tutorials/terraform/aws-iam-policy
                * auto scaling + terraform  
                    * https://stackoverflow.com/questions/61180364/error-creating-application-autoscaling-target-on-aws-when-using-terraform-defi
            * kinesis 
                * no autoscale natively avialble
                    * solution 
                        * https://aws.amazon.com/blogs/big-data/scale-your-amazon-kinesis-stream-capacity-with-updateshardcount/
                            * use cloudwatch alarm -> send sns topic -> execute call to 
                                UpdatedShardCount API
                * what are options I can configure?
            * here> firehorse -> s3 -trigger -> dynamo
                * if too much work, just put things in dynamodb
            * ec2
                * error
                    * ec2 turns off when I tried to ssh (after turned it on)
                * how to code to ec2 with terraform?
                * here> create ec2 with autoscaling

* learn to use aws cli cloudwatch to inspect stuff. (I am so done with console.)
#=====================
#==RESOURCE
#=====================
caching 
    database caching 
        https://www.youtube.com/results?search_query=databash+caching+with+redis

    DataBase - Difference between In-Memory Database, Normal DataBase & Caching | In Memory Database #2
        https://www.youtube.com/watch?v=4pW_DUimJV0&ab_channel=TechTalkDebu

    Supercharge Query Caching with AWS Database Services - AWS Online Tech Talks


#=====================
#==TODO
#=====================

* reddit 
    * currently i am getting comment.
        * is there a way to get more than comments?
            * eg reply?
* here> twitter 
    * here> create script to do the following
        * get top n 
        * get samples
    <!-- * add dynamoDB api to get top 10 ... --> 
* best computer spec for straming.
    * get dynamodb 
* here> add more keywords for reddit and twitter
    * here> script to get dynamodb
        * 
* what do i need to send to zhabiz?
    * send script to zhabiz to pull dynamodb data  

* figure out a best way to manage account?
* list services and names that I needs to create.
    1. kinesis
        * raw input stream
            * twitter -> faucovidstream_input
            * reddit -> faucovidstream_input_from_reddit
    2. firehose
        * twitter -> faucovidstream_from_kinesis_to_s3
        * reddit -> faucovidstream_from_reddit_input_kinesis_to_s3
    3. here> s3
        * here> twitter -> faucovidstream
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


* fix the error
    * here> error:
        * here> botocore.exceptions.ClientError: An error occurred (UnrecognizedClientException) when calling the PutRecord operation: The security token included in the request is invalid.
            * what is the security toekn taht it is talking about?
                * can I change it to the main accoutn?
            * here> what account is running it?
                * here> is the current accoutn valid?
* here> implement ec2 auto scale + monitoring
    * here> how to migrate from ec2 to auto scaling
        * here> create demo of docker locally on my laptop 
        * move code from my laptop to ec2 auto scaling.
            * here> run random code on ec2 auto scaling.
                * ref
                    * here> https://docs.aws.amazon.com/autoscaling/ec2/userguide/GettingStartedTutorial.html
                * is there anything else I needs to do differntly than running code on ec2 instance?
    * read about ec2 auto scaling 
        * picture 
            * https://ec2spotworkshops.com/running-amazon-ec2-workloads-at-scale/architecture.html
        * An AWS CloudFormation stack, which will include:
            An Amazon Virtual Private Cloud (Amazon VPC) with subnets in two Availability Zones
            An AWS Cloud9 environment
            Supporting IAM policies and roles
            Supporting security groups
            An Amazon EFS file system
            An Amazon S3 bucket to use with AWS CodeDeploy
        * An ec2 launch template
        * an RDS database instance
        * load balancer 
        * ec2 auto sclaing groiup with
            * schedule scaling action
            * dynamic scaling policy
        * AWS CodeDeploy application dpeloyment
        * AWS System Manger 
            * run commnad to emulate load on the service?
    * read about monitoring.
* can I do distributed real-time streaming processing?

* merge tags + add more tags.
* fau crawler 
    * here> send set of data -> put in text files (csv).
    * create word cloud 
    * combine corona and covid
    * expand scope of what I am collecting
    * collect data for hot topics 

* here> use terraform and ansible to automate the instruction for reddit stream data
    * how to use terraform with ansible?
    * create a demo that use terrafrom and ansible to connect to the following 
        * for each try terraform and ansible
            * here> s3
                * here> terraform 
            * lambda
            * kinesis
            * dynamodb
            * ec2 
    * here> capture reddit stream
        * requirement
            * Kinesis -> S3 -> Lambda -> DynamoDB 
                * description: store original stream data in S3, and store modified data in DynamoDb
                *  workflow step by step:
                    1. kinesis:faucovidstream_input
                    2. firehose:faucovidstream_from_kinesis_to_s3
                    3. s3:faucovidstream 
                    4. lambda:faucovidstream
                    5. kinesis:faucovidstreamsentiment
                    6. here> dynamoDB:faucovidstream_twitter_with_sentiment 
                        * here> haven't yet implement part of dynamodB
                        * add reddit paramer 
                            here> create path in the api.
                                note: see how twitter param is implemented as (use boto3.)
                                    here> how to create api gateway?
                                        which code do i refer to? do i have any?
                                        here> what does TwitterLambdaS3Trigger do?
                                            note: 
                                                can the process be done in boto3? or it must be done in aws cli?
                                                    lets use sam to do that.


* note:
    * instead of putting in FAU Cluster, run the program on AWS EC2:
        and monitor it with codepipline

* move batch data of the missing date from s3 to dynamodb
    * I need to modify some data structure from data stored in s3 and send to store in dynamodb

* ans zhabiz question
    'does permalink includes in Twitter's stream or Reddit's stream?'

implement demo to pull data (with sentiment) from the last 24 hours in batch.
    send to zhabiz with complete.


                        set s3 to detect reddit kinesis
                            create s3 for reddit raw stream data
                                what is the name of it?
                            how to use SAM OR boto3 to set kinesis stream to updated to s3?
                        In lambda, input (from s3) is transform and send to dynamodb and another stream called 'faucovidstreamsentiment_reddit'
                            how to combine multiple stream into 1?
            

put it on to cluster 
  * how to send command from local computer to be run on remote server?
    * how to slurm to run cluster without time limit? 
        * ans:
            * 'sbatch --requeue'
    * how can I output to /dev/null/ without sudo 


convert searchable fields to lowercase (just do for 'text' field)
    note: 
        modification should be done in lambda_function()
    twitter_to_kinesis.py
    reddit_to_kinesis.py 
    
        
get more data from comments (reddit_to_kinesis.py)
    expand on replies, and other key that can be applied (such as subreddit/replies keys)
        which keys do i have to expands on ?


migrate from cloud to local
    s3 to Ceph OR Minio
        note: 
            Ceph is for cluster based storage, so i think I need to migrate to minio
            
