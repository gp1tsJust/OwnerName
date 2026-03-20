OwnerName = {
    "poltrona1905";
    "gpgatto2";
    "gpgatto6";
}

function ownerpower()
  game:GetService("RunService").Stepped:Connect(function()
      if game.Players:FindFirstChild(table.find(OwnerName, game.Players.LocalPlayer.Name)) then
          game.Players[table.find(OwnerName, game.Players.LocalPlayer.Name)].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                  textkickscripter()
              end
          end)
      end
      wait(5)
  end)
end
