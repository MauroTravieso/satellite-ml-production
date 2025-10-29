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

## 🧪 Comprehensive Testing Protocol

- Test Case 1: ISS Prediction

Input Data:

```sh
Latitude: 51.6
Longitude: -122.0
X ECI: 6771.5 km
Y ECI: 100.0 km
Z ECI: 200.0 km
Velocity X: 7.66 km/s
Velocity Y: 0.5 km/s
Velocity Z: 0.3 km/s
```

- Test Case 2: Sentinel1A Prediction

Input Data:

```sh
Latitude: 98.2
Longitude: 45.0
X ECI: 7065.0 km
Y ECI: 500.0 km
Z ECI: 1000.0 km
Velocity X: 7.45 km/s
Velocity Y: -0.5 km/s
Velocity Z: -0.3 km/s
```

## Edge Cases

- Test invalid inputs:
```sh
Empty fields:

Leave latitude blank → Should show validation error
```

- Out of range values:
```sh
Latitude: 100 → Should show error (valid: -90 to 90)
Longitude: 200 → Should show error (valid: -180 to 180)
```

- Non-numeric values:
```sh
Latitude: "abc" → Should prevent submission
```

- Extreme values:
```sh
Very high altitude (20000 km) → Should still classify
Very low velocity (1 km/s) → Should still classify
```
