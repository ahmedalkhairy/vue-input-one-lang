
import Vue from 'vue'



Vue.mixin({
    methods: {
    
        check_lang(event,lang){
        
            var arabicAlphabetAndWhiteSpace = /[ -.#ا-ي^0-9]/g;
            
            var englishAlphabetAndWhiteSpace = /[A-Za-z0-9 .#-]/g;
            
            var key = String.fromCharCode(event.which);
            
            var locale=lang==='ar'? arabicAlphabetAndWhiteSpace :englishAlphabetAndWhiteSpace;
            
            if (event.keyCode == 8 || event.keyCode == 37 || event.keyCode == 39 || locale.test(key)) {
            
                return true;
                
            }
            
            
            event.preventDefault();
            
        }
        
    }
    
})
