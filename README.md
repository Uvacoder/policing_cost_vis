# Where I got the data from and how I treated it:

These steps could be way more streamlined and efficient; I'm just recalling what I did at the time.

1. Download state outline from pre-built source (https://github.com/topojson/us-atlas) for convenience. Here it's called states_outline.json.

2. Create CSV in Excel from the data table on policing costs from the Vera Institute for Justice (https://www.vera.org/publications/what-policing-costs-in-americas-biggest-cities)
Also do some minor cleaning, like separating strings for city and state, removing colon in ratio value.
Convert this CSV into a JSON file 🤦🏾‍♀️

3. Compile by hand on Excel a list of coordinates for all cities from Step 2. Download this list as CSV and convert to JSON 🤦🏾‍♀️🤦🏾‍♀️🤦🏾‍♀️

4. Join the two JSON files; do more cleaning like removing the dollar signs and percent signs, string/number conversions
Also, before joining the coordinate data, convert it into pixel coordinates through a geographic projection matching the pre-built source in Step 1.
### `cd src/data`
### `node clean_city_data.js`


This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `yarn start`

Runs the app in the development mode.<br />
Open [http://localhost:3000](http://localhost:3000) to view it in the browser.

The page will reload if you make edits.<br />
You will also see any lint errors in the console.

### `yarn test`

Launches the test runner in the interactive watch mode.<br />
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `yarn build`

Builds the app for production to the `build` folder.<br />
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.<br />
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.



