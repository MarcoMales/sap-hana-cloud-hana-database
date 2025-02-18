<!-- loioc7a96e0bcc51447fa2af31413dbaff41 -->

# VALIDATE\_USERGROUP\_CONNECT\_RESTRICTION Function \(Security\)

Displays whether a connect attempt would be possible given the active connect restrictions of a user group.



<a name="loioc7a96e0bcc51447fa2af31413dbaff41__section_s1j_djn_lyb"/>

## Syntax

```
VALIDATE_USERGROUP_CONNECT_RESTRICTION( [usergroup_name=>]'<usergroup_name>' [, [ client_IP_address=>]'<client_IP_address>' 
   [, [ connect_timestamp=>]'<connect_timestamp>' [, [ application_name=>]'<application_name>' ] ] ] )
```



<a name="loioc7a96e0bcc51447fa2af31413dbaff41__section_a1w_dkn_lyb"/>

## Syntax Elements


<dl>
<dt><b>

*<usergroup\_name\>*

</b></dt>
<dd>

Specifies the name of the group to check.



</dd><dt><b>

*<client\_IP\_address\>*

</b></dt>
<dd>

Specifies the client IP address to check. If not specified or NULL, the actual IP address is used.



</dd><dt><b>

*<connect\_timestamp\>*

</b></dt>
<dd>

Specifies the login time to check. If not specified or NULL, the actual time is used.



</dd><dt><b>

*<application\_name\>*

</b></dt>
<dd>

Specifies the name of the application to check. If not set or NULL, the application name of the actual login is used.



</dd>
</dl>



<a name="loioc7a96e0bcc51447fa2af31413dbaff41__section_t1j_djn_lyb"/>

## Description

Specification of the parameter name is optional when specifying parameter values in the designated left to right order. For example,

```
SYS.VALIDATE_USERGROUP_CONNECT_RESTRICTION('MY_GROUP', '1.2.3.4');
```

is valid, but

```
SYS.VALIDATE_USERGROUP_CONNECT_RESTRICTION('MY_GROUP', 'hdbsql');
```

is invalid because it skips the *<client\_IP\_address\>* parameter, violating the preservation of the left to right parameter requirement.

The order requirement is waived if you preface each parameter value with the parameter name, but with this scenario all parameters are required. For example,

```
SYS.VALIDATE_USERGROUP_CONNECT_RESTRICTION(application_name=>'hdbsql',
   usergroup_name=>'MY_GROUP', client_IP_address=>'1.2.3.4', CURRENT_TIMESTAMP);
```

is valid because each value is specified, but

```
SYS.VALIDATE_USERGROUP_CONNECT_RESTRICTION(application_name=>'hdbsql',
   usergroup_name=>'MY_GROUP');
```

is invalid because two parameter names are not specified.



<a name="loioc7a96e0bcc51447fa2af31413dbaff41__section_n5q_2kn_lyb"/>

## Example

The following example is based on the following statements:

```
CREATE USERGROUP MY_GROUP CONNECT RESTRICTION (R1 IP ('1.2.3.4') APPLICATION ('hdbsql'));
ALTER USERGROUP MY_GROUP ADD CONNECT RESTRICTION (R2 IP ('9.9.9.9', '8.8.8.8'));
ALTER USERGROUP MY_GROUP ENABLE CONNECT RESTRICTION R1;

```

The following two statements are equivalent. They both return connection restriction details on the usergroup name MY\_GROUP, where the client IP address is 1.2.3.4, the connection time is August 17, 2023, and the application name is hdlsql.

```
SELECT * from SYS.VALIDATE_USERGROUP_CONNECT_RESTRICTION('MY_GROUP', '1.2.3.4', CURRENT_TIMESTAMP, 'hdbsql');
SELECT * from SYS.VALIDATE_USERGROUP_CONNECT_RESTRICTION(usergroup_name=>'MY_GROUP', client_IP_address=>'1.2.3.4',
    connect_timestamp=>'2023-08-17', application_name=>'hdbsql');
```

**Output:**


<table>
<tr>
<th valign="top">

USERGROUP\_NAME

</th>
<th valign="top">

USERGROUP\_ID

</th>
<th valign="top">

IS\_CONNECT\_ALLOWED

</th>
</tr>
<tr>
<td valign="top">

MY\_GROUP

</td>
<td valign="top">

158328

</td>
<td valign="top">

FALSE

</td>
</tr>
</table>


<table>
<tr>
<th valign="top">

CONNECT\_TIMESTAMP

</th>
<th valign="top">

APPLICATION\_NAME

</th>
</tr>
<tr>
<td valign="top">

2023-08-17 19:16:13.751000000

</td>
<td valign="top">

SAP\_HANARuntimeTools\_HRA

</td>
</tr>
</table>

**Related Information**  


[CREATE USERGROUP Statement \(Access Control\)](../012-SQL-Statements/create-usergroup-statement-access-control-9869125.md "Creates a usergroup.")

[ALTER USERGROUP Statement \(Access Control\)](../012-SQL-Statements/alter-usergroup-statement-access-control-aa94ca8.md "Alters a usergroup.")

