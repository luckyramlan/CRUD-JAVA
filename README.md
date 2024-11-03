# CRUD-JAVA
//Apk Perpustakaan 

package CRUD;

import java.io.BufferedReader;
import java.io.BufferedWriter;
import java.io.File;
import java.io.FileReader;
import java.io.FileWriter;
import java.io.IOException;
import java.time.Year;
import java.util.Arrays;
import java.util.Scanner;
import java.util.StringTokenizer;


public class main {
    public static void main(String[] args)throws IOException {
                Scanner InputConsole = new Scanner(System.in);
                String InputanUser;
                Boolean IsLanjutkan = true;
                
                //Menampilkan Data Perpustakaan 
                while (IsLanjutkan) {
                tampilData("");
                System.out.print("Masukan pilihan anda : ");
                InputanUser = InputConsole.nextLine();
                System.out.println("");
                System.out.println("");
                

                    
                switch (InputanUser) {
                    case "1":
                        // Data yang di tampilkan 
                        System.out.println("\t\t\t\t\t =====================");
                        System.out.println("\t\t\t\t\t  DAFTAR SELURUH BUKU ");
                        System.out.println("\t\t\t\t\t =====================");
                        System.out.println("");
                        databuku();
                        break;
                    case "satu":
                        // Data yang di tampilkan 
                        System.out.println("\t\t\t\t\t =====================");
                        System.out.println("\t\t\t\t\t  DAFTAR SELURUH BUKU ");
                        System.out.println("\t\t\t\t\t =====================");
                        System.out.println("");
                        databuku();
                        break;
                    case "daftar data buku":
                        System.out.println("\t\t\t\t\t =====================");
                        System.out.println("\t\t\t\t\t  DAFTAR SELURUH BUKU ");
                        System.out.println("\t\t\t\t\t =====================");
                        System.out.println("");
                        databuku();
                        break;    
                    case "2":
                        // Data yang di tampilkan 
                        System.out.println("\t\t\t\t\t===================");
                        System.out.println("\t\t\t\t\t MENCARI DATA BUKU  ");
                        System.out.println("\t\t\t\t\t===================");
                        System.out.println("");
                        CariDataBuku();
                        break;
                    case "dua":
                        // Data yang di tampilkan 
                        System.out.println("\t\t\t\t\t===================");
                        System.out.println("\t\t\t\t\t MENCARI DATA BUKU  ");
                        System.out.println("\t\t\t\t\t===================");
                        System.out.println("");
                        CariDataBuku();
                        break;
                    case "cari data buku":
                        System.out.println("\t\t\t\t\t===================");
                        System.out.println("\t\t\t\t\t MENCARI DATA BUKU  ");
                        System.out.println("\t\t\t\t\t===================");
                        System.out.println("");
                        CariDataBuku();
                        break;
                    case "3":
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("\t\t\t\t\t MENAMBAH DATA BUKU  ");
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("");
                        tambahData();
                        databuku();
                        break;
                    case "tiga":
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("\t\t\t\t\t MENAMBAH DATA BUKU  ");
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("");
                        tambahData();
                        databuku();
                        break;
                    case "tambah data buku":
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("\t\t\t\t\t MENAMBAH DATA BUKU : ");
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("");
                        tambahData();
                        databuku();
                        break;    
                    case "4":
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("\t\t\t\t\tMENGUBAH DATA BUKU : ");
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("");
                        UbahData();
                        break;
                        case "empat":
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("\t\t\t\t\tMENGUBAH DATA BUKU : ");
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("");
                        UbahData();
                        break;
                        case "ubah data buku":
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println( "\t\t\t\t\tMENGUBAH DATA BUKU : ");
                        System.out.println("\t\t\t\t\t====================");
                        System.out.println("");
                        UbahData();
                        break;    
                        case "5":
                        System.out.println("\t\t\t\t\t=====================");                
                        System.out.println( "\t\t\t\t\tMENGHAPUS DATA BUKU : ");
                        System.out.println("\t\t\t\t\t=====================");                
                        System.out.println("");
                        Deletdata();
                        break;
                        case "lima":
                        System.out.println("\t\t\t\t\t=====================");                
                        System.out.println( "\t\t\t\t\tMENGHAPUS DATA BUKU : ");
                        System.out.println("\t\t\t\t\t=====================");                
                        System.out.println("");
                        Deletdata();
                        break;
                        case "hapus data buku":
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println( "\t\t\t\t\tMENGHAPUS DATA BUKU : ");
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println("");
                        Deletdata();
                        break;    
                        case "Keluar Dari Program":
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println( "\t\t\t\t\tKELUAR DARI PROGRAM : ");
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println("");
                        Exit();
                        break;
                        case "6":
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println( "\t\t\t\t\tKELUAR DARI PROGRAM : ");
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println("");
                        Exit();
                        break;
                        case "enam":
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println( "\t\t\t\t\tKELUAR DARI PROGRAM : ");
                        System.out.println("\t\t\t\t\t=====================");
                        System.out.println("");
                        Exit();
                        break;
                        default:
                        System.err.println("inputan yang anda masukan salah coba ulang kembali !");
                        break;
                }   
                    System.out.println("");
                    IsLanjutkan =dataPilihan("\nApakah mau ulang program (ya / tidak) : ");
                    
                }
                
                System.out.println("\n\n== INI ADALAH AKHIR DARI PROGRAM DATABASE BUKU ! --\n\n");
                
    }
            private static void tampilData (String message){
                message="Silakan pilih anda akan melakukan apa ";
                System.out.print("\n"+message);
                System.out.println("\n");
                    System.out.println("\t ==============================");
                System.out.println("\t|  Ini Adalah Daftar Pustaka  |\n\t|=============================|");
                System.out.println("\t|    1. Daftar Data Buku      |");
                System.out.println("\t|    2. Cari Data Buku        |");
                System.out.println("\t|    3. Tambah Data Buku      |");
                System.out.println("\t|    4. Ubah Data Buku        |");
                System.out.println("\t|    5. Hapus Data Buku       |");
                System.out.println("\t|    6. Keluar Dari Program   |");
                System.out.println("\t ==============================");
                System.out.println("");
            }

