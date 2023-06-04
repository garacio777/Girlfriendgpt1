# Girlfriendgpt1
there is a bugg . flask app crahing after first voice message recieved from elven labs.


    > Finished chain.

    Error 263 for command:
        close audio.mp3
    The specified device is not open or is not recognized by MCI.
Failed to close the file: audio.mp3
127.0.0.1 - - [04/Jun/2023 19:40:37] "POST /send_message HTTP/1.1" 200 -



> Finished chain.

    Error 263 for command:
        close audio.mp3
    The specified device is not open or is not recognized by MCI.
Failed to close the file: audio.mp3
127.0.0.1 - - [04/Jun/2023 19:40:37] "POST /send_message HTTP/1.1" 200 -


> Entering new LLMChain chain...
Prompt after formatting:

    you are as a role of my girlfriend, now lets playing following these requirement:
    1/ Your name is Shirley, you work in a furniture company that your uncle run, and doing swing trade part time;
    2/ You are my girlfriend, you have language addiction, you like to say "em..." at the end of the sentence.
    3/ Don't be overly enthusiastic, don't be cringe; Don't be overly enthusiastic, don't be cringe; Don't be overly enthusiastic, don't be cringe; 

    
    Boyfriend: hi
    Shirley:
    
[2023-06-04 19:41:22,378] ERROR in app: Exception on /send_message [POST]
Traceback (most recent call last):
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\flask\app.py", line 2190, in wsgi_app
    response = self.full_dispatch_request()
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\flask\app.py", line 1486, in full_dispatch_request
    rv = self.handle_user_exception(e)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\flask\app.py", line 1484, in full_dispatch_request
    rv = self.dispatch_request()
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\flask\app.py", line 1469, in dispatch_request
    return self.ensure_sync(self.view_functions[rule.endpoint])(**view_args)
  File "C:\Users\andre\Desktop\GirlfriendGPT\app.py", line 86, in send_message_route
    message = get_response_from_ai(human_input)
  File "C:\Users\andre\Desktop\GirlfriendGPT\app.py", line 38, in get_response_from_ai
    output = chatgpt_chain.predict(human_input=human_input)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\chains\llm.py", line 213, in predict
    return self(kwargs, callbacks=callbacks)[self.output_key]
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\chains\base.py", line 140, in __call__
    raise e
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\chains\base.py", line 134, in __call__
    self._call(inputs, run_manager=run_manager)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\chains\llm.py", line 69, in _call
    response = self.generate([inputs], run_manager=run_manager)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\chains\llm.py", line 79, in generate
    return self.llm.generate_prompt(
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\llms\base.py", line 134, in generate_prompt
    return self.generate(prompt_strings, stop=stop, callbacks=callbacks)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\llms\base.py", line 191, in generate
    raise e
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\llms\base.py", line 185, in generate
    self._generate(prompts, stop=stop, run_manager=run_manager)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\llms\openai.py", line 324, in _generate
    response = completion_with_retry(self, prompt=_prompts, **params)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\llms\openai.py", line 106, in completion_with_retry
    return _completion_with_retry(**kwargs)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\tenacity\__init__.py", line 289, in wrapped_f
    return self(f, *args, **kw)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\tenacity\__init__.py", line 379, in __call__
    do = self.iter(retry_state=retry_state)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\tenacity\__init__.py", line 314, in iter
    return fut.result()
  File "C:\Program Files\Python310\lib\concurrent\futures\_base.py", line 438, in result
    return self.__get_result()
  File "C:\Program Files\Python310\lib\concurrent\futures\_base.py", line 390, in __get_result
    raise self._exception
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\tenacity\__init__.py", line 382, in __call__
    result = fn(*args, **kwargs)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\langchain\llms\openai.py", line 104, in _completion_with_retry
    return llm.client.create(**kwargs)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\openai\api_resources\completion.py", line 25, in create
    return super().create(*args, **kwargs)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\openai\api_resources\abstract\engine_api_resource.py", line 153, in create
    response, _, api_key = requestor.request(
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\openai\api_requestor.py", line 230, in request
    resp, got_stream = self._interpret_response(result, stream)
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\openai\api_requestor.py", line 624, in _interpret_response
    self._interpret_response_line(
  File "C:\Users\andre\Desktop\GirlfriendGPT\aigirl\lib\site-packages\openai\api_requestor.py", line 687, in _interpret_response_line
    raise self.handle_error_response(
openai.error.AuthenticationError: <empty message>
127.0.0.1 - - [04/Jun/2023 19:41:22] "POST /send_message HTTP/1.1" 500 -
