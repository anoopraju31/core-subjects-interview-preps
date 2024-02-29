# Types of Keys and Basics SQL Commands

### Keys
- Keys are combination of attributes that uniquely indentity each tuples/row/record.
- Total Combination = **2<sup>n</sup> - 1**, where **n** number of rows

#### Types of keys
1. **Super Keys:**
    - Key are combination of attributes that uniquely identify each **tuple/row/record**.
    - It may contains some extra attributes than necessary.
    - | Combination of Attributes | Super Keys                 |
      |---------------------------|----------------------------|
      | f_name                    | ❌                        |
      | f_name, l_name            | ❌                        |
      | f_name, l_name, email     | ✅                        |
      | f_name, email             | ✅                        |
      | f_name, roll_no,          | ❌                        | 
      | f_name, roll_no, d_id     | ✅                        | 
      | email                     | ✅                        |
      | roll_no, d_id             | ✅                        |
