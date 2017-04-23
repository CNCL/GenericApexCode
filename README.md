# GenericApexCode
Generic Reusable Apex Classes

#UpdateFieldBatchClass
We can use this Apex class to mass update fields of any object.
to instantiate this batch use below snippet
Database.executebatch(batch,200);﻿
string query='select id,website from account';
Map<String, String> fldValues = new Map<String, String>();
fldValues.put('website', 'www.dskvap.com');
fldValues.put('email' , 'someemail@test.com');
// and so on for all fields you want to udpate
batchupdatefield batch=new batchupdatefield(query,fldValues);
