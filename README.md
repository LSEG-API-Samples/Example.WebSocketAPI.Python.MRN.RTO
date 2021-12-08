# Example.WebSocketAPI.Python.MRN.RTO
A Python WebSocket API example that Consumes MRN STORY data from Refinitiv Real-Time Optimised using Service Discovery (rather than a fixed host/endpoint)

Whilst we have individual examples/tutorials that 
* show you how to consume Refinitiv Machine Readable News Stories (MRN_STORY) from Refinitiv Real-Time Optimized  
* show you how to use Refinitiv Platform Service Discovery Gateway to automatically select a host/endpoint for your preferred region  

we don't have an example that combines both of the above.

We have been asked by inexperienced coders if we provide such an example - as they don't wish to rely on a single hardcoded endpoint when consuming MRN data.

To address this, I have simply taken the exsiting source code for a <a href="https://github.com/Refinitiv/websocket-api/blob/master/Applications/Examples/RDP/python/market_price_rdpgw_service_discovery.py" target="_blank">Service Discovery example</a> and combined it with an <a href="https://github.com/Refinitiv-API-Samples/Example.WebSocketAPI.Python.MRN/tree/ERT-in-Cloud" target="_blank">MRN_STORY example</a> to produce the attached example.

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
