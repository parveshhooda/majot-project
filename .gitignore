# major-project
# i n c l u d e <A d a f r u i t F i n g e r p r i n t . h>
# d e f i n e m y S e ri al S e r i a l 1
A d a f r u i t F i n g e r p r i n t f i n g e r = A d a f r u i t F i n g e r p r i n t (& m y S e ri al ) ;
u i n t 8 t i d ;
c h a r s s i d [ ] = ”Ammuzzz ” ;
c h a r p a s s [ ] = ” a d i i c c c c c ” ;
c h a r s e r v e r [ ] = ”www. s o u t h e r n v i b e s . i n ” ;
S t r i n g u r i =” h t t p : / / www. s o u t h e r n v i b e s . i n / embedded / r v c s / r e s u l t . php ” ;
S t r i n g a =”08008837BF08 ” ;
S t r i n g b ;
S t r i n g c = ” ”; S t r i n g t o l l i d =”270029DE65B5 ” ;
S t r i n g s p e e d l i m i t 1 =”430077B7B132 ” ;
S t r i n g s p e e d l i m i t 2 =”08008837BF08 ” ;
S t r i n g n o rm al s p e e d 1 =”080089360EB9 ” ;
S t r i n g n o rm al s p e e d 2 =”27001939 F1F6 ” ;
S t r i n g t o l l i d g e t ;
i n t t o l l ;
# i n c l u d e <TinyGPS . h>
TinyGPS g p s ;
f l o a t l a t , l o n ;
i n t y e a r ;
49
College of Engineering Cherthala APPENDIX
b yt e month , day , hou r , mi n ute , s e c o n d ;
# d e f i n e Swit c h 1 A0
# d e f i n e Swit c h 2 A1
# d e f i n e Moto r 6
f l o a t v a l u e = 0;
f l o a t r e v = 0;
i n t rpm ;
i n t o l d t i m e = 0;
i n t tim e ;
i n t c o u nt = 0;
v oi d i s r ( )
{
r e v ++;
}
v oi d s e t u p ( )
{
S e r i a l . b e gi n ( 9 6 0 0 ) ;
f i n g e r . b e gi n ( 5 7 6 0 0 ) ;
a t t a c h I n t e r r u p t ( 0 , i s r , RISING ) ;
S e r i a l . p r i n t l n (”−−−−−−−−−−−−REAL TIME VEHICLE MONITORING AND CONTROLL SYSTEM−−−−−−−−−−−−−−−−−”);
i f ( f i n g e r . v e r i f y P a s s w o r d ( ) )
{
S e r i a l . p r i n t l n ( ” Found f i n g e r p r i n t s e n s o r ! ! ! ! ! ” ) ;
}
e l s e
{
S e r i a l . p r i n t l n ( ” Did n ot f i n d f i n g e r p r i n t s e n s o r : ( ” ) ;
w hil e ( 1 )
Department of Electronics & Communication Engineering 50
College of Engineering Cherthala APPENDIX
{
d e l a y ( 1 ) ;
}
}
pinMode ( Switc h 1 , OUTPUT ) ;
pinMode ( Switc h 2 , OUTPUT ) ;
pinMode ( Motor , OUTPUT ) ;
pinMode ( Motor1 , OUTPUT ) ;
S e r i a l 2 . b e gi n ( 1 1 5 2 0 0 ) ; / / WIFI
S e r i a l 3 . b e gi n ( 9 6 0 0 ) ; / / RFID
}
u i n t 8 t r e a d n um b e r ( v oi d )
{
u i n t 8 t num = 0 ;
w hil e ( num == 0 )
{
w hil e ( ! S e r i a l . a v a i l a b l e ( ) ) ;
num = S e r i a l . p a r s e I n t ( ) ;
}
r e t u r n num ;
}
v oi d l o o p ( )
{
i f ( S e r i a l . a v a i l a b l e ( ) )
{
i f ( g p s . e nc o de ( S e r i a l . r e a d ( ) ) )
Department of Electronics & Communication Engineering 51
College of Engineering Cherthala APPENDIX
{
g p s . f g e t p o s i t i o n (& l a t ,& l o n ) ;
d e l a y ( 1 0 0 0 ) ;
g p s . c r a c k d a t e t i m e (& y e a r ,&month ,& day ,& hou r ,& mi n ute ,& s e c o n d ) ;
}
}
i f ( c o u nt ==0 )
{
r e s e t ( ) ;
w i f i i n i t ( ) ;
c o n n e ct Wi fi ( ) ;
}
i f ( c o u nt ==1 )
{
i f ( d i g i t a l R e a d ( Swit c h 1 )==HIGH )
{
w hil e ( d i g i t a l R e a d ( Swit c h 1 )==HIGH ) ;
S e r i a l . p r i n t l n ( ” Ready t o e n r o l l a f i n g e r p r i n t ! ” ) ;
S e r i a l . p r i n t l n ( ” P l e a s e t y p e i n t h e ID # you want t o s a v e t h i s f i n g e r a s . . . ” ) ;
i d = r e a d n um b e r ( ) ;
i f ( i d == 0 )
{
r e t u r n ;
}
S e r i a l . p r i n t ( ” E n r o l l i n g ID # ” ) ;
S e r i a l . p r i n t l n ( i d ) ;
w hil e ( ! g e t F i n g e r p r i n t E n r o l l ( ) ) ;
Department of Electronics & Communication Engineering 52
College of Engineering Cherthala APPENDIX
}
i f ( d i g i t a l R e a d ( Swit c h 2 )==HIGH )
{
w hil e ( d i g i t a l R e a d ( Swit c h 2 )==HIGH ) ;
S e r i a l . p r i n t l n ( ” W aiti n g f o r v a l i d f i n g e r . . . ” ) ;
d e l a y ( 5 0 0 0 ) ;
g e t F i n g e r p r i n t I D e z ( ) ;
d e l a y ( 5 0 ) ;
}
}
i f ( c o u nt ==2 )
{
d i g i t a l W r i t e ( Motor , HIGH ) ;
d i g i t a l W r i t e ( Motor1 ,LOW) ;
d e l a y ( 1 0 0 0 ) ;
d e t a c h I n t e r r u p t ( 0 ) ;
tim e = m i l l i s ()− o l d t i m e ;
rpm = ( r e v / tim e ) * 6 0 0 0 0;
o l d t i m e = m i l l i s ( ) ;
r e v = 0;
S e r i a l . p r i n t ( rpm ) ;
S e r i a l . p r i n t l n ( ” RPM” ) ;
a t t a c h I n t e r r u p t ( 0 , i s r , RISING ) ;
d e l a y ( 1 0 0 0 ) ;
S e r i a l . p r i n t l n ( ”* * * * * The GPS R e c ei v e d S i g n a l * * * * * ” ) ;
S e r i a l . p r i n t ( ” P o s i t i o n : ” ) ;
S e r i a l . p r i n t ( ” h t t p : / / maps . g o o gl e . com / maps ? q= l o c : ” ) ;
Department of Electronics & Communication Engineering 53
College of Engineering Cherthala APPENDIX
S e r i a l . p r i n t ( l a t == TinyGPS : : GPS INVALID F ANGLE ? 0 . 0 : l a t , 6 ) ;
S e r i a l . p r i n t ( l a t ) ;
S e r i a l . p r i n t ( ” , ” ) ;
S e r i a l . p r i n t ( l o n == \ p a r TinyGPS : : GPS INVALID F ANGLE ? 0 . 0 : l o n , 6 ) ;
S e r i a l . p r i n t l n ( l o n ) ;
d e l a y ( 2 0 0 ) ;
S e r i a l . p r i n t ( ” Date : ” ) ;
S e r i a l . p r i n t ( day , DEC ) ;
S e r i a l . p r i n t ( ” / ” ) ;
S e r i a l . p r i n t ( month , DEC ) ;
S e r i a l . p r i n t ( ” / ” ) ;
S e r i a l . p r i n t l n ( y e a r ) ;
d e l a y ( 1 0 0 0 ) ;
i f ( S e r i a l 3 . a v a i l a b l e ( ) >0 )
{
b= S e r i a l 3 . r e a d S t r i n g ( ) ;
S e r i a l . p r i n t ( b ) ;
i f ( b==a )
{
S e r i a l . p r i n t ( ” T o l l b o ot h : ” ) ;
t o l l = 4 0;
S e r i a l . p r i n t l n ( t o l l ) ;
}
}
d e l a y ( 3 0 0 0 ) ;
h t t p p o s t ( ) ;
d e l a y ( 2 0 0 0 ) ;
t o l l = 0;
}
Department of Electronics & Communication Engineering 54
College of Engineering Cherthala APPENDIX
} # d e f i n e Moto r1 7
f l o a t v a l u e = 0;
f l o a t r e v = 0;
i n t rpm ;
i n t o l d t i m e = 0;
i n t tim e ;
i n t c o u nt = 0;
v oi d i s r ( )
{
r e v ++;
}
v oi d s e t u p ( )
{
S e r i a l . b e gi n ( 9 6 0 0 ) ;
f i n g e r . b e gi n ( 5 7 6 0 0 ) ;
a t t a c h I n t e r r u p t ( 0 , i s r , RISING ) ;
S e r i a l . p r i n t l n (”−−−−−−−−−−−−REAL TIME VEHICLE MONITORING AND CONTROLL SYSTEM−−−−−−−−−−−−−−−−−”);
i f ( f i n g e r . v e r i f y P a s s w o r d ( ) )
{
S e r i a l . p r i n t l n ( ” Found f i n g e r p r i n t s e n s o r ! ! ! ! ! ” ) ;
}
e l s e
{
S e r i a l . p r i n t l n ( ” Did n ot f i n d f i n g e r p r i n t s e n s o r : ( ” ) ;
w hil e ( 1 )
{
d e l a y ( 1 ) ;
}
}
Department of Electronics & Communication Engineering 55
College of Engineering Cherthala APPENDIX
pinMode ( Switc h 1 , OUTPUT ) ;
pinMode ( Switc h 2 , OUTPUT ) ;
pinMode ( Motor , OUTPUT ) ;
pinMode ( Motor1 , OUTPUT ) ;
S e r i a l 2 . b e gi n ( 1 1 5 2 0 0 ) ;
S e r i a l 3 . b e gi n ( 9 6 0 0 ) ;
}
u i n t 8 t r e a d n um b e r ( v oi d )
{
u i n t 8 t num = 0 ;
w hil e ( num == 0 )
{
w hil e ( ! S e r i a l . a v a i l a b l e ( ) ) ;
num = S e r i a l . p a r s e I n t ( ) ;
}
r e t u r n num ;
}
v oi d l o o p ( )
{
i f ( S e r i a l . a v a i l a b l e ( ) )
{
i f ( g p s . e nc o de ( S e r i a l . r e a d ( ) ) )
{
g p s . f g e t p o s i t i o n (& l a t ,& l o n ) ;
d e l a y ( 1 0 0 0 ) ;
g p s . c r a c k d a t e t i m e (& y e a r ,&month ,& day ,& hou r ,& mi n ute ,& s e c o n d ) ;
}
Department of Electronics & Communication Engineering 56
College of Engineering Cherthala APPENDIX
}
i f ( c o u nt ==0 )
{
r e s e t ( ) ;
w i f i i n i t ( ) ;
c o n n e c tWi fi ( ) ;
}
i f ( c o u nt ==1 )
{
i f ( d i g i t a l R e a d ( Swit c h 1 )==HIGH )
{
w hil e ( d i g i t a l R e a d ( Swit c h 1 )==HIGH ) ;
S e r i a l . p r i n t l n ( ” Ready t o e n r o l l a f i n g e r p r i n t ! ” ) ;
S e r i a l . p r i n t l n ( ” P l e a s e t y p e i n t h e ID # you want t o s a v e t h i s f i n g e r a s . . . ” ) ;
i d = r e a d n um b e r ( ) ;
i f ( i d == 0 )
{
r e t u r n ;
}
S e r i a l . p r i n t ( ” E n r o l l i n g ID # ” ) ;
S e r i a l . p r i n t l n ( i d ) ;
w hil e ( ! g e t F i n g e r p r i n t E n r o l l ( ) ) ;
}
i f ( d i g i t a l R e a d ( Swit c h 2 )==HIGH )
{
w hil e ( d i g i t a l R e a d ( Swit c h 2 )==HIGH ) ;
Department of Electronics & Communication Engineering 57
College of Engineering Cherthala APPENDIX
S e r i a l . p r i n t l n ( ” W aiti n g f o r v a l i d f i n g e r . . . ” ) ;
d e l a y ( 5 0 0 0 ) ;
g e t F i n g e r p r i n t I D e z ( ) ;
d e l a y ( 5 0 ) ;
}
}
i f ( c o u nt ==2 )
{
d i g i t a l W r i t e ( Motor , HIGH ) ;
d i g i t a l W r i t e ( Motor1 ,LOW) ;
d e l a y ( 1 0 0 0 ) ;
d e t a c h I n t e r r u p t ( 0 ) ;
tim e = m i l l i s ()− o l d t i m e ;
rpm = ( r e v / tim e ) * 6 0 0 0 0;
o l d t i m e = m i l l i s ( ) ;
r e v = 0;
S e r i a l . p r i n t ( rpm ) ;
S e r i a l . p r i n t l n ( ” RPM” ) ;
a t t a c h I n t e r r u p t ( 0 , i s r , RISING ) ;
d e l a y ( 1 0 0 0 ) ;
/ / g p s 1 ( ) ; / / g p s
S e r i a l . p r i n t l n ( ”* * * * * The GPS R e c ei v e d S i g n a l * * * * * ” ) ;
S e r i a l . p r i n t ( ” P o s i t i o n : ” ) ;
S e r i a l . p r i n t ( ” h t t p : / / maps . g o o gl e . com / maps ? q= l o c : ” ) ;
S e r i a l . p r i n t ( l a t == TinyGPS : : GPS INVALID F ANGLE ? 0 . 0 : l a t , 6 ) ;
S e r i a l . p r i n t ( l a t ) ;
S e r i a l . p r i n t ( ” , ” ) ;
S e r i a l . p r i n t ( l o n ==
Department of Electronics & Communication Engineering 58
College of Engineering Cherthala APPENDIX
TinyGPS : : GPS INVALID F ANGLE ? 0 . 0 : l o n , 6 ) ;
S e r i a l . p r i n t l n ( l o n ) ;
d e l a y ( 2 0 0 ) ;
S e r i a l . p r i n t ( ” Date : ” ) ;
S e r i a l . p r i n t ( day , DEC ) ;
S e r i a l . p r i n t ( ” / ” ) ;
S e r i a l . p r i n t ( month , DEC ) ;
S e r i a l . p r i n t ( ” / ” ) ;
S e r i a l . p r i n t l n ( y e a r ) ;
d e l a y ( 1 0 0 0 ) ;
i f ( S e r i a l 3 . a v a i l a b l e ( ) >0 )
{
t o l l i d g e t = S e r i a l 3 . r e a d S t r i n g ( ) ;
S e r i a l . p r i n t ( t o l l i d g e t ) ;
i f ( t o l l i d g e t == t o l l i d )
{
S e r i a l . p r i n t l n ( ”TOLL NEAR YOU . . . . . . . . . . . . . . . . . . . ” ) ;
d e l a y ( 2 0 0 0 ) ;
S e r i a l . p r i n t ( ” T o l l b o ot h : ” ) ;
t o l l = 4 0;
S e r i a l . p r i n t l n ( t o l l ) ;
}
i f ( t o l l i d g e t == s p e e d l i m i t 1 )
{
S e r i a l . p r i n t l n ( ” Speed l i m i t a r e a
: GO SLOW . . . . . . . . . . . . . ” ) ;
a n al o gW rit e ( Motor , 1 0 0 ) ;
d e l a y ( 1 0 0 0 ) ;
}
Department of Electronics & Communication Engineering 59
College of Engineering Cherthala APPENDIX
i f ( t o l l i d g e t == n o rm al s p e e d 1 )
{
S e r i a l . p r i n t l n ( ”NORMAL SPEED . . . . . . . . . . . . . . ” ) ;
d i g i t a l W r i t e ( Motor , HIGH ) ;
d i g i t a l W r i t e ( Motor1 ,LOW) ;
d e l a y ( 1 0 0 0 ) ;
}
i f ( t o l l i d g e t == s p e e d l i m i t 2 )
{
S e r i a l . p r i n t l n ( ” Speed l i m i t a r e a
: GO SLOW . . . . . . . . . . . . . ” ) ;
a n al o gW rit e ( Motor , 1 0 0 ) ;
d e l a y ( 1 0 0 0 ) ;
}
i f ( t o l l i d g e t == n o rm al s p e e d 2 )
{
S e r i a l . p r i n t l n ( ”NORMAL SPEED . . . . . . . . . . . . . . ” ) ;
d i g i t a l W r i t e ( Motor , HIGH ) ;
d i g i t a l W r i t e ( Motor1 ,LOW) ;
d e l a y ( 1 0 0 0 ) ;
}
}
d e l a y ( 3 0 0 0 ) ;
h t t p p o s t ( ) ;
d e l a y ( 2 0 0 0 ) ;
t o l l = 0;
}
}
Department of Electronics & Communication Engineering 60
College of Engineering Cherthala APPENDIX
u i n t 8 t g e t F i n g e r p r i n t I D ( )
{
u i n t 8 t p = f i n g e r . g et Im a g e ( ) ;
s w i t c h ( p )
{
c a s e FINGERPRINT OK :
S e r i a l . p r i n t l n ( ” Image t a k e n ” ) ;
b r e a k ;
c a s e FINGERPRINT NOFINGER :
S e r i a l . p r i n t l n ( ” No f i n g e r d e t e c t e d ” ) ;
r e t u r n p ;
c a s e FINGERPRINT PACKETRECIEVEERR :
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
c a s e FINGERPRINT IMAGEFAIL :
S e r i a l . p r i n t l n ( ” Ima gi n g e r r o r ” ) ;
r e t u r n p ;
d e f a u l t :
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
r e t u r n p ;
}
p = f i n g e r . image2Tz ( ) ;
s w i t c h ( p )
{
c a s e FINGERPRINT OK :
S e r i a l . p r i n t l n ( ” Image c o n v e r t e d ” ) ;
b r e a k ;
Department of Electronics & Communication Engineering 61
College of Engineering Cherthala APPENDIX
c a s e FINGERPRINT IMAGEMESS :
S e r i a l . p r i n t l n ( ” Image t o o messy ” ) ;
r e t u r n p ;
c a s e FINGERPRINT PACKETRECIEVEERR :
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
c a s e FINGERPRINT FEATUREFAIL :
S e r i a l . p r i n t l n ( ” Could n ot f i n d
f i n g e r p r i n t f e a t u r e s ” ) ;
r e t u r n p ;
c a s e FINGERPRINT INVALIDIMAGE :
S e r i a l . p r i n t l n ( ” Could n ot f i n d f i n g e r p r i n t f e a t u r e s ” ) ;
r e t u r n p ;
d e f a u l t :
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
r e t u r n p ;
}
p = f i n g e r . f i n g e r F a s t S e a r c h ( ) ;
i f ( p == FINGERPRINT OK )
{
S e r i a l . p r i n t l n ( ” Found a p r i n t match ! ” ) ;
}
e l s e i f ( p == FINGERPRINT PACKETRECIEVEERR )
{
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
}
Department of Electronics & Communication Engineering 62
College of Engineering Cherthala APPENDIX
e l s e i f ( p == FINGERPRINT NOTFOUND ) {
S e r i a l . p r i n t l n ( ” Did n ot f i n d a match ” ) ;
r e t u r n p ;
}
e l s e
{
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
r e t u r n p ;
}
S e r i a l . p r i n t ( ” Found ID # ” ) ;
S e r i a l . p r i n t ( f i n g e r . f i n g e r I D ) ;
S e r i a l . p r i n t ( ” wit h c o n f i d e n c e o f ” ) ;
S e r i a l . p r i n t l n ( f i n g e r . c o n f i d e n c e ) ;
r e t u r n f i n g e r . f i n g e r I D ;
}
i n t g e t F i n g e r p r i n t I D e z ( )
{
u i n t 8 t p = f i n g e r . g et Im a g e ( ) ;
i f ( p != FINGERPRINT OK ) r e t u r n −1;
p = f i n g e r . image2Tz ( ) ;
i f ( p != FINGERPRINT OK ) r e t u r n −1;
p = f i n g e r . f i n g e r F a s t S e a r c h ( ) ;
i f ( p != FINGERPRINT OK ) r e t u r n −1;
Department of Electronics & Communication Engineering 63
College of Engineering Cherthala APPENDIX
S e r i a l . p r i n t ( ” Found ID # ” ) ;
S e r i a l . p r i n t ( f i n g e r . f i n g e r I D ) ;
S e r i a l . p r i n t ( ” wit h c o n f i d e n c e o f ” ) ;
S e r i a l . p r i n t l n ( f i n g e r . c o n f i d e n c e ) ;
c o u nt = 2;
S e r i a l . p r i n t l n (”−−−−−−−TACHOMETER AND GPS−−−−−−−−”);
r e t u r n c o u nt ;
r e t u r n f i n g e r . f i n g e r I D ;
}
/* * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * * */
/* * * * * * * * * * * * * * * * * * * * * * *FUNCTION FOR ENROLL
FINGERPRINT* * * * * * * * * * * * * * * */
u i n t 8 t g e t F i n g e r p r i n t E n r o l l ( )
{
i n t p = −1;
S e r i a l . p r i n t ( ” W aiti n g f o r v a l i d f i n g e r t o e n r o l l a s \ p a r # ” ) ; S e r i a l . p r i n t l n ( i d ) ;
w hil e ( p != FINGERPRINT OK )
{
p = f i n g e r . g et Im a g e ( ) ;
s w i t c h ( p ) {
c a s e FINGERPRINT OK :
S e r i a l . p r i n t l n ( ” Image t a k e n ” ) ;
b r e a k ;
c a s e FINGERPRINT NOFINGER :
S e r i a l . p r i n t l n ( ” . ” ) ;
b r e a k ;
c a s e FINGERPRINT PACKETRECIEVEERR :
Department of Electronics & Communication Engineering 64
College of Engineering Cherthala APPENDIX
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
b r e a k ;
c a s e FINGERPRINT IMAGEFAIL :
S e r i a l . p r i n t l n ( ” Ima gi n g e r r o r ” ) ;
b r e a k ;
d e f a u l t :
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
b r e a k ;
}
}
p = f i n g e r . image2Tz ( 1 ) ;
s w i t c h ( p )
{
c a s e FINGERPRINT OK :
S e r i a l . p r i n t l n ( ” Image c o n v e r t e d ” ) ;
c a s e FINGERPRINT IMAGEMESS :
S e r i a l . p r i n t l n ( ” Image t o o messy ” ) ;
r e t u r n p ;
c a s e FINGERPRINT PACKETRECIEVEERR :
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
c a s e FINGERPRINT FEATUREFAIL :
S e r i a l . p r i n t l n ( ” Could n ot f i n d f i n g e r p r i n t f e a t u r e s ” ) ;
r e t u r n p ;
c a s e FINGERPRINT INVALIDIMAGE :
S e r i a l . p r i n t l n ( ” Could n ot f i n d f i n g e r p r i n t f e a t u r e s ” ) ;
r e t u r n p ;
d e f a u l t :
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
Department of Electronics & Communication Engineering 65
College of Engineering Cherthala APPENDIX
r e t u r n p ;
}
S e r i a l . p r i n t l n ( ” Remove f i n g e r ” ) ;
d e l a y ( 2 0 0 0 ) ;
p = 0 ;
w hil e ( p != FINGERPRINT NOFINGER )
{
p = f i n g e r . g et Im a g e ( ) ;
}
S e r i a l . p r i n t ( ” ID ” ) ; S e r i a l . p r i n t l n ( i d ) ;
p = −1;
S e r i a l . p r i n t l n ( ” P l a c e same f i n g e r a g a i n ” ) ;
w hil e ( p != FINGERPRINT OK ) {
p = f i n g e r . g et Im a g e ( ) ;
s w i t c h ( p )
{
c a s e FINGERPRINT OK :
S e r i a l . p r i n t l n ( ” Image t a k e n ” ) ;
b r e a k ;
c a s e FINGERPRINT NOFINGER :
S e r i a l . p r i n t ( ” . ” ) ;
b r e a k ;
c a s e FINGERPRINT PACKETRECIEVEERR :
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
b r e a k ;
c a s e FINGERPRINT IMAGEFAIL :
S e r i a l . p r i n t l n ( ” Ima gi n g e r r o r ” ) ;
b r e a k ;
Department of Electronics & Communication Engineering 66
College of Engineering Cherthala APPENDIX
d e f a u l t :
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
b r e a k ;
}
}
p = f i n g e r . image2Tz ( 2 ) ;
s w i t c h ( p )
{
c a s e FINGERPRINT OK :
S e r i a l . p r i n t l n ( ” Image c o n v e r t e d ” ) ;
b r e a k ;
c a s e FINGERPRINT IMAGEMESS :
S e r i a l . p r i n t l n ( ” Image t o o messy ” ) ;
r e t u r n p ;
c a s e FINGERPRINT PACKETRECIEVEERR :
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
c a s e FINGERPRINT FEATUREFAIL :
S e r i }
} }
a l . p r i n t l n ( ” Could n ot f i n d f i n g e r p r i n t f e a t u r e s ” ) ;
r e t u r n p ;
c a s e FINGERPRINT INVALIDIMAGE :
S e r i a l . p r i n t l n ( ” Could n ot f i n d f i n g e r p r i n t f e a t u r e s ” ) ;
r e t u r n p ;
d e f a u l t :
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
r e t u r n p ;
}
Department of Electronics & Communication Engineering 67
College of Engineering Cherthala APPENDIX
S e r i a l . p r i n t ( ” C r e a t i n g model f o r # ” ) ;
S e r i a l . p r i n t l n ( i d ) ;
p = f i n g e r . c r e at eM o d el ( ) ;
i f ( p == FINGERPRINT OK )
{
S e r i a l . p r i n t l n ( ” P r i n t s matc he d ! ” ) ;
}
e l s e i f ( p == FINGERPRINT PACKETRECIEVEERR )
{
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
}
e l s e i f ( p == FINGERPRINT ENROLLMISMATCH )
{
S e r i a l . p r i n t l n ( ” F i n g e r p r i n t s di d n ot match ” ) ;
r e t u r n p ;
}
e l s e
{
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
r e t u r n p ;
}
S e r i a l . p r i n t ( ” ID ” ) ;
S e r i a l . p r i n t l n ( i d ) ;
p = f i n g e r . st o r eM o d el ( i d ) ;
i f ( p == FINGERPRINT OK )

{
S e r i a l . p r i n t l n ( ” S t o r e d ! ” ) ;
}
e l s e i f ( p == FINGERPRINT PACKETRECIEVEERR )
{
S e r i a l . p r i n t l n ( ” Communication e r r o r ” ) ;
r e t u r n p ;
}
e l s e i f ( p == FINGERPRINT BADLOCATION )
{
S e r i a l . p r i n t l n ( ” Could n ot s t o r e i n t h a t l o c a t i o n ” ) ;
r e t u r n p ;
}
e l s e i f ( p == FINGERPRINT FLASHERR )
{
S e r i a l . p r i n t l n ( ” E r r o r w r i t i n g t o f l a s h ” ) ;
r e t u r n p ;
}
e l s e
{
S e r i a l . p r i n t l n ( ” Unknown e r r o r ” ) ;
r e t u r n p ;
}
}
v oi d r e s e t ( )
{
S e r i a l 2 . p r i n t l n ( ”AT+RST ” ) ;
Department of Electronics & Communication Engineering 69
College of Engineering Cherthala APPENDIX
d e l a y ( 5 0 0 0 ) ;
i f ( S e r i a l 2 . f i n d ( ”OK” ) )
{
S e r i a l . p r i n t l n ( ” Module R e s et ” ) ;
}
}
v oi d w i f i i n i t ( )
{
S e r i a l 2 . p r i n t l n ( ”AT ” ) ;
S e r i a l 2 . p r i n t l n ( ”AT+CWMODE= 3 ” ) ;
S e r i a l 2 . p r i n t l n ( ”AT+GMR= ? ” ) ;
}
v oi d c o n n e ctWi fi ( )
{
S t r i n g cmd = ”AT+CWJAP=\”” + S t r i n g ( s s i d ) + ”\” ,\” ” + \ p a r S t r i n g ( p a s s ) + ” \ ” ” ;
S e r i a l 2 . p r i n t l n ( cmd ) ;
d e l a y ( 5 0 0 0 ) ;
i f ( S e r i a l 2 . f i n d ( ”OK” ) )
{
S e r i a l . p r i n t l n ( ” C o n n e ct e d ! ” ) ;
c o u nt = 1;
r e t u r n c o u nt ;
}
e l s e
{
S e r i a l . p r i n t l n ( ” Ca n n ot c o n n e ct t o w i f i ” ) ;
c o n n e c tWi fi ( ) ;
}

}
v oi d h t t p p o s t ( )
{
S t r i n g d a t a 2 = ” \ 0 ” ;
d a t a 2 = d a t a 2 + ” xyz= ” + ”KL07CR3456” +”*”+ ( S t r i n g ( f i n g e r . f i n g e r I D ) ) + ” * ” + ( S t r i n g ( rpm ) ) + ”*” + ” h t t p : / / maps . g o o gl e . com / maps ? q= l o c : ” + ( S t r i n g ( l a t , 6 ) ) + ” , ” + ( S t r i n g ( l o n , 6 ) ) + ”*” + S t r i n g ( t o l l ) ;
/ / c o n c a t e n a t i n g s t r i n g s
S e r i a l 2 . p r i n t ( ”AT+CIPSTART=\”TCP \ ” , \ ” ” ) ; / / s t a r t a TCP c o n n e c t i o n .
S e r i a l 2 . p r i n t ( s e r v e r ) ; / / s t a r t a TCP c o n n e c t i o n .
S e r i a l 2 . p r i n t l n ( ” \ ” , 8 0 ” ) ; / / s t a r t a TCP c o n n e c t i o n .
S e r i a l . p r i n t l n ( ” s e n t . . . . . . . . . ” ) ;
d e l a y ( 1 0 0 0 ) ;
i f ( S e r i a l 2 . f i n d ( ”OK” ) )
{
S e r i a l . p r i n t l n ( ” TCP c o n n e c t i o n r e a d y ” ) ;
}
d e l a y ( 1 0 0 0 ) ;
S t r i n g p o s t R e q u e s t = ”POST ” + u r i +” HTTP / 1 . 0 \ r \n ” + ” H o st : ” + s e r v e r + ”\ r \n ” + ” Acce pt : *” + ” / ” + ”*\ r \n ” + ” C o nt e nt−Le n gt h : ” + d a t a 2 . l e n g t h ( ) + ”\ r \n ” + ” C o nt e nt−Type : a p p l i c a t i o n / x−www−form−u r l e n c o d e d \ r \n ” + ”\ r \n ” + d a t a 2 ;
S t r i n g sendCmd = ”AT+CIPSEND = ” ; / / d e t e r m i n e t h e number o f c a r a c t e r s t o be s e n t .
S e r i a l 2 . p r i n t ( sendCmd ) ;
S e r i a l 2 . p r i n t l n ( p o s t R e q u e s t . l e n g t h ( ) ) ;
d e l a y ( 5 0 0 ) ;
d e l a y ( 1 0 0 0 ) ;
i f ( S e r i a l 2 . f i n d ( ” >” ) )
{
S e r i a l . p r i n t l n ( ” S e n di n g . . ” ) ;
S e r i a l 2 . p r i n t ( p o s t R e q u e s t ) ;
d e l a y ( 1 0 0 0 ) ;
i f ( S e r i a l 2 . f i n d ( ”SEND OK” ) )
{

S e r i a l . p r i n t l n ( ” P a c k et s e n t ” ) ;
w hil e ( S e r i a l 2 . a v a i l a b l e ( ) )
{
S t r i n g tmpResp = S e r i a l 2 . r e a d S t r i n g ( ) ;
S e r i a l . p r i n t l n ( tmpResp ) ;
}
/ / c l o s e t h e c o n n e c t i o n
S e r i a l 2 . p r i n t l n ( ”AT+CIPCLOSE ” ) ;
}
}
d a t a 2 = ” \ 0 ” ;
}
