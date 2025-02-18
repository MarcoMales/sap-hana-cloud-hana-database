<!-- loio20b7ea517519101496d5ecc1166ba4b9 -->

# M\_PREPARED\_STATEMENTS System View

Provides information about prepared statements.



<a name="loio20b7ea517519101496d5ecc1166ba4b9___m__p_r_e_p_a_r_e_d__s_t_a_t_e_m_e_n_t_s_1struct_M_PREPARED_STATEMENTS"/>

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

HOST

</td>
<td valign="top">

NVARCHAR\(64\)

</td>
<td valign="top">

Displays the host name.

</td>
</tr>
<tr>
<td valign="top">

PORT

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the internal port number.

</td>
</tr>
<tr>
<td valign="top">

CONNECTION\_ID

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the connection ID.

</td>
</tr>
<tr>
<td valign="top">

STATEMENT\_ID

</td>
<td valign="top">

NVARCHAR\(20\)

</td>
<td valign="top">

Displays the prepared statement ID.

</td>
</tr>
<tr>
<td valign="top">

STATEMENT\_HASH

</td>
<td valign="top">

NVARCHAR\(32\)

</td>
<td valign="top">

Displays the MD5 hash value for the statement string.

</td>
</tr>
<tr>
<td valign="top">

START\_MVCC\_TIMESTAMP

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the internal MVCC timestamp of the transaction start time.

</td>
</tr>
<tr>
<td valign="top">

COMPILED\_TIME

</td>
<td valign="top">

TIMESTAMP

</td>
<td valign="top">

Displays the compilation timestamp of the statement.

</td>
</tr>
<tr>
<td valign="top">

STATEMENT\_STATUS

</td>
<td valign="top">

NVARCHAR\(128\)

</td>
<td valign="top">

Displays the status of the SQL statement.

</td>
</tr>
<tr>
<td valign="top">

STATEMENT\_STRING

</td>
<td valign="top">

NCLOB

</td>
<td valign="top">

Displays the SQL statement.

</td>
</tr>
<tr>
<td valign="top">

ALLOCATED\_MEMORY\_SIZE

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the memory peak used for executing this statement. In case of distributed execution it is a sum of the local peak memories of multiple servers.

</td>
</tr>
<tr>
<td valign="top">

PLAN\_ID

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the logical plan ID.

</td>
</tr>
<tr>
<td valign="top">

LAST\_EXECUTED\_TIME

</td>
<td valign="top">

TIMESTAMP

</td>
<td valign="top">

Displays the recently executed time of the statement. This timestamp is updated when opening cursors and executing DML/DDL but not when fetching cursor results or closing cursors.

</td>
</tr>
<tr>
<td valign="top">

LAST\_ACTION\_TIME

</td>
<td valign="top">

TIMESTAMP

</td>
<td valign="top">

Displays the recently performed time of action against the statement. This timestamp is updated when opening cursors, executing DML/DDL, fetching results, and closing cursors.

</td>
</tr>
<tr>
<td valign="top">

RECOMPILE\_COUNT

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the recompile count.

</td>
</tr>
<tr>
<td valign="top">

EXECUTION\_COUNT

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the count of executions.

</td>
</tr>
<tr>
<td valign="top">

AVG\_EXECUTION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the average time of statement execution.

</td>
</tr>
<tr>
<td valign="top">

MAX\_EXECUTION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the maximum time of statement execution.

</td>
</tr>
<tr>
<td valign="top">

MIN\_EXECUTION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the minimum time of statement execution.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_EXECUTION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the sum of statement execution time.

</td>
</tr>
<tr>
<td valign="top">

AVG\_CURSOR\_DURATION

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the average time of statement execution including communication time with clients.

</td>
</tr>
<tr>
<td valign="top">

MAX\_CURSOR\_DURATION

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the maximum time of statement execution including communication time with clients

</td>
</tr>
<tr>
<td valign="top">

