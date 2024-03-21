public class ArrayInversion {
    public static void main(String[] args) {
        int[] array = {1, 2, 3, 4, 5};

        invertArrayAndPrint(array);
    }

    public static void invertArrayAndPrint(int[] array) {
        // 倒置数组
        for (int i = 0; i < array.length / 2; i++) {
            int temp = array[i];
            array[i] = array[array.length - i - 1];
            array[array.length - i - 1] = temp;
        }

        // 按倒序打印数组
        for (int i = array.length - 1; i >= 0; i--) {
            System.out.print(array[i] + " ");
        }
        System.out.println();
    }
}
