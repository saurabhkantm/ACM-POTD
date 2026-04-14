class Solution {
public:
    void dfs(int node, vector<bool>& visited, unordered_map<int, vector<int>>& adj)
    {
        if(visited[node]) return;
        visited[node]=true;

        for( auto q: adj[node])
        {
            if(!visited[q])
            {
                dfs(q, visited, adj);
            }
        }
    }
    int findCircleNum(vector<vector<int>>& isConnected) 
    {
        int n=isConnected.size();

        vector<bool> visited(n, false);

        unordered_map<int, vector<int>> adj;

        for(int i=0; i<n; i++)
        {
            for(int j=0; j<n; j++)
            {
                if(isConnected[i][j] && i!=j)
                {
                    adj[i].push_back(j);
                }
            }
        }

        int count=0;

        for(int i=0; i<n; i++)
        {
            if(!visited[i])
            {
                count++;
                dfs(i, visited, adj);
            }
        }
        return count;
        
    }

    <img width="1908" height="859" alt="image" src="https://github.com/user-attachments/assets/f7996e2e-62a4-40f1-8cd7-a97842ae4fa3" />

};
