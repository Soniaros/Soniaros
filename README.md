/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */
package todolistawal;

/**
 *
 * @author FTI UNSAP
 */
public class TodoListAwal {

    /**
     * @param args the command line arguments
     */
    
    public static String[]model = new String[10];
    
    public static java.util.Scanner scanner = new java.util.Scanner(System.in);
    
    public static void main(String[] args) {
        // TODO code application logic here
    }/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

    private static String input(String nama) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void viewremovetodolist() {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void showTodoList() {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void addTodoList(String satu) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void addTodoLIst(String tiga) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static void viewShowTodoList() {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

    private static boolean removeTodoList(Integer valueOf) {
        throw new UnsupportedOperationException("Not supported yet."); //To change body of generated methods, choose Tools | Templates.
    }

/**
 *
 * @author FTI UNSAP
 */
public class Todolist {


    //testshowtodolist();
    
    //testremovetodolist();
    
    //testinput();
    
   
    }
    
    public static void showtablelist() {
    
    }
    
    public static void todolist() {
    
    }
    
   
    
    public static void showtodolist() {
    for(int i = 0 ; i < model.length ; i++){
         String todo = model[i];
         int no = i + 1 ;
         
         if(todo != null){
            System.out.println(no+" . "+ todo);
            }
        }
    }
    
    public static void testshowtodolist() {
     for (int i = 0 ; i < 25 ; i++){
         addtodolist("Contoh todo: ke-"+ i );
        }
        showtodolist();
    }
    
    public static void addtodolist(String todo) {
        boolean isFull = true ;
        for (int i = 0 ; i < model.length; i++){
        if (model[i] == null){
            isFull = false ;
            break;
            }
        }
        if (isFull) {
            String[] temp = model ;
            model = new String[model.length * 2];
            
            for (int i = 0 ; i < temp.length ; i++){
                model[i] = temp[i];
                }
            } 
        for ( int i = 0 ; i < model.length ; i++){
        if (model[i] == null){
            model[i] = todo ;
            break;
            }
        }
    }
    
    public static boolean removetodolist(Integer number ) {
        if ((number -1) >= model.length){
            return false;
        } else if(model[number - 1] == null){
            return false;
            }else{
                for (int i = (number - 1); i < model.length ; i++){
                    if (i == (model.length - 1)){
                    model[i] = null ;
                    }else {
                    model[i] = model[i + 1];
                    }
                }
                }
            
        return true;
    }
    
    public static void testremovetodolist(){
        addtodolist("Satu");
        addtodolist("dua");
        addtodolist("tiga");
        addtodolist("empat");
        addtodolist("lima");
        
        boolean result = removetodolist(20);
        System.out.println(result);
        
        result = removetodolist(7);
        System.out.println(result);
        
        result = removetodolist(2);
        System.out.println(result);
        
        showtodolist();
    }
    
     public static void testinput(){
        String name = input ("Nama");
        System.out.println("Hi " + name);
        
        String channel = input ("Channel");
        System.out.println(channel);
    }
     
    public static void viewshowtodolist() {
        System.out.println("MENU : ");
        System.out.println("1. Tambah");
        System.out.println("2. Hapus");
        System.out.println("3. Keluar ");
        
        String input = input("pilih");
        if(input.equals("1")){
        viewaddtodolist();
        }else if (input.equals("2")){
        viewremovetodolist();
        }else if (input.equals("x")){
        }else {
        System.out.println("Pilihan tidak ditemukan");
        }
        
    }
    
    
    public static void viewaddtodolist() {
        while (true) {
            showTodoList();
            
            System.out.println ("Menu :");
            System.out.println("1. Tambah");
            System.out.println("2. Hapus");
            System.out.println("x. Keluar");
            
            String input = input("pilih");
            if (input.equals("1")){
                viewAddTodoList();
            } else if (input.equals("x")){
                viewRemoveTodoList();
            } else if (input.equals("x")){
                break;
            } else {
                System.out.println("Pilihan tidak dimengerti");
            }
        }
    }
    
public static void testViewShowTodoList() {
        addTodoList("Satu");
        addTodoList("Dua");
        addTodoLIst("Tiga");
        addTodoList("Empat");
        addTodoList("Lima)");
        viewShowTodoList();
    }
    /**
     * Menampilkan view menambahkan todo list
     */
    public static void viewAddTodoList() {
        System.out.println("MENAMBAH TODOLIST");
        
        String todo = input("Todo (x Jika Batal)");
        
        if (todo.equals("x")) {
            //batal
        } else {
            addTodoList(todo);
        }
    }
    
    public static void testViewAddTodoList (){
        addTodoList("Satu");
        addTodoList("Dua");
        
        viewAddTodoList();
        
        showTodoList();
    }
    
    public static void viewRemoveTodoList(){
        System.out.println("MENGHAPUS TODOLIST");
        
        String number = input("Nomor yang Dihapus (x Jika Batal)");
        
        if (number.equals("x")) {
            //batal
        } else {
            boolean success = removeTodoList(Integer.valueOf(number));
            boolean succes = false;
            if (!succes) {
                System.out.println("Gagal menghapus todolist : " + number);
            }
        }
    }
    
    public static void testViewRemoveTodoList(){
        addtodolist("Satu");
        addtodolist("Dua");
        addtodolist("Tiga");
        
        showTodoList();
        
        viewRemoveTodoList();
        
        showTodoList();
    }
}
import java.util.HashSet;

/*
 * To change this license header, choose License Headers in Project Properties.
 * To change this template file, choose Tools | Templates
 * and open the template in the editor.
 */

/**
 *
 * @author user
 */
public class Hashset {

    /**
     * @param args the command line arguments
     */
    public static void main(String[] args) {
        // TODO code application logic here

HashSet<String> set = new HashSet<String>();
set.add("Eko");
        set.add("Kurniawan");
        set.add("saeppani"); 
      set.add("Eko");
        set.add("Kurniawan");
      set.add("saeppani");
      set.add("Eko");
      set.add("Kurniawan");
      set.add("saeppani");
        
      for(String value : set){
            System.out.println(value);
        }

    }
    }
    


run:
Kurniawan
Eko
saeppani
BUILD SUCCESSFUL (total time: 0 seconds)
