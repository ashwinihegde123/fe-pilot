# WhatsappShare

  A short description about the component


  ## Demo

  A minimal [Online demo](link of codesandbox).


  ## Usage/Examples

###### <i>You can use AutoFillOtp as Component/Service. Either First letter should be in ```CAPS``` to use as a ```Component``` or First letter should be in ```small letter``` to use as a ```Service```. ```Default Import``` will always be a ```Component```.</i>
<br />


  2. Here's an example of basic usage with Multiple Import:
  ```javascript
  import { WhatsappShare, whatsappShare } from 'fe-pilot/WhatsappShare';

  <WhatsappShare /> // Used as a Component

  whatsappShare(); // Used as a Service
  ```

  3. Here's an example of a advance usage:

  ```javascript
  import { WhatsappShare } from 'fe-pilot/WhatsappShare';

  const successCb = (response) => {
    console.log("success response:", response);
  }

  const failureCb = (response) => {
    console.log("failure response:", response);
  }

  return (
    <WhatsappShare
      successCb={successCb}
      failureCb={failureCb}
      mobile="7204535372"
      msg="Welcome to fe-pilot "
    >
      Pass clickable element (button, anchor etc)  here to bind onClick event
    </WhatsappShare>
  );

  ```

  ### Props

  <table>
    <tr>
      <th>
        Props
      </th>
      <th>
        Type
      </th>
      <th>
        Description
      </th>
      <th>
        Response
      </th>
    </tr>
    <tr>
      <td>
          successCb
      </td>
      <td>Function</td>
      <td> It will be called on success</td>
      <td>
        <pre>
  {
      data: "Can be array/object/string/number",
      msgType: "SUCCESSFUL",
      msg: "A success msg",
      status: "SUCCESS"
  }
        </pre>
      </td>
    </tr>
    <tr>
      <td>
          loadingCb
      </td>
      <td>Function</td>
      <td>
        It will be called before success/failure.
      </td>
      <td>
        <pre>
  {
    msgType: "LOADING",
    msg: "LOADING...",
    status: "LOADING"
  }
  </pre>
      </td>
    </tr>
    <tr>
      <td>
          failureCb
      </td>
      <td>Function</td>
      <td>
        It will be called on failure
      </td>
      <td>
         <pre>
  {
    msgType: "ERROR",
    msg: "A failed msg",
    status: "FAILURE"
  }
         </pre>
      </td>
    </tr>
     <tr>
      <td>
          showForever
      </td>
       <td>Boolean</td>
      <td>To hide/remove unsupported feature, make it <b>false</b>. Default value is <b>true</b></td>
      <td> <pre>---</pre> </td>
    </tr>
    <tr>
      <td></td>
      <td></td>
      <td></td>
      <td></td>
    </tr>
    <tr>
      <td>mobile</td>
      <td>number</td>
      <td></td>
      <td> <pre>---</pre> </td>
    </tr>
     <tr>
      <td>msg</td>
      <td>String</td>
      <td></td>
      <td> <pre>---</pre> </td>
    </tr>
  </table>

