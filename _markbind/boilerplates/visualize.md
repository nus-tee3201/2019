<trigger trigger="click" for="modal:visualize{{ title | replace(' ', '') }}">%%[Visualize execution]%%</trigger>

<modal large title="{{ title }}" id="modal:visualize{{ title | replace(' ', '') }}">

<iframe width="800" height="500" frameborder="0" src="http://pythontutor.com/iframe-embed.html#code={{ code | safe }}&codeDivHeight=400&codeDivWidth=350&cumulative=false&curInstr=0&heapPrimitives=false&origin=opt-frontend.js&py=3&rawInputLstJSON=%5B%5D&textReferences=false"> </iframe>

</modal>