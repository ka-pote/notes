![[Ite16 2026-02-16 08.23.17.excalidraw]]

1. Course
	- C_id
	- c_name
	- sem
2. Dept
	- d_name
3. Student
	- S_id 
	- s_name
	- yr
	- sem
	- grade
		- gpa (d)
4. Prof
	- P_id
	- P_name
---
D \<offer> C = 1N
S \<take> C = MN
S \<belong to> D = M1
P : C = MN
P \<handle> S = MN
P \<belong to> D = M1
![[Ite16 2026-03-24 09.59.32.excalidraw]]

# Final
## region
- region_code: char(3), pk
- region_name: varchar, !nil
## patent_attorney
- attorney_id: varchar, pk
- attorney_name: varchar, !nil
- firm: varchar, !nil
## applicant
- applicant_no: varchar, pk
- applicant: varchar, !nil
- inventor: varchar, !nil
- assignee: varchar, !nil
## patent_application
- appl_no: varchar, pk
- region_code: char(3), fk (from region) !nil
- applicant_no: varchar, fk (from aplicant) !nil
- appl_date: date, !nil
- document: blob, !nil
- attorney_id: varchar, fk (from patent_attorney) !nil
## pct
- pct_no: varchar, pk
- appl_no: varchar, pfk (from patent_application)
- pct_date: date, !nil
- pct_pub_no: varchar
- pct_pub_date: date
## patent_status
- appl_no: varchar, pfk (from patent_application)
- appl_date: date, fk (from patent_application) !nil
- region_code: char(3) fk (from patent_application) !nil
- pct_no: varchar, fk (from pct)
- status(pending, withdrawn, active, abandoned, expired): enum, !nil
- anticipated_expiry: date !nil
- renewal_date: date
## patent_publication
- appl_no: varchar, pfk (from patent_status)
- patent_pub_no: varchar, pk
- patent_kind_code: char(3), pk
- country_code: char(3), pfk (from patent_status)
- patent_pub_date: date !nil
- attorney_id: varchar fk (from patent_application) !nil
- ipc: char !nil
- ptc_no: varchar fk
- ptc_pub_no: varchar fk