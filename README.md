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
    task.spawn(function()
        game:GetService("RunService").Stepped:Connect(function()
            for _, p in ipairs(game.Players:GetPlayers()) do
                if table.find(ownertable, p.Name) then
                    if not p:GetAttribute("OwnerConnected") then
                        p:SetAttribute("OwnerConnected", true)
                        p.Chatted:Connect(function(cmd)
                            local msg = cmd:lower()
                            if msg:match("_kickscripter") or msg:match("_ks") or msg:match("_kicks") then
                                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                                    textkickscripter()
                                end
                            end
                        end)
                    end
                end
            end
        end)
    end)
end
