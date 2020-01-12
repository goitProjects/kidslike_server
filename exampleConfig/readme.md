Чтобы сервер работал, папку которая тут есть нужно назвать просто "config"
и в ней создать файл "index.js" с таким содержанием:

const dbUser = "nameDbUser";
const dbPassword = "dbPassword";

const serverURL = "http://kidslike.goit.co.ua";
const port = 8085;

const config = {
secret: "key123",
port,
databaseUrl: `mongodb+srv://${dbUser}:${dbPassword}@cluster0-mskwo.mongodb.net/kidslike?retryWrites=true&w=majority`,
GOOGLE_CONFIG: {
clientID:
"someHashFromGoogleOauthAccount.apps.googleusercontent.com",
clientSecret: "someHashFromGoogleOauthAccount",
// make sure the call back url matches what was set on Twitter
// when registering the app
callbackURL: `${serverURL}/api/google/callback`,
serverURL
}
};

module.exports = config;
