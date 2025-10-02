# Environment Setup Instructions

## Create .env File

1. Create a file named `.env` in the root directory of this project
2. Add your OpenAI API key:

```bash
OPENAI_API_KEY=your_openai_api_key_here
PORT=3000
```

Replace `your_openai_api_key_here` with your actual OpenAI API key from https://platform.openai.com/api-keys

## Important Security Notes

- **NEVER commit your .env file to Git** - it's already in .gitignore
- Keep your API key secure and private
- Don't share your API key with anyone
- Monitor your API usage at https://platform.openai.com/usage

## Getting an OpenAI API Key

1. Go to https://platform.openai.com/api-keys
2. Sign in or create an account
3. Click "Create new secret key"
4. Copy the key (you won't be able to see it again!)
5. Paste it in your .env file

