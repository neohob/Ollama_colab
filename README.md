# Run Ollama Locally Using Google Colab's Free GPU

Many computers lack the powerful GPUs required to run large models like Ollama, preventing numerous users from enjoying the conveniences of local large models, such as article optimization, meeting summary extraction, and English email composition. A new method now enables local Ollama invocation of Google Colab's free GPU for rapid AI response generation.

## Step 1: Have a Google Account

Naturally, the first step is to have a Google account. This is widely covered online, so we won't delve into the details here.

## Step 2: Access the Prepared Ollama Notebook

Visit the prepared Ollama.ipynb at [![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1JNOrMvmkNvugoglaOKCqceL5XSXCOaAh).

## Step 3: Register and Get Your Ngrok Token

Sign up for Ngrok (free) and obtain your token at [Ngrok Dashboard](https://dashboard.ngrok.com/get-started/your-authtoken). Fill in your token in the Colab notebook.

## Step 4: Enter Your Ngrok Token

In the Colab notebook, replace `token="Your Ngrok token"` within the code block 3 with your actual Ngrok token.

## Step 5: Select the GPU T4

Choose the GPU T4 for your session.

## Step 6: Execute Steps in the Notebook

Follow the steps 1, 2, 3 in the notebook. After completing step 3, you will receive an URL like `https://xxxxxxx.ngrok-free.app`.

## Step 7: Install Ollama on Your Computer

Install Ollama from [Ollama Download Page](https://ollama.com/download), available for macOS, Linux, and Windows.

## Step 8: Set Environment Variable

On your computer, set the environment variable with `export OLLAMA_HOST=https://xxxxxxx.ngrok-free.app/`.

## Step 9: Run Ollama

Execute `ollama run model_name`, for example, `ollama run gemma`. Wait for the model to load. Although it appears to run locally, it actually invokes the remote Colab's T4 GPU.

Now, you can input questions to receive answers or use more apps to call Ollama, like setting the OpenAi-Translator tool to use Ollama, bypassing the need for a VPN to use ChatGPT and avoiding account bans.

**Note:** The free version of Google Colab's GPU has a daily limit of 12 hours. If you find it useful, consider purchasing the Pay as you go option, which allows 90 days of use with 100 GPU units.
