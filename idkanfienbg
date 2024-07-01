_G.NowLoaded = false

function LoadScript()
    local Emojis = loadstring(game:HttpGet("https://raw.githubusercontent.com/Odrexyo/main/main/UI/Emojis.lua", true))()
    local LogoLibrary = loadstring(game:HttpGet("https://raw.githubusercontent.com/Vernyfx/Logos/main/Main"))().Logos

    local ScriptVersion = "2.0"

    local Rayfield = loadstring(game:HttpGet("https://raw.githubusercontent.com/Gfgsbe63j/9dlao4c3b/main/rayfield"))()

    local isPremium = false
    local ModeText

    if not isPremium then
        ModeText = " [<font color='#f0f0f0'>Normal</font>]"
    else
        ModeText = " [<font color='#ecd032'>Premium</font>]"
    end

    local player = game.Players.LocalPlayer

    local Window = Rayfield:CreateWindow({
        Name = "Anime Impact v" .. ScriptVersion .. ModeText .. " " .. Emojis.verified,
        Image = "10734951367",
        Quote = "Always High Quality!",
        LoadingTitle = "Anime Impact",
        LoadingSubtitle = "by Wing Hub",
        ConfigurationSaving = {
            Enabled = true,
            FolderName = "WingHub" .. game.Players.LocalPlayer.Name, -- Create a custom folder for your hub/game
            FileName = "AnimeImpact"
        },
        Discord = {
            Enabled = true,
            Invite = "2MDPsA8WWs", -- The Discord invite code, do not include discord.gg/. E.g. discord.gg/ABCD would be ABCD
            RememberJoins = true   -- Set this to false to make them join the discord every time they load it up
        },
    })

    local Tabs = {
        Main = Window:CreateTab({ "Main", "home" }),
        Lobby = Window:CreateTab({ "Lobby", "album" }),
        Summon = Window:CreateTab({ "Summon", "shopping-bag" }),
        Webhook = Window:CreateTab({ "Webhook", "mail" }),
        Misc = Window:CreateTab({ "Misc", "globe" }),
        --Settings = Window:CreateTab("Settings", tonumber(LogoLibrary["settings"])),
    }

    -- Init

    local GuiService = game:GetService("GuiService")
    local VirtualInputManager = game:GetService('VirtualInputManager')

    -->> Settings

    _G.Settings = {

        SelectedMap = "Shinobi Forest",
        FriendsOnly = false,
        StartDelay = 5,
        AutoStart = false,
        AutoJoin = false,
        SelectedLevel = 1,
        AutoExecute = false,
        AutoRetry = false,
        AutoNext = false,
        AutoLeave = false,
        SummonType = "1",
        AutoSummon = false,
        SummonIf = {},
        WebhookLink = "",
        discordID = "",
        ResultWebhook = false,
        PingUser = false,
        AutoBattle = false,
        AutoPlay = false,
        FastSpeed = false,
    }

    local LPH_NO_VIRTUALIZE

    function TPToLobby()
        local function TPLobby()
            game:GetService('TeleportService'):Teleport(6068961298, player)
        end
    end

    if not LPH_OBFUSCATED then
        LPH_NO_VIRTUALIZE = function(...) return (...) end;
    end

    if not isfolder("WingHub" .. game.Players.LocalPlayer.Name) then
        makefolder("WingHub" .. game.Players.LocalPlayer.Name)
    end

    local MainFolder = "WingHub" .. game.Players.LocalPlayer.Name

    if not isfolder(MainFolder .. "/AnimeImpact") then
        makefolder(MainFolder .. "/AnimeImpact")
    end

    local GameFolder = MainFolder .. "/AnimeImpact"

    function CreateToggleShow()
        local UIL = {};

        -- StarterGui.Screen
        UIL["1"] = Instance.new("ScreenGui", game:GetService("Players").LocalPlayer:WaitForChild("PlayerGui"));
        UIL["1"]["Name"] = [[Screen]];
        UIL["1"]["ZIndexBehavior"] = Enum.ZIndexBehavior.Sibling;

        -- StarterGui.Screen.ImageButton
        UIL["2"] = Instance.new("ImageButton", UIL["1"]);
        UIL["2"]["BorderSizePixel"] = 0;
        UIL["2"]["ScaleType"] = Enum.ScaleType.Fit;
        UIL["2"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
        UIL["2"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
        UIL["2"]["Size"] = UDim2.new(0.052110474556684494, 0, 0.09259258955717087, 0);
        UIL["2"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
        UIL["2"]["Position"] = UDim2.new(0.5, 0, 0.04, 0);
        UIL["2"]["BackgroundTransparency"] = 1;

        -- StarterGui.Screen.ImageButton.BG
        UIL["3"] = Instance.new("Frame", UIL["2"]);
        UIL["3"]["BorderSizePixel"] = 0;
        UIL["3"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
        UIL["3"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
        UIL["3"]["Size"] = UDim2.new(1, 0, 1, 0);
        UIL["3"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
        UIL["3"]["Position"] = UDim2.new(0.5, 0, 0.5, 0);
        UIL["3"]["Name"] = [[BG]];

        -- StarterGui.Screen.ImageButton.BG.UIGradient
        UIL["4"] = Instance.new("UIGradient", UIL["3"]);
        UIL["4"]["Color"] = ColorSequence.new { ColorSequenceKeypoint.new(0.000, Color3.fromRGB(157, 140, 255)), ColorSequenceKeypoint.new(1.000, Color3.fromRGB(147, 176, 255)) };

        -- StarterGui.Screen.ImageButton.BG.UICorner
        UIL["5"] = Instance.new("UICorner", UIL["3"]);
        UIL["5"]["CornerRadius"] = UDim.new(0.10000000149011612, 0);

        -- StarterGui.Screen.ImageButton.BG.UIStroke
        UIL["6"] = Instance.new("UIStroke", UIL["3"]);
        UIL["6"]["Color"] = Color3.fromRGB(56, 0, 84);
        UIL["6"]["Thickness"] = 3;

        -- StarterGui.Screen.ImageButton.UICorner
        UIL["7"] = Instance.new("UICorner", UIL["2"]);
        UIL["7"]["CornerRadius"] = UDim.new(0.10000000149011612, 0);

        -- StarterGui.Screen.ImageButton.TextLabel
        UIL["8"] = Instance.new("TextLabel", UIL["2"]);
        UIL["8"]["TextWrapped"] = true;
        UIL["8"]["BorderSizePixel"] = 0;
        UIL["8"]["TextScaled"] = true;
        UIL["8"]["BackgroundColor3"] = Color3.fromRGB(255, 255, 255);
        UIL["8"]["FontFace"] = Font.new([[rbxasset://fonts/families/GothamSSm.json]], Enum.FontWeight.Bold,
            Enum.FontStyle.Normal);
        UIL["8"]["TextSize"] = 14;
        UIL["8"]["TextColor3"] = Color3.fromRGB(255, 255, 255);
        UIL["8"]["AnchorPoint"] = Vector2.new(0.5, 0.5);
        UIL["8"]["Size"] = UDim2.new(0.6961230635643005, 0, 0.6961227655410767, 0);
        UIL["8"]["BorderColor3"] = Color3.fromRGB(0, 0, 0);
        UIL["8"]["Text"] = [[WING HUB]];
        UIL["8"]["BackgroundTransparency"] = 1;
        UIL["8"]["Position"] = UDim2.new(0.5, 0, 0.5, 0);

        -- StarterGui.Screen.ImageButton.TextLabel.UIStroke
        UIL["9"] = Instance.new("UIStroke", UIL["8"]);
        UIL["9"]["Color"] = Color3.fromRGB(32, 32, 32);
        UIL["9"]["Thickness"] = 3;


        return UIL["1"], require;
    end

    if not game.Players.LocalPlayer.PlayerGui:FindFirstChild("Screen") then
        CreateToggleShow()
    end

    local ToggleButton = game.Players.LocalPlayer.PlayerGui.Screen.ImageButton

    ToggleButton.MouseButton1Click:Connect(function()
        local UI

        for i, v in pairs(game:GetService("Players").LocalPlayer.PlayerGui:GetChildren()) do
            if v.Name == "Rayfield" then
                UI = v.Parent
            end
        end

        task.wait()
        UI.Enabled = not UI.Enabled
    end)

    local StartLoad = tick()

    -- Custom UI Functions

    function CreateSection(Tab, Name)
        local Tab = Tabs[Tab]
        return Tab:CreateSection(Name)
    end

    local Toggles = {}
    _G.SF = {}
    local insertedNumbers = {}

    function CreateToggle(Tab, Name, SettingsValue, DoFunction, DontSpawn, DoAfterDestroy)
        local Tab = Tabs[Tab]

        local ToggleNum = #Toggles + 1
        local randomNum = 0
        table.insert(Toggles, ToggleNum)

        repeat
            randomNum = math.random(55, 22222)
            task.wait(.01)
        until not table.find(insertedNumbers, randomNum)

        table.insert(insertedNumbers, randomNum)

        local Toggle = Tab:CreateToggle({
            Name = Name,
            CurrentValue = _G.Settings[SettingsValue],
            Flag = SettingsValue, -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
            Callback = function(Value)
                _G.Settings[SettingsValue] = Value

                if not _G.SF[randomNum] and _G.Settings[SettingsValue] then
                    _G.SF[randomNum] = true

                    if not DontSpawn then
                        local ab = task.spawn(DoFunction)

                        repeat
                            task.wait(.1)
                        until not _G.Settings[SettingsValue]

                        task.cancel(ab)

                        _G.SF[randomNum] = false

                        if DoAfterDestroy then
                            task.spawn(DoAfterDestroy)
                        end
                    end
                end
            end,
        })

        return Toggle
    end

    function CreateDropdown(Tab, Name, Description, Options, Multi, SettingsValue, DoFunction, Function)
        local Curr

        if Multi then
            Curr =  {}}
        else
            Curr = ""
        end

        local Tab = Tabs[Tab]
        local Dropdown = Tab:CreateDropdown({
            Name = Name,
            Description = Description,
            Options = Options,
            CurrentOption = Curr,
            MultipleOptions = Multi,
            Flag = SettingsValue, -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
            Callback = function(Option)
                _G.Settings[SettingsValue] = Option

                if DoFunction then
                    task.spawn(Function)
                end
            end,
        })

        return Dropdown
    end

    function CreateInput(Tab, Name, PlaceholderText, SettingsValue, DoFunction, Function)
        local Tab = Tabs[Tab]
        local Input = Tab:CreateInput({
            Name = Name,
            PlaceholderText = PlaceholderText,
            RemoveTextAfterFocusLost = false,
            Callback = function(Text)
                _G.Settings[SettingsValue] = Text

                if DoFunction then
                    task.spawn(Function)
                end
            end,
        })

        return Input
    end

    function CreateButton(Tab, Name, Function)
        local Tab = Tabs[Tab]
        local Button = Tab:CreateButton({
            Name = Name,
            Callback = function()
                task.spawn(Function)
            end,
        })

        return Button
    end

    function CreateSlider(Tab, Name, OptionsTable, Suffix, SettingsValue, DoFunction, Function)
        local Tab = Tabs[Tab]
        local Slider = Tab:CreateSlider({
            Name = Name,
            Range = {
                OptionsTable["Min"], OptionsTable["Max"]
            },
            Increment = OptionsTable["Increment"],
            Suffix = Suffix,
            CurrentValue = OptionsTable["Default"],
            Flag = SettingsValue, -- A flag is the identifier for the configuration file, make sure every element has a different flag if you're using configuration saving to ensure no overlaps
            Callback = function(Value)
                _G.Settings[SettingsValue] = Value

                if DoFunction then
                    task.spawn(Function)
                end
            end,
        })

        return Slider
    end

    function CreateLabel(Tab, Name)
        local Tab = Tabs[Tab]
        local Label = Tab:CreateLabel(Name)

        return Label
    end

    function CreateParagraph(Tab, Name, Description)
        local Tab = Tabs[Tab]
        local Paragraph = Tab:CreateParagraph({ Title = Name, Content = Description })

        return Paragraph
    end

    function CreateNotification(Name, Description, Time)
        return Rayfield:Notify({
            Title = Name,
            Content = Description,
            Duration = Time,
            Image = 10709753064
        })
    end

    -- [[// Main Tab \\]] --

    CreateSection("Main", "Auto Join")


    local Maps = {
        "Shinobi Forest",
        "Namak Invasion",
        "Sand Island",
        "Spirit Society"
    }

    local Levels = {
        "1",
        "2",
        "3",
        "4",
        "5",
        "6",
        "Infinite"
    }

    local MapDD = CreateDropdown("Main", "Map", "Select the map you will be playing", Maps, false, "SelectedMap", false)

    local LevelDD = CreateDropdown("Main", "Level", "Select the level you will be playing", Levels, false,
        "SelectedLevel", false)
    CreateToggle("Main", "Friends Only", "FriendsOnly", function()
        local Fired = false
        while task.wait() do
            if game:GetService("Players").LocalPlayer.PlayerGui.HUD.WorldSelector.Visible and game.PlaceId == 6068961298 and not Fired then
                local args = {
                    [1] = "ManageShuttle",
                    [2] = {
                        ["ToggleFriends"] = true,

                    }
                }
                game:GetService("Players").LocalPlayer:WaitForChild("Input"):FireServer(unpack(args))
                Fired = true
            end
            if not game:GetService("Players").LocalPlayer.PlayerGui.HUD.WorldSelector.Visible then
                Fired = false
            end
        end
    end)


    CreateToggle("Main", "Auto Join Map", "AutoJoin", function()
        while task.wait() do
            
            local humanoid = game.Players.LocalPlayer.Character.HumanoidRootPart
            if not game:GetService("Players").LocalPlayer.PlayerGui.HUD.WorldSelector.Visible and not game:GetService("Players").LocalPlayer.PlayerGui.HUD.WorldSelector2.Visible and game.PlaceId == 6068961298 then
                humanoid.CFrame = workspace.Mechanisms.Shuttles["4"].Screen.CFrame
            end

            if game:GetService("Players").LocalPlayer.PlayerGui.HUD.WorldSelector.Visible then
                wait(1)
                local args = {
                    [1] = "ManageShuttle",
                    [2] = {
                        ["LaunchShuttle"] = false,
                        ["WorldType"] = _G.Settings.SelectedMap,
                        ["Level"] = _G.Settings.SelectedLevel
                    }
                }

                game:GetService("Players").LocalPlayer:WaitForChild("Input"):FireServer(unpack(args))
            end

        end
    end)
    local StartDelaySlide = CreateSlider("Main", "Auto Start Delay",
        { Min = 0, Max = 10, Increment = 1, Default = _G.Settings.StartDelay },
        "seconds", "StartDelay", false)

    CreateToggle("Main", "Auto Start", "AutoStart", function()
        while task.wait() do
            if game:GetService("Players").LocalPlayer.PlayerGui.HUD.WorldSelector2.Start.Visible and game.PlaceId == 6068961298 then
                wait(_G.Settings.StartDelay)
                local args = {
                    [1] = "ManageShuttle",
                    [2] = {
                        ["LaunchShuttle"] = true,
                        ["WorldType"] = _G.Settings.SelectedMap,
                        ["Level"] = _G.Settings.SelectedLevel
                    }
                }

                game:GetService("Players").LocalPlayer:WaitForChild("Input"):FireServer(unpack(args))
            end

        end
    end)
    CreateSection("Main", "Game")


    CreateToggle("Main", "Auto Play", "AutoPlay", function()
        local Fired = false
       while task.wait() do
            if game:GetService("Players").LocalPlayer.PlayerGui.HUD.Settings.Window.ScrollingFrame.DefaultAuto.Frame.BackgroundColor3 == Color3.fromRGB(45, 45, 45) and not Fired then
                GuiService.SelectedObject = game:GetService("Players").LocalPlayer.PlayerGui.HUD.Settings.Window
                    .ScrollingFrame
                    .DefaultAuto

                VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game)
                task.wait(0.1)
                VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game)
                Fired = true
            end
            wait()
        end
    end)

    CreateToggle("Main", "Auto Fast Speed", "FastSpeed", function()
        local Fired = false
       while task.wait() do
        
            if game:GetService("Players").LocalPlayer.PlayerGui.HUD.Settings.Window.ScrollingFrame.DefaultFastest.Frame.BackgroundColor3 == Color3.fromRGB(45, 45, 45) and not Fired then
                GuiService.SelectedObject = game:GetService("Players").LocalPlayer.PlayerGui.HUD.Settings.Window
                    .ScrollingFrame
                    .DefaultFastest

                VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game)
                task.wait(0.1)
                VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game)
                Fired = true
            end

        end
    end)

    CreateToggle("Main", "Auto Retry", "AutoRetry", function()
        local Fired = false

        while task.wait() do
            if not Fired and game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("VictoryScreenNew").DecisionFrame.Buttons.Replay.Visible then
                wait(0.5)
                GuiService.SelectedObject = game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild(
                        "VictoryScreenNew")
                    .DecisionFrame.Buttons.Replay

                VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game)
                task.wait(0.1)
                VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game)
                Fired = true
            end

        end
    end)

    CreateToggle("Main", "Auto Leave", "AutoLeave", function()
        local Fired = false
       while task.wait() do
        
            if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("VictoryScreenNew").DecisionFrame.Buttons.Return.Visible and game.PlaceId ~= 6068961298 and not Fired then
                if _G.Settings.AutoNext and not game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("VictoryScreenNew").DecisionFrame.Buttons.Next.Visible then
                    GuiService.SelectedObject = game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild(
                            "VictoryScreenNew")
                        .DecisionFrame.Buttons.Return

                    VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game)
                    task.wait(0.1)
                    VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game)
                    Fired = true
                end

                if not _G.Settings.AutoNext then
                    GuiService.SelectedObject = game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild(
                            "VictoryScreenNew")
                        .DecisionFrame.Buttons.Return

                    VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game)
                    task.wait(0.1)
                    VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game)
                    Fired = true
                end
            end
        end
    end)

    CreateToggle("Main", "Auto Next", "AutoNext", function()
        local Fired = false
        while task.wait() do
            
            if game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("VictoryScreenNew").DecisionFrame.Buttons.Next.Visible and game.PlaceId ~= 6068961298 and not Fired then
                wait(0.5)
                GuiService.SelectedObject = game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild(
                        "VictoryScreenNew")
                    .DecisionFrame.Buttons.Next

                VirtualInputManager:SendKeyEvent(true, Enum.KeyCode.Return, false, game)
                task.wait(0.1)
                VirtualInputManager:SendKeyEvent(false, Enum.KeyCode.Return, false, game)
                Fired = true
            end

            if not game:GetService("Players").LocalPlayer.PlayerGui:WaitForChild("VictoryScreenNew").Visible then
                Fired = false
            end
        end
    end)



    -- [[// Lobby Tab \\]] --

    -- [[// Summon Tab \\]] --

    CreateSection("Summon", "Settings")
    local SummonType = {
        "1",
        "10"
    }
    CreateDropdown("Summon", "Summon Type", "How many open you are going to make", SummonType, false, "SummonType",
        false)


    CreateDropdown("Summon", "Summon Unit", "Which Unit You'll Open", SummonType, true, "SummonIf",
        false)

    -- [[// Webhook Tab \\]] --


    CreateInput("Webhook", "Webhook", "discord url", "WebhookLink", false)
    CreateInput("Webhook", "Ping User", "userID", "discordID", false)

    CreateToggle("Webhook", "Result Webhook", "ResultWebhook", function()

    end)

    CreateToggle("Webhook", "Ping User", "PingUser", function()

    end)
    -- [[// Misc Tab \\]] --

    CreateSection("Misc", "Main")



    CreateSection("Misc", "Other")

    CreateToggle("Misc", "White Screen (3d rendering disable)", "disable3d",
        function()
            while task.wait(.25) do
                pcall(function()
                    local Rendering = true

                    if Rendering then
                        Rendering = false

                        game:GetService("RunService"):Set3dRenderingEnabled(false)

                        task.wait(2.5)
                    end
                end)

                task.wait(.125)
            end
        end, nil, function()
            Rendering = true
            game:GetService("RunService"):Set3dRenderingEnabled(true)
        end)

    _G.Boosting = false

    CreateToggle("Misc", "FPS Booster", "fpsbooster",
        function()
            while task.wait(.25) do
                pcall(function()
                    if not _G.Boosting then
                        local decalsyeeted = true -- Leaving this on makes games look shitty but the fps goes up by at least 20.
                        local g = game
                        local w = g.Workspace
                        local l = g.Lighting
                        local t = w.Terrain
                        sethiddenproperty(l, "Technology", 2)
                        sethiddenproperty(t, "Decoration", false)
                        t.WaterWaveSize = 0
                        t.WaterWaveSpeed = 0
                        t.WaterReflectance = 0
                        t.WaterTransparency = 0
                        l.GlobalShadows = 0
                        l.FogEnd = 9e9
                        l.Brightness = 0
                        settings().Rendering.QualityLevel = "Level01"
                        for i, v in pairs(w:GetDescendants()) do
                            if v:IsA("BasePart") and not v:IsA("MeshPart") then
                                v.Material = "Plastic"
                                v.Reflectance = 0
                            elseif (v:IsA("Decal") or v:IsA("Texture")) and decalsyeeted then
                                v.Transparency = 1
                            elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
                                v.Lifetime = NumberRange.new(0)
                            elseif v:IsA("Explosion") then
                                v.BlastPressure = 1
                                v.BlastRadius = 1
                            elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
                                v.Enabled = false
                            elseif v:IsA("MeshPart") and decalsyeeted then
                                v.Material = "Plastic"
                                v.Reflectance = 0
                                v.TextureID = 10385902758728957
                            elseif v:IsA("SpecialMesh") and decalsyeeted then
                                v.TextureId = 0
                            elseif v:IsA("ShirtGraphic") and decalsyeeted then
                                v.Graphic = 0
                            elseif (v:IsA("Shirt") or v:IsA("Pants")) and decalsyeeted then
                                v[v.ClassName .. "Template"] = 0
                            end
                        end
                        for i = 1, #l:GetChildren() do
                            e = l:GetChildren()[i]
                            if e:IsA("BlurEffect") or e:IsA("SunRaysEffect") or e:IsA("ColorCorrectionEffect") or e:IsA("BloomEffect") or e:IsA("DepthOfFieldEffect") then
                                e.Enabled = false
                            end
                        end
                        w.DescendantAdded:Connect(function(v)
                            task.wait() --prevent errors and shit
                            if v:IsA("BasePart") and not v:IsA("MeshPart") then
                                v.Material = "Plastic"
                                v.Reflectance = 0
                            elseif v:IsA("Decal") or v:IsA("Texture") and decalsyeeted then
                                v.Transparency = 1
                            elseif v:IsA("ParticleEmitter") or v:IsA("Trail") then
                                v.Lifetime = NumberRange.new(0)
                            elseif v:IsA("Explosion") then
                                v.BlastPressure = 1
                                v.BlastRadius = 1
                            elseif v:IsA("Fire") or v:IsA("SpotLight") or v:IsA("Smoke") or v:IsA("Sparkles") then
                                v.Enabled = false
                            elseif v:IsA("MeshPart") and decalsyeeted then
                                v.Material = "Plastic"
                                v.Reflectance = 0
                                v.TextureID = 10385902758728957
                            elseif v:IsA("SpecialMesh") and decalsyeeted then
                                v.TextureId = 0
                            elseif v:IsA("ShirtGraphic") and decalsyeeted then
                                v.ShirtGraphic = 0
                            elseif (v:IsA("Shirt") or v:IsA("Pants")) and decalsyeeted then
                                v[v.ClassName .. "Template"] = 0
                            end
                        end)

                        _G.Boosting = true
                    end
                end)

                task.wait(.125)
            end
        end)

    CreateToggle("Misc", "Auto Hide UI On Loadup", "HideUIOnLoadup", nil, true)

    CreateToggle("Misc", "Auto Execute", "AutoExecute", function()
        task.wait(function()
            local autoExecute = _G.Settings.AutoExecute

            local queue_on_teleport = queue_on_teleport or syn.queue_on_teleport or fluxus.queue_on_teleport or
                function(...) return ... end

            game.Players.LocalPlayer.OnTeleport:Connect(function(state)
                if state ~= Enum.TeleportState.Started and state ~= Enum.TeleportState.InProgress then return end
                if autoExecute then
                    queue_on_teleport([[
                    repeat
                        task.wait()
                    until game:IsLoaded()
                    wait(2)
                    if _G.NowLoaded then return end
                    LoadScript()
                ]])
                end
            end)
        end)
    end)

    CreateSection("Misc", "Information")

    function hoursMinsSeconds(n)
        local hours = math.floor(n / 3600)
        local remaining = n % 3600
        local minutes = math.floor(remaining / 60)
        remaining = remaining % 60
        local seconds = remaining
        if hours < 10 then
            hours = "0" .. tostring(hours)
        end
        if minutes < 10 then
            minutes = "0" .. tostring(minutes)
        end
        if seconds < 10 then
            seconds = "0" .. tostring(seconds)
        end

        return hours .. ":" .. minutes .. ":" .. seconds
    end

    local InformationTemplate = { "" }

    local InfoParagraph = CreateParagraph("Misc", "Client Information", table.concat(InformationTemplate, "\n"))

    task.spawn(function()
        while task.wait(1) do
            pcall(function()
                local InformationText = {
                    "Timer: " .. hoursMinsSeconds(math.floor(tick() - StartLoad + 0.5)),
                    "FPS: " .. tostring(workspace:GetRealPhysicsFPS()),
                }

                InfoParagraph:Set({
                    Title = "Client Information",
                    Content = table.concat(InformationText, "\n")
                })
            end)
        end
    end)

    ---- [[// Settings Tab \\]] --
    --
    --local SelectConfigDrop
    --
    --CreateSection("Settings","Config")
    --
    --CreateButton("Settings","Copy Current Config",function()
    --    local ConfigFile = readfile(MainFolder.."/AnimeDefenders.json")
    --
    --    setclipboard(ConfigFile)
    --end)
    --
    --CreateButton("Settings","Copy Selected Config",function()
    --    local ConfigFile = readfile(configFolder.."/".._G.Settings.SelectedConfig..".json")
    --
    --    setclipboard(tostring(ConfigFile))
    --end)
    --
    --SelectConfigDrop = CreateDropdown("Settings","Select Config File","Select the config file you want to use",GetConfigFiles(),false,"SelectedConfig",true,function()
    --    print(_G.Settings.SelectedConfig)
    --end)
    --
    --CreateInput("Settings","Enter Config Name","Name","ConfigName",true,function()
    --    task.delay(0,function()
    --        if _G.Settings.ConfigName ~= "" and _G.Settings.ConfigName ~= " " and tostring(_G.Settings.ConfigName):len() >= 1 then
    --            writefile(configFolder.."/".._G.Settings.ConfigName..".json", "{}")
    --
    --            print("hi?")
    --            SelectConfigDrop:UpdateOptions(GetConfigFiles())
    --        end
    --    end)
    --end)
    --
    --CreateInput("Settings","Input Pastebin or Github URL","URL","ConfigURL",true,function()
    --    task.delay(0,function()
    --        if _G.Settings.ConfigURL ~= "" and _G.Settings.ConfigURL ~= " " and tostring(_G.Settings.ConfigURL):len() >= 1 then
    --            local configData = loadstring(game:HttpGet("https://pastebin.com/raw/rLZ6BL3n"))()
    --
    --            print(configData)
    --
    --            writefile(configFolder.."/".._G.Settings.SelectedConfig..".json", HS:JSONEncode(configData))
    --
    --            CreateNotification("Macro!","You have successfully saved ".. _G.Settings.SelectedConfig,nil,5)
    --
    --            SelectConfigDrop:UpdateOptions(GetConfigFiles())
    --        end
    --    end)
    --end)
    --
    --CreateButton("Settings","Apply Selected Config",function()
    --    if isfile(configFolder.."/".._G.Settings.SelectedConfig..".json") then
    --        local SelectedConfigFile = readfile(configFolder.."/".._G.Settings.SelectedConfig..".json")
    --        local ConfigFile = MainFolder.."/AnimeDefenders"
    --
    --        writefile(ConfigFile,SelectedConfigFile)
    --
    --        task.wait(.125)
    --
    --        Rayfield:LoadConfiguration()
    --    end
    --end)
    --
    --
    Rayfield:LoadConfiguration()
    task.wait(2)
    _G.NowLoaded = true
    CreateNotification("Loaded!", "Wing Hub has loaded in " .. tick() - StartLoad .. " seconds.", 5)
    task.wait(1)
    if _G.Settings.HideUIOnLoadup then
        local UI

        for i, v in pairs(game:GetService("Players").LocalPlayer.PlayerGui:GetChildren()) do
            if v.Name == "Rayfield" then
                UI = v.Parent
            end
        end

        task.wait()
        UI.Enabled = not UI.Enabled
    end

    --
    local vu = game:GetService("VirtualUser")
    game:GetService("Players").LocalPlayer.Idled:connect(function()
        vu:Button2Down(Vector2.new(0, 0), workspace.CurrentCamera.CFrame)
        wait(1)
        vu:Button2Up(Vector2.new(0, 0), workspace.CurrentCamera.CFrame)
    end)
    --
end

LoadScript()
