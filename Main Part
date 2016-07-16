import java.util.Scanner;

class Node {
	private Object data; 

	private Node next; 
	public Node() { 
		this(null, null);
	}
public Node(Object data) { 
		this(data, null);
	}
public Node(Object data, Node next) {
		this.data = data;
		this.next = next;
	}
public Object getData() {
		return data;
	}
public Node getNext() {
		return next;
	}
	public void setData(Object data) {
		this.data = data;
	}
public void setNext(Node next) {
		this.next = next;
	}
}


class LinkList {
	private Node head; 

	public LinkList() {
		head = new Node();	}

	public LinkList(int n, boolean Order) throws Exception {
		this();
		if (Order)			create1(n);
		else
		
			create2(n);
	}

	public void create1(int n) throws Exception {
		Scanner sc = new Scanner(System.in);		for (int j = 0; j < n; j++)
						insert(length(), sc.next());	}

	public void create2(int n) throws Exception {
		Scanner sc = new Scanner(System.in); 
		for (int j = 0; j < n; j++)
		
			insert(0, sc.next());
	}
	public void clear() {
		head.setData(null);
		head.setNext(null);
	}

	public boolean isEmpty() {
		return head.getNext() == null;	}

	public int length() {
		Node p = head.getNext();
		int length = 0;
		while (p != null) {
			p = p.getNext();			++length;
		}
		return length;}

	public Object get(int i) throws Exception {
		Node p = head.getNext();		int j = 0;
		while (p != null && j < i) { 
			p = p.getNext();
			++j;
		}
		if (j > i || p == null) { 
			throw new Exception( i + "th unit is not exist");		}
		return p.getData();
	}

	public void insert(int i, Object x) throws Exception {
		Node p = head;		int j = -1; 
		while (p != null && j < i - 1) {			p = p.getNext();
			++j;
		}
		if (j > i - 1 || p == null) 
			throw new Exception("Inserting Position is Improper"); 

		Node s = new Node(x); 
		s.setNext(p.getNext());
		p.setNext(s);
	}


		public void display() {
		Node node = head.getNext();		while (node != null) {
			System.out.print(node.getData() + " ");			node = node.getNext();}
		System.out.println();	}

	public Node getHead() {
		return head;
	}

	public void setHead(Node head) {
		this.head = head;
	}
    public void insert(int  x) {
		Node p = head.getNext();
		Node q = head; 
		int temp;
		while (p != null) {
			temp = ((Integer) p.getData()).intValue();
			if (temp < x) {
				q = p;
				p = p.getNext();
			} else
				break;
		}

		Node s = new Node(x); 
		s.setNext(p);		q.setNext(s);
	}
    public void insert1(int  x) {
		Node p = head.getNext();

		while (p.getNext() != null&&((Integer) p.getNext().getData()).intValue()<x) {
            p = p.getNext();
		}
		Node s = new Node(x);		s.setNext(p.getNext());		p.setNext(s);
	}

	public void reverse() {
		Node p = head.getNext();
		head.setNext(null);
		Node q;
		while (p != null) {
			q = p.getNext();
			p.setNext(head.getNext());
			head.setNext(p);
			p = q;
		}
	}

	public int removeAll(Object x) {
		Node p = head.getNext();
		Node q = head;		int j = 0; 
		while (p != null) {			if (p.getData().equals(x)) {
				q.setNext(p.getNext());
				++j;
			} else
				q = p;
			p = p.getNext();}
		return j;}}


interface IList {
	public void clear();
	public boolean isEmpty(); 
	public int length();	
public Object get(int i) throws Exception;	
public void insert(int i, Object x) throws Exception;
	public void remove(int i) throws Exception; 
	public int indexOf(Object x);	
	public void display();
}




public class nizhi {
	public static void main(String[] args) throws Exception{
		System.out.println("Plz Insert ten values in this Linked List");
		
		LinkList L=new LinkList(10,true);
		System.out.println("The Linked List is：");
		L.display();
		Node x=L.getHead();
		Node p = x.getNext();
		x.setNext(null);
		Node q;
		while (p != null) {
			q = p.getNext();
			p.setNext(x.getNext());
			x.setNext(p);
			p = q;}

			System.out.println("After Reversing ：");L.display();
	}}
