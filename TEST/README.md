### NOTES
- This is an example application that uses multiple services:
    
    (a) OnOffControlService
    
    (b) LocationInformation
    
    (c) CurrentPlaylistControlService

- We can have one or more services in an application. 

- There exists one broker per service.

- We have the flexibility to call bStartLogging() multiple times, by either pushing one broker at a time (or some/all brokers at a time) to the vector and sending the vector as argument.

    i.e say we have broker1, broker2 and broker3. The following are the different possibilities of calling bStartLogging():

    i) All at once :
                    std::vector<::thrift::shared_ptr<::thrift::TServiceBroker>> vecBrokers;
                    vecBrokers.push_back(broker1);
                    vecBrokers.push_back(broker2);
                    vecBrokers.push_back(broker3);
                    UDCLogger::CUDCLogger::cGetLoggerInstance().bStartLogging(vecBrokers,...)

    ii) One at a time :
                    std::vector<::thrift::shared_ptr<::thrift::TServiceBroker>> vecBroker1;
                    vecBroker1.push_back(broker1);
                    UDCLogger::CUDCLogger::cGetLoggerInstance().bStartLogging(vecBroker1,...)
                    ...
                    ...
                    std::vector<::thrift::shared_ptr<::thrift::TServiceBroker>> vecBroker2;
                    vecBroker2.push_back(broker2);
                    UDCLogger::CUDCLogger::cGetLoggerInstance().bStartLogging(vecBroker2,...)
                    ...

    iii) Any other combinations are possible. Just make sure you send a std::vector as argument.

- vStopLogging() API also expects a std::vector<broker>.
