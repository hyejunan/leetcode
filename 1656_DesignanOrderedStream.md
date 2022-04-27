### 1656. Design an Ordered Stream

***Easy***

There is a stream of n (idKey, value) pairs arriving in an arbitrary order, where idKey is an integer between 1 and n and value is a string. No two pairs have the same id.

Design a stream that returns the values in increasing order of their IDs by returning a chunk (list) of values after each insertion. The concatenation of all the chunks should result in a list of the sorted values.

Implement the OrderedStream class:

OrderedStream(int n) Constructs the stream to take n values.
String[] insert(int idKey, String value) Inserts the pair (idKey, value) into the stream, then returns the largest possible chunk of currently inserted values that appear next in the order.

```Java
class OrderedStream {
    int ptr;
    String[] res;

    public OrderedStream(int n) {
        ptr = 0;
        res = new String[n];
    }
    
    public List<String> insert(int idKey, String value) {
        List<String> list = new ArrayList<>();
        res[idKey-1] = value;
        while(ptr<res.length && res[ptr] != null) {
            list.add(res[ptr]);
            ptr++;
        }
        return list;
    }
}
```
Runtime: 73 ms, faster than 80.87% of Java online submissions for Design an Ordered Stream.
Memory Usage: 43.4 MB, less than 94.27% of Java online submissions for Design an Ordered Stream.

