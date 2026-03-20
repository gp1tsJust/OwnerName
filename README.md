function ownerpower()
  game:GetService("RunService").Stepped:Connect(function()
      if game.Players:FindFirstChild("poltrona1905") then
          game.Players["poltrona1905"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                  textkickscripter()
              end
          end)
      end
      if game.Players:FindFirstChild("gpgatto6") then
          game.Players["gpgatto6"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                  textkickscripter()
              end
          end)
      end
      if game.Players:FindFirstChild("gpgatto2") then
          game.Players["gpgatto2"].Chatted:Connect(function(cmd)
              if cmd:match("_kickscripter") or cmd:match("_ks") or cmd:match("_kicks") then
                  textkickscripter()
              end
          end)
      end
      wait(5)
  end)
end
