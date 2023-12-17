
### Hiển thị tất cả các 
```
kafka-consumer-groups --bootstrap-server localhost:8081 --all-groups --describe
```

```
kafka-console-consumer --bootstrap-server localhost:8081 --topic userTopic --partition 0 --reset-offsets 5 --max-messages 10
```