            private static void databuku ()throws IOException{ 
                    System.out.println(" ==============================================================================================================");
                    System.out.println("| No  | Tahun Terbit   | Nama Penerbit       |  Media Penerbit       |              Judul Buku                 ");
                    System.out.println("===============================================================================================================");
                    FileReader fileInput ;
                    BufferedReader buffdata;
                    fileInput =new FileReader("C:\\java tutorial\\src\\com\\CRUD\\DataBase.txt");
                    buffdata=new BufferedReader(fileInput);
                    try{

                        }catch(Exception e){
                            System.err.println("data tidak ditemukan");
                            System.err.println("Silahkan isi data terlebih dahulu");
                            tambahData();
                        }
                        String Data =buffdata.readLine();
                        // System.out.println(Data);
                        int angka=0;
                        try{
                        while (Data != null) {
                            angka++;
                            StringTokenizer stringToken = new StringTokenizer(Data,",");
                            stringToken.nextToken();
                            System.out.printf("| %-2d  ",angka); /*ini untuk angka  */
                            System.out.printf("|     %4s       ",stringToken.nextToken());/*untuk tahun terbit */
                            System.out.printf("| %-15s     ",stringToken.nextToken());/*untuk nama penerbit */
                            System.out.printf("|  %-10s           ",stringToken.nextToken());/*untuk media penerbit */
                            System.out.printf("|        %-10s",stringToken.nextToken());/*untuk juful buku */
                            System.out.println("");
                            System.out.println("===============================================================================================================");
                            Data = buffdata.readLine();
                        }
                        }catch(Exception e){
                            System.out.print("");
                        }
                        System.out.println("");
                        // Tutup Data
                        fileInput.close();
            }

            private static void CariDataBuku ()throws IOException{
              
                // membaca database 
                
                try{
                    File file = new File("DataBase.txt");
                }catch(Exception e){
                    System.out.println("Database tidak ditemukan ! ");
                    System.out.println("Silakan isi Database terlebih dahulu ");
                    return;
                }
                // ambil keyword dari user 
                Scanner inputconsole = new Scanner(System.in);
                System.out.print("Masukan judul buku : ");
                String cariJudul =inputconsole.nextLine();
                String [] keywords = cariJudul.split("\\s+");
                
                pencarian(keywords,true);
            }
            
