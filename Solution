// you can also use imports, for example:

import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
  public static void main(String[] args) {
    System.out.println(solution(1041));
  }

  public static int solution(Integer N) {
    ArrayList<Integer> binaries = new ArrayList<Integer>();
    Integer n2 = N;
    while (n2 != 0) {
      if (n2 % 2 == 0) {
        binaries.add(0);
        n2 = n2 / 2;
      } else {
        binaries.add(1);
        n2 = n2 / 2;
      }
    }
    String binaries_num = "";
    ArrayList<Integer> binaries_num_array = new ArrayList<Integer>();
    for (int i = binaries.size() - 1; i >= 0; i--) {
      binaries_num += binaries.get(i);
      binaries_num_array.add(binaries.get(i));
    }
    System.out.println(binaries_num);
    return binary_gap(binaries_num_array);
  }

  public static int binary_gap(ArrayList<Integer> binaries_num_array) {
    ArrayList<Integer> gaps = new ArrayList<Integer>();
    for (int x = 0; x < binaries_num_array.size(); x++) {
      System.out.println("x= " + x);
      System.out.println("Start");
      if (binaries_num_array.get(x) == 1) {
        Integer counter = 0;
        Integer y = 0;
        if (y < binaries_num_array.size()) {
          y = x + 1;
        } else {
          break;
        }
        try {
          while (binaries_num_array.get(y) == 0) {
            counter++;
            y++;
            System.out.println(y);
            System.out.println("zero");
          }
          gaps.add(counter);
          x = y - 1;
          System.out.println(x);
          System.out.println("end of zeros");
        } catch (Exception e) {
          System.out.println("error");
        }
      }
    }
    return get_max(gaps);
  }

  public static int get_max(ArrayList<Integer> array) {
    Integer max = 0;
    for (int w = 0; w < array.size(); w++) {
      System.out.println("gabs " + array.get(w));
      if (array.get(w) > max) {
        max = array.get(w);
      }
    }
    return max;
  }

}

