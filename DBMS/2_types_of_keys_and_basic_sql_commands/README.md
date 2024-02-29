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

2. **Candidate Key:**
    - A **candidate key** is minimal of **super key**.
    - **Candidate key** must be a **Super Key**.
    - It is a subset of **Super Key**.
    - | Combination of Attributes | Super Keys                 | Candidate Keys            |
      |---------------------------|----------------------------|---------------------------|
      | f_name, l_name, email     | ✅                        | ❌                        |
      | f_name, email             | ✅                        | ❌                        |
      | f_name, roll_no, d_id     | ✅                        | ❌                        | 
      | email                     | ✅                        | ✅                        | 
      | roll_no, d_id             | ✅                        | ✅                        |
3. **Primary Key:**
    - **A primary key** is selected from candidate key by the database designer.
    - Primary Key must be **unique**.
    - Primary Key cannot be **null**.
    - There must only one primary key in a table.
    - examples:
        - **s_id** can be used a primary key.
        - **m_no** cannot be used as a primary key.
        - | s_id | f_name   | l_name | roll_no | d_id | email             | m_no       |
          |------|----------|--------|---------|------|-------------------|------------|
          | 1    | Akhilesh | Yadav  | 15      | 2    | akilesh@gmail.com | 9823456708 |
          | 2    | Apoorva  | KR     | 30      | 5    | apoorva@gmail.com | 9235856804 |
          | 3    | Mayur    | Yadav  | 15      | 1    | mayur@gmail.com   | 6854357065 |
        
4. **Composite Key:**   
    - A Composite key is a combination of two or more attributes
    - example
        - **{roll_no, d_id}** is an example of composite key.
        - **{f_name, roll_no, d_id}** is not a composite key.