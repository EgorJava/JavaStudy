
/// Современный динамический массив объектов, очень хорошая штука, не использовать если надо  
/// часто удалять или добавлять элементы в середине  
ArrayList<Integer> numbers = new ArrayList<Integer>(List.of(1, 2, 3, 4, 5, 0, 7, 8, 9, 10));  
numbers.remove(7);  
numbers.add(7, 11);  
numbers.set(7, 5);  
for (int num : numbers) {  
    System.out.print(num + " ");  
}  
System.out.println();  
  
/// Динамический массив, хорошая штука, но старая, операции синхронизированы  
Vector<Integer> vector = new Vector<>(numbers);  
vector.remove(7);  
vector.add(7, 11);  
vector.set(7, 5);  
for (int num : vector) {  
    System.out.print(num + " ");  
}  
System.out.println();  
  
/// Очередь, Last in - first out  
Stack st = new Stack();  
st.push(1);  
st.push(2);  
st.push(3);  
System.out.print(st);  
st.pop();  
System.out.print(st);  
  
/// LinkedList это то же самое что ArrayList, но с возможностью стэка, имба полная  
LinkedList<Integer> llist = new LinkedList<>(numbers);  
llist.remove(2);  
llist.add(2, 11);  
llist.set(2, 5);  
llist.push(6);  
llist.pop();  
System.out.println();  
  
/// Map - это пары ключ-значение, HashMap - несинхронизиированная коллекция, есть всё необходимое  
  
Map<Integer, Integer> hmap = new HashMap<>();  
hmap.put(1, 3);  
hmap.put(2, 5);  
hmap.put(3, 6);  
System.out.print(hmap);  
hmap.remove(5);  
System.out.print(hmap);  
  
System.out.println();  
  
/// То же самое что и HashMap,но упорядоченная, тут быстрее работает добавление удаление из середины, но занимает больше места  
  
Map<Integer, Integer> lhmap = new LinkedHashMap<>();  
lhmap.put(1, 3);  
lhmap.put(2, 5);  
lhmap.put(3, 6);  
lhmap.get(2);  
System.out.print(lhmap);  
System.out.print(lhmap.get(3));  
System.out.println();  
  
/// TreeMap - вроде такой же как предыдущий, но основан на деревьях, я не понял, но работает так же  
  
Map<Integer, Integer> tmap = new TreeMap<>();  
tmap.put(1, 3);  
tmap.put(2, 5);  
tmap.put(3, 6);  
System.out.print(tmap);  
tmap.replace(2, 10);  
System.out.print(tmap);  
  
System.out.println();  
  
/// Set - как массив, но с реализацией через Map, просто в качестве ключа используется сам элемент, а значения - пустышка.