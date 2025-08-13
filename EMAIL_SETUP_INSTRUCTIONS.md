# Email Notification Setup Instructions

## Overview
Your Roamer Respite booking website now includes email notifications that will send booking details to **Roamersrespite1@gmail.com** whenever a customer completes a booking.

## Setup Steps

### 1. Create EmailJS Account
1. Go to [https://www.emailjs.com](https://www.emailjs.com)
2. Click "Sign Up" and create a free account
3. Verify your email address

### 2. Connect Your Gmail Account
1. In EmailJS dashboard, go to "Email Services"
2. Click "Add New Service"
3. Select "Gmail"
4. Click "Connect Account" and authorize with your Gmail (Roamersrespite1@gmail.com)
5. Copy the **Service ID** (you'll need this later)

### 3. Create Email Template
1. Go to "Email Templates" in EmailJS dashboard
2. Click "Create New Template"
3. Copy and paste this template:

```
Subject: New Booking: {{property_name}} - {{booking_reference}}

Dear Roamer Respite Team,

You have received a new booking! Here are the details:

🏠 BOOKING DETAILS
Booking Reference: {{booking_reference}}
Property: {{property_name}}
Booking Date: {{booking_datetime}}

👤 GUEST INFORMATION
Name: {{guest_name}}
Email: {{guest_email}}
Phone: {{guest_phone}}
Number of Guests: {{guests}}

📅 STAY DETAILS
Check-in: {{checkin_date}}
Check-out: {{checkout_date}}
Number of Nights: {{nights}}

💰 PAYMENT DETAILS
Rate per Night: {{rate_per_night}}
Total Amount: {{total_amount}}
Payment Method: {{payment_method}}

📝 SPECIAL REQUESTS
{{special_requests}}

---
Roamer Respite Booking System
```

4. Save the template and copy the **Template ID**

### 4. Get Your Public Key
1. In EmailJS dashboard, go to "Account" → "General"
2. Copy your **Public Key**

### 5. Update Website Code
1. Open `script.js` file
2. Find line 4 and replace `YOUR_PUBLIC_KEY` with your actual public key
3. Find lines 501-502 and replace:
   - `YOUR_SERVICE_ID` with your Gmail service ID
   - `YOUR_TEMPLATE_ID` with your template ID

### Example Configuration
```javascript
// Line 4:
emailjs.init('user_abc123xyz'); // Your public key

// Lines 501-502:
const response = await emailjs.send(
    'service_abc123', // Your service ID
    'template_xyz789', // Your template ID
    templateParams
);
```

## Testing
1. Save all changes
2. Go to your website
3. Complete a test booking
4. Check your email (Roamersrespite1@gmail.com) for the notification

## Free Plan Limits
- EmailJS free plan allows 200 emails per month
- This should be sufficient for most small to medium BnB operations
- If you need more, you can upgrade to a paid plan

## Troubleshooting
- If emails don't arrive, check your spam folder
- Verify all IDs are correctly entered in the code
- Check the browser console for any error messages
- Make sure your Gmail account is properly connected in EmailJS

## Security Note
Your email notifications are secure and will only be sent when someone completes a legitimate booking through your website.