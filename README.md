# Example.WebSocketAPI.Python.MRN.RTO
A Python WebSocket API example that Consumes MRN STORY data from Refinitiv Real-Time Optimised using Service Discovery (rather than a fixed host/endpoint)

Whilst we have individual examples/tutorials that 
* show you how to consume Refinitiv Machine Readable News Stories (MRN_STORY) from Refinitiv Real-Time Optimized  
* show you how to use Refinitiv Platform Service Discovery Gateway to automatically select a host/endpoint for your preferred region  

we don't have an example that combines both of the above.

We have been asked by inexperienced coders if we provide such an example - as they don't wish to rely on a single hardcoded endpoint when consuming MRN data.

To address this, I have simply taken the existing source code for a <a href="https://github.com/Refinitiv/websocket-api/blob/master/Applications/Examples/RDP/python/market_price_rdpgw_service_discovery.py" target="_blank">Service Discovery example</a> and combined it with an <a href="https://github.com/Refinitiv-API-Samples/Example.WebSocketAPI.Python.MRN/tree/ERT-in-Cloud" target="_blank">MRN_STORY example</a> to produce the attached example.

This example has only undergone basic testing, and is itself based on other educational examples and is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied. See the License for the specific language governing permissions and limitations under the License.

For further details on Service Discovery and parsing Refinitiv Machine Readable News Stories, please refer to the above links and Websocket API and RTO documentation materials:

<a href="https://github.com/Refinitiv-API-Samples/Example.WebSocketAPI.Python.MRN/tree/ERT-in-Cloud" target="_blank">Websocket API MRN Tutorial example</a>  
<a href="https://developers.refinitiv.com/en/api-catalog/refinitiv-real-time-opnsrc/refinitiv-websocket-api/quick-start" target="_blank">Websocket API QuickStart</a>  
<a href="https://developers.refinitiv.com/en/api-catalog/refinitiv-real-time-opnsrc/refinitiv-websocket-api/documentation" target="_blank">Websocket API & RTO Documentation</a>  
<a href="https://developers.refinitiv.com/en/api-catalog/refinitiv-real-time-opnsrc/refinitiv-websocket-api/tutorials#connect-to-refinitiv-real-time-optimized" target="_blank">Websocket API Tutorials</a>  

### REGION choice 
The example currently has the region coded as *'us-east-1'*. If you are in a different region, you can change this value - allowing the service discovery mechanism to select a potentially closer host/endpoint.

The current available region choices are:
* *eu-west-1* 
* *ap-southeast-1*
* *us-east-1*
* *us-east-2*

You can find more information on the regions and their associated endpoints by referring to the <a href="https://developers.refinitiv.com/en/api-catalog/refinitiv-real-time-opnsrc/refinitiv-websocket-api/documentation#refinitiv-real-time-optimized-install-and-config-guide" target="_blank">RTO Documentation</a>.

## Prerequisite
This example requires the following dependencies softwares and libraries.
1. RDP Credentials with MRN Service.
2. [Python](https://www.python.org/) compiler and runtime
3. Python's [requests 2.x](https://pypi.org/project/requests/) library.
4. Python's [websocket-client](https://pypi.org/project/websocket-client/) library (*version 1.2.1 or greater*).

### Running the example
1. Go to project folder in console  
2. Run ```$> pip install -r requirements.txt``` command in a console to install all the dependencies libraries.  
3. Then you can run example application with the following command  
    `$> python mrn_rdpgw_service_discovery.py --client_id <RDP Client ID/AppKey> --user <RDP Username> --password <RDP Password>`  
    
The above will run with the default region - which you can override on the command line e.g.  
    `$> python mrn_rdpgw_service_discovery.py --client_id <RDP Client ID/AppKey> --user <RDP Username> --password <RDP Password> --region eu-west-1`


