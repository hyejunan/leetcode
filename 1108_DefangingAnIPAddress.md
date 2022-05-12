### 1108. Defanging an IP Address

***Easy***

Given a valid (IPv4) IP address, return a defanged version of that IP address.

A defanged IP address replaces every period "." with "[.]".

```Java
class Solution {
    public String defangIPaddr(String address) {
        return address.replace(".","[.]");
    }
}
```
Runtime: 1 ms
Memory Usage: 41.9 MB
