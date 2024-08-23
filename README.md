BEGIN TRANSACTION;
CREATE TABLE IF NOT EXISTS "Tbl_product" (
	"id"	INTEGER NOT NULL,
	"sku"	TEXT,
	"nama_product"	TEXT,
	"kategori"	TEXT,
	PRIMARY KEY("id" AUTOINCREMENT)
);
CREATE TABLE IF NOT EXISTS "customer" (
	"id"	INTEGER NOT NULL,
	"nama_pelanggan"	TEXT,
	"alamat"	TEXT,
	"email"	TEXT,
	PRIMARY KEY("id" AUTOINCREMENT)
);
INSERT INTO "Tbl_product" VALUES (1,'KB0001','Keyboard','Asesoris');
INSERT INTO "Tbl_product" VALUES (2,'MO0001','Mouse','Asesoris');
INSERT INTO "Tbl_product" VALUES (3,'MN0001','Monitor','Asesoris');
INSERT INTO "Tbl_product" VALUES (4,'PR0001','Procesor','Asesoris');
INSERT INTO "Tbl_product" VALUES (5,'PR0001','Printer','Pendukung');
INSERT INTO "customer" VALUES (1,'Riski','Taman Krakatau','riski@gmail.com');
INSERT INTO "customer" VALUES (2,'Zahudin','Kopo','zahudin@gmail.com');
INSERT INTO "customer" VALUES (3,'Haris','Temu Putih','haris@gmail.com');
INSERT INTO "customer" VALUES (4,'Nanda','Wadasari','nanda@gmail.com');
INSERT INTO "customer" VALUES (5,'Sarjuni','Cigading','sarjuni@gmail.com');
CREATE VIEW "master" AS SELECT * FROM "main"."Tbl_product"  ORDER BY "sku" DESC;
CREATE VIEW "master1" AS SELECT * FROM "main"."customer";
COMMIT;