            private static boolean pencarian(String [] keywords,boolean isDisplay)throws IOException{
                // Baca file 
                FileReader filecari = new FileReader("C:\\java tutorial\\src\\com\\CRUD\\DataBase.txt");
                BufferedReader buffpencari = new BufferedReader(filecari);
                String dabes= buffpencari.readLine();
                
                // Buat perulangan untuk membaca semua data 
                boolean isexist=false;

                isDisplay=true;

                if (isDisplay){
                    System.out.println(" ==============================================================================================================");
                    System.out.println("| No  | Tahun Terbit   | Nama Penerbit       |  Media Penerbit       |        Judul Buku                 ");
                    System.out.println("===============================================================================================================");
                }
                // jika data ada maka jalankan ini 
                int jumdatAD = 0;
                while (dabes != null) {
                        isexist= true;
                        // cek keyword didalam baris 
                        for (String baru : keywords){
                            isexist =isexist && dabes.toLowerCase().contains(baru.toLowerCase());
                        }
                        // jika data ada akan di print sesuai data 
                        if (isexist){
                                if (isDisplay) {
                                    jumdatAD++;
                                    StringTokenizer stringToken = new StringTokenizer(dabes,",");
                                    stringToken.nextToken();
                                    System.out.printf("| %-2d  ",jumdatAD); /*ini untuk angka  */
                                    System.out.printf("|     %4s       ",stringToken.nextToken());/*untuk tahun terbit */
                                    System.out.printf("| %-15s     ",stringToken.nextToken());/*untuk nama penerbit */
                                    System.out.printf("|  %-10s           ",stringToken.nextToken());/*untuk media penerbit */
                                    System.out.printf("|        %-10s",stringToken.nextToken());/*untuk juful buku */
                                    System.out.println("");
                                }else{
                                    break;    
                                }
                            }
                            dabes = buffpencari.readLine(); 
                        }
                        if (isDisplay){
                            System.out.println("===============================================================================================================");
                        }
            // jika is exist false maka tambah data buku terlebih dahulu 
            buffpencari.close();
            return isexist;
        }

            private static void tambahData ()throws IOException{
                // membuka file writer untuk menulis 

                FileWriter filewriter = new FileWriter("C:\\java tutorial\\src\\com\\CRUD\\DataBase.txt",true);
                BufferedWriter buffwrite = new BufferedWriter(filewriter);
                
                Scanner inputconsole = new Scanner(System.in); 
                String penulis,judul,penerbit,tahun;
            
                System.out.print("Masukan nama penulis : ");
                penulis= inputconsole.nextLine();
                System.out.print("Masukan judul buku : ");
                judul= inputconsole.nextLine();
                System.out.print("Masukan nama penerbit : ");
                penerbit= inputconsole.nextLine();
                System.out.print("Masukan tahun terbit : ");
                tahun = ambiltahun();
                System.out.println("");

                // cek buku di database 
                
                String [] keywords = {tahun+","+penulis+","+penerbit+","+judul};
                System.out.println(Arrays.toString(keywords));
                
                boolean isexist = pencarian(keywords, true);
                System.out.println("");

                // menulis buku di database
                if (!isexist){
                    long nomorEntry = ambilEntryPertahun(penulis, tahun)+1;
                    String penulisTanpaSepasi = penulis.replaceAll("\\s+", "");
                    String primaryKey = penulisTanpaSepasi+"_"+tahun+"_"+nomorEntry;
                    System.out.println("Data yang akan anda masukan adalah ");
                    System.out.println("====================================");
                    System.out.println("primayKey    = "+ primaryKey);
                    System.out.println("Tahun terbit = "+ tahun);
                    System.out.println("Penulis      = "+ penulis);
                    System.out.println("Judul        = "+   judul);
                    System.out.println("Penerbit     = "+ penerbit);
                    
                    boolean istambah = dataPilihan("Apakah kamu ingin menambahkan data buku tersebut ? (ya / tidak ) : ");
                    System.out.print(isexist);
                    if (istambah){
                        buffwrite.write(primaryKey+","+tahun+","+penulis+","+penerbit+","+judul);
                        buffwrite.newLine();
                        buffwrite.flush();
                    
                    } else{
                    System.out.println("Data yang anda tambahkan sudah ada dalam database ");
                    pencarian(keywords,false);
                }
                }    
                buffwrite.close();
                filewriter.close();
            }    
            
