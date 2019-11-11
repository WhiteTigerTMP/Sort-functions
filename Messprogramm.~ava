public class Messprogramm{
  int[] a = new int[100];
  public Messprogramm(){
    System.out.println("The numbers are:");
    for (int b = 0;b<a.length ;b++) {
      a[b] = ((int)(Math.random()*100));
      System.out.print(a[b]+ " ");
    }
    System.out.println();
    System.out.println();
    long istart = System.nanoTime();
    insertionsort();
    long iend = System.nanoTime();
    System.out.println("Insertionsort: " + (iend-istart) + "ns");
    for (int x=0; x<a.length; x++) {
      System.out.print(a[x] + " ");
    }
    
    System.out.println();
    long sstart = System.nanoTime();
    selectionsort();
    long send = System.nanoTime();
    System.out.println();
    System.out.println("Selectionsort: " + (send-sstart) + "ns");
    for (int x=0; x<a.length; x++) {
      System.out.print(a[x] + " ");
    }
    
    System.out.println();
    long qstart = System.nanoTime();
    for(int b=0;b<a.length; b++){
      quicksort(a, 0, a.length-1);
    }
    long qend = System.nanoTime();
    System.out.println();
    System.out.println("Quicksort: " + (qend-qstart) + "ns");
    for (int x=0; x<a.length; x++) {
      System.out.print(a[x] + " ");
    }
  }
  public void insertionsort(){
    for(int i=1;i<a.length;i++){
      int elem = a[i];
      int j = i;
      while (j>0 && a[j-1]>elem) { 
        a[j] = a[j-1];
        j--;
      }
      a[j]=elem;                                  
    }
  }
  private void selectionsort(){
    for (int n=0;n<a.length;n++) { 
      int min = n;
      for (int s=n+1; s<a.length;s++) {
        if (a[s]<a[min]) {
          min = s;
        } 
        int x = a[n];
        a[min]=a[n];
        a[min] = x;
      } 
    }
  }
  
  public int partition(int a[], int low, int high){
    int pivot = a[high];
    int i = low-1;
    for (int k=low; k<high;k++){
      if (a[k] <= pivot){
        i++;
        swap(a[i],a[k]);
      }
    }
    swap(a[i+1],a[high]);
    return i+1;
  }
  
  private void quicksort(int a[], int low, int high) {
    if (low<high) {
      int s = partition(a, low, high);
      quicksort(a, low, s-1);
      quicksort(a, s+1, high);
    }
  }
  
  private void swap (int a, int b){
    int c = a;
    a = b;
    b = c;
  } 
  
  public static void main(String[] args){
    new Messprogramm();
  }
}
