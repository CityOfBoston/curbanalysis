# Define MUTCD code categories for better organization
PARKING_CODES = {'PB-24', 'PB-24B', 'PB-24C', 'PB-24H', 'PB-24I', 'PBS-XX', 'P-6A', 'R7-107a'}
NO_PARKING_CODES = {'R7-1', 'R7-2', 'R7-4', 'MPBZ', 'R7-107a'}
REGULATORY_CODES = {'R-1', 'R-2', 'R-6', 'R-10', 'R-12', 'R-30', 'R-35', 'R-36', 'R1-2', 'R2-6aP', 
                   'R3-1', 'R3-2', 'R3-7L', 'R3-7R', 'R3-11b', 'R3-17', 'R3-17aP', 'R3-17bP', 'R3-20L',
                   'R4-4', 'R4-7', 'R4-11', 'R5-1', 'R6-1L', 'R6-1R', 'R10-3', 'R10-3a', 'R10-3b', 'R10-3c',
                   'R10-4', 'R10-7', 'R10-11b', 'R10-15R', 'R10-32P', 'R12-5'}
WARNING_CODES = {'W-6', 'W-23', 'W1-4L', 'W1-4R', 'W4-2R', 'W5-1', 'W11-2', 'W14-1', 'W14-2aR',
                'W15-1', 'W16-7PL', 'W16-7PR', 'W16-9P', 'W20-1', 'W20-8'}
GUIDE_CODES = {'D1-1', 'D1-1b', 'D3-1', 'D3-1a', 'D9-6', 'E6-2a', 'M1-1', 'M3-3', 'M3-4', 'M4-15',
              'M5-1R', 'M6-1L', 'S-#', 'S-30', 'S-50', 'S1-1', 'S5-1', 'S5-2'}
TEMPORARY_CODES = {'T-#', 'T-1', 'T-1A', 'T-1E', 'T-4', 'T-4A', 'T-5', 'T-7', 'T-12', 'T-19',
                  'T-23', 'T-23(L)', 'T-23(R)', 'T-23B', 'T-24', 'T-28', 'T-33', 'T-36'}
SPECIAL_CODES = {'TS-1', 'TS-1CC', 'TS-1J', 'TS-1N', 'TS-1Q', 'AC-#', 'AC-2', 'AC-3'}

