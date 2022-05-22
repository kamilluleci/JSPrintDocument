# JSPrintDocument
Java Script Pritnt Document
<script type="text/javascript">

    if ('False' == "True" && ''=="true") {
        $(document).ready(function () {
            window.location.href = $("#pdfOlusturBtn").attr("href");
            });
        }

    function printPage(divName) {
        if ('False'=="True") {

            var printContentsYedek = document.getElementById(divName).innerHTML;
            var beyani = document.getElementsByClassName("printYok");
            for (var i = 0; i < beyani.length; i++) {
                beyani[i].style.display = "none";
            }
        }

        var printContents = document.getElementById(divName).innerHTML;
        if ('False' == "True") {
            document.getElementById(divName).innerHTML = printContentsYedek;
        }
        w = window.open();
        w.document.write(printContents);
        w.print();
        w.close();
    }
</script>
