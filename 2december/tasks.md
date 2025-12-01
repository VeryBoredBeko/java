# **Техническое задание: Простые задания на Generics**

## **Инструкция для студентов**

1. Все задания выполняются на **Java**.
2. Для каждой задачи создайте отдельный класс.
3. В каждом классе используйте **Generics** (`<T>`, `<T, U>`).
4. Проверяйте работу классов через `main()` или тестовые примеры.

---

### **Задача 1. Box**

**Описание:** Класс для хранения одного значения любого типа.
**Требования:**

* Поле `value` типа `T`.
* Методы: `set(T value)` и `get()`.
  **Пример использования:**

```java
Box<String> box = new Box<>();
box.set("Hello");
System.out.println(box.get()); // Hello
```

---

### **Задача 2. Pair**

**Описание:** Класс, который хранит два значения разных типов.
**Требования:**

* Поля: `first` (T), `second` (U).
* Методы: `getFirst()`, `getSecond()`, `setFirst(T value)`, `setSecond(U value)`.
  **Пример:**

```java
Pair<String, Integer> p = new Pair<>("Age", 20);
System.out.println(p.getFirst()); // Age
System.out.println(p.getSecond()); // 20
```

---

### **Задача 3. Storage**

**Описание:** Класс для хранения списка объектов одного типа.
**Требования:**

* Внутри `ArrayList<T> items`.
* Методы: `add(T item)`, `T get(int index)`, `int size()`.
  **Пример:**

```java
Storage<String> storage = new Storage<>();
storage.add("Apple");
System.out.println(storage.get(0)); // Apple
```

---

### **Задача 4. Container**

**Описание:** Класс для хранения одного объекта с методом печати.
**Требования:**

* Поле `item` типа `T`.
* Методы: `set(T item)`, `get()`, `printValue()` (выводит значение на экран).
  **Пример:**

```java
Container<Integer> c = new Container<>();
c.set(42);
c.printValue(); // 42
```

---

### **Задача 5. Repository**

**Описание:** Класс для хранения коллекции объектов.
**Требования:**

* Поле `List<T> items`.
* Методы: `add(T item)`, `List<T> getAll()`.
  **Пример:**

```java
Repository<String> repo = new Repository<>();
repo.add("Book");
System.out.println(repo.getAll()); // [Book]
```

---

### **Задача 6. Node**

**Описание:** Класс для создания простой связанной структуры.
**Требования:**

* Поля: `value` (T), `next` (Node<T>).
* Методы: `setNext(Node<T> next)`, `getNext()`, `getValue()`.
  **Пример:**

```java
Node<String> n1 = new Node<>("A");
Node<String> n2 = new Node<>("B");
n1.setNext(n2);
System.out.println(n1.getNext().getValue()); // B
```

---

### **Задача 7. KeyValue**

**Описание:** Класс для хранения пары ключ-значение.
**Требования:**

* Поля: `key` (K), `value` (V).
* Методы: `getKey()`, `getValue()`, `setKey(K key)`, `setValue(V value)`.
  **Пример:**

```java
KeyValue<String, Integer> kv = new KeyValue<>("Score", 100);
System.out.println(kv.getKey()); // Score
System.out.println(kv.getValue()); // 100
```

---

### **Задача 8. Stack**

**Описание:** Класс для хранения элементов как стек.
**Требования:**

* Поле: `List<T> items`.
* Методы: `push(T item)`, `T pop()`, `T peek()`, `int size()`.
  **Пример:**

```java
Stack<String> stack = new Stack<>();
stack.push("First");
System.out.println(stack.peek()); // First
```

---

### **Задача 9. ItemHolder**

**Описание:** Класс для хранения одного элемента с проверкой на пустоту.
**Требования:**

* Поле `item` типа `T`.
* Методы: `set(T item)`, `get()`, `isEmpty()` возвращает true, если `item == null`.
  **Пример:**

```java
ItemHolder<Integer> holder = new ItemHolder<>();
System.out.println(holder.isEmpty()); // true
holder.set(10);
System.out.println(holder.get()); // 10
```

---

### **Задача 10. ContainerPair**

**Описание:** Класс для хранения двух объектов разных типов с возможностью поменять их местами.
**Требования:**

* Поля: `first` (T), `second` (U).
* Методы: `swap()` меняет местами `first` и `second`.
  **Пример:**

```java
ContainerPair<String, Integer> pair = new ContainerPair<>("A", 1);
pair.swap();
System.out.println(pair.getFirst()); // 1
System.out.println(pair.getSecond()); // A
```
