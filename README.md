# IPA-Keyboard
<i>IPA Keyboard</i> - strona umożliwiająca pisanie w alfabecie fonetycznym <a href="https://pl.wikipedia.org/wiki/Mi%C4%99dzynarodowy_alfabet_fonetyczny">IPA</a> za pomocą klawiatury oraz przycisków na stronie. Wprowadzony tekst będzie się pojawiać w elemencie <code>input</code>. Następnie po kliknięciu na element lewym przyciskiem myszy, tekst zostanie skopiowany do schowka.<br>

Zestaw znaków IPA jest początkowo ograniczony, jednak można samemu dodać inne znaki w pliku <code><b>ipa-chars.js</b></code>, dodając nowy obiekt JSON do tablicy JSON znajdującej się w pliku. Trzeba jednak zachować prawidłowy format obiektu, dodając do niego następujące elementy (nie wszystkie są wymagane):
<ul>
<li><i><b>char</b></i> (<b>Wymagane</b>) - zawiera symbol IPA, który ma być wyświetlany na stronie. 
<li><i><b>code</b></i> (<b>Wymagane</b>) - powinien zawierać heksadecymalny kod HTML znaku (np. dla <b>ø</b> będzie to <b>&#38#248</b>), jeżeli znak ten nie zawiera się w tabeli ASCII (czyli jeżeli posiada jakikolwiek znak diakrytyczny lub jest innym niestandardowym znakiem IPA). W przeciwnym przypadku <i><b>code</b></i> musi mieć wartość <code>null</code></li>
<li><i><b>key</b></i> (<b>Opcjonalne</b>) - określa klawisz, po którego kliknięciu znak zostanie wstawiony do elementu <code>input</code>. Mała litera (<i>lower case</i>) oznacza klawisz bez <b>Shift</b>, natomiast duża litera (<i>upper case</i>) klawisz z przytrzymanym <b>Shift</b>. Dodatkowo nazwa klawisza może być poprzedzona znakiem "<b>$</b>", wtedy będzie dodatkowo wymaganie trzymanie klawisza <b>alt</b>. Jeżeli klucz <i><b>key</b></i> będzie <code><span style="color:#b0b0b0;">undefined</span></code>, zostanie do niego skopiowana wartość klucza <i><b>char</b></i>.</li>
</ul>
