������ ��������� ����: 123
---------------------------------------------------------------------
*** ����� ����� � �� ***

** ������ (autob) ��������� = ������� **
bdatetime 		����/�����	INDEX
scales			I[2]		INDEX ������ � �������
auto_num		C[8]
brutto			F
tare	 		F
netto	 		F		������ � �������
cargotype		C[32]
invoice_num		C[16]
invoice_supplier	C[32]
invoice_recipient	C[32]
driver			C[32]
operator		C[32]
send			B		������ � ���������


** ���� (autot) ��������� = ������� **
bdatetime		����/�����	INDEX
auto_num		C[8]		INDEX
scales			I[2]		INDEX ������ � �������
tare			F
driver			C[32]
operator		C[32]
send			B		������ � ���������

---------------------------------------------------------------------
*** ��������� ������-42 ***
SErIAL
	bAUd	9600
	Protoc	Prn1

---------------------------------------------------------------------
*** �������� ������� ��� ***

** ������ **

CREATE TABLE autob (
bdatetime DATETIME,
scales SMALLINT,
auto_num CHAR(8),
brutto FLOAT(16,2),
tare FLOAT(16,2),
netto FLOAT(16,2),
cargotype CHAR(32),
invoice_num CHAR(16),
invoice_supplier CHAR(32),
invoice_recipient CHAR(32),
driver CHAR(32),
operator CHAR(32),
PRIMARY KEY (bdatetime),
KEY (scales));

** ���� **

CREATE TABLE autot (
auto_num CHAR(8),
scales SMALLINT,
tare FLOAT(16,2),
bdatetime DATETIME,
driver CHAR(32),
operator CHAR(32),
PRIMARY KEY (number),
KEY (scales));

