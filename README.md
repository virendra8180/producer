kafka-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
bin/zookeeper-server-start.sh config/zookeeper.propertie



bin/kafka-server-start.sh config/server.properties
bin/kafka-topics.sh --create --topic my_topic --bootstrap-server localhost:9092 --replication-factor 1 --partitions 1
bin/kafka-console-producer.sh --topic my_topic --bootstrap-server localhost:9092
bin/kafka-console-consumer.sh --topic my_topic --from-beginning --bootstrap-server localhost:9092

You, Mar 12, 2:46 PM
kafka-server-start.sh config/server.properties


def kafka
kafka.create_topic('first-topic', num_partitions: 1, replication_factor: 1)
 kafka = Kafka.new(
3.0.0 :004 >   seed_brokers: ['localhost:9092'], # Change this to your Kafka broker address
3.0.0 :005 >   client_id: 'producer',
3.0.0 :006 >   logger: Rails.logger
3.0.0 :007 > )


     user ={
       "id": 1,
       "username": "test@yopmail.com",
       "email": "user@example.com",
       "created_at": "2024-03-23T10:00:00.000+00:00",
       "updated_at": "2024-03-23T10:00:00.000+00:00"
   }

    kafka = Kafka.new(seed_brokers: ['localhost:9092'])
    producer = kafka.producer
    producer.produce(product, topic: 'second-topic',partition:2)
    producer.deliver_messages
 
  
end 



require 'kafka'

def consumer
kafka = Kafka.new(seed_brokers: ['localhost:9092'])
consumer = kafka.consumer(group_id: 'second-topic')

consumer.subscribe('second-topic')

begin
  consumer.each_message do |message|
    puts "Received message: #{message.value}"
  end
ensure
  consumer.stop
end
end 



