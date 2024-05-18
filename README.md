
# Registration Form

This project is a simple registration form built with React and Material UI.

## Installation

To use this project, you'll need to install the required dependencies. Follow the steps below to get started:

1. Clone the repository:
    ```bash
    git clone <repository-url>
    ```
2. Navigate to the project directory:
    ```bash
    cd <project-directory>
    ```
3. Install the dependencies:
    ```bash
    npm install
    npm install @mui/material @emotion/react @emotion/styled
    npm install @mui/icons-material
    ```

## Usage

To start the project, use the following command:
```bash
npm start
```
This will run the app in development mode. Open [http://localhost:3000](http://localhost:3000) to view it in your browser.

## `RegistrationForm` Component

The `RegistrationForm` component is a simple registration form with the following features:
- Username field
- Password field
- Repeat Password field
- Terms & Privacy checkbox
- Register button
- Sign in button for existing users

### Code

Here is the code for the `RegistrationForm` component:

```javascript
import {
  Button,
  Checkbox,
  FormControlLabel,
  Stack,
  TextField,
  Typography,
} from "@mui/material";

// 
// Requires to install these dependencies to use material ui and icons
//
// npm install @mui/material @emotion/react @emotion/styled
// npm install @mui/icons-material
//

export const RegistrationForm = () => {
  return (
    <Stack
      sx={{
        minHeight: "100svh",
        width: "100%",
        bgcolor: "#222",
        display: "flex",
        justifyContent: "center",
        alignItems: "center",
      }}
    >
      <form>
        <Stack
          sx={{
            minWidth: 300,
            padding: "30px",
            bgcolor: "#ffffff",
            borderRadius: "5px",
          }}
          gap={3}
        >
          <Typography variant="h5">Register</Typography>
          <Typography variant="body1">
            Please fill in this form to create an account
          </Typography>

          <TextField required label="Username"></TextField>

          <TextField required label="Password" />

          <TextField required label="Repeat Password" />

          <FormControlLabel
            control={<Checkbox />}
            required
            label="Terms & Privacy."
          />

          <Button variant="contained" color="success" type="submit">
            Register
          </Button>

          <Stack
            direction={"row"}
            justifyContent={"space-between"}
            alignItems={"center"}
          >
            <Typography variant="body1">Already have an account?</Typography>
            <Button>Sign in</Button>
          </Stack>
        </Stack>
      </form>
    </Stack>
  );
};
```
