Q. You are given an image represented by an m x n grid of integers image, where image[i][j] represents the pixel value of the image. You are also given three integers sr, sc, and color. Your task is to perform a flood fill on the image starting from the pixel image[sr][sc].

To perform a flood fill:

Begin with the starting pixel and change its color to color.
Perform the same process for each pixel that is directly adjacent (pixels that share a side with the original pixel, either horizontally or vertically) and shares the same color as the starting pixel.
Keep repeating this process by checking neighboring pixels of the updated pixels and modifying their color if it matches the original color of the starting pixel.
The process stops when there are no more adjacent pixels of the original color to update.

Return the modified image after performing the flood fill.

ANS:

class Solution {  
public:  
    vector<vector<int>> floodFill(vector<vector<int>>& image, int sr, int sc, int color) {  
    int orig=image[sr][sc]; if(orig==color)return image;  
    function<void(int,int)> dfs=[&](int r,int c){  
        if(r<0||r>=image.size()||c<0||c>=image[0].size()||image[r][c]!=orig)return;  
        image[r][c]=color;  
        dfs(r+1,c);dfs(r-1,c);dfs(r,c+1);dfs(r,c-1);  
    };  
    dfs(sr,sc); return image;  

    }  
};  
<img width="1449" height="753" alt="image" src="https://github.com/user-attachments/assets/18b0fa6f-3b5b-4dd6-ba6b-ee586b9869d8" />
