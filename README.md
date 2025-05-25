# Vortex

Vortex is an e-commerce platform built by [Codeville](https://github.com/Codeville), combining a robust MedusaJS backend with a modern Next.js 15 storefront for a scalable and performant online shopping experience.

## Repository Structure

This repository is the root for the Vortex project and includes the following submodules:

- **vortex-backend**: MedusaJS-based e-commerce backend, handling product management, orders, payments, and more.
- **vortex-frontend**: Next.js 15 storefront, providing a fast and responsive user interface for customers.

## Prerequisites

Before setting up the project, ensure you have the following installed:

- [Node.js](https://nodejs.org/) (v18 or higher)
- [Git](https://git-scm.com/)
- [Yarn](https://yarnpkg.com/) or [npm](https://www.npmjs.com/)
- [Docker](https://www.docker.com/) (optional, for running MedusaJS with PostgreSQL)

## Setup Instructions

1. **Clone the Repository with Submodules**

   ```bash
   git clone --recurse-submodules https://github.com/Codeville/Vortex.git
   cd Vortex
   ```

2. **Initialize Submodules (if not cloned with `--recurse-submodules`)**

   ```bash
   git submodule update --init --recursive
   ```

3. **Set Up the Backend (vortex-backend)**

   ```bash
   cd vortex-backend
   yarn install
   ```

   - Configure environment variables (e.g., `.env`) for MedusaJS, including database and payment provider settings.
   - Run the MedusaJS server:
     ```bash
     yarn start
     ```

4. **Set Up the Frontend (vortex-frontend)**

   ```bash
   cd vortex-frontend
   yarn install
   ```

   - Configure environment variables (e.g., `.env.local`) to point to the backend API.
   - Start the Next.js development server:
     ```bash
     yarn dev
     ```

5. **Access the Application**
   - Backend: `http://localhost:9000` (default MedusaJS port)
   - Storefront: `http://localhost:3000` (default Next.js port)

## Project Structure

```
Vortex/
├── vortex-backend/    # MedusaJS e-commerce backend
└── vortex-frontend/   # Next.js 15 storefront
```

## Contributing

We welcome contributions from the community! To contribute:

1. Fork the repository.
2. Create a feature branch (`git checkout -b feature/your-feature`).
3. Commit your changes (`git commit -m "Add your feature"`).
4. Push to your branch (`git push origin feature/your-feature`).
5. Open a pull request against the `main` branch.

Please ensure your code follows our coding standards and includes relevant tests.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

For questions or support, reach out to the Codeville team at [support@codeville.org](mailto:support@codeville.org) or open an issue in this repository.

---

## _Best Practices_

# 1. Always update submodules when starting work

git submodule update --remote --merge

# 2. Work in individual submodules

cd storefront

# make changes

git add .
git commit -m "feat: add product listing"
git push

# 3. Update main repository to track changes

cd ..
git add storefront
git commit -m "Update storefront submodule"
git push
