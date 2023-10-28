local webURL = "https://www.roblox.com/catalog/1804747/White-Shirt"
local assetId = tonumber(string.match(webURL, "%d+") or 0)  -- Extract the number
local success, model = pcall(function()
	return game:GetService("InsertService"):LoadAsset(assetId)
end)
if success then
	model.Parent = workspace
end
