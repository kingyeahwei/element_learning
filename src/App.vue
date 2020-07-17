<template>
  <div id="app">
    <div style="margin-bottom: 20px">
      <el-button
        size="small"
        @click="addTab(editableTabsValue)">
        add tab
      </el-button>
    </div>
    <el-tabs v-model="editableTabsValue" type="card" closable @tab-remove="removeTab">
      <el-tab-pane
        v-for="(item, index) in editableTabs"
        :key="item.name"
        :label="item.title"
        :name="item.name">
        {{item.content}}
      </el-tab-pane>
    </el-tabs>
  </div>
</template>

<script>
    export default {
        name: "app",
        data() {
            return {
                editableTabsValue: '2',
                editableTabs: [
                    {
                        title: 'Tab 1',
                        name: '1',
                        content: 'Tab 1 content'
                    }, {
                        title: 'Tab 2',
                        name: '2',
                        content: 'Tab 2 content'
                    }, {
                        title: 'Tab 3',
                        name: '3',
                        content: 'Tab 3 content'
                    }, {
                        title: 'Tab 4',
                        name: '4',
                        content: 'Tab 4 content'
                    }
                ],
                tabIndex: 2
            }
        },
        methods: {
            addTab(targetName) {
                let newTabName = ++this.tabIndex + "";
                this.editableTabs.push({
                    title: "new tab",
                    name: newTabName,
                    content: "new tab content"
                })
                this.editableTabsValue = newTabName
            },
            removeTab(targetName) {
                let tabs = this.editableTabs;
                let activeName = this.editableTabsValue;
                // 更改那个被选中
                if (activeName === targetName) {
                    tabs.forEach((tab, index) => {
                        if (tab.name === targetName) {
                            let nextTab = tabs[index + 1] || tabs[index - 1];
                            if (nextTab) {
                                activeName = nextTab.name;
                            }
                        }
                    });
                }

                this.editableTabs = tabs.filter(tab => tab.name !== targetName);
                if (this.editableTabs.length > 0) {
                  this.editableTabsValue = activeName;
                } else  {
                    this.editableTabsValue = ""
                }
            }
        }
    }
</script>

<style lang="less">
</style>
