# conway-en-simula
begin 

Class Tablero(filas, columnas); integer filas,columnas,n; 
begin
    boolean array board(0:filas,0:columnas);

    Procedure Initialize;
    begin
        Ref(Coordenada) coord;
        integer i,j,k,n;
        i:=0;
        j:=0;
        n:= coordenadas.length;
        
        while (i < filas) do begin
            while j < columnas do begin
                board(i,j):= false;
                j:=j+1;
            End While;
            i:=i+1;
        End While;
        
        for k:=0 step 1 until n do begin
            i:= coordenadas(k).getX;
            j:= coordenadas(k).getY;
            board(i,j):=true;
        end for;
                
            
    end of Initialize;

Initialize;

End of Tablero;



Class Coordenada (x,y); integer x,y;
begin
    
    integer procedure getX;
    begin
            getX :=x;
    end of getX;

    integer procedure getY;
    begin
            getY :=y;
    end of getY;
    
    procedure printCoord;
    begin
            character coord;
            OutText("(");
            OutInt(x,1);
            OutText(",");
            OutInt(y,1);
            OutText(")");
            OutImage;
    end of printCoord;
    
end of Coordenada;


end
