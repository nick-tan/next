{"title":"重设列的尺寸","meta":{"title":"重设列的尺寸","description":"\n<p>通过onResizeChange来让列宽可以调整</p>\n","order":"18"},"codes":{"jsx":"import { Table } from '@alifd/next';\n\nconst onChange = function(...args) {\n        console.log(...args);\n    },\n    dataSource = () => {\n        const result = [];\n        for (let i = 0; i < 5; i++) {\n            result.push({\n                title: {\n                    name: `Quotation for 1PCS Nano ${3 + i}.0 controller compatible`,\n                },\n                id: 100306660940 + i,\n                time: 2000 + i\n            });\n        }\n        return result;\n    },\n    render = (value, index, record) => {\n        return <a>Remove({record.id})</a>;\n    },\n    rowSelection = {\n        onChange: onChange,\n        getProps: (record) => {\n            return {\n                disabled: record.id === 100306660942\n            };\n        }\n    };\n\nclass App extends React.Component {\n    state = {\n        widths: {\n            id: 100,\n        }\n    }\n    onResizeChange = (dataIndex, value) => {\n        const {widths} = this.state;\n        widths[dataIndex] = widths[dataIndex] + value;\n        this.setState({\n            widths\n        });\n    }\n    render() {\n        return (<Table dataSource={dataSource()}\n            rowSelection={rowSelection} onResizeChange={this.onResizeChange}>\n            <Table.Column title=\"Id\" dataIndex=\"id\" resizable width={this.state.widths.id}/>\n            <Table.Column title=\"Title\" dataIndex=\"title.name\" width={400}/>\n            <Table.Column title=\"Time\" dataIndex=\"time\" width={600}/>\n            <Table.Column cell={render} width={200}/>\n        </Table>);\n    }\n}\n\nReactDOM.render(<App/>, mountNode);\n"},"body":"\n\n````jsx\nimport { Table } from '@alifd/next';\n\nconst onChange = function(...args) {\n        console.log(...args);\n    },\n    dataSource = () => {\n        const result = [];\n        for (let i = 0; i < 5; i++) {\n            result.push({\n                title: {\n                    name: `Quotation for 1PCS Nano ${3 + i}.0 controller compatible`,\n                },\n                id: 100306660940 + i,\n                time: 2000 + i\n            });\n        }\n        return result;\n    },\n    render = (value, index, record) => {\n        return <a>Remove({record.id})</a>;\n    },\n    rowSelection = {\n        onChange: onChange,\n        getProps: (record) => {\n            return {\n                disabled: record.id === 100306660942\n            };\n        }\n    };\n\nclass App extends React.Component {\n    state = {\n        widths: {\n            id: 100,\n        }\n    }\n    onResizeChange = (dataIndex, value) => {\n        const {widths} = this.state;\n        widths[dataIndex] = widths[dataIndex] + value;\n        this.setState({\n            widths\n        });\n    }\n    render() {\n        return (<Table dataSource={dataSource()}\n            rowSelection={rowSelection} onResizeChange={this.onResizeChange}>\n            <Table.Column title=\"Id\" dataIndex=\"id\" resizable width={this.state.widths.id}/>\n            <Table.Column title=\"Title\" dataIndex=\"title.name\" width={400}/>\n            <Table.Column title=\"Time\" dataIndex=\"time\" width={600}/>\n            <Table.Column cell={render} width={200}/>\n        </Table>);\n    }\n}\n\nReactDOM.render(<App/>, mountNode);\n````","html":"<script>(function(){\"use strict\";\n\nvar _createClass = function () { function defineProperties(target, props) { for (var i = 0; i < props.length; i++) { var descriptor = props[i]; descriptor.enumerable = descriptor.enumerable || false; descriptor.configurable = true; if (\"value\" in descriptor) descriptor.writable = true; Object.defineProperty(target, descriptor.key, descriptor); } } return function (Constructor, protoProps, staticProps) { if (protoProps) defineProperties(Constructor.prototype, protoProps); if (staticProps) defineProperties(Constructor, staticProps); return Constructor; }; }();\n\nvar _next = require(\"@alifd/next\");\n\nfunction _classCallCheck(instance, Constructor) { if (!(instance instanceof Constructor)) { throw new TypeError(\"Cannot call a class as a function\"); } }\n\nfunction _possibleConstructorReturn(self, call) { if (!self) { throw new ReferenceError(\"this hasn't been initialised - super() hasn't been called\"); } return call && (typeof call === \"object\" || typeof call === \"function\") ? call : self; }\n\nfunction _inherits(subClass, superClass) { if (typeof superClass !== \"function\" && superClass !== null) { throw new TypeError(\"Super expression must either be null or a function, not \" + typeof superClass); } subClass.prototype = Object.create(superClass && superClass.prototype, { constructor: { value: subClass, enumerable: false, writable: true, configurable: true } }); if (superClass) Object.setPrototypeOf ? Object.setPrototypeOf(subClass, superClass) : subClass.__proto__ = superClass; }\n\nvar onChange = function onChange() {\n    var _console;\n\n    (_console = console).log.apply(_console, arguments);\n},\n    dataSource = function dataSource() {\n    var result = [];\n    for (var i = 0; i < 5; i++) {\n        result.push({\n            title: {\n                name: \"Quotation for 1PCS Nano \" + (3 + i) + \".0 controller compatible\"\n            },\n            id: 100306660940 + i,\n            time: 2000 + i\n        });\n    }\n    return result;\n},\n    _render = function _render(value, index, record) {\n    return React.createElement(\n        \"a\",\n        null,\n        \"Remove(\",\n        record.id,\n        \")\"\n    );\n},\n    rowSelection = {\n    onChange: onChange,\n    getProps: function getProps(record) {\n        return {\n            disabled: record.id === 100306660942\n        };\n    }\n};\n\nvar App = function (_React$Component) {\n    _inherits(App, _React$Component);\n\n    function App() {\n        var _ref;\n\n        var _temp, _this, _ret;\n\n        _classCallCheck(this, App);\n\n        for (var _len = arguments.length, args = Array(_len), _key = 0; _key < _len; _key++) {\n            args[_key] = arguments[_key];\n        }\n\n        return _ret = (_temp = (_this = _possibleConstructorReturn(this, (_ref = App.__proto__ || Object.getPrototypeOf(App)).call.apply(_ref, [this].concat(args))), _this), _this.state = {\n            widths: {\n                id: 100\n            }\n        }, _this.onResizeChange = function (dataIndex, value) {\n            var widths = _this.state.widths;\n\n            widths[dataIndex] = widths[dataIndex] + value;\n            _this.setState({\n                widths: widths\n            });\n        }, _temp), _possibleConstructorReturn(_this, _ret);\n    }\n\n    _createClass(App, [{\n        key: \"render\",\n        value: function render() {\n            return React.createElement(\n                _next.Table,\n                { dataSource: dataSource(),\n                    rowSelection: rowSelection, onResizeChange: this.onResizeChange },\n                React.createElement(_next.Table.Column, { title: \"Id\", dataIndex: \"id\", resizable: true, width: this.state.widths.id }),\n                React.createElement(_next.Table.Column, { title: \"Title\", dataIndex: \"title.name\", width: 400 }),\n                React.createElement(_next.Table.Column, { title: \"Time\", dataIndex: \"time\", width: 600 }),\n                React.createElement(_next.Table.Column, { cell: _render, width: 200 })\n            );\n        }\n    }]);\n\n    return App;\n}(React.Component);\n\nReactDOM.render(React.createElement(App, null), mountNode);})()</script><div class=\"highlight\"><pre class=\"language-jsx\"><code class=\"language-jsx\"><span class=\"token keyword\">import</span> <span class=\"token punctuation\">{</span> Table <span class=\"token punctuation\">}</span> <span class=\"token keyword\">from</span> <span class=\"token string\">'@alifd/next'</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">const</span> <span class=\"token function-variable function\">onChange</span> <span class=\"token operator\">=</span> <span class=\"token keyword\">function</span><span class=\"token punctuation\">(</span><span class=\"token operator\">...</span>args<span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        console<span class=\"token punctuation\">.</span><span class=\"token function\">log</span><span class=\"token punctuation\">(</span><span class=\"token operator\">...</span>args<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span><span class=\"token punctuation\">,</span>\n    <span class=\"token function-variable function\">dataSource</span> <span class=\"token operator\">=</span> <span class=\"token punctuation\">(</span><span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">const</span> result <span class=\"token operator\">=</span> <span class=\"token punctuation\">[</span><span class=\"token punctuation\">]</span><span class=\"token punctuation\">;</span>\n        <span class=\"token keyword\">for</span> <span class=\"token punctuation\">(</span><span class=\"token keyword\">let</span> i <span class=\"token operator\">=</span> <span class=\"token number\">0</span><span class=\"token punctuation\">;</span> i <span class=\"token operator\">&lt;</span> <span class=\"token number\">5</span><span class=\"token punctuation\">;</span> i<span class=\"token operator\">++</span><span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n            result<span class=\"token punctuation\">.</span><span class=\"token function\">push</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">{</span>\n                title<span class=\"token punctuation\">:</span> <span class=\"token punctuation\">{</span>\n                    name<span class=\"token punctuation\">:</span> <span class=\"token template-string\"><span class=\"token string\">`Quotation for 1PCS Nano </span><span class=\"token interpolation\"><span class=\"token interpolation-punctuation punctuation\">${</span><span class=\"token number\">3</span> <span class=\"token operator\">+</span> i<span class=\"token interpolation-punctuation punctuation\">}</span></span><span class=\"token string\">.0 controller compatible`</span></span><span class=\"token punctuation\">,</span>\n                <span class=\"token punctuation\">}</span><span class=\"token punctuation\">,</span>\n                id<span class=\"token punctuation\">:</span> <span class=\"token number\">100306660940</span> <span class=\"token operator\">+</span> i<span class=\"token punctuation\">,</span>\n                time<span class=\"token punctuation\">:</span> <span class=\"token number\">2000</span> <span class=\"token operator\">+</span> i\n            <span class=\"token punctuation\">}</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n        <span class=\"token punctuation\">}</span>\n        <span class=\"token keyword\">return</span> result<span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span><span class=\"token punctuation\">,</span>\n    <span class=\"token function-variable function\">render</span> <span class=\"token operator\">=</span> <span class=\"token punctuation\">(</span>value<span class=\"token punctuation\">,</span> index<span class=\"token punctuation\">,</span> record<span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">return</span> <span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>a</span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">Remove(</span><span class=\"token punctuation\">{</span>record<span class=\"token punctuation\">.</span>id<span class=\"token punctuation\">}</span><span class=\"token plain-text\">)</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>a</span><span class=\"token punctuation\">></span></span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span><span class=\"token punctuation\">,</span>\n    rowSelection <span class=\"token operator\">=</span> <span class=\"token punctuation\">{</span>\n        onChange<span class=\"token punctuation\">:</span> onChange<span class=\"token punctuation\">,</span>\n        getProps<span class=\"token punctuation\">:</span> <span class=\"token punctuation\">(</span>record<span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">{</span>\n            <span class=\"token keyword\">return</span> <span class=\"token punctuation\">{</span>\n                disabled<span class=\"token punctuation\">:</span> record<span class=\"token punctuation\">.</span>id <span class=\"token operator\">===</span> <span class=\"token number\">100306660942</span>\n            <span class=\"token punctuation\">}</span><span class=\"token punctuation\">;</span>\n        <span class=\"token punctuation\">}</span>\n    <span class=\"token punctuation\">}</span><span class=\"token punctuation\">;</span>\n\n<span class=\"token keyword\">class</span> <span class=\"token class-name\">App</span> <span class=\"token keyword\">extends</span> <span class=\"token class-name\">React<span class=\"token punctuation\">.</span>Component</span> <span class=\"token punctuation\">{</span>\n    state <span class=\"token operator\">=</span> <span class=\"token punctuation\">{</span>\n        widths<span class=\"token punctuation\">:</span> <span class=\"token punctuation\">{</span>\n            id<span class=\"token punctuation\">:</span> <span class=\"token number\">100</span><span class=\"token punctuation\">,</span>\n        <span class=\"token punctuation\">}</span>\n    <span class=\"token punctuation\">}</span>\n    <span class=\"token function-variable function\">onResizeChange</span> <span class=\"token operator\">=</span> <span class=\"token punctuation\">(</span>dataIndex<span class=\"token punctuation\">,</span> value<span class=\"token punctuation\">)</span> <span class=\"token operator\">=></span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">const</span> <span class=\"token punctuation\">{</span>widths<span class=\"token punctuation\">}</span> <span class=\"token operator\">=</span> <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>state<span class=\"token punctuation\">;</span>\n        widths<span class=\"token punctuation\">[</span>dataIndex<span class=\"token punctuation\">]</span> <span class=\"token operator\">=</span> widths<span class=\"token punctuation\">[</span>dataIndex<span class=\"token punctuation\">]</span> <span class=\"token operator\">+</span> value<span class=\"token punctuation\">;</span>\n        <span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span><span class=\"token function\">setState</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">{</span>\n            widths\n        <span class=\"token punctuation\">}</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n    <span class=\"token function\">render</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">)</span> <span class=\"token punctuation\">{</span>\n        <span class=\"token keyword\">return</span> <span class=\"token punctuation\">(</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Table</span> <span class=\"token attr-name\">dataSource</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token function\">dataSource</span><span class=\"token punctuation\">(</span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">}</span></span>\n            <span class=\"token attr-name\">rowSelection</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>rowSelection<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">onResizeChange</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>onResizeChange<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Table.Column</span> <span class=\"token attr-name\">title</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>Id<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">dataIndex</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>id<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">resizable</span> <span class=\"token attr-name\">width</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token keyword\">this</span><span class=\"token punctuation\">.</span>state<span class=\"token punctuation\">.</span>widths<span class=\"token punctuation\">.</span>id<span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Table.Column</span> <span class=\"token attr-name\">title</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>Title<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">dataIndex</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>title.name<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">width</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token number\">400</span><span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Table.Column</span> <span class=\"token attr-name\">title</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>Time<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">dataIndex</span><span class=\"token attr-value\"><span class=\"token punctuation\">=</span><span class=\"token punctuation\">\"</span>time<span class=\"token punctuation\">\"</span></span> <span class=\"token attr-name\">width</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token number\">600</span><span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n            </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>Table.Column</span> <span class=\"token attr-name\">cell</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span>render<span class=\"token punctuation\">}</span></span> <span class=\"token attr-name\">width</span><span class=\"token script language-javascript\"><span class=\"token script-punctuation punctuation\">=</span><span class=\"token punctuation\">{</span><span class=\"token number\">200</span><span class=\"token punctuation\">}</span></span><span class=\"token punctuation\">/></span></span><span class=\"token plain-text\">\n        </span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;/</span>Table</span><span class=\"token punctuation\">></span></span><span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span>\n    <span class=\"token punctuation\">}</span>\n<span class=\"token punctuation\">}</span>\n\nReactDOM<span class=\"token punctuation\">.</span><span class=\"token function\">render</span><span class=\"token punctuation\">(</span><span class=\"token tag\"><span class=\"token tag\"><span class=\"token punctuation\">&lt;</span>App</span><span class=\"token punctuation\">/></span></span><span class=\"token punctuation\">,</span> mountNode<span class=\"token punctuation\">)</span><span class=\"token punctuation\">;</span></code></pre></div>"}