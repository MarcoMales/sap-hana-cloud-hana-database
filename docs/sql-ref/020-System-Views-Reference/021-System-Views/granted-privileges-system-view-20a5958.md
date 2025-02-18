<!-- loio20a5958e751910149536e9ab4b54dd87 -->

# GRANTED\_PRIVILEGES System View

Provides information about privileges and roles granted to users.



<a name="loio20a5958e751910149536e9ab4b54dd87___g_r_a_n_t_e_d__p_r_i_v_i_l_e_g_e_s_1struct_GRANTED_PRIVILEGES"/>

## Structure


<table>
<tr>
<th valign="top">

Column name

</th>
<th valign="top">

Data type

</th>
<th valign="top">

Description

</th>
</tr>
<tr>
<td valign="top">

GRANTEE\_SCHEMA\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the name of the schema of the grantee.

</td>
</tr>
<tr>
<td valign="top">

GRANTEE

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the user or role the privilege is granted to.

</td>
</tr>
<tr>
<td valign="top">

GRANTEE\_TYPE

</td>
<td valign="top">

NVARCHAR\(4\)

</td>
<td valign="top">

Displays the grantee type: USER/ROLE.

</td>
</tr>
<tr>
<td valign="top">

GRANTOR

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the user who granted the privilege.

</td>
</tr>
<tr>
<td valign="top">

GRANTOR\_TYPE

</td>
<td valign="top">

NVARCHAR\(10\)

</td>
<td valign="top">

Displays the grantor type: USER, ROLE or ROLEGROUP.

</td>
</tr>
<tr>
<td valign="top">

OBJECT\_TYPE

</td>
<td valign="top">

NVARCHAR\(32\)

</td>
<td valign="top">

Displays the type of the granted object like: TABLE, SCHEMA, and so on.

</td>
</tr>
<tr>
<td valign="top">

SCHEMA\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the schema name the object belongs to.

</td>
</tr>
<tr>
<td valign="top">

OBJECT\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the object name of granted object.

</td>
</tr>
<tr>
<td valign="top">

PRIVILEGE

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the privilege granted.

</td>
</tr>
<tr>
<td valign="top">

IS\_GRANTABLE

</td>
<td valign="top">

NVARCHAR\(5\)

</td>
<td valign="top">

Displays whether the privilege was granted with WITH GRANT OPTION or WITH ADMIN OPTION: TRUE/FALSE.

</td>
</tr>
<tr>
<td valign="top">

IS\_VALID

</td>
<td valign="top">

NVARCHAR\(5\)

</td>
<td valign="top">

Displays whether the privilege is valid or has become invalid because of implicit revoking: TRUE/FALSE.

</td>
</tr>
</table>



<a name="loio20a5958e751910149536e9ab4b54dd87__section_h5b_bpb_dzb"/>

## Permissions

Unless otherwise specified, system views are available to all users granted the PUBLIC role. The data returned for each view is filtered according to the granted privileges of the user accessing a view. Users granted the CATALOG READ system privilege have unfiltered access to all system views and their data regardless of the PUBLIC role and privilege grants.

**Related Information**  


[GRANT Statement \(Access Control\)](../../010-SQL-Reference/012-SQL-Statements/grant-statement-access-control-20f674e.md "Grants various types of privileges to users and roles.")

[REVOKE Statement \(Access Control\)](../../010-SQL-Reference/012-SQL-Statements/revoke-statement-access-control-20fc91c.md "Revokes roles or privileges for the specified objects from a user or role.")

[PRIVILEGES System View](privileges-system-view-20cc29b.md "Provides information about available privileges.")

[EFFECTIVE\_PRIVILEGES System View](effective-privileges-system-view-20a2f3e.md "Provides the privileges of the specified user.")

[EFFECTIVE\_PRIVILEGE\_GRANTEES System View](effective-privilege-grantees-system-view-2a8987c.md "Provides information about who was granted (explicitly or implicitly via roles) a specified privilege.")

[Granting and Revoking Privileges and Roles](https://help.sap.com/viewer/a1317de16a1e41a6b0ff81849d80713c/2023_4_QRC/en-US/c719b2e7d9761014b9d798770c3d0958.html "To be able to grant and revoke privileges and roles to and from users and roles, the granting or revoking user must meet a number of prerequisites.") :arrow_upper_right:

[Managing User Privileges](https://help.sap.com/viewer/477aa413a36c4a95878460696fcc8896/2023_4_QRC/en-US/20fc276e8f22423fb6eba66f03f541e1.html "Various privileges are required to manage remote sources, virtual tables, and linked database.") :arrow_upper_right:

[Privileges](https://help.sap.com/viewer/a1317de16a1e41a6b0ff81849d80713c/2023_4_QRC/en-US/fb0f9b103d6940f28f3479b533c351e9.html "Several privilege types are used in SAP HANA (system, object, and analytic).") :arrow_upper_right:

[System Privileges](https://help.sap.com/viewer/a1317de16a1e41a6b0ff81849d80713c/2023_4_QRC/en-US/cadbcfc38b084808b80b3551b1cd756e.html "System privileges control general system activities.") :arrow_upper_right:

[System Views for Verifying Users' Authorization](https://help.sap.com/viewer/a1317de16a1e41a6b0ff81849d80713c/2023_4_QRC/en-US/ddae823e3b27477ea4c949607eebc435.html "You can query several system views to get detailed information about exactly which privileges and roles users have and how they come to have them. This can help you to understand why a user is authorized to perform particular actions, access particular data, or not.") :arrow_upper_right:

