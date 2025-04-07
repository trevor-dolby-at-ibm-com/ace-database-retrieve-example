# ace-database-retrieve-example
Example using the ACE Database Retrieve node

Assumes a DB2 database in line with https://github.com/ot4i/ace-demo-pipeline/

## Commands 

```
mqsicreateworkdir ~/tmp/ace-database-retrieve-work-dir
mqsisetdbparms -w ~/tmp/ace-database-retrieve-work-dir -n jdbc::tea -u user -p passw0rd

mqsibar -c -w ~/tmp/ace-database-retrieve-work-dir -a BARfiles/DRApplication.bar
IntegrationServer -w ~/tmp/ace-database-retrieve-work-dir
```

Should produce output of the form
```
  (0x01000000:Folder):XMLNSC     = ( ['xmlnsc' : 0x7fa5bc12f6f0]
    (0x03000000:PCDataField):test = NULL
    (
      (0x03000000:PCDataField):name = 'Assam' (CHARACTER)
    )
  )
```

