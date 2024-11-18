# House Price Predictor and Mortgage Calculator

## Overview
This Flask-based application provides tools for estimating house prices based on various features and calculating monthly mortgage payments. Additionally, it integrates with Firebase for storing user activity and includes a trends visualization feature.

## Features
- **House Price Prediction**: Predicts house prices using a machine learning model based on location, square footage, number of bedrooms, and bathrooms.
- **Mortgage Calculator**: Calculates monthly mortgage payments based on the principal amount, interest rate, and loan tenure.
- **Contact Form**: Allows users to send inquiries via email.
- **Search History**: Tracks and stores user searches in a Firebase Firestore database.
- **Trends Visualization**: Displays trends based on past house price predictions.

## Technologies Used
- **Backend**: Flask
- **Database**: Firebase Firestore
- **Frontend**: HTML, CSS, Bootstrap
- **Machine Learning**: Pre-trained model using scikit-learn
- **Email Notifications**: SMTP integration for contact form

## Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/kishorekaarthik/220701135-CS19542-IP-Project.git
   cd 220701135-CS19542-IP-Project
   ```

2. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Add your Firebase service account key:
   - Place your Firebase service account JSON file as `servicekey.json` in the root directory.

4. Set up the artifacts:
   - Place the pre-trained model (`model.pkl`) and columns metadata (`columns.json`) in the `artifacts/` directory.

5. Update email credentials:
   - Replace `EMAIL_ADDRESS` and `EMAIL_PASSWORD` in the code with your SMTP email credentials.

6. Run the application:
   ```bash
   python app.py
   ```

7. Access the application at `http://127.0.0.1:5000`.

## Routes
- `/` : Home page with a contact form.
- `/predict` : House price prediction page.
- `/get_locations` : API to fetch supported locations.
- `/mortgage` : Mortgage calculator page.
- `/trends` : Displays trends of past searches.
- `/get_trends` : API for fetching trends data.

## Usage
1. Navigate to the **Predict** page and input the required details to get an estimated house price.
2. Use the **Mortgage** page to calculate monthly payments for a given loan.
3. View past searches and trends on the **Trends** page.

## Firebase Integration
- The app uses Firebase Firestore to store:
  - House price search details (`searched_houses` collection)
  - Mortgage calculation details (`calculated_mortgages` collection)

## Contributing
1. Fork the repository.
2. Create a new branch: `git checkout -b feature-name`.
3. Commit your changes: `git commit -m "Add feature"`.
4. Push to the branch: `git push origin feature-name`.
5. Open a pull request.

## License
This project is licensed under the [MIT License](LICENSE).

## Contact
For inquiries or suggestions:
- Email: 220701135@rajalakshmi.edu.in
