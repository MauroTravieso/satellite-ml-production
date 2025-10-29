# 🛰️ Satellite Trajectory Classification System

Production ML system for real-time satellite identification based on orbital parameters.

## 🎯 Features
- Real-time single prediction
- Batch CSV processing
- 100% accuracy on test set
- No backend required
- Fully client-side processing

## 🚀 Live Demo
[https://MauroTravieso.github.io/satellite-ml-predictor/](https://MauroTravieso.github.io/satellite-ml-predictor/)

## 📊 Model Performance
- **Algorithm**: Random Forest (100 trees, depth 10)
- **Accuracy**: 100%
- **F1 Score**: 1.0000
- **Classes**: ISS, Sentinel1A
- **Features**: 10 (8 input + 2 derived)

## 📖 Usage

### Single Prediction
1. Enter orbital parameters
2. Click "Classify Satellite"
3. View prediction and confidence

### Batch Prediction
1. Prepare CSV with columns: `lat,lon,x_eci,y_eci,z_eci,vel_x,vel_y,vel_z`
2. Upload file
3. Download results

## 📄 License
MIT License
