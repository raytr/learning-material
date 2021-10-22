HASH FUNCTION
    1. What is a Hash Function?\
     any function that can be used to map data of arbitrary size to fixed-size values.

HASH TABLE
1. What is Hash Table?  
        a data structure which maps keys to values.\
        format:  array of slots (buckets).\
        hash table uses hash functions to compute an index (hashcode) from key.


2. What is the complexity of a Hash Table?
    ![complexity](https://user-images.githubusercontent.com/91000353/138256644-e1855158-0b3e-415c-8049-690bb2f6eda9.png)
    - space complexity: O(n)
    - time complexity: O(1) - O(n)\
        Open addressing: 
        - insert: O(1)
        - search: O(1) - O(n)
        - delete: O(n)\
        Chaining method: O(n)

3. When worst case happen?\
    Search: when all the keys on the same slot O(n).

4. Explain in simple terms how Hash Tables are implemented?\
    Open addressing:\
        insert:\
            compose the index by hash function\
            => if the index is fiiled, PROBING until found the empty/delete slot\
            => insert value into this index 

        search:
            keep probing until:
                - encounter the key => return value
                - meet empty slot => return not found
        
        delete
            mart table is delete

    Chaining method:
        inserch: key = hash(value) => slot[key].push(value) => O(1)
        search: search in linked list => O(1) -> O(n)(when all key in the same slot)
        delete: delete key in linked list -> O(n)

5. Hash Collision?
    is a problem when 2 key generate the same hash value
   How to prevent?
    each slot of the table is linked list

6. What is load factor? 
    measure how full is the hash table
   When do we extend the hashtable size?
    if hash table has 100 slots and 70 slots is filled => load factor = 70% => double size of hash table


7. Differentiate hashing, encoding and encryption? When to use what?
    ![hee](https://user-images.githubusercontent.com/91000353/138256785-55bab666-7305-4e13-a3af-231fe29c9016.png)

8. Why search in hashtable is O(1) on average?
    n: keys stored in the hash table
    m: slots in the hash table
    complexity: O(n/m) ~ O(1)
