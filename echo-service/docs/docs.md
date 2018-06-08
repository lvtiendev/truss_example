# echo

The package name determines the name of the directories that truss creates
 for `package echo;` truss will create the directory "echo-service".

## echo.proto

### Messages

<a name="EchoRequest"></a>

#### EchoRequest

| Name | Type | Field Number | Description|
| ---- | ---- | ------------ | -----------|
| In | TYPE_STRING | 1 |  |

<a name="LouderRequest"></a>

#### LouderRequest

| Name | Type | Field Number | Description|
| ---- | ---- | ------------ | -----------|
| In | TYPE_STRING | 1 | In is the string to echo back |
| Loudness | TYPE_INT32 | 2 | Loudness is the number of exclamations marks to add to the echoed string |

<a name="EchoResponse"></a>

#### EchoResponse

| Name | Type | Field Number | Description|
| ---- | ---- | ------------ | -----------|
| Out | TYPE_STRING | 1 |  |

### Services

#### Echo

| Method Name | Request Type | Response Type | Description|
| ---- | ---- | ------------ | -----------|
| Echo | EchoRequest | EchoResponse | Echo "echos" the incoming string |
| Louder | LouderRequest | EchoResponse | Louder "echos" the incoming string with `Loudness` additional exclamation marks |
| LouderGet | LouderRequest | EchoResponse | LouderGet is the same as Louder, but pulls fields other than Loudness (i.e. In) from query params instead of POST |

#### Echo - Http Methods

##### GET `/echo/`



| Parameter Name | Location | Type |
| ---- | ---- | ------------ |
| In | query | TYPE_STRING |

##### GET `/echo`



| Parameter Name | Location | Type |
| ---- | ---- | ------------ |
| In | query | TYPE_STRING |

##### POST `/louder/{Loudness}`



| Parameter Name | Location | Type |
| ---- | ---- | ------------ |
| In | body | TYPE_STRING |
| Loudness | path | TYPE_INT32 |

##### HEAD `/louder/{Loudness}`



| Parameter Name | Location | Type |
| ---- | ---- | ------------ |
| In | query | TYPE_STRING |
| Loudness | path | TYPE_INT32 |

##### GET `/louder/{Loudness}`



| Parameter Name | Location | Type |
| ---- | ---- | ------------ |
| In | query | TYPE_STRING |
| Loudness | path | TYPE_INT32 |


<style type="text/css">

body{
    font-family      : helvetica, arial, freesans, clean, sans-serif;
    color            : #003269;
    background-color : #fff;
    border-color     : #999999;
    border-width     : 2px;
    line-height      : 1.5;
    margin           : 2em 3em;
    text-align       :left;
    font-size        : 16px;
    padding          : 0 100px 0 100px;

    width         : 1024px;
    margin-top    : 0px;
    margin-bottom : 2em;
    margin-left   : auto;
    margin-right  : auto;
}

h1 {
    font-family : 'Gill Sans Bold', 'Optima Bold', Arial, sans-serif;
    color       : #577AD3;
    font-weight : 400;
    font-size   : 48px;
}
h2{
    margin-bottom : 1em;
    padding-top   : 0.5em;
    color         : #003269;
    font-size     : 36px;
}
h3{
    border-bottom : 1px dotted #aaa;
    color         : #4660A4;
    font-size     : 30px;
}
h4 {
    font-size: 24px;
}
h5 {
    font-size: 18px;
}
code {
    font-family      : Consolas, "Inconsolata", Menlo, Monaco, Lucida Console, Liberation Mono, DejaVu Sans Mono, Bitstream Vera Sans Mono, Courier New, monospace, serif; /* Taken from the stackOverflow CSS*/
    background-color : #f5f5f5;
    border           : 1px solid #e1e1e8;
}


pre {
    display          : block;
    background-color : #f5f5f5;
    border           : 1px solid #ccc;
    padding          : 3px 3px 3px 3px;
}
pre code {
    white-space      : pre-wrap;
    padding          : 0;
    border           : 0;
    background-color : code;
}

table {
	border-collapse: collapse; border-spacing: 0;
	width: 100%;
	margin-bottom : 3em;
}
td, th {
	vertical-align: top;
	padding: 4px 10px;
	border: 1px solid #9BC3EB;
}
tr:nth-child(even) td, tr:nth-child(even) th {
	background: #EBF4FE;
}
th:nth-child(4) {
	width: auto;
}

</style>
