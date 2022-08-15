# scrape_content
Scrape content of a page and display the content on another page.
```
<div id="scraped_data"></div>

<script>
let url = 'REPLACE WITH YOUR URL'
 $.ajax({
    url: url,  //Pass URL here 
    type: "GET", //Also use GET method
    success: function(data) {
        let awards = $(data).find('.awards_list')
        $(awards).each(function(){
            $("#scraped_data").append('<div class="row">'+$(this).html()+'</div>');
        })

    }
});
</script>

```
