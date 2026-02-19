/*
 * Click `Run` to execute the snippet below!
 */

import java.io.*;
import java.util.*;

/*
 * To execute Java, please define "static void main" on a class
 * named Solution.
 *
 * If you need more classes, simply define them inline.
 */

class Solution {
  public static String findTopIpaddress(String[] lines) {
    if(lines == null || lines.length == 0)
      return "";
    Map<String, Integer> freqMap = new HashMap<>();
    for(String line : lines) {
      if(line == null || line.trim().isEmpty())
        continue;
      String ip = line.split(" ")[0].trim();
      freqMap.put(ip, freqMap.getOrDefault(ip, 0)+1);
      }
      if(freqMap.isEmpty())
        return "";
      Integer maxFreq = 0;
      for(Integer freq: freqMap.values())
      {
        maxFreq = Math.max(maxFreq, freq);
      }
      List<String> topIps = new ArrayList<>();
      for(String ip: freqMap.keySet())
      {
        if(maxFreq == freqMap.get(ip));
        topIps.add(ip);
      }
      Collections.sort(topIps);
    return String.join(",", topIps);
  }
  public static void main(String[] args) {
    // Test case 1 (given in question)
        String[] lines1 = {
            "10.0.0.1 - log entry 1 11",
            "10.0.0.1 - log entry 2 213",
            "10.0.0.2 - log entry 133132",
            "10.0.0.2 - log entry 133132"
        };
        System.out.println(findTopIpaddress(lines1));  
        // Expected: "10.0.0.1,10.0.0.2"

        // Test case 2: Ek hi top
        String[] lines2 = {
            "192.168.1.1 abc",
            "192.168.1.1 def",
            "10.10.10.10 ghi",
            "192.168.1.1 jkl"
        };
        System.out.println(findTopIpaddress(lines2));  
        // Expected: "192.168.1.1"

        // Test case 3: Multiple ties
        String[] lines3 = {
            "1.1.1.1 a",
            "2.2.2.2 b",
            "3.3.3.3 c",
            "1.1.1.1 d",
            "2.2.2.2 e",
            "3.3.3.3 f"
        };
        System.out.println(findTopIpaddress(lines3));  
        // Expected: "1.1.1.1,2.2.2.2,3.3.3.3"

        // Test case 4: Empty / invalid
        System.out.println(findTopIpaddress(new String[]{}));  // ""
  }
}
