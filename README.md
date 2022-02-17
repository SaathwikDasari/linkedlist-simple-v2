# linkedlist-simpe-v2

A better version of my linkedlist-simple


    #[derive(Debug)]
        struct List {
        elem: u32,
        next: Node
    }

    #[derive(Debug)]
    enum Node {
        Empty,
        NonEmpty(Box<List>)
    }

    fn main() {
        let linked_list = Node::NonEmpty(Box::new(List {
            elem: 1,
            next: Node::Empty
        }));

        println!("{:?}", linked_list);
    }

**Output: NonEmpty(List { elem: 1, next: Empty })**
