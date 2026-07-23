# Payment Service API Gateway PoC (Kong + Node.js)

Proof of Concept (PoC) for a payment gateway architecture integrated with Kong API Gateway to manage security, authentication, and rate-limiting.

 #Architecture Flow
[Client] ---> (Port 8000: Kong Gateway w/ API Key & Rate Limit) ---> (Port 3000: Payment Backend)

#File Structure
- `หลังบ้าน.js`: Node.js Express Backend handling checkout, webhook, and order status logic.
- `Kong.yml`: Declarative configuration for Kong API Gateway (routes, key-auth, and rate limiting).
- `Runcommand.yml`: Docker Compose file to orchestrate and run services.

 #How to Run

1. Run all services using Docker Compose:
```bash
docker-compose -f Runcommand.yml up -d
