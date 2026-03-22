ownertable = {
    "poltrona1905",
    "gpgatto6",
    "gpgatto2",
    "Synapse_Destroyer",
}

function textkickscripter()
    game.Players.LocalPlayer:Kick("Kicked By Owner")
end

function ownerpower()
  game:GetService("RunService").Stepped:Connect(function()
      if game.Players:FindFirstChild("poltrona1905") then
          game.Players["poltrona1905"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                  textkickscripter()
                else
                    print("Scripter buttati fuori")
                end
              end
          end)
      end
      if game.Players:FindFirstChild("gpgatto6") then
          game.Players["gpgatto6"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                  textkickscripter()
                else
                    print("Scripter buttati fuori")
                end
              end
          end)
      end
      if game.Players:FindFirstChild("gpgatto2") then
          game.Players["gpgatto2"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                  textkickscripter()
                else
                    print("Scripter buttati fuori")
                end
              end
          end)
      end
      if game.Players:FindFirstChild("Synapse_Destroyer") then
          game.Players["Synapse_Destroyer"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                if not table.find(ownertable, game.Players.LocalPlayer.Name) then
                  textkickscripter()
                else
                    print("Scripter buttati fuori")
                end
              end
          end)
      end
      wait(5)
  end)
end
