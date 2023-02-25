# Scott_Portfolio
Data Analyst Portfolio
#[Project 1: Bike Analysis Company: Project Overview] (https://github.com/Scottc097/Scottc097.github.io/blob/main/test.py)
Data Cleaning Process

`# replace missing values with "N/A"`
`'df.fillna("N/A", inplace=True)'`

`'# replace blank entries with NaN values'`
`df = df.replace('', pd.NA)`

# check for duplicates and remove them
df.drop_duplicates(inplace=True)

# rename columns
df.rename(columns={'rideable_type': 'vehicle_type', 'member_casual': 'user_type'}, inplace=True)


##type
#turning columns into correct type
# convert the "started_at" and "ended_at" columns to datetime
df['started_at'] = pd.to_datetime(df['started_at'])
df['ended_at'] = pd.to_datetime(df['ended_at'])
df['start_lat'] = df['start_lat'].astype(float)
df['start_lng'] = df['start_lng'].astype(float)
df['end_lat'] = df['end_lat'].replace('N/A', np.nan).astype(float)
df['end_lng'] = df['end_lng'].replace('N/A', np.nan).astype(float)`

*
*
*
*
