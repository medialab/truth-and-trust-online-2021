## Truth and Trust online 2021

## General installation

The code was developped on Python 3.9.0.

To install the needed libraries, run in your terminal:

```
pip install -r requirements.txt
```

[Explain the .env file]

## Collect the data

All the collected data will be saved as CSV files in the `data` folder.

### YouTube:
- For collecting youtube data run
```
  python3 code/collect_youtube_data.py 'Your_Youtube_API_key'
```
- Two new csv files will be generated in the data file with the name of the channels, and they will contain the videos posted for the selected channels since 2019/01/01 with the date of publishing, likes, dislikes, comments count.
- The study focused on two channels OANN and Tony Heller. The ids of these channels are included in the code. To add/remove channels, you can change the list ``` list_id ``` under ``` collect_youtube_data.py``` file.


### Facebook:

To collect the Trump Facebook data from CrowdTangle, run (the collection takes around 2 minutes):

```
./code/collect_facebook_crowdtangle_trump_data.sh 1559721
```

To collect the Infowars Facebook data from CrowdTangle, run (takes around 20 minutes):

```
./code/collect_facebook_crowdtangle_infowars_data.sh
```

To collect the Infowars Facebook data from Buzzsumo, run (takes around 4 min):
```
python code/collect_facebook_buzzsumo_infowars_data.py
```

## Plot the figures

Once the collected data is in CSV files in the `data` folder, you can plot it using:

```
python code/create_figures.py
```

The created PNG figures will appear in the `figure` folder.