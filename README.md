ownertable = {
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
  game:GetService("RunService").Stepped:Connect(function()
      if game.Players:FindFirstChild("poltrona1905","gpgatto6","gpgatto2","gpgatto13","Synapse_Destroyer",) then
          game.Players[table.find(ownertable, game.Players.LocalPlayer.Name)].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                  textkickscripter()
                end
              end
          end)
      end
      wait(5)
  end)
end
