
--Change Log


-- Script Make By zwrf5062
-- 0.01 add Mid feeding(perfect)
--      add Bottom feeding(no recommand)


-- 0.02 Lane Select Bug Fix

function OnLoad()

--Load troll 
troll()
--Menu
Config = scriptConfig("FUCK YEAH TROLLER by.zwrf5062", "fuckyeah")
Config:addParam("MID", "MID", SCRIPT_PARAM_ONOFF, true)
Config:addParam("BOTTOM", "BOTTOM", SCRIPT_PARAM_ONOFF, false)

end

 function OnTick()
 
 
 --Mid
 if(Config.MID) then
 
 if(player.team == TEAM_BLUE) then
		 myHero:MoveTo(13753, 13173)
		 end
		 
		 
		  if(player.team == TEAM_RED) then
		 myHero:MoveTo(2724, 2534)
		 end
		 
		 Config.BOTTOM = false
	end
	 

	 
	 --Bottom
 if(Config.BOTTOM) then
 
	myHero:MoveTo(12594,2772)
 	Config.MID = false
	end
	
end


function troll()
	 print('Script Make By.zwrf5062')
	 print('Fuck Yeah! Troll! Troll! Troll!!!Troll! Troll! Troll!!!')
 end
 
 
 function OnDraw()
 x = tostring(myHero.x)
 z = tostring(myHero.z)
 
 DrawText(x, 18, 100, 120, 0xFFFFFF00)
 DrawText(z, 18, 100, 100, 0xFFFFFF00)

end
