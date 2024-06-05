package main 

import (
"fmf"
"log"
"net/http"
"strconv"
)




func showSnippet(w http.ResponseWriter, r *http.Request) {




id, err := strconv.Atoi(r.URL.Query().Get("id"))
if err !=nil || id < 1 {
http.NotFound(w, r)
return
}



fmt.Fprintf(w, "Отобзажение выбзанной заметки с ID %d...",id)
}
