<h1>CSS-Flexbox - Sass-Mixins</h1>

Excellent CSS-Flexbox - Sass-Mixins

<b>How to use?</b>
<pre>
.div{
    @include flex(row,center,between)
}
</pre>

1: Direction. Column or Row. Default = row<br>
2: Vertical Align. Default = flex-start<br>
3: Horizontal align. Default = flex-start<br>
4: Wrap. Default = nowrap. No required <br>

<pre>
@mixin flex($direction:row, $vertical:flex-start, $horizontal:flex-start, $wrap:nowrap){
    display:flex;
    @if($direction==row){
        flex-direction: row;
        @if($vertical==center){
            align-items:center;
        }@else if($vertical==start){
            align-items: flex-start;
        }@else if($vertical==end){
            align-items: flex-end;  
        }
        @if($horizontal==center){
            justify-content: center;
        }@else if($horizontal==start){
            justify-content: flex-start;
        }@else if($horizontal==end){
            justify-content: flex-end;
        }@else if($horizontal==between){
            justify-content: space-between;
        }
        @if($wrap==wrap){
            flex-wrap:wrap;
        }
    }@else if($direction==column){
        flex-direction: column;
        @if($vertical==center){
            align-items: center;
        }@else if($vertical==start){
            align-items: flex-start;
        }@else if($vertical==end){
            align-items: flex-end;
        }   
        @if($horizontal==center){
            justify-content:center;
        }@else if($horizontal==start){
            justify-content: flex-start;
        }@else if($horizontal==end){
            justify-content: flex-end;  
        }@else if($horizontal==between){
            justify-content: space-between;  
        }@else{
            justify-content:center;
        }
    }
}
</pre>

