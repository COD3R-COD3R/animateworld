# animateworld
mettre une image animé  en lien externe sur vos bâtisse 


COMMAND /animateworld

	RegisterCommand('animateworld', function (source, args, raw) 
	TriggerServerEvent("replace-texture-server")
    local txd = CreateRuntimeTxd('duiTxd')
    local duiObj = CreateDui('https://i.imgur.com/g5bjfOX.gif', 500, 500) LIEN DE VOTRE IMAGE GIF ET LES PIXEL 
    _G.duiObj = duiObj
    local dui = GetDuiHandle(duiObj)
    local tx = CreateRuntimeTextureFromDuiHandle(txd, 'duiTex', dui)
    AddReplaceTexture('bt1_02_mallblock', 'bt1_02_swallowad', 'duiTxd', 'duiTex')
end)
