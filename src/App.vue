<script lang="ts">
import { Component, Vue } from "vue-property-decorator";
import Teatree from "./components/Teatree.vue";
import NodeName from "./components/shelf/NodeName.vue";
import NodeToggle from "./components/shelf/NodeToggle.vue";
import NodeType from "./types/NodeType";

@Component({
  components: {
    Teatree,
    NodeName,
    NodeToggle,
  },
})
export default class App extends Vue {
  public data: NodeType[] = [
    {
      name: "Can the order be found in OMS?",
      show: true,
      showChildren: true,
      selected: false,
      children: [
        {
          name: "Yes",
          show: true,
          showChildren: false,
          selected: false,
          children: [
            {
              name: "Did the customer purchase the item on under their name and billing address?",
              show: true,
              showChildren: true,
              selected: false,
              children: [
                {
                  name: "Yes",
                  show: true,
                  showChildren: false,
                  selected: false,
                  children: [
                    {
                      name: "Are any items being returned a Truck Line or Hazardous item?",
                      show: true,
                      showChildren: true,
                      selected: false,
                      children: [
                        {
                          name: "No",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Does the customer have a printer or a smart phone?",
                              show: true,
                              showChildren: true,
                              selected: false,
                              children: [
                                {   
                                  name: "Yes",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Use a Narvar return label.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: [],
                                    }
                                  ],
                                },
                                {
                                  name: "No",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Was the item being received damaged or defective or did we make an error on the order?",
                                      show: true,
                                      showChildren: true,
                                      selected: false,
                                      children: [
                                        {
                                          name: "Yes",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Is the item less than 8 lbs in weight and less than 6 feet in length?",
                                              show: true,
                                              showChildren: true,
                                              selected: false,
                                              children: [
                                                {
                                                  name: "Yes",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Request a USPS return label be mailed to the customer.",
                                                      show: true,
                                                      showChildren: false,
                                                      selected: false,
                                                      children: [],
                                                    } 
                                                  ],
                                                },
                                                {
                                                  name: "No",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Request a FedEx return label be mailed to the customer.",
                                                      show: true,
                                                      showChildren: false,
                                                      selected: false,
                                                      children: [],
                                                    }
                                                  ],
                                                } 
                                              ],
                                            }
                                          ],
                                        },
                                        {
                                          name: "No",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Provide customer with return address and instructions to return item for exchange or refund. Do NOT offer a return label unless the customer requests.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: [
                                                {
                                                  name: "Customer requests label.",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Is the item less than 8 lbs in weight and less than 6 feet in length?",
                                                      show: true,
                                                      showChildren: true,
                                                      selected: false,
                                                      children: [
                                                        {
                                                          name: "Yes",
                                                          show: true,
                                                          showChildren: false,
                                                          selected: false,
                                                          children: [
                                                            {
                                                              name: "Request a USPS Return Label be mailed to the customer.",
                                                              show: true,
                                                              showChildren: true,
                                                              selected: false,
                                                              children: [],
                                                            }
                                                          ],
                                                        },
                                                        {
                                                          name: "No",
                                                          show: true,
                                                          showChildren: false,
                                                          selected: false,
                                                          children: [
                                                            {
                                                              name: "Request a FedEx Return Label be mailed to the customer.",
                                                              show: true,
                                                              showChildren: true,
                                                              selected: false,
                                                              children: [],
                                                            }
                                                          ],
                                                        }
                                                      ],
                                                    }
                                                  ],
                                                }
                                              ],
                                            }
                                          ],
                                        }  
                                      ],
                                    }
                                  ],
                                }
                              ] 
                            }
                          ],
                        },
                        {
                          name: "Yes, Truck Line.",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Complete a Truck Line Return Request Alert.",
                              show: true,
                              showChildren: false,
                              selected: false,
                              children: [],
                            }
                          ],
                        },
                        {
                          name: "Yes, Hazardous.",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Is the item returnable?",
                              show: true,
                              showChildren: true,
                              selected: false,
                              children: [
                                {
                                  name: "Yes",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Use Alert Guidance to request a hazardous item return label.  NOTE: This is NOT a prepaid label. THe customer will need to pay to use the label.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: [],
                                    }
                                  ],
                                },
                                {
                                  name: "No",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "A return label CANNOT be issued for a nonreturnable item.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: [],
                                    }
                                  ],
                                }
                              ],
                            }
                          ],
                        }
                      ]
                    },                      
                  ]
                },
                {
                  name: "No, it was a gift.",
                  show: true,
                  showChildren: false,
                  selected: false,
                  children: [
                    {
                      name: "Was the item being returned damaged or defective or did we make an error on the order?",
                      show: true,
                      showChildren: true,
                      selected: false,
                      children: [
                        {
                          name: "Yes",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Is the item less than 8 lbs in weight and less than 6 feet in length?",
                              show: true,
                              showChildren: true,
                              selected: false,
                              children: [
                                {
                                  name: "Yes",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Can the customer print a return label if one is emailed to them?",
                                      show: true,
                                      showChildren: true,
                                      selected: false,
                                      children: [
                                        {
                                          name: "Yes",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a USPS Return Label be emailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        },
                                        {
                                          name: "No",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a USPS Return Label be mailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        }
                                      ],
                                    }
                                  ],
                                },
                                {
                                  name: "No",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Can the customer print a return label if one is emailed to them?",
                                      show: true,
                                      showChildren: true,
                                      selected: false,
                                      children: [
                                        {
                                          name: "Yes",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a FedEx Label be emailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        },
                                        {
                                          name: "No",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a FedEx Return Label be mailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        }
                                      ],
                                    }
                                  ],
                                }
                              ],
                            }
                          ],
                        },
                        {
                          name: "No",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Provide customer with return address and instructions to return item for exchange or refund. Do NOT offer a return label unless the customer requests.",
                              show: true,
                              showChildren: false,
                              selected: false,
                              children: [
                                {
                                  name: "Customer requests label.",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Is the item less than 8 lbs in weight and less than 6 feet in length?",
                                      show: true,
                                      showChildren: true,
                                      selected: false,
                                      children: [
                                        {
                                          name: "Yes",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Can the customer print a return label is one is emailed to them?",
                                              show: true,
                                              showChildren: true,
                                              selected: false,
                                              children: [
                                                {
                                                  name: "Yes",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Request a USPS Label be emailed to the customer.",
                                                      show: true,
                                                      showChildren: false,
                                                      selected: false,
                                                      children: []
                                                    }
                                                  ],
                                                },
                                                {
                                                  name: "No",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Request a USPS Return Label be mailed to the customer.",
                                                      show: true,
                                                      showChildren: false,
                                                      selected: false,
                                                      children: []
                                                    }
                                                  ],
                                                }
                                              ],
                                            }
                                          ],
                                        },
                                        {
                                          name: "No",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Can the customer print a return label is one is emailed to them?",
                                              show: true,
                                              showChildren: true,
                                              selected: false,
                                              children: [
                                                {
                                                  name: "Yes",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Request a FedEx Label be emailed to the customer.",
                                                      show: true,
                                                      showChildren: false,
                                                      selected: false,
                                                      children: []
                                                    }
                                                  ],
                                                },
                                                {
                                                  name: "No",
                                                  show: true,
                                                  showChildren: false,
                                                  selected: false,
                                                  children: [
                                                    {
                                                      name: "Request a FexEx Return Label be mailed to the customer.",
                                                      show: true,
                                                      showChildren: false,
                                                      selected: false,
                                                      children: []
                                                    }
                                                  ],
                                                }
                                              ],
                                            }
                                          ],
                                        }
                                      ],
                                    }
                                  ],
                                }
                              ],
                            }
                          ],
                        }
                      ],
                    }
                  ],
                },
              ],
            }
          ],
        },
        {
          name: "No, it was a retail purchase.",
          show: true,
          showChildren: false,
          selected: false,
          children: [
            {
              name: "Was the item being returned damaged or defective?",
              show: true,
              showChildren: true,
              selected: false,
              children: [
                {
                  name: "Yes",
                  show: true,
                  showChildren: false,
                  selected: false,
                  children: [
                    {
                      name: "Is the item less than 8 lbs in weight and less than 6 feet in length?",
                      show: true,
                      showChildren: true,
                      selected: false,
                      children: [
                        {
                          name: "Yes",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Can the customer print a return label if one is emailed to them?",
                              show: true,
                              showChildren: true,
                              selected: false,
                              children: [
                                {
                                  name: "Yes",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Request a USPS Return Label be emailed to the customer.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: []
                                    }
                                  ],
                                },
                                {
                                  name: "No",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Request a USPS Return Label be mailed to the customer.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: []
                                    }
                                  ],
                                }
                              ],
                            }
                          ],
                        },
                        {
                          name: "No",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Can the customer print a return label if one is emailed to them?",
                              show: true,
                              showChildren: true,
                              selected: false,
                              children: [
                                {
                                  name: "Yes",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Request a FedEx Label be emailed to the customer.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: []
                                    }
                                  ],
                                },
                                {
                                  name: "No",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Request a FedEx Return Label be mailed to the customer.",
                                      show: true,
                                      showChildren: false,
                                      selected: false,
                                      children: []
                                    }
                                  ],
                                }
                              ],
                            }
                          ],
                        }
                      ],
                    }
                  ],
                },
                {
                  name: "No",
                  show: true,
                  showChildren: false,
                  selected: false,
                  children: [
                    {
                      name: "Provide customer with return address and instructions to return item for exchange or refund. Do NOT offer a return label unless the customer requests.",
                      show: true,
                      showChildren: false,
                      selected: false,
                      children: [
                        {
                          name: "Customer requests label.",
                          show: true,
                          showChildren: false,
                          selected: false,
                          children: [
                            {
                              name: "Is the item less than 8 lbs in weight and less than 6 feet in length?",
                              show: true,
                              showChildren: true,
                              selected: false,
                              children: [
                                {
                                  name: "Yes",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Can the customer print a return label is one is emailed to them?",
                                      show: true,
                                      showChildren: true,
                                      selected: false,
                                      children: [
                                        {
                                          name: "Yes",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a USPS Label be emailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        },
                                        {
                                          name: "No",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a USPS Return Label be mailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        }
                                      ],
                                    }
                                  ],
                                },
                                {
                                  name: "No",
                                  show: true,
                                  showChildren: false,
                                  selected: false,
                                  children: [
                                    {
                                      name: "Can the customer print a return label is one is emailed to them?",
                                      show: true,
                                      showChildren: true,
                                      selected: false,
                                      children: [
                                        {
                                          name: "Yes",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a FedEx Label be emailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        },
                                        {
                                          name: "No",
                                          show: true,
                                          showChildren: false,
                                          selected: false,
                                          children: [
                                            {
                                              name: "Request a FexEx Return Label be mailed to the customer.",
                                              show: true,
                                              showChildren: false,
                                              selected: false,
                                              children: []
                                            }
                                          ],
                                        }
                                      ],
                                    }
                                  ],
                                }
                              ],
                            }
                          ],
                        }
                      ],
                    }
                  ],
                }
              ],
            }
          ],
        }
      ],
    }
  ];
}
</script>

