# Laravel B2B E-commerce Platform

A modern, scalable B2B e-commerce solution designed for wholesale businesses, distributors, and enterprise customers. Built with Laravel 11 and Docker, this platform provides comprehensive tools for managing complex business-to-business transactions, multi-tiered pricing, and enterprise-grade features.

## 📋 About This Project

### Overview
This B2B e-commerce platform is specifically designed to handle the complexities of business-to-business commerce, where traditional B2C solutions fall short. Unlike consumer-focused platforms, this system addresses the unique needs of wholesale operations, corporate purchasing, and multi-user business accounts.

### Target Users
- **Wholesale Distributors** - Managing large inventories with complex pricing structures
- **Manufacturing Companies** - Direct-to-business sales with custom pricing
- **Corporate Procurement Teams** - Streamlined purchasing workflows with approval processes
- **Multi-location Businesses** - Centralized ordering with location-specific pricing

### Problem It Solves
Traditional e-commerce platforms are built for individual consumers, but B2B transactions require:
- Complex pricing tiers based on volume, customer type, and contracts
- Multi-user accounts with different permission levels
- Quote-to-order workflows and approval processes
- Integration with existing ERP and accounting systems
- Advanced inventory management with backorder handling

## ⭐ Main Features

### 🏢 **Multi-Company Management**
- **Company Profiles**: Complete business information, tax details, and billing addresses
- **Multi-User Accounts**: Multiple employees per company with role-based access
- **User Hierarchies**: Managers, purchasers, and approvers with different permission levels
- **Department Management**: Organize users by departments with budget controls

### 💰 **Advanced Pricing Engine**
- **Tiered Pricing**: Volume-based discounts and quantity breaks
- **Customer-Specific Pricing**: Contract pricing and negotiated rates
- **Regional Pricing**: Location-based pricing variations
- **Currency Support**: Multi-currency transactions and conversion
- **Tax Management**: Complex tax rules including VAT, GST, and exemptions

### 📊 **Product Catalog Management**
- **Complex Product Hierarchies**: Categories, subcategories, and product families
- **Product Variants**: Size, color, material variations with individual SKUs
- **Bulk Product Management**: CSV imports and batch operations
- **Product Relationships**: Cross-sells, upsells, and alternative products
- **Digital Assets**: Multiple product images, documents, and specifications

### 🛒 **Quote & Order Management**
- **Request for Quote (RFQ)**: Customers can request custom pricing
- **Quote Generation**: Sales team can create and manage quotes
- **Quote-to-Order Conversion**: Seamless conversion with approval workflows
- **Purchase Order Integration**: Support for PO numbers and corporate purchasing
- **Order Approval Chains**: Multi-level approval based on order value and user roles

### 📈 **Business Intelligence**
- **Sales Analytics**: Revenue tracking, customer analysis, and product performance
- **Customer Insights**: Purchase history, payment behavior, and loyalty metrics
- **Inventory Reports**: Stock levels, turnover rates, and reorder points
- **Financial Reporting**: Profit margins, commission tracking, and tax reports

### 🔧 **System Integration**
- **ERP Integration**: Connect with existing business systems
- **Payment Gateway Support**: Multiple payment methods including terms and credit
- **Shipping Integration**: Real-time rates and tracking from major carriers
- **API-First Design**: RESTful APIs for custom integrations

### 🔐 **Enterprise Security**
- **Role-Based Access Control**: Granular permissions system
- **Audit Trails**: Complete activity logging for compliance
- **Data Encryption**: Secure handling of sensitive business data
- **GDPR Compliance**: Privacy controls and data management tools

## 🛠️ How to Build the Project

### Prerequisites
Before starting, ensure you have:
- **Docker** (version 20.0 or higher)
- **Docker Compose** (version 2.0 or higher)
- **Git** for version control
- **Minimum 4GB RAM** for development environment

### Quick Start

#### 1. Clone the Project
```bash
# Clone the repository
git clone https://github.com/hai-hq/laravel-b2b-ecommerce.git
cd laravel-b2b-ecommerce
```

#### 2. Run Build Commands
```bash
# Copy environment configuration
cp .env.example .env

# Build and start Docker containers
docker-compose up -d --build

# Install dependencies and setup Laravel
docker-compose exec app composer install
docker-compose exec app php artisan key:generate
docker-compose exec app php artisan migrate
docker-compose exec app php artisan storage:link

# Set proper permissions
docker-compose exec app chown -R www-data:www-data storage bootstrap/cache
docker-compose exec app chmod -R 775 storage bootstrap/cache

# (Optional) Install frontend dependencies
docker-compose exec app npm install
docker-compose exec app npm run dev

# (Optional) Seed database with sample data
docker-compose exec app php artisan db:seed
```

#### 3. Access Application
- **Application**: http://localhost:8001
- **Database**: localhost:3308 (user: `laravel_user`, password: `laravel_password`)
- **Redis Cache**: localhost:6379

## 🏗️ Project Structure

## 🤝 Contributing

We welcome contributions to improve this B2B e-commerce platform! Please follow these guidelines to ensure smooth collaboration.
