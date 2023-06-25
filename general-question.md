
# General topics to think before solving  

- Ready heavy or Write heavy
- Read write ratio
- High availablity needed?
- Throttling requests for users
- is any service is having sigle point of failure

## High level es timates
- Traffic estimates
- Bandwidth estimates
- Memory Estimated


## How does base64 work?
Base64 encoding converts every three bytes of data (three bytes is 3*8=24 bits) into four base64 characters.
Each six-bit sequence is uniquely mapped to one of the 64 characters used:
![image](https://github.com/l0geshd/system-design/assets/61483272/fe5833d6-4909-4bbe-917e-10b66959f308)

# Take aways from each topic
## 1 Url Shortening
- KGS - Key Generation Service
- hash genration - md5 hash + base64 encoding
## 2 Pastebin
- KGS - Key Generation Service
## 3 Instagram
- Multi DB approach
- Story/Feed pre - generation
## 4 DropBox / GoogleDrive / OneDrive
- split large files into chunks and calculate the hash
- if the systems can go offline then use queues to deliver the messages
- when storing large files use block storage and use separate metadata db
- partitioning based on fileid hash so that realted chunks will be in same partition
## 5 Facebook Messenger


