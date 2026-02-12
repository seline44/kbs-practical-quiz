# Practical Quiz: Mini Rule-Based Knowledge-Based System (KBS) (Forward Chaining)
Student Details

Name: Seline Atieno Ochieng
Registration Number: 668853

# Brief Description

This project implements a forward-chaining Knowledge-Based System (KBS) in Python to determine campus access.
It represents campus access and safety rules as facts and logical rules. The system automatically infers new facts to decide whether a person is allowed to enter campus.

The system demonstrates:

Forward-chaining reasoning

Rule-based decision-making

Fact inference from multiple conditions

# How to Run

Open kbs_quiz.ipynb

Run all cells sequentially

Observe the inferred facts and the final entry decision

# Base Facts

The KBS starts with the following facts:

-has_student_id

-enrolled_in_university

-fees_cleared

-has_entry_pass

-wears_face_mask

# Rules (IF–THEN)

-IF has_student_id THEN identity_verified

-IF enrolled_in_university THEN student_status_confirmed

-IF identity_verified AND student_status_confirmed THEN basic_clearance

-IF basic_clearance AND fees_cleared THEN financial_clearance

-IF has_entry_pass THEN special_authorization (originality rule)

-IF financial_clearance AND wears_face_mask AND special_authorization THEN entry_granted

# Final Decision Logic

After forward-chaining inference:

If entry_granted exists in the knowledge base → FINAL DECISION: ENTRY GRANTED

Otherwise → FINAL DECISION: ENTRY DENIED

# Inference Process
The KBS repeatedly applies rules until no new facts can be inferred.
During inference, any new fact discovered is printed for transparency.

## Originality
This implementation uses customized fact names (has_student_id, enrolled_in_university, etc.) and an additional originality rule (special_authorization) for enhanced realism and complexity.