# Define MUTCD code mappings with extended support
MUTCD_MEANINGS = {
    # Parking regulation signs
    'PB-24': {'description': '2 Hour Parking', 'color': '#81b29a', 'rule_type': 'time_limited_parking'},
    'PB-24B': {'description': '2 Hour Parking (Left Side)', 'color': '#f9bc60', 'rule_type': 'time_limited_parking'},
    'PB-24C': {'description': '2 Hour Parking (Commercial)', 'color': '#81b29a', 'rule_type': 'time_limited_parking'},
    'PB-24H': {'description': '2 Hour Parking (Handicap)', 'color': '#81b29a', 'rule_type': 'time_limited_parking'},
    'PB-24I': {'description': '2 Hour Parking (Residential)', 'color': '#81b29a', 'rule_type': 'time_limited_parking'},
    'PBS-XX': {'description': '2 Hour Parking Limit Except Resident Permit 5pm-7am', 'color': '#81b29a', 'rule_type': 'time_limited_parking'},
    'P-6A': {'description': 'Parking regulation', 'color': '#81b29a', 'rule_type': 'parking'},
    
    # No parking signs
    'MPBZ': {'description': 'No parking (Bus Zone)', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R7-1': {'description': 'No Parking Any Time', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R7-2': {'description': 'No Parking (Street Cleaning)', 'color': '#e76f51', 'rule_type': 'no_parking'},
    'R7-4': {'description': 'No Standing', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R7-107a': {'description': 'Reserved Parking', 'color': '#81b29a', 'rule_type': 'parking'},
    
    # Regulatory signs
    'R-1': {'description': 'Stop', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-2': {'description': 'Yield', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-6': {'description': 'One Way', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-10': {'description': 'Speed Limit', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-12': {'description': 'Turn Restriction', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-30': {'description': 'Regulatory', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-35': {'description': 'Regulatory', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R-36': {'description': 'Regulatory', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R1-2': {'description': 'Yield', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R2-6aP': {'description': 'Speed Limit', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R3-1': {'description': 'No Right Turn', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R3-2': {'description': 'No Left Turn', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R3-7L': {'description': 'Left Lane Only', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R3-7R': {'description': 'Right Lane Only', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R3-11b': {'description': 'Bicycle/Bus Only', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R3-17': {'description': 'Bike Lane', 'color': '#7ca5e8', 'rule_type': 'bike_lane'},
    'R3-17aP': {'description': 'Bike Lane', 'color': '#7ca5e8', 'rule_type': 'bike_lane'},
    'R3-17bP': {'description': 'Bike Lane', 'color': '#7ca5e8', 'rule_type': 'bike_lane'},
    'R3-20L': {'description': 'Left Lane Bicycle/Bus Only', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R4-4': {'description': 'Begin Right Turn Lane', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R4-7': {'description': 'Keep Right', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R4-11': {'description': 'Bicycle May Use Full Lane', 'color': '#7ca5e8', 'rule_type': 'bike_lane'},
    'R5-1': {'description': 'Do Not Enter', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R6-1L': {'description': 'One Way (Left)', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R6-1R': {'description': 'One Way (Right)', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R10-3': {'description': 'Parking Restrictions', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R10-3a': {'description': 'Parking Restrictions', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R10-3b': {'description': 'Parking Restrictions', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R10-3c': {'description': 'Parking Restrictions', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R10-4': {'description': 'Parking Regulations', 'color': '#81b29a', 'rule_type': 'parking'},
    'R10-7': {'description': 'Bus Stop', 'color': '#e07a5f', 'rule_type': 'no_parking'},
    'R10-11b': {'description': 'Accessible Parking', 'color': '#81b29a', 'rule_type': 'parking'},
    'R10-15R': {'description': 'Transit Regulations', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R10-32P': {'description': 'Regulatory', 'color': '#cc444b', 'rule_type': 'traffic'},
    'R12-5': {'description': 'Weight Limit', 'color': '#cc444b', 'rule_type': 'traffic'},
    
    # Warning signs
    'W-6': {'description': 'Warning', 'color': '#f4a261', 'rule_type': 'warning'},
    'W-23': {'description': 'Warning', 'color': '#f4a261', 'rule_type': 'warning'},
    'W1-4L': {'description': 'Merge Left', 'color': '#f4a261', 'rule_type': 'warning'},
    'W1-4R': {'description': 'Merge Right', 'color': '#f4a261', 'rule_type': 'warning'},
    'W4-2R': {'description': 'Lane Ends', 'color': '#f4a261', 'rule_type': 'warning'},
    'W5-1': {'description': 'Road Narrows', 'color': '#f4a261', 'rule_type': 'warning'},
    'W11-2': {'description': 'Pedestrian Crossing', 'color': '#f4a261', 'rule_type': 'warning'},
    'W14-1': {'description': 'Dead End', 'color': '#f4a261', 'rule_type': 'warning'},
    'W14-2aR': {'description': 'No Outlet', 'color': '#f4a261', 'rule_type': 'warning'},
    'W15-1': {'description': 'Playground', 'color': '#f4a261', 'rule_type': 'warning'},
    'W16-7PL': {'description': 'Arrow Plaque (Left)', 'color': '#f4a261', 'rule_type': 'warning'},
    'W16-7PR': {'description': 'Arrow Plaque (Right)', 'color': '#f4a261', 'rule_type': 'warning'},
    'W16-9P': {'description': 'Warning Plaque', 'color': '#f4a261', 'rule_type': 'warning'},
    'W20-1': {'description': 'Road Work Ahead', 'color': '#f4a261', 'rule_type': 'warning'},
    'W20-8': {'description': 'Road Closed', 'color': '#f4a261', 'rule_type': 'warning'},
    
    # Guide signs
    'D1-1': {'description': 'Destination Sign', 'color': '#999999', 'rule_type': 'info'},
    'D1-1b': {'description': 'Destination Distance', 'color': '#999999', 'rule_type': 'info'},
    'D3-1': {'description': 'Street Name', 'color': '#999999', 'rule_type': 'info'},
    'D3-1a': {'description': 'Street Name', 'color': '#999999', 'rule_type': 'info'},
    'D9-6': {'description': 'Trail Marker', 'color': '#999999', 'rule_type': 'info'},
    'E6-2a': {'description': 'Interstate Route', 'color': '#999999', 'rule_type': 'info'},
    'M1-1': {'description': 'Route Marker', 'color': '#999999', 'rule_type': 'info'},
    'M3-3': {'description': 'Junction', 'color': '#999999', 'rule_type': 'info'},
    'M3-4': {'description': 'Junction', 'color': '#999999', 'rule_type': 'info'},
    'M4-15': {'description': 'Route Marker', 'color': '#999999', 'rule_type': 'info'},
    'M5-1R': {'description': 'Route Direction', 'color': '#999999', 'rule_type': 'info'},
    'M6-1L': {'description': 'Directional Arrow', 'color': '#999999', 'rule_type': 'info'},
    'S-#': {'description': 'School Sign', 'color': '#999999', 'rule_type': 'info'},
    'S-30': {'description': 'School Sign', 'color': '#999999', 'rule_type': 'info'},
    'S-50': {'description': 'School Sign', 'color': '#999999', 'rule_type': 'info'},
    'S1-1': {'description': 'School Crossing', 'color': '#999999', 'rule_type': 'info'},
    'S5-1': {'description': 'School Speed Limit', 'color': '#999999', 'rule_type': 'info'},
    'S5-2': {'description': 'School End Zone', 'color': '#999999', 'rule_type': 'info'},
    
    # Temporary signs
    'T-#': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-1': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-1A': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-1E': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-4': {'description': 'Traffic control sign', 'color': '#999999', 'rule_type': 'traffic'},
    'T-4A': {'description': 'Traffic control sign', 'color': '#999999', 'rule_type': 'traffic'},
    'T-5': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-7': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-12': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-19': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-23': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-23(L)': {'description': 'Temporary Sign (Left)', 'color': '#999999', 'rule_type': 'info'},
    'T-23(R)': {'description': 'Temporary Sign (Right)', 'color': '#999999', 'rule_type': 'info'},
    'T-23B': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-24': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-28': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-33': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    'T-36': {'description': 'Temporary Sign', 'color': '#999999', 'rule_type': 'info'},
    
    # Special signs
    'TS-1': {'description': 'Traffic Signal', 'color': '#999999', 'rule_type': 'traffic'},
    'TS-1CC': {'description': 'Traffic Signal', 'color': '#999999', 'rule_type': 'traffic'},
    'TS-1J': {'description': 'Traffic Signal', 'color': '#999999', 'rule_type': 'traffic'},
    'TS-1N': {'description': 'Traffic Signal', 'color': '#999999', 'rule_type': 'traffic'},
    'TS-1Q': {'description': 'Traffic Signal', 'color': '#999999', 'rule_type': 'traffic'},
    'AC-#': {'description': 'Advisory sign', 'color': '#999999', 'rule_type': 'info'},
    'AC-2': {'description': 'Advisory sign', 'color': '#999999', 'rule_type': 'info'},
    'AC-3': {'description': 'Advisory sign', 'color': '#999999', 'rule_type': 'info'},
    
    # Additional signs
    'RIGHT LANE BUS AND BIKE ONLY': {'description': 'Bus and Bike Lane', 'color': '#7ca5e8', 'rule_type': 'bike_lane'},
    'NO IDLING SIGN': {'description': 'No Idling', 'color': '#cc444b', 'rule_type': 'traffic'}
}
