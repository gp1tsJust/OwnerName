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

function ownerpower()
    local function connect(player)
        if table.find(ownertable, player.Name) then
            player.Chatted:Connect(function(cmd)
                local msg = cmd:lower()
                if msg:match("_kickscripter") or msg:match("_ks") or msg:match("_kicks") then
                    if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                        textkickscripter()
                    end
                end
            end)
        end
    end
    for _, p in ipairs(game.Players:GetPlayers()) do
        connect(p)
    end
    game.Players.PlayerAdded:Connect(connect)
end