            private static long ambilEntryPertahun (String penulis, String tahun)throws IOException{
                FileReader fileinput = new FileReader("C:\\java tutorial\\src\\com\\CRUD\\DataBase.txt");
                BufferedReader BuffInput = new BufferedReader(fileinput);
                long entry = 0;
                String data = BuffInput.readLine();
                Scanner dataScanner;
                String primarykey;
                while (data!= null) {
                    dataScanner= new Scanner(data);
                    dataScanner.useDelimiter(",");
                    primarykey= dataScanner.next();
                    dataScanner = new Scanner(primarykey);
                    dataScanner.useDelimiter("_");
                    penulis= penulis.replaceAll("\\s+", "");
                    if (penulis.equalsIgnoreCase(dataScanner.next())&& tahun.equalsIgnoreCase(dataScanner.next())){
                        entry=dataScanner.nextInt();
                    }    
                    data = BuffInput.readLine();
                }    
                BuffInput.close();
                return entry;
            }    

            private static String ambiltahun()throws IOException{
                    boolean tahunValid = false;
                    Scanner inputconsole = new Scanner(System.in);
                    String thunInput = inputconsole.nextLine(); 
                    while (!tahunValid) {
                        try{
                        Year.parse(thunInput);
                        tahunValid = true;
                    }catch(Exception e){
                        System.err.println("Tahun tidak sesuai dengan data (YYYY) ");
                        System.out.print("Masukan tahun terbit kembali (YYYY) : ");
                        tahunValid = false;
                        thunInput = inputconsole.nextLine();
                    }
                }
                return thunInput;
                
            }
  
            private static boolean dataPilihan (String Message){
                System.out.print(Message);
                Scanner InputConsole = new Scanner(System.in);
                String InputanUser =InputConsole.nextLine();

        // ini untuk menegaskan pilihan 
                while (!InputanUser.equalsIgnoreCase("ya")&&!InputanUser.equalsIgnoreCase("tidak")) {
                    System.out.println("Inputan yang anda masukan bukan ya / tidak ");
                    System.out.print(Message);
                    InputanUser =InputConsole.nextLine();
                }

                return InputanUser.equalsIgnoreCase("ya");


        }  

            private static void Deletdata() throws IOException{
                // mengambil datta base ori 
                File dataB = new File("C:\\java tutorial\\src\\com\\CRUD\\DataBase.txt");
                FileReader Finput = new FileReader(dataB);
                BufferedReader Binput = new BufferedReader (Finput);

                //Buat data base sementara

                File tdb = new File("C:\\java tutorial\\src\\com\\CRUD\\tdb.txt");
                FileWriter Foutput = new FileWriter(tdb);
                BufferedWriter BW = new BufferedWriter(Foutput);

                //tampilkan data yang di punya di data base 

                System.out.println(" Ini adalah list buku yang ada : ");
                databuku();
                //Pilih yang akan di hapus 
                Scanner inputU = new Scanner(System.in);
                System.out.print(" Masukan nomer buku yang akan di Hapus : ");
                int inputus =inputU.nextInt();


                // Lakukan Loop untuk membaca sekaligus memindahkan data 

                int nomerdata = 0;
                Boolean isfound =true;
                String data = Binput.readLine();
                
                while (data != null) {
                    nomerdata++;
                    boolean isdelet = false;
                    StringTokenizer ST = new StringTokenizer(data,",");

                    // tampilkan data yang ingin di hapus 
                    
                    if (inputus == nomerdata){
                        System.out.println("\nData yang ingin anda hapus adalah : ");
                        System.out.println("_________________________\n");                        
                        System.out.println("Refernsi : "+ST.nextToken());                        
                        System.out.println("Tahun    : "+ST.nextToken());                        
                        System.out.println("Penulis  : "+ST.nextToken());                        
                        System.out.println("Penerbit : "+ST.nextToken());                        
                        System.out.println("Judul    : "+ST.nextToken());

                        System.out.println("_________________________");                        

                        isfound = false;

                        //buat pernyataan untuk hapus atau tidak agar tidak otomatid terhapus 
                        isdelet = dataPilihan("Apakah anda yakin ingin menghapus? (Ya / Tidak) : ");
                    }
                    if (!isfound){
                        System.out.println("Data Buku tidak ditemukan ");
                    }
                    
                    if (isdelet){
                        System.out.println("Data Berhasil di hapus ");
                    }else{
                        BW.write(data);
                        BW.newLine();


                    }
                    data = Binput.readLine();
                }
                // Untuk menulis data 
                BW.flush();
                dataB.delete();
                tdb.renameTo(dataB);

                
            }

