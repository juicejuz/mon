<!--
* Copyright 2020 @dave-db.com
*
* Licensed under the Apache License, Version 2.0 (the "License");
* you may not use this file except in compliance with the License.
* You may obtain a copy of the License at
*    http://www.apache.org/licenses/LICENSE-2.0
*
* Unless required by applicable law or agreed to in writing, software
* distributed under the License is distributed on an "AS IS" BASIS,
* WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
* See the License for the specific language governing permissions and
* limitations under the License.
-->

<!--
 * --------------------------------------------------------------------------------
 * Description:
 *        ToDo:
 * --------------------------------------------------------------------------------
 -->

# Alert Rules Node RAM Usage
<[back](./prom)

### RAM Usage
- alert: 
    > node_ram_usage_60%
    - trigger
        > gt: 60%

        > for: 120 min

    - serevity: 
        > indeterminate (purple)
    - summary
        > Memory alert for Swarm node {{ node_name }}
    - description
        > Swarm node {{ node_name }} memory usage is at {{ value % }}.

- alert: 
    > node_ram_usage_65%
    - trigger
        > gt: 65%

        > for: 60 min

    - serevity: 
        > warning (blue)
    - summary
        > Memory alert for Swarm node {{ node_name }}
    - description
        > Swarm node {{ node_name }} memory usage is at {{ value % }}.

- alert: 
    > node_ram_usage_75%
    - trigger
        > gt: 75%

        > for: 45 min

    - serevity: 
        > minor (yellow)
    - summary
        > Memory alert for Swarm node {{ node_name }}
    - description
        > Swarm node {{ node_name }} memory usage is at {{ value % }}.

- alert: 
    > node_ram_usage_85%
    - trigger
        > gt: 85%

        > for: 30 min

    - serevity: 
        > major (orange)
    - summary
        > Memory alert for Swarm node {{ node_name }}
    - description
        > Swarm node {{ node_name }} memory usage is at {{ value % }}.

- alert: 
    > node_ram_usage_95%
    - trigger
        > gt: 95%
        
        > for: 1 min
        
    - serevity:         
        > critical (red)
    - summary
        > Memory alert for Swarm node {{ node_name }}
    - description
        > Swarm node {{ node_name }} memory usage is at {{ value % }}.

## License

![LICENCE](https://img.shields.io/github/license/davedb459/davedb-api)

- **[Apache2.0 license](http://www.apache.org/licenses/LICENSE-2.0)**
- Copyright 2020 © <a href="https://github.com/davedb459/davedb.api.git" target="_blank">dave-db.com</a>.