MIN\_CURSOR\_DURATION

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the minimum time of statement execution including communication time with clients.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_CURSOR\_DURATION

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the sum of statement execution time including communication time with clients.

</td>
</tr>
<tr>
<td valign="top">

AVG\_EXECUTION\_MEMORY\_SIZE

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the average memory size in bytes used during each execution.

</td>
</tr>
<tr>
<td valign="top">

MAX\_EXECUTION\_MEMORY\_SIZE

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the maximum memory size in bytes used during each execution.

</td>
</tr>
<tr>
<td valign="top">

MIN\_EXECUTION\_MEMORY\_SIZE

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the minimum memory size in bytes used during each execution.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_EXECUTION\_MEMORY\_SIZE

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the sum of memory size in bytes used during each execution.

</td>
</tr>
<tr>
<td valign="top">

AVG\_LOCKWAIT\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the average lock wait time for the statement.

</td>
</tr>
<tr>
<td valign="top">

MAX\_LOCKWAIT\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the maximum lock wait time for the statement.

</td>
</tr>
<tr>
<td valign="top">

MIN\_LOCKWAIT\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the minimum lock wait time for the statement.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_LOCKWAIT\_COUNT

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the total lock wait count for the statement.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_LOCKWAIT\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the accumulated lock wait time for the statement.

</td>
</tr>
<tr>
<td valign="top">

AVG\_PREPARATION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the average time of statement preparation.

</td>
</tr>
<tr>
<td valign="top">

MAX\_PREPARATION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the maximum time of statement preparation.

</td>
</tr>
<tr>
<td valign="top">

MIN\_PREPARATION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the minimum time of statement preparation.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_PREPARATION\_TIME

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the total time of statement preparation.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_PREPARATION\_COUNT

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the total count of statement preparation.

</td>
</tr>
<tr>
<td valign="top">

HAS\_HOLDABLE\_CURSOR

</td>
<td valign="top">

NVARCHAR\(5\)

</td>
<td valign="top">

Displays the holdable cursor existence.

</td>
</tr>
<tr>
<td valign="top">

CURSOR\_TYPE

</td>
<td valign="top">

NVARCHAR\(18\)

</td>
<td valign="top">

Displays the type of cursor.

</td>
</tr>
<tr>
<td valign="top">

PARENT\_STATEMENT\_ID

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the parent prepared statement ID.

</td>
</tr>
<tr>
<td valign="top">

APPLICATION\_SOURCE

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the application source information.

</td>
</tr>
<tr>
<td valign="top">

STATEMENT\_MEMORY\_LIMIT

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the effective statement memory limit.

</td>
</tr>
<tr>
<td valign="top">

STATEMENT\_THREAD\_LIMIT

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the effective statement thread limit.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_STATEMENT\_MEMORY\_LIMIT

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the effective total statement memory limit.

</td>
</tr>
<tr>
<td valign="top">

TOTAL\_STATEMENT\_THREAD\_LIMIT

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the effective total statement thread limit.

</td>
</tr>
<tr>
<td valign="top">

WORKLOAD\_CLASS\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the name of the effective workload class used for the execution.

</td>
</tr>
</table>



<a name="loio20b7ea517519101496d5ecc1166ba4b9__section_yjl_flg_rkb"/>

## Additional Information

Setting the value of the APPLICATION\_SOURCE is only available via internal APIs of the SAP HANA database client interfaces \(for more information see SAP Note 2873396\).

**Related Information**  


[SAP Note 2873396](https://me.sap.com/notes/2873396)

[Reduce the Complexity of SQL Statements](https://help.sap.com/viewer/4466fb5b5e3f4388a00b44aad5a4bffa/2023_4_QRC/en-US/aea3021952d8419493993e68b491fee1.html "Variables in SQLScript enable you to arbitrarily break up a complex SQL statement into many simpler ones. This makes a SQLScript procedure easier to comprehend.") :arrow_upper_right:

