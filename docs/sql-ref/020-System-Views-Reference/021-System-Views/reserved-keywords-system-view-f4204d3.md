<!-- loiof4204d3e6f5b1014ade0e12064d00743 -->

# RESERVED\_KEYWORDS System View

Provides a list of reserved keywords that are not allowed to be used as a simple identifier.



<a name="loiof4204d3e6f5b1014ade0e12064d00743___r_e_s_e_r_v_e_d__k_e_y_w_o_r_d_s_1struct_RESERVED_KEYWORDS"/>

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

RESERVED\_KEYWORD

</td>
<td valign="top">

NVARCHAR\(256\)

</td>
<td valign="top">

Displays the reserved keyword.

</td>
</tr>
</table>



<a name="loiof4204d3e6f5b1014ade0e12064d00743__section_a1c_fbp_dzb"/>

## Additional Information

Unless otherwise specified, system views are available to all users granted the PUBLIC role. The data returned for each view is filtered according to the granted privileges of the user accessing a view. Users granted the CATALOG READ system privilege have unfiltered access to all system views and their data regardless of the PUBLIC role and privilege grants.

**Related Information**  


[Reserved Words](../../010-SQL-Reference/reserved-words-28bcd6a.md "Reserved words are words which have a special meaning to the SQL parser in the SAP HANA database and cannot be used as when defining an identifier.")

