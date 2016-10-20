# BotSavesPrincess
//https://www.hackerrank.com/challenges/saveprincess
using System;
using System.Collections.Generic;
using System.IO;
class Solution {
static void displayPathtoPrincess(int n, String [] grid){
    int rowM=0,colM=0,rowP=0,colP=0;
    for(int i=0;i<n;i++){
        for(int j=0;j<n;j++){
            if(grid[i][j]=='m'){
                rowM=i;
                colM=j;                
            }
            if(grid[i][j]=='p'){
                rowP=i;
                colP=j;                
            }
          }
    }
        while(rowM!=rowP){
            if(rowM<rowP){
                rowM=rowM+1;
                Console.WriteLine("DOWN");
            }
            if(rowM>rowP){
                rowM=rowM-1;
                Console.WriteLine("UP");
            }
        }
        while(colM!=colP){
            if(colM>colP){
                colM=colM-1;
                Console.WriteLine("LEFT");
            }
            if(colM<colP){
                colM=colM+1;
                Console.WriteLine("RIGHT");
            }
        }
        }
    
static void Main(String[] args) {
        int m;

        m = int.Parse(Console.ReadLine());

        String[] grid  = new String[m];
        for(int i=0; i < m; i++) {
            grid[i] = Console.ReadLine(); 
        }

        displayPathtoPrincess(m,grid);
     }
}

