class Solution {
public:
	bool canVisitAllRooms(vector<vector<int>>& rooms) {
		int n=rooms.size();
		unordered_map<int,vector<int>> g;
		for(int i=0;i<rooms.size();i++){
			g[i]=rooms[i];
		}
		unordered_set<int> seen;
		vector<int> stack;
		for(auto x:rooms[0]){
			stack.push_back(x);
		}
		seen.insert(0);
		while(stack.size()>0){
			vector<int> temp;
			for(auto x:stack){
				seen.insert(x);
				for(auto v:g[x]){
					if(!seen.count(v)){
						temp.push_back(v);

					}
				}
			}
			stack=temp;
		}
		return seen.size()==n;   
	}
};
