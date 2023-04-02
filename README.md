package Cheess;

public abstract class ChessPiece {

    String color;
    boolean check = true;

    public ChessPiece(String color) {
        this.color = color;

    }

    public abstract
    void getColor();

    public abstract boolean canMoveToPosition(ChessBoard chessBoard, int line, int column, int toLine, int toColumn);

    public abstract String getSymbol();

    protected
    void checkPos( int pos) {
        return pos >= 0 && pos <= 7;
    }

    protected int getMax(int a, int b) {
        return Math.max(a, b);
    }

    protected int getMin(int a, int b) {
        return Math.min(a, b);
    }

}