<template>
  <div id="app">
    <div style="margin-bottom: 10px">
      <h1>Return Label Decision Tree</h1>
      <span style="font-weight: bold">Click on the chevrons below to follow the decision tree and determine the correct return label to use. </span>
      </div>
    <div class="sidebar">
      <Teatree :roots="data">
        <!-- Recursive node toggle slot -->
        <template slot="node-toggle" slot-scope="{ node }">
          <!-- Off-shelf component provided by default, which inserts itself recursively into all slots -->
          <NodeToggle :node="node" />
        </template>

        <!-- Recursive node name slot -->
        <template slot="node-name" slot-scope="{ node }">
          <!-- Off-shelf component provided by default, which inserts itself recursively into all slots -->
          <NodeName
            :node="node"
            :handleNodeLeftClick="() => {}"
            :handleNodeRightClick="() => {}"
          />
        </template>
      </Teatree>
    </div>
  </div>
</template>

<style lang="scss">
@import url("https://fonts.googleapis.com/css2?family=Arima+Madurai:wght@700&family=Inter:wght@400;500;600&display=swap");

#app {
  width: 100%;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  margin-top: 60px;
  font-family: "Inter", sans-serif;
}

.text {
  width: 100%;
  text-align: center;
  margin-bottom: 50px;
}

.header {
  font-size: 2rem;
  font-family: "Arima Madurai", serif;
  font-weight: 700;
}

.subheader {
  margin-bottom: 30px;
}

.sidebar {
  background-color: black;
  width: 98%;
  min-width: 20px;
  margin-left: auto;
  margin-right: auto;
}
</style>
