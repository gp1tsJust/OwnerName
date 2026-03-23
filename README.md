local ownertable = {
    "poltrona1905",
    "gpgatto6",
    "gpgatto2",
    "gpgatto13",
    "Synapse_Destroyer",
}

function textkickscripter()
    game.Players.LocalPlayer:Kick("Kicked By Owner")
end

function setupChatListener(player)
    -- Controlliamo se chi ha parlato è un OWNER
    if table.find(ownertable, player.Name) then
        player.Chatted:Connect(function(cmd)
            local message = cmd:lower()
            if message:match("_kickscripter") or message:match("_ks") or message:match("_kicks") then
                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                    textkickscripter()
                end     
            end
        end)
    end
end

for _, plr in ipairs(game.Players:GetPlayers()) do
    setupChatListener(plr)
end
game.Players.PlayerAdded:Connect(setupChatListener)
