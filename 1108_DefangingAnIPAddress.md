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
