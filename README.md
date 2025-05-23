Tanaka Fortune Singana 
21665202 
Headless CMS Website
Submitted on 23 May 2025
Website Url: Wildlife Conservative. Org - Wildlife Lives Matter 
WordPress Url: http://myfirstsite.local/

Wildlife Conservation Platform 
This project serves as a digital hub for wildlife conservation awareness combining the content management power of WordPress with the dynamic front-end capabilities of react. The project aims to 
Educate visitors about endangered species conservation efforts 
Showcase wildlife protection initiatives and success stories 
Provide an engaging user experience for conservation content
Demonstrate modern web development practices by integrating WordPress with react 
Technologies Used 
Word Press 6.8.1 (Headless CMS)
Yoast SEO for content optimization
Custom post types for wildlife content 
REST API for front-end 

Frontend
React  18+ with functional components 
React Router for navigation
Axios for API requests
CSS Modules 
Netlify for deployment 

Infrastructure
Netlify for frontend hosting
Wordpress hosting 
Github for version control

Word Press backend setup 
Install required plugins 
Install Plugins 
Configure Permalinks
Enable REST API access
# Clone the repository
git clone [your-repo-url]
cd react-frontend

# Install dependencies
npm install

# Configure environment variables
cp .env.example .env
# Update with your WordPress API endpoint

# Start development server
npm start
Deployment Instructions 
Maintain your existing word press hosting 
Ensuring REST API is publicly accessible 
Configure CORS if needed for frontend access
React Frontend Deployment to Netlify 
Push your code to Github
Connect your repository to Netlify 
Set up NPM run build 
Set publish directory build 
Add environment variables matching your .env file 
import axios from 'axios';

const API_URL = process.env.REACT_APP_WP_API_URL;

// Get all conservation posts
const fetchPosts = async () => {
  try {
    const response = await axios.get(`${API_URL}/wp-json/wp/v2/posts`);
    return response.data;
  } catch (error) {
    console.error('Error fetching posts:', error);
    return [];
  }
};

// Get single post by slug
const fetchPostBySlug = async (slug) => {
  try {
    const response = await axios.get(
      `${API_URL}/wp-json/wp/v2/posts?slug=${slug}`
    );
    return response.data[0];
  } catch (error) {
    console.error('Error fetching post:', error);
    return null;
  }
};


# Getting Started with Create React App

This project was bootstrapped with [Create React App](https://github.com/facebook/create-react-app).

## Available Scripts

In the project directory, you can run:

### `npm start`

Runs the app in the development mode.\
Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

The page will reload when you make changes.\
You may also see any lint errors in the console.

### `npm test`

Launches the test runner in the interactive watch mode.\
See the section about [running tests](https://facebook.github.io/create-react-app/docs/running-tests) for more information.

### `npm run build`

Builds the app for production to the `build` folder.\
It correctly bundles React in production mode and optimizes the build for the best performance.

The build is minified and the filenames include the hashes.\
Your app is ready to be deployed!

See the section about [deployment](https://facebook.github.io/create-react-app/docs/deployment) for more information.

### `npm run eject`

**Note: this is a one-way operation. Once you `eject`, you can't go back!**

If you aren't satisfied with the build tool and configuration choices, you can `eject` at any time. This command will remove the single build dependency from your project.

Instead, it will copy all the configuration files and the transitive dependencies (webpack, Babel, ESLint, etc) right into your project so you have full control over them. All of the commands except `eject` will still work, but they will point to the copied scripts so you can tweak them. At this point you're on your own.

You don't have to ever use `eject`. The curated feature set is suitable for small and middle deployments, and you shouldn't feel obligated to use this feature. However we understand that this tool wouldn't be useful if you couldn't customize it when you are ready for it.

## Learn More

You can learn more in the [Create React App documentation](https://facebook.github.io/create-react-app/docs/getting-started).

To learn React, check out the [React documentation](https://reactjs.org/).

### Code Splitting

This section has moved here: [https://facebook.github.io/create-react-app/docs/code-splitting](https://facebook.github.io/create-react-app/docs/code-splitting)

### Analyzing the Bundle Size

This section has moved here: [https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size](https://facebook.github.io/create-react-app/docs/analyzing-the-bundle-size)

### Making a Progressive Web App

This section has moved here: [https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app](https://facebook.github.io/create-react-app/docs/making-a-progressive-web-app)

### Advanced Configuration

This section has moved here: [https://facebook.github.io/create-react-app/docs/advanced-configuration](https://facebook.github.io/create-react-app/docs/advanced-configuration)

### Deployment

This section has moved here: [https://facebook.github.io/create-react-app/docs/deployment](https://facebook.github.io/create-react-app/docs/deployment)

### `npm run build` fails to minify

This section has moved here: [https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify](https://facebook.github.io/create-react-app/docs/troubleshooting#npm-run-build-fails-to-minify)
