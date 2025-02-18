<!-- loiof3f74ec66f5b1014850e8cb59fd084ef -->

# M\_EFFECTIVE\_TABLE\_PLACEMENT System View

Provides information about effective placement of tables.



<a name="loiof3f74ec66f5b1014850e8cb59fd084ef___m__e_f_f_e_c_t_i_v_e__t_a_b_l_e__p_l_a_c_e_m_e_n_t_1struct_M_EFFECTIVE_TABLE_PLACEMENT"/>

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

SCHEMA\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the schema.

</td>
</tr>
<tr>
<td valign="top">

TABLE\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the table.

</td>
</tr>
<tr>
<td valign="top">

RECORD\_COUNT

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the record count.

</td>
</tr>
<tr>
<td valign="top">

TABLE\_TYPE

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the type.

</td>
</tr>
<tr>
<td valign="top">

GROUP\_NAME

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the group name.

</td>
</tr>
<tr>
<td valign="top">

GROUP\_TYPE

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the group type.

</td>
</tr>
<tr>
<td valign="top">

SUBTYPE

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the sub type.

</td>
</tr>
<tr>
<td valign="top">

LOCATION

</td>
<td valign="top">

NVARCHAR\(75\)

</td>
<td valign="top">

Displays the location.

</td>
</tr>
<tr>
<td valign="top">

POSSIBLE\_LOCATION

</td>
<td valign="top">

NVARCHAR\(5000\)

</td>
<td valign="top">

Displays the possible location.

</td>
</tr>
<tr>
<td valign="top">

LOCATION\_MATCH

</td>
<td valign="top">

NVARCHAR\(41\)

</td>
<td valign="top">

Displays a string representing the matching rule for the possible location.

</td>
</tr>
<tr>
<td valign="top">

MIN\_ROWS\_FOR\_PARTITIONING

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the minimum row count for partitioning.

</td>
</tr>
<tr>
<td valign="top">

MIN\_ROWS\_FOR\_PARTITIONING\_MATCH

</td>
<td valign="top">

NVARCHAR\(41\)

</td>
<td valign="top">

Displays a string representing the matching rule for the minimum row count for partitioning.

</td>
</tr>
<tr>
<td valign="top">

PARTITIONING\_THRESHOLD

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the repartitioning threshold.

</td>
</tr>
<tr>
<td valign="top">

PARTITIONING\_THRESHOLD\_MATCH

</td>
<td valign="top">

NVARCHAR\(41\)

</td>
<td valign="top">

Displays a string representing the matching rule for the repartitioning threshold.

</td>
</tr>
<tr>
<td valign="top">

INITIAL\_PARTITION

</td>
<td valign="top">

INTEGER

</td>
<td valign="top">

Displays the initial partitions.

</td>
</tr>
<tr>
<td valign="top">

INITIAL\_PARTITION\_MATCH

</td>
<td valign="top">

NVARCHAR\(41\)

</td>
<td valign="top">

Displays a string representing the matching rule for the initial partitions.

</td>
</tr>
<tr>
<td valign="top">

DYNAMIC\_RANGE\_THRESHOLD

</td>
<td valign="top">

BIGINT

</td>
<td valign="top">

Displays the dynamic range threshold.

</td>
</tr>
<tr>
<td valign="top">

DYNAMIC\_RANGE\_THRESHOLD\_MATCH

</td>
<td valign="top">

NVARCHAR\(41\)

</td>
<td valign="top">

Displays a string representing the matching rule for the dynamic range threshold.

</td>
</tr>
</table>

**Related Information**  


[Table Placement](https://help.sap.com/viewer/f9c5015e72e04fffa14d7d4f7267d897/2023_4_QRC/en-US/22888f9344954f258284d2dd936d0d0a.html "Table classification and table placement configuration, enhanced by partitioning, build the foundation for controlling the data distribution in a SAP HANA scale-out environment.") :arrow_upper_right:

[ALTER SYSTEM ALTER TABLE PLACEMENT Statement \(System Management\)](../../010-SQL-Reference/012-SQL-Statements/alter-system-alter-table-placement-statement-system-management-0715b97.md "Changes table classification and placement settings for table groups.")

[TABLE\_PLACEMENT System View](../021-System-Views/table-placement-system-view-522cc8e.md "Provides table placement information.")

