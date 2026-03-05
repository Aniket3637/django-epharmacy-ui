# django-epharmacy-ui

Modern e-pharmacy UI with Django templates - Complete HTML/TailwindCSS implementation for online medicine delivery platform

## Overview

This project provides a complete, modern, and responsive UI for an online pharmacy platform built with Django templates and styled with TailwindCSS. The design focuses on user experience and modern web design principles with a teal color scheme.

## Features

- **Responsive Design**: Mobile-first approach ensuring compatibility across all devices
- **Modern UI**: Clean and intuitive interface using TailwindCSS utilities
- **Django Templates**: Full Django template inheritance structure
- **Complete Pages**: All essential e-pharmacy pages included
- **Professional Styling**: Teal color scheme with modern components
- **Admin Dashboard**: Comprehensive admin panel for pharmacy management

## Project Structure

```
templates/
├── base.html                 # Base template with navigation and footer
├── index.html                # Homepage with hero section and featured products
├── products.html             # Product listing with filters and pagination
├── product_detail.html       # Individual product detail page
├── checkout.html             # Checkout page with payment options
└── admin_dashboard.html      # Admin dashboard with analytics and order management
```

## Template Files

### 1. **base.html**
The foundation template containing:
- Navigation bar with search and user menu
- Logo and branding
- Footer with links and information
- Block structure for template inheritance
- TailwindCSS styling

### 2. **index.html**
Homepage featuring:
- Hero section with call-to-action
- Featured products section
- Category showcase
- Promotional banners
- Newsletter subscription

### 3. **products.html**
Product listing page with:
- Product grid layout
- Filter sidebar (category, price range, ratings)
- Search functionality
- Pagination controls
- Product cards with image, price, and ratings

### 4. **product_detail.html**
Detailed product page containing:
- Product image gallery
- Product information and specifications
- Price and availability status
- Add to cart functionality
- Related products section
- Customer reviews

### 5. **checkout.html**
Checkout and payment page with:
- Shipping address form
- Multiple payment method options (Card, Digital Wallet)
- Card payment details form
- Order summary with itemized costs
- Place order and continue shopping buttons

### 6. **admin_dashboard.html**
Comprehensive admin panel featuring:
- Sidebar navigation
- Dashboard statistics (Orders, Revenue, Users, Conversion Rate)
- Recent orders table
- Order status tracking
- User management interface
- Analytics overview

## Technology Stack

- **Django Templates**: For server-side templating
- **TailwindCSS**: For responsive and modern styling
- **HTML5**: Semantic markup
- **Responsive Design**: Mobile-first approach

## Getting Started

### Prerequisites
- Python 3.8+
- Django 3.2+
- TailwindCSS (via CDN or NPM)

### Installation

1. Clone the repository:
```bash
git clone https://github.com/Aniket3637/django-epharmacy-ui.git
cd django-epharmacy-ui
```

2. Create a Django project if you haven't already:
```bash
django-admin startproject pharmacy_project
cd pharmacy_project
django-admin startapp pharmacy
```

3. Copy the templates folder into your Django app:
```bash
cp -r ../templates ./pharmacy/templates
```

4. Update your Django settings to include the app:
```python
INSTALLED_APPS = [
    # ...
    'pharmacy',
]

TEMPLATES = [
    {
        'BACKEND': 'django.template.backends.django.DjangoTemplates',
        'DIRS': [],
        'APP_DIRS': True,
        'OPTIONS': {
            'context_processors': [
                'django.template.context_processors.debug',
                'django.template.context_processors.request',
                'django.contrib.auth.context_processors.auth',
            ],
        },
    },
]
```

5. Create URL patterns in your app's urls.py:
```python
from django.urls import path
from . import views

urlpatterns = [
    path('', views.index, name='index'),
    path('products/', views.products, name='products'),
    path('product/<int:id>/', views.product_detail, name='product_detail'),
    path('checkout/', views.checkout, name='checkout'),
    path('admin/dashboard/', views.admin_dashboard, name='admin_dashboard'),
]
```

6. Run the development server:
```bash
python manage.py runserver
```

## Customization

### Colors
The templates use TailwindCSS classes with a teal color scheme. To customize:
- Update color classes (teal-600, teal-700, etc.) to your brand colors
- Modify background and text colors in the class attributes

### Content
- Replace placeholder text with your actual product data
- Update navigation links to match your URL structure
- Customize footer content and links

### Images
- Replace image paths with your actual product images
- Update hero section images
- Modify category icons and thumbnails

## Features in Development

- [ ] Product search functionality integration
- [ ] Shopping cart system
- [ ] User authentication pages (Login, Register)
- [ ] Order tracking page
- [ ] Prescription upload page
- [ ] Mobile app templates
- [ ] Dark mode support

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Performance Optimization

- Lazy loading for product images
- Optimized CSS with TailwindCSS purging
- Responsive image sizes
- Efficient DOM structure

## License

MIT License - Feel free to use this project for personal or commercial purposes.

## Contributing

Contributions are welcome! Feel free to submit issues and pull requests.

## Author

**Aniket3637**
- GitHub: [@Aniket3637](https://github.com/Aniket3637)
- Project: [django-epharmacy-ui](https://github.com/Aniket3637/django-epharmacy-ui)

## Support

If you find this project helpful, please consider:
- Starring the repository
- Sharing with others
- Contributing improvements
- Reporting issues

---

**Last Updated**: March 5, 2026
**Version**: 1.0.0
