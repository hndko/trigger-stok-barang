# Trigger Stok MySQL
In:
- hapusStok : [After-Delete] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok - old.jumlah WHERE tb_barang.barang_id = old.barang_id
- tambahStok : [After-Insert] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok + NEW.jumlah WHERE tb_barang.barang_id = NEW.barang_id
- ubahStokKurang : [After-Update] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok - old.jumlah WHERE tb_barang.barang_id = old.barang_id
- ubahStokTambah : [After-Update] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok + NEW.jumlah WHERE tb_barang.barang_id = NEW.barang_id

Out: 
- AfterDelete: [After-Delete] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok + old.jumlah WHERE tb_barang.barang_id = old.barang_id
- AfterInsert : [After-Insert] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok - NEW.jumlah WHERE tb_barang.barang_id = NEW.barang_id
- AfterUpdateKurang : [After-Update] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok + old.jumlah WHERE tb_barang.barang_id = old.barang_id
- AfterUpdateTambah : [After-Update] UPDATE tb_barang SET tb_barang.stok = tb_barang.stok - NEW.jumlah WHERE tb_barang.barang_id = NEW.barang_id
