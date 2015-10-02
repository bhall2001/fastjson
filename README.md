# fastjson
A Livecode library for Array to JSON and back again.

By combining the best of easyjson and libjson and adding in performance enhancements, fastjson improves the speed of encoding and decoding Livecode arrays to/from JSON.

Credit goes first to Mark Smith for creating the original libjson library and to Igor de Oliveira Couto who created the also excellent easyJson library.

I am combining routines from both of these libraries to give us a decent boost in performance for JSON to/from Array needs. Yes, you can go faster than this with an custom coded extension. But I find the speed of this library to be pretty impressive.

-------------------------------------------------------------------
 Instructions
-------------------------------------------------------------------

There are 3 calls that you will make from your Livecode scripts.

      arrayToJson(pArrayData)
      jsonToArray(pJsonData, asUnicode, skipValidation)
      isJson(pJsonData)

NOTE:
You will also find the following for compatibilty with existing easyJson scripts

     arrayFromJson(pJsonData) (NOT TESTED)
     jsonFromArray(pArrayData) (NOT TESTED)

All other functions and commands in this script are for local use only.

To use this library in a Stack I would suggest creating a substack of your main project named fastJson. Copy and paste the text of fastjson.lc minus the first line (<?lc) into the stack script of your new substack. In the preOpenStack handler of your main stack:

     start using stack "fastJson"

For livecode server use, include "fastjson.lc" in your server script.