            private static void UbahData ()throws IOException{
                
                //buat database untuk melihat data 
                File dataB = new File("C:\\java tutorial\\src\\com\\CRUD\\DataBase.txt");
                FileReader Finput = new FileReader(dataB);
                BufferedReader Binput = new BufferedReader (Finput);

                //buat database sementara
                File tdb = new File("C:\\java tutorial\\src\\com\\CRUD\\tdb.txt");
                FileWriter Foutput = new FileWriter(tdb);
                BufferedWriter BW = new BufferedWriter(Foutput);

                //Menampilkan data 

                System.out.println("Ini adalah data buku yang ada : ");
                databuku();

                //mengambil user input 
                Scanner Userinput= new Scanner(System.in);
                System.out.print("Masukan nomer list buku yang akan di ubah :");
                int updateNum =Userinput.nextInt();

                //tamppilkan data yang di update 
                String data = Binput.readLine();
               int entrycounts = 0;

                while (data != null) {
                    entrycounts ++;
                    StringTokenizer st=new StringTokenizer(data,",");

                   //menampilkan semua data yang akan di ubah   
                    if (updateNum == entrycounts){
                        if (st.hasMoreTokens()){

                            System.out.println("\nData yang ingin anda ubah adalah : ");
                            System.out.println("_________________________\n");                        
                            System.out.println("Refernsi : "+st.nextToken());                        
                            System.out.println("Tahun    : "+st.nextToken());                        
                            System.out.println("Penulis  : "+st.nextToken());                        
                            System.out.println("Penerbit : "+st.nextToken());                        
                            System.out.println("Judul    : "+st.nextToken());
                            
                            System.out.println("_________________________");                        
                            //update data 
                            
                        }
                            //Mengambil Input user baru 
                            String [] fildsData = {"tahun","penulis","penerbit","judul"};
                            String [] TempData = new String[4];    
                            
                              // refres token 
                            st=new StringTokenizer(data,",");
                            String Originaldata =st.nextToken();
                            
                             for (int i = 0 ; i < fildsData.length; i++){
                                Boolean IsUpdate=dataPilihan("Apakah anda akan merubah data "+fildsData[i]+" (Ya / Tidak): ");
                                // st=new StringTokenizer(fildsData[i]);
                                Originaldata=st.nextToken();
                            if (IsUpdate){
                                Userinput= new Scanner(System.in);
                                System.out.print("Masukan "+fildsData[i]+" Baru : ");
                                TempData[i]=Userinput.nextLine();
                            }else{
                                // System.out.println("Data nomer buku yang anda masukan tidak ada ");
                                TempData[i]=Originaldata;
                            }
                        }
                        
                        // Menampilkan data baru 

                        System.out.println(Arrays.toString(TempData));
                        st=new StringTokenizer(data,",");
                        st.nextToken();
                        //menampilkan data baru 
                        System.out.println("\nData yang Sudah di ubah : ");
                        System.out.println("_________________________\n");                        
                        System.out.println("Tahun    : "+st.nextToken()+"\t===> "+TempData[0]);                        
                        System.out.println("Penulis  : "+st.nextToken()+"\t===> "+TempData[1]);                        
                        System.out.println("Penerbit : "+st.nextToken()+"\t===> "+TempData[2]);                        
                        System.out.println("Judul    : "+st.nextToken()+"\t===> "+TempData[3]);

                        System.out.println("_________________________");
                        Boolean IsUpdate=dataPilihan("Apakah anda ingin mengubah data buku tersebut (Ya / Tidak)");

                        if (IsUpdate){
                            // mengupdate data yang ada di database 
                            
                            // Cek data terlebih dahulu 
                            Boolean isexist = pencarian(TempData, false);
                            if (isexist){
                                System.err.println("Data Buku sudah ada di data base \nProses Ubah data DiBATALKAN");
                            }else{

                                // Format data baru ke data base 
                                String tahun = TempData[0];
                                String penulis = TempData[1];
                                String penerbit = TempData[2];
                                String judul = TempData[3];
                                    long nomorEntry = ambilEntryPertahun(penulis, tahun)+1;
                                   String penulisTanpaSepasi = penulis.replaceAll("\\s+", "");
                                String primaryKey = penulisTanpaSepasi+"_"+tahun+"_"+nomorEntry;

                                // Tulis data e data base 

                                BW.write(primaryKey+","+tahun+","+penulis+","+penerbit+","+judul);
                            }


                        }else{
                            BW.write(data);
                        }
                        
                    }else{
                    //copy data
                    BW.write(data);
                }
                    BW.newLine();
                    data= Binput.readLine();
        }           
                    BW.flush();
      
    }

            private static void Exit()throws IOException{
                System.out.println(" KELUAR DARI PROGRAM ? ");
                
    }
}
