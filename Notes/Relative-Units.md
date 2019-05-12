# Relative Units

<p>Ems are relative to the parent or inherits font-size from their parent so it always looks up for the parent font-size</p>
Eg:

<pre>
      <div class="parent">
      content
      </div>

      .parent{
            font-size:1em; which will default to 16px
            padding:1.2em;which will be 1.2em * the absolute value of font-size 16px=19.2px;
      }

      So if font-size changes the padding will also change relatively and the rendered or computed value will be always in absolute value(pixels).

      
</pre>

<pre>
      body{
            font-size:10px
      }

      <div class="text-content">
      Sample text
      
      </div>

      .text-content{
            font-size:1.5em;this will calculate to 15px(font-size inherited from the body)
            padding:0.5em;this will be based on the text-content font-size since it is the parent here
            so it will be calulated 0.5*15px(always the absolute value)=7.5px;
      }


</pre>

The caveat with em is they create issues when we have nested elements. So in order to correct it we have
<i>rem</i> Root em.

So it is usually given to the Root that is HTML using :root which will default to HTML.

<pre>
      :root{
            font-size:1em; defaults to 16px;
      }

      .div{
            font-size:1.2 rem which will be 16*1.2 =19.2px;
            padding:0.5em;
      }
</pre>

The advantage is, however deep the nesting is font-size will be always 19.2px and so it removes the problem with inheritance

Tip: Always use rem for fonts and em for paddings
