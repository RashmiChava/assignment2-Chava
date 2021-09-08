# assignment2-Chava
# Rashmi Chava
###### Hyderabad

My favourite place is Hyderabad. The state is famous for its beauty as well as affluence. The Mughals conquered Hyderabad. Hyderabad is famous and is known for its food that is **Hyderabadi Biriyani**. And most people love food. In Hyderabad, the majority is Muslim, and that is the reason why Hyderabadi Biriyani is famous. The town is known for its monuments, including the fort of **Golconda** and the marvellous **Charminar**.Before some years, the state was called Baghnagar,and later on, it was changed into the name Hyderabad.

***

###### Directions from Maryville to Hyderabad
1. Travel from Maryville to kansas
2. Kansas to Chicago
3. Chicago to Hyderabad
  - Cameras
  - food

  **[Bio](AboutMe.md)**

  # Food Recommendations
  | Food Items         | Location      | Cost          |
  | :---               |    :----:     |          ---: |
  | Hyderabadi Biryani | Hyderabad     | 4$ - 6$       |
  | Thick Shake        | Telangana     | 3$ - 5$       |
  | Dal with Avakai    | India         | 5$ - 10S      |
  | Bamboo Chciken     | AndhraPradesh | 7$ - 11$      |

  # Quotes
  > Do good and good will come to you
  >
  > Be positive. Be true. Be kind
  >
  *Roy T. Bennett*

  # Disjoint-set data structure algorithm
  > In computer science, a disjoint-set data structure, also called a union–find data structure or merge–find set, is a data structure that stores a collection of disjoint sets. Equivalently, it stores a partition of a set into disjoint subsets

  ---
  void make_set(int v) {
    parent[v] = make_pair(v, 0);
    rank[v] = 0;
}
  ---

pair<int, int> find_set(int v) {
    if (v != parent[v].first) {
        int len = parent[v].second;
        parent[v] = find_set(parent[v].first);
        parent[v].second += len;
    }
    return parent[v];
}

  ---

void union_sets(int a, int b) {
    a = find_set(a).first;
    b = find_set(b).first;
    if (a != b) {
        if (rank[a] < rank[b])
            swap(a, b);
        parent[b] = make_pair(a, 1);
        if (rank[a] == rank[b])
            rank[a]++;
    }
}
---
[ Code Source](https://cp-algorithms.com/data_structures/disjoint_set_union.html)
  