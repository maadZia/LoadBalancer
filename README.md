# Load Balancer System

A Python-based Load Balancer designed to distribute requests across multiple servers efficiently. Built with scalability, modularity, and extensibility in mind, the project demonstrates key software design patterns in action.

---

## 🚀 Features

- **Dynamic Server Management**: Add or remove servers at runtime.
- **Flexible Load Balancing**: Choose from multiple algorithms:
  - Round Robin
  - Random Selection
  - Least Connections
- **Health Monitoring**: Real-time server health checks.
- **Centralized Logging**: Consistent event tracking with a Singleton Logger.

---

## 🛠️ Tech Stack

- **Python 3.10+**: Core programming language.
- **Docker & Docker Compose**: Deployment and database management.
- **unittest**: For robust testing.
- **UML Modeling Tools**: Architecture design.

---

## 📂 Project Structure

```plaintext
├── Connection/               # Database connection configuration
│   └── db.json               # JSON config file for databases
├── Docker/                   # Docker-related files
│   └── docker-compose.yml    # Docker configuration
├── factory/                  # Factory pattern implementation
│   ├── strategy_factory.py   # Factory for load-balancing strategies
├── logger/                   # Singleton logger implementation
│   └── singleton_logger.py   # Logger class
├── observer/                 # Observer pattern implementation
│   ├── base_observer.py      # Base Observer interface
│   └── health_checker.py     # Health monitoring implementation
├── strategies/               # Load balancing strategies
│   ├── base_strategy.py      # Base strategy interface
│   ├── least_connections.py  # Least connections strategy
│   ├── random_strategy.py    # Random selection strategy
│   └── round_robin.py        # Round robin strategy
├── loadbalancer.py           # Core load balancer logic
├── main.py                   # Entry point of the application
└── README.md                 # Project documentation
```

---

## 🧑‍💻 Usage

### Prerequisites

1. Install **Python 3.10+**.
2. Install **Docker** and **Docker Compose**.

### Setup

Clone the repository:

```bash
git clone https://github.com/maadZia/LoadBalancer.git
cd loadBalancer
```

Install dependencies:

```bash
pip install -r requirements.txt
```

### Run the System

Start the services using Docker:

```bash
cd docker
docker-compose up
```

Access the load balancer and interact via the command line or integrated tools.

```bash
python main.py
```


---

## 📐 Design Patterns Used

### 1. Strategy Pattern
Encapsulates load-balancing algorithms, enabling dynamic selection at runtime.

### 2. Observer Pattern
Monitors server states and dynamically reacts to changes.

### 3. Factory Pattern
Centralizes the creation of load-balancing strategies for ease of maintenance.

### 4. Singleton Pattern
Ensures a single Logger instance for consistent log management.

---

## 🚧 Future Enhancements

- **Advanced Strategies**: Weighted round-robin and other algorithms.
- **Database Grouping**: Separate read/write operations.
- **Enhanced Observability**: Add metrics and monitoring tools.
- **Cloud Support**: Integrate with AWS or Azure for dynamic database management.




> Designed with ❤️ by the Load Balancer Team:   https://github.com/olaignacyk/loadBalancer
