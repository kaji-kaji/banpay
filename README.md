import java.util.*;

public class Main {
    public static void main(String args[] ) throws Exception {
        Scanner sc = new Scanner(System.in);
       
        int b=sc.nextInt(),n=sc.nextInt(),i;    //bは登録数、nは検索したい数、iはループ用。
       
        int[] a = new int[b+1];     //番兵分として+１しておく
       
        for(i=0;i<b;i++)
            a[i]=i;                 //配列の入力    0~b-1まで登録されている。
       
        a[b]=n;                     //番兵  探したい番号を入れておく。
                                    //また、配列は[10]と入力すると[0]~[9]まで作られているため、[b+1]ではなく[b]になる。
       
        for(i=0;;i++)               //番兵を使えば、最大何個かをいちいち確認せずとも大丈夫になる。
            if(n==a[i])             //もし一致した場合にbreak。
                break;
       
        if(i<b)                     //最初に指定した数よりループの試行回数が多いかどうかを確かめる。
        System.out.println("見つかりました");
        else
            System.out.println("見つかりませんでした");
    }
}
