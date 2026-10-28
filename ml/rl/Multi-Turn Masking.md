For multi-turn conversations there are two masking choices
1. **Final turn only**: Only the tokens in the final assistant turn are included in the loss, while all other earlier context is masked. 
2. **Mask user turns only**: All user turns are masked, but every assistant turn is included in the loss. 