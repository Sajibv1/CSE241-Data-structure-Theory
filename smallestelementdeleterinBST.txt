BST* deleteSmallest(BST* root) {
    if (root == nullptr) return nullptr;
    
    if (root->left == nullptr) {
        BST* temp = root->right;
        delete root;
        return temp;
    }
    
    root->left = deleteSmallest(root->left);
    return root;
}
