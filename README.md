# Language-based Agents for CivRealm

This code base includes the language-based agents for CivRealm, including `BaseLang` and `Mastaba`. In this implementation, we use the [OpenAI API from Azure](https://learn.microsoft.com/en-us/azure/ai-services/openai/) to generate the language-based actions.

## Usage

1. Install `civrealm` from `<https://github.com/civrealm/civrealm>`. More documentation about the environment can be found [here](https://civrealm.github.io/civrealm/).

2. Set the environment varibles for the Azure OpenAI API and Pinecone API.

    ```
    # Use AZURE_OPENAI_API_TYPE="azure" to use Azure LLM, otherwise use "openai"
    export AZURE_OPENAI_API_TYPE="<your_open_api_type>"
    export AZURE_OPENAI_API_VERSION='<your_openai_api_version>'
    export AZURE_OPENAI_API_BASE='<your_openai_api_base>'
    export AZURE_OPENAI_API_KEY='<your_openai_api_key>'
    export LOCAL_LLM_URL='<if_need_local_llm_inference>'
    export MY_PINECONE_API_KEY='<your_pinecone_api_key>'
    export MY_PINECONE_ENV='<your_pinecone_env_name>'
    ```

3. Execute the code:
    ```
    python main.py
    ```

## Customization
`agents/language_agent.py` is the base class for language-based agents. You can customize your own language-based agents by inheriting from this class. 

For concreate examples, `agents/baselang_agent.py` and `agents/mastaba_agent.py` are the implementations of `BaseLang` and `Mastaba` agent. 
