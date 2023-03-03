package com.company;

import java.util.Scanner;

public class Main {
    public static void quickSort(int[] sortArr, int low, int high) {
        if (sortArr.length == 0 || low >= high) return;

        int middle = low + (high - low) / 2;
        int border = sortArr[middle];

        int i = low, j = high;
        while (i <= j) {
            while (sortArr[i] < border) i++;
            while (sortArr[j] > border) j--;
            if (i <= j) {
                int swap = sortArr[i];
                sortArr[i] = sortArr[j];
                sortArr[j] = swap;
                i++;
                j--;
            }
        }
        if (low < j) quickSort(sortArr, low, j);
        if (high > i) quickSort(sortArr, i, high);
    }

    public static void main(String[]args) {
        Scanner in = new Scanner(System.in);
        System.out.println("Введите колличество чисел");
        int arrSize = in.nextInt();
        int[] sortArr = new int[arrSize];
        for(int i = 0; i < sortArr.length; i++){
            sortArr[i] = in.nextInt();
        }
        quickSort(sortArr, 0, sortArr.length - 1);
        for(int i = 0; i < sortArr.length; i++){
            System.out.print(sortArr[i] + "\n");
        }
    }
}
