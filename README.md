# human_level_control_drl

## pseudo code

class repeat_action_and_max_frame

  derives from : gym.Wrapper
  
  input : environment, repeat
  
  init frame buffer as an array of zeros in shape 2 x the obs space 
  
  
  function step :
  
    input : action
    
    set total reward  = 0 
    
    set done to false
    
    for i in range repeat 
    
      call the step function ----> env.step()
      
        receive obs, reward, done, info
        
      increment total reward
      
      insert obs in frame buffer
      
      if done
      
        break 
        
     end for 
     
    
     find the max frame
     
     return : max frame, total reward, done, info
