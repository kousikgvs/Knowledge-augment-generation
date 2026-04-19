# NetworkX — Order & Payment Knowledge Graph

A Jupyter Notebook that models an order-payment scenario as a directed knowledge graph using [NetworkX](https://networkx.org/) and [Matplotlib](https://matplotlib.org/).

## Scenario

- **Alice** (Customer) places **Order#101**
- **Order#101** contains the item **Laptop** (price: $1200)
- **Order#101** has an associated **Payment#1** whose status is **pending**
- The notebook queries the graph to determine whether Alice has completed payment

## Graph Structure

```
Alice ──[placed_order]──► Order#101 ──[contains_item]──► Laptop
                               │
                          [has_payment]
                               │
                               ▼
                          Payment#1  (status: pending)
```

### Node Types & Attributes

| Node       | Type     | Attributes            |
|------------|----------|-----------------------|
| Alice      | Customer | —                     |
| Order#101  | Order    | status: placed        |
| Laptop     | Item     | price: 1200           |
| Payment#1  | Payment  | status: pending       |

### Edge Relationships

| From       | To         | Relation        |
|------------|------------|-----------------|
| Alice      | Order#101  | placed_order    |
| Order#101  | Laptop     | contains_item   |
| Order#101  | Payment#1  | has_payment     |

## Requirements

```
networkx
matplotlib
```

Install with:

```bash
pip install -r requirements.txt
```

## Running the Notebook

Open `networkx.ipynb` in VS Code (or JupyterLab) and run all cells in order.
