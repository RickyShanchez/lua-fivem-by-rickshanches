# lua-fivem-by-rickshanches
backup do meu modmenu

# feito pelo manorick
# injet in to fivem in sloned to is have bypass and fast banned to you
# https://www.instagram.com/rickysantoxs/

Citizen.CreateThread(function()   
    Tabbuton = {}
    Tabbuton2 = {}
    Meincluir = false
    Espcolor = {R = 255, G = 255, B = 255}
    cursortext = '^'
    local _CiTiZeN_ = Citizen
    freecam = { 
        mode = 1,
        modes = {
            'Olhar em Volta',
            'Teleport',
            'Explosão Azul',
            'Lançar Veiculos',
            'Chuva de Veiculos',
            'Colocar Veiculos',
            'Rampa Spawner',
            'Animal Spawner',
            'Aviao Spawner',
        },
    }
    freecam2 = { 
        mode2 = 1,
        modes2 = {
            'Olhar em Volta',
            'Teleport',
            'Explodir',
            'Explosão Azul',
            'Lançar Veiculos',
            'Chuva de Veiculos',
            'Colocar Veiculos',
            'Cargoplane Spawner',
        },
    }
    local Menu_Ggzera = {
        ['NoclipKeyV'] = 1234,
        ['NoclipKeyL'] = "Nenhuma",
        ['OpenKeyV'] = 1234,
        ['OpenKeyL'] = "...",
        ['CapuzKeyV'] = 1234,
        ['CapuzKeyL'] = "Nenhuma",
        ['RageBotKeyV'] = 25,
        ['RageBotKeyL'] = "MOUSE2",
        ['RageBotKeyV2'] = 25,
        ['RageBotKeyL2'] = "MOUSE2",
        ['MouseMenu'] = false,
        Keys = {
			["BACKSPACE"] = 177, ["ESC"] = 322, ["F1"] = 288, ["F2"] = 289, ["F3"] = 170, ["F5"] = 166, ["F6"] = 167, ["F7"] = 168, ["F8"] = 169, ["F9"] = 56,
			["F10"] = 57, ["F11"] = 344, ["~"] = 243, ["-"] = 84, ["="] = 83, ["TAB"] = 37, ["Q"] = 44, ["W"] = 32, ["E"] = 38, ["R"] = 45, ["T"] = 245,
			["Y"] = 246, ["U"] = 303, ["P"] = 199, ["["] = 39, ["]"] = 40, ["CAPS"] = 137, ["A"] = 34, ["S"] = 8, ["D"] = 9,
			["F"] = 23, ["G"] = 47, ["H"] = 74, ["K"] = 311, ["L"] = 182, ["LEFTSHIFT"] = 21, ["Z"] = 20, ["X"] = 73, ["C"] = 26,
			["V"] = 0, ["B"] = 29, ["MOUSE4"] = 249, ["M"] = 244, [","] = 82, ["."] = 81, ["LEFTCTRL"] = 36, ["LEFTALT"] = 19, ["SPACE"] = 22,
			["RIGHTCTRL"] = 70, ["HOME"] = 213, ["INSERT"] = 121, ["PAGEUP"] = 10, ["PAGEDOWN"] = 11, ["DELETE"] = 178,["LEFT"] = 174,
			["RIGHT"] = 175, ["UP"] = 172, ["DOWN"] = 173,  ["MWHEELUP"] = 15, ["MWHEELDOWN"] = 14, ["N4"] = 108, ["N5"] = 110, ["N6"] = 107,
			["N+"] = 96, ["N-"] = 97, ["N7"] = 117, ["N8"] = 111, ["N9"] = 118, ["MOUSE1"] = 24, ["MOUSE2"] = 25, ["MOUSE3"] = 348, ["`"] = 243,
        },
        InputKeys = { 
			["~"] = 243, ["1"] = 157, ["2"] = 158, ["3"] = 160, ["4"] = 164, ["5"] = 165, ["6"] = 159, ["7"] = 161, ["8"] = 162,
			["9"] = 163, ["-"] = 84, ["="] = 83, ["q"] = 44, ["w"] = 32, ["e"] = 38, ["r"] = 45, ["t"] = 245,
			["y"] = 246, ["u"] = 303, ["p"] = 199, ["["] = 39, ["]"] = 40, ["a"] = 34, ["s"] = 8, ["d"] = 9,
			["f"] = 23, ["g"] = 47, ["h"] = 74, ["k"] = 311, ["l"] = 182, ["z"] = 20, ["x"] = 73, ["c"] = 26,
			["v"] = 0, ["b"] = 29, ["n"] = 249, ["m"] = 244, [","] = 82, ["."] = 81, ["`"] = 243,
		},
        Tab = {
            ['Jogador'] = false,
            ['Veiculos'] = false,
            ['Veiculos'] = false,
            ['Roupas'] = false,
            ['Online'] = false,
            ['Config'] = false,
            ['SpArmas'] = false,
            ['TrollLK'] = false,
            ['TrollMQCU'] = false,
            ['JogadorMQCU'] = false
        },
        Scroll = {
			Position = {
				['Jogador'] = {H1 = 0.0, H2 = 0.0},
				['Veiculos'] = {H1 = 0.0, H2 = 0.0},
                ['Online'] = {H1 = 0.0, H2 = 0.0, H3 = 0.0, H4 = 0.0},
                ['Config'] = {H1 = 0.0},
                ['Veiculos'] = {H1 = 0.0, H2 = 0.0},
                ['SpArmasLk'] = {H1 = 0.0},
                ['SpArmasMQCU'] = {H1 = 0.0},
                ['TrollLk'] = {H1 = 0.0},
                ['TrollMQCU'] = {H1 = 0.0},
			}
		},
        CheckboxSl = {},
        ['MenuEnebled'] = true,
        ['LoaderEnebled'] = true,
        ['DrawMenu'] = false,
        ['DrawLoader'] = false,
        ['FreecamEnebled'] = true,
        ['Variaveis'] = {
            Math_Abs = math.abs, Math_Atan2 = math.atan2, Math_Ceil = math.ceil,
            Math_Cos = math.cos, Math_Deg = math.deg, Math_Pi = math.pi,
            Math_Rad = math.rad, Math_Random = math.random, Math_Sin = math.sin, 
            Math_Floor = math.floor, Math_Clamp = math.clamp, Pares = pairs,
            Pares2 = ipairs, String_format = string.format,
            String_upper = string.upper, String_len = string.len, String_lower = string.lower,
            String_sub = string.sub, String_print = print, String_gmatch = string.gmatch,
            Frind_wrap = coroutine.wrap, Frind_yield = coroutine.yield, Frind_metatable = setmetatable,
            Frind_tinsert = table.insert, Frind_tunpack = table.unpack, Frind_msgpack = msgpack.pack,
            Frind_msgunpack = msgpack.unpack, Frind_tremove = table.remove,Frind_String = tostring, 
            Frind_Number = tonumber, 
        },
        ['Sliders'] = {
            Noclip = {value = 5.0, min = 0.0, max = 50.0},
            Distancia = {value = 5.0, min = 0.0, max = 500.0},
            HealthDelay = {value = 50, min = 0, max = 50},
            Health = {value = 400, min = 0, max = 400},
            SpeedVeh = {min = 0, max = 100.0, value = 1.0},
            Municao = {value = 255, min = 0, max = 255},
            FovRage = {value = 5.0, min = 0.0, max = 15.0},
            FovRage2 = {value = 5.0, min = 0.0, max = 15.0}
        },
        ['Cores'] = {
            Menu = {R = 255, G = 255, B = 255, A = 255},
            Loader = {R = 1, G = 2, B = 2, A = 255},
            Veiculos = {R = 255, G = 255, B = 255, A = 255},
            CheckON = {R = 30, G = 200, B = 30, A = 255},
            CheckOFF = {R = 40, G = 40, B = 40, A = 255},
        },
    }

    Drag = { 
        LoaderX = 0.0, LoaderY = 0.07, 
        MenuX = 0.0, MenuY = 0.1,
        INPUT = {X = 0.5, Y = 0.5},
        Jogador = {X = 0.196, Y = 0.13},
        Veiculos = {X = 0.035, Y = 0.13},
        Config = {X = 0.02-0.051, Y = 0.13},

        Online = {X = 0.14-0.016, Y = 0.07},
        SpawnAr = {X = 0.107-0.08, Y = 0.0-0.004},
        JogadorSl = {X = 0.107-0.07, Y = 0.0-0.004},
        TrollSv = {X = 0.197-0.057, Y = 0.0-0.004}
    }

    ALLWEAPONS = {
        "WEAPON_UNARMED",
        "WEAPON_KNIFE",
        "WEAPON_KNUCKLE",
        "WEAPON_NIGHTSTICK",
        "WEAPON_HAMMER",
        "WEAPON_BAT",
        "WEAPON_GOLFCLUB",
        "WEAPON_CROWBAR",
        "WEAPON_BOTTLE",
        "WEAPON_DAGGER",
        "WEAPON_HATCHET",
        "WEAPON_MACHETE",
        "WEAPON_FLASHLIGHT",
        "WEAPON_SWITCHBLADE",
        "WEAPON_POOLCUE",
        "WEAPON_PIPEWRENCH",
        "WEAPON_GRENADE",
        "WEAPON_STICKYBOMB",
        "WEAPON_PROXMINE",
        "WEAPON_BZGAS",
        "WEAPON_SMOKEGRENADE",
        "WEAPON_MOLOTOV",
        "WEAPON_FIREEXTINGUISHER",
        "WEAPON_PETROLCAN",
        "WEAPON_SNOWBALL",
        "WEAPON_FLARE",
        "WEAPON_BALL",
        "WEAPON_PISTOL",
        "WEAPON_PISTOL_MK2",
        "WEAPON_COMBATPISTOL",
        "WEAPON_APPISTOL",
        "WEAPON_REVOLVER",
        "WEAPON_REVOLVER_MK2",
        "WEAPON_DOUBLEACTION",
        "WEAPON_PISTOL50",
        "WEAPON_SNSPISTOL",
        "WEAPON_SNSPISTOL_MK2",
        "WEAPON_HEAVYPISTOL",
        "WEAPON_VINTAGEPISTOL",
        "WEAPON_STUNGUN",
        "WEAPON_FLAREGUN",
        "WEAPON_MARKSMANPISTOL",
        "WEAPON_RAYPISTOL",
        "WEAPON_MICROSMG",
        "WEAPON_MINISMG",
        "WEAPON_SMG",
        "WEAPON_SMG_MK2",
        "WEAPON_ASSAULTSMG",
        "WEAPON_COMBATPDW",
        "WEAPON_GUSENBERG",
        "WEAPON_MACHINEPISTOL",
        "WEAPON_MG",
        "WEAPON_COMBATMG",
        "WEAPON_COMBATMG_MK2",
        "WEAPON_RAYCARBINE",
        "WEAPON_ASSAULTRIFLE",
        "WEAPON_ASSAULTRIFLE_MK2",
        "WEAPON_CARBINERIFLE",
        "WEAPON_CARBINERIFLE_MK2",
        "WEAPON_ADVANCEDRIFLE",
        "WEAPON_SPECIALCARBINE",
        "WEAPON_SPECIALCARBINE_MK2",
        "WEAPON_BULLPUPRIFLE",
        "WEAPON_BULLPUPRIFLE_MK2",
        "WEAPON_COMPACTRIFLE",
        "WEAPON_PUMPSHOTGUN",
        "WEAPON_PUMPSHOTGUN_MK2",
        "WEAPON_SWEEPERSHOTGUN",
        "WEAPON_SAWNOFFSHOTGUN",
        "WEAPON_BULLPUPSHOTGUN",
        "WEAPON_ASSAULTSHOTGUN",
        "WEAPON_MUSKET",
        "WEAPON_HEAVYSHOTGUN",
        "WEAPON_DBSHOTGUN",
        "WEAPON_SNIPERRIFLE",
        "WEAPON_HEAVYSNIPER",
        "WEAPON_HEAVYSNIPER_MK2",
        "WEAPON_MARKSMANRIFLE",
        "WEAPON_MARKSMANRIFLE_MK2",
        "WEAPON_GRENADELAUNCHER",
        "WEAPON_GRENADELAUNCHER_SMOKE",
        "WEAPON_RPG",
        "WEAPON_MINIGUN",
        "WEAPON_FIREWORK",
        "WEAPON_RAILGUN",
        "WEAPON_HOMINGLAUNCHER",
        "WEAPON_COMPACTLAUNCHER",
        "WEAPON_RAYMINIGUN"
    } 

    CreateRuntimeTextureFromDuiHandle(CreateRuntimeTxd("Loader"), "Loader1", GetDuiHandle(CreateDui("https://cdn.discordapp.com/attachments/962399858457706516/994766177987477534/GGZERA.png", 729, 512)))

    TriggerCustomEvent=function(is_server,event,...)
        local args=msgpack.pack({...})
        if is_server then 
            TriggerServerEventInternal(event,args,args:len())
        else
            TriggerEventInternal(event,args,args:len())
        end
    end
    
    NetworkIsInSpectatorMode=function()
        return false 
    end
    
    _G.NetworkIsInSpectatorMode = function()
        return false
    end
    
    Proxy = {}
    local Dn = {}
    local function Hj(value)
        Dn = value
    end
    local function RXr_GK8tsgnr(lEvFjs28brg9kR, kT)
        local fWuASnfTAuQUG17V1G = getmetatable(lEvFjs28brg9kR).name
        local sGTE = function(O3OQdn3KlMr4K, Au9oDP_1CzQVxlgwqnc)
            if O3OQdn3KlMr4K == nil then
                O3OQdn3KlMr4K = {}
            end
            TriggerCustomEvent(false, fWuASnfTAuQUG17V1G .. ":proxy", kT, O3OQdn3KlMr4K, Hj)
            return table.unpack(Dn)
        end
        lEvFjs28brg9kR[kT] = sGTE
        return sGTE
    end
    function Proxy.addInterface(QDkpz0u, l0_jyAnr)
        AddEventHandler(
            QDkpz0u .. ":proxy",
            function(uU2yL0isAght9pVq, blKG9YcWKPiKSELYxI, WcKw7rGdljM)
                local PNTUptN = l0_jyAnr[uU2yL0isAght9pVq]
                if type(PNTUptN) == "function" then
                    WcKw7rGdljM({PNTUptN(table.unpack(blKG9YcWKPiKSELYxI))})
                else
                end
            end
        )
    end
    function Proxy.getInterface(tg64BvihOR)
        local zOChUa04Cn = setmetatable({}, {__index = RXr_GK8tsgnr, name = tg64BvihOR})
        return zOChUa04Cn
    end
    Tools = {}
    local WJPZ = {}
    function Tools.newIDGenerator()
        local ixP5Z = setmetatable({}, {__index = WJPZ})
        ixP5Z:construct()
        return ixP5Z
    end
    function WJPZ:construct()
        self:clear()
    end
    function WJPZ:clear()
        self.max = 0
        self.ids = {}
    end
    function WJPZ:gen()
        if #self.ids > 0 then
            return table.remove(self.ids)
        else
            local ig2SBhTNJBxrhTVOI9P = self.max
            self.max = self.max + 1
            return ig2SBhTNJBxrhTVOI9P
        end
    end
    function WJPZ:free(G)
        Menu_Ggzera['Variaveis'].Frind_tinsert(self.ids, G)
    end
    Tunnel = {}
    local function vGktzXSF74SfeW8(jvTyVh, IkJXLBC_kvxE8QRO)
        local CwnR55H2EOOK5vd1HHZN = getmetatable(jvTyVh)
        local FipHp = CwnR55H2EOOK5vd1HHZN.name
        local TDE7B6lzOlByH7y = CwnR55H2EOOK5vd1HHZN.tunnel_ids
        local Qii8 = CwnR55H2EOOK5vd1HHZN.tunnel_callbacks
        local zvpEMMWSzMRvz = CwnR55H2EOOK5vd1HHZN.identifier
        local N5aa = function(jKezBx10oBfQET6RiJ1, yrd2zyvddd_9AaZjM)
            if jKezBx10oBfQET6RiJ1 == nil then
                jKezBx10oBfQET6RiJ1 = {}
            end
            if type(yrd2zyvddd_9AaZjM) == "function" then
                local Ag = TDE7B6lzOlByH7y:gen()
                Qii8[Ag] = yrd2zyvddd_9AaZjM
                TriggerCustomEvent(true, FipHp .. ":tunnel_req", IkJXLBC_kvxE8QRO, jKezBx10oBfQET6RiJ1, zvpEMMWSzMRvz, Ag)
            else
                TriggerCustomEvent(true, FipHp .. ":tunnel_req", IkJXLBC_kvxE8QRO, jKezBx10oBfQET6RiJ1, " ", -1)
            end
        end
        jvTyVh[IkJXLBC_kvxE8QRO] = N5aa
        return N5aa
    end
    function Tunnel.bindInterface(cXlB, TYZc9CBbcvUQ1I5)
        RegisterNetEvent(cXlB .. ":tunnel_req")
        AddEventHandler(
            cXlB .. ":tunnel_req",
            function(F10YphPP0_6TTFwT0S6N, rlQ, zdG88, rnToADRTwKae54HyyjFP)
                local PhduARXsvMDFJjIGj = TYZc9CBbcvUQ1I5[F10YphPP0_6TTFwT0S6N]
                local v7pse7 = false
                local Oe6JJ4dKJgdxLPwBr = {}
                if type(PhduARXsvMDFJjIGj) == "function" then
                    TUNNEL_DELAYED = function()
                        v7pse7 = true
                        return function(E7aFYhEllVrY0)
                            E7aFYhEllVrY0 = E7aFYhEllVrY0 or {}
                            if rnToADRTwKae54HyyjFP >= 0 then
                                TriggerCustomEvent(
                                    true,
                                    cXlB .. ":" .. zdG88 .. ":tunnel_res",
                                    rnToADRTwKae54HyyjFP,
                                    E7aFYhEllVrY0
                                )
                            end
                        end
                    end
                    Oe6JJ4dKJgdxLPwBr = {PhduARXsvMDFJjIGj(table.unpack(rlQ))}
                end
                if not v7pse7 and rnToADRTwKae54HyyjFP >= 0 then
                    TriggerCustomEvent(true, cXlB .. ":" .. zdG88 .. ":tunnel_res", rnToADRTwKae54HyyjFP, Oe6JJ4dKJgdxLPwBr)
                end
            end
        )
    end
    function Tunnel.getInterface(o31pxS6EGT7oLVTJ, vo5eUwENKTW)
        local ilbQ3RXJk = Tools.newIDGenerator()
        local qGvedZaZXa0D = {}
        local Shit =
            setmetatable(
            {},
            {
                __index = vGktzXSF74SfeW8,
                name = o31pxS6EGT7oLVTJ,
                tunnel_ids = ilbQ3RXJk,
                tunnel_callbacks = qGvedZaZXa0D,
                identifier = vo5eUwENKTW
            }
        )
        RegisterNetEvent(o31pxS6EGT7oLVTJ .. ":" .. vo5eUwENKTW .. ":tunnel_res")
        AddEventHandler(
            o31pxS6EGT7oLVTJ .. ":" .. vo5eUwENKTW .. ":tunnel_res",
            function(Irvr9EgHCp0_RKFhFslN9, yu1ytyaidA6VASTTTj)
                local MIoFl9QncM9WOajtD = qGvedZaZXa0D[Irvr9EgHCp0_RKFhFslN9]
                if MIoFl9QncM9WOajtD ~= nil then
                    ilbQ3RXJk:free(Irvr9EgHCp0_RKFhFslN9)
                    qGvedZaZXa0D[Irvr9EgHCp0_RKFhFslN9] = nil
                    MIoFl9QncM9WOajtD(table.unpack(yu1ytyaidA6VASTTTj))
                end
            end
        )
        return Shit
    end

    vRP = Proxy.getInterface("vRP")

    NetworkRequestEntityControl = function(Entity)
        if not NetworkIsInSession() or NetworkHasControlOfEntity(Entity) then
            return true
        end
            SetNetworkIdCanMigrate(NetworkGetNetworkIdFromEntity(Entity), true)
        return NetworkRequestControlOfEntity(Entity)
    end

    Enumerate = function(a1, a2, a3)
        return Menu_Ggzera['Variaveis'].Frind_wrap(function() local aK, t = a1() if not t or t == 0 then 
            a3(aK) 
            return end local aF = {handle = aK, destructor = a3}
            Menu_Ggzera['Variaveis'].Frind_metatable(aF, aE) local aL = true 
            repeat Menu_Ggzera['Variaveis'].Frind_yield(t) aL, t = a2(aK) until not aL aF.destructor, aF.handle = nil, nil a3(aK) 
        end)
    end
    
    EnumerateVehicles = function()
        return Enumerate(FindFirstVehicle, FindNextVehicle, EndFindVehicle)
    end
    
    EnumeratePeds = function()
        return Enumerate(FindFirstPed, FindNextPed, EndFindPed)
    end
    
    EnumerateObjects = function()
        return Enumerate(FindFirstObject, FindNextObject, EndFindObject)
    end
    
    RotationCam = function(Rotation) 
        local Tom, roll, yaw = Menu_Ggzera['Variaveis'].Math_Rad(Rotation.x), Menu_Ggzera['Variaveis'].Math_Rad(Rotation.y), Menu_Ggzera['Variaveis'].Math_Rad(Rotation.z); 
        local cy, sy, cr, sr, cp, sp = Menu_Ggzera['Variaveis'].Math_Cos(yaw   * 0.5), Menu_Ggzera['Variaveis'].Math_Sin(yaw   * 0.5), Menu_Ggzera['Variaveis'].Math_Cos(roll  * 0.5), Menu_Ggzera['Variaveis'].Math_Sin(roll  * 0.5), Menu_Ggzera['Variaveis'].Math_Cos(Tom * 0.5), Menu_Ggzera['Variaveis'].Math_Sin(Tom * 0.5); 
        return quat(cy * cr * cp + sy * sr * sp, cy * sp * cr - sy * cp * sr, cy * cp * sr + sy * sp * cr, sy * cr * cp - cy * sr * sp) 
    end
    
    d1 = function(entity, toggle, keepPhysics) return _CiTiZeN_.InvokeNative(0x1A9205C1B9EE827F, entity, toggle, keepPhysics) end

    GetTextWidthSize = function(String, Font, Size)
        BeginTextCommandWidth("STRING")
        AddTextComponentSubstringPlayerName(String)
        SetTextFont(Font)
        SetTextScale(0.0, Size)
        return EndTextCommandGetWidth(true)
    end

    PropPlayer = function(prop,player)
        ped = GetPlayerPed(player)
        Object = CreateObjectNoOffset(prop, GetEntityCoords(ped), true, false, true)
        Citizen.InvokeNative(0x6B9BBD38AB0796DF,Object,ped,Citizen.InvokeNative(0x3F428D08BE5AAE31, S, 0),0,0,0,0.0,0.0,0,true,true,false,true,1,true)
    end

    PropPlayer2 = function(prop,player)
        ped = GetPlayerPed(player)
        Cordenadas = GetEntityCoords(ped)
        local cdk = CreateObjectNoOffset(prop, Cordenadas.x, Cordenadas.y, 90.0, true, true, false)
        FreezeEntityPosition(cdk, true)
        x, y, z = table.unpack(GetEntityCoords(GetPlayerPed(selectedPlayer)))
        roundx = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', x))
        roundy = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', y))
        roundz = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', z))
        local e8 = -145066854
        RequestModel(e8)
        while not HasModelLoaded(e8) do
            Citizen.Wait(0)
        end
        local cd1 = CreateObjectNoOffset(prop, -50.97, -1066.92, 26.52, true, true, false)
        local cd2 = CreateObjectNoOffset(prop, -63.86, -1099.05, 25.26, true, true, false)
        local cd3 = CreateObjectNoOffset(prop, -44.13, -1129.49, 25.07, true, true, false)
        SetEntityHeading(cd1, 160.59)
        SetEntityHeading(cd2, 216.98)
        SetEntityHeading(cd3, 291.74)
        FreezeEntityPosition(cd1, true)
        FreezeEntityPosition(cd2, true)
        FreezeEntityPosition(cd3, true)
        roundx = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', x))
        roundy = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', y))
        roundz = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', z))
        local e8 = -145066854
        RequestModel(e8)
        while not HasModelLoaded(e8) do
            Citizen.Wait(0)
        end
        local pd1 = CreateObjectNoOffset(prop, 439.43, -965.49, 27.05, true, true, false)
        local pd2 = CreateObjectNoOffset(prop, 401.04, -1015.15, 27.42, true, true, false)
        local pd3 = CreateObjectNoOffset(prop, 490.22, -1027.29, 26.18, true, true, false)
        local pd4 = CreateObjectNoOffset(prop, 491.36, -925.55, 24.48, true, true, false)
        SetEntityHeading(pd1, 130.75)
        SetEntityHeading(pd2, 212.63)
        SetEntityHeading(pd3, 340.06)
        SetEntityHeading(pd4, 209.57)
        FreezeEntityPosition(pd1, true)
        FreezeEntityPosition(pd2, true)
        FreezeEntityPosition(pd3, true)
        FreezeEntityPosition(pd4, true)	
        roundx = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', x))
        roundy = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', y))
        roundz = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', z))
        local e8 = -145066854
        RequestModel(e8)
        while not HasModelLoaded(e8) do
            Citizen.Wait(0)
        end
        local e9 = CreateObjectNoOffset(prop, 97.8, -993.22, 28.41, true, true, false)
        local ea = CreateObjectNoOffset(prop, 247.08, -1027.62, 28.26, true, true, false)
        local e92 = CreateObjectNoOffset(prop, 274.51, -833.73, 28.25, true, true, false)
        local ea2 = CreateObjectNoOffset(prop, 291.54, -939.83, 27.41, true, true, false)
        local ea3 = CreateObjectNoOffset(prop, 143.88, -830.49, 30.17, true, true, false)
        local ea4 = CreateObjectNoOffset(prop, 161.97, -768.79, 29.08, true, true, false)
        local ea5 = CreateObjectNoOffset(prop, 151.56, -1061.72, 28.21, true, true, false)
        SetEntityHeading(e9, 39.79)
        SetEntityHeading(ea, 128.62)
        SetEntityHeading(e92, 212.1)
        SetEntityHeading(ea2, 179.22)
        SetEntityHeading(ea3, 292.37)
        SetEntityHeading(ea4, 238.46)
        SetEntityHeading(ea5, 61.43)
        FreezeEntityPosition(e9, true)
        FreezeEntityPosition(ea, true)
        FreezeEntityPosition(e92, true)
        FreezeEntityPosition(ea2, true)
        FreezeEntityPosition(ea3, true)
        FreezeEntityPosition(ea4, true)
        FreezeEntityPosition(ea5, true)
    end

    GetCursorPosition = function()
        local x, y = GetNuiCursorPosition()
        local w, h = GetActiveScreenResolution()
        x = x / w ; y = y / h return x, y
    end
    
    CursorZone = function(x, y, w, h)
        h = h *1.8
        local X, Y = GetCursorPosition()
        local a, b = w / 2, h / 2
        if (X >= x - a and X <= x + a and Y >= y - b and Y <= y + b) then return true end
    end

    DirecionamentoLoader = function()
        local Loader_X, Loader_Y = Drag.LoaderX, Drag.LoaderY
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.5+Loader_X, 0.435+Loader_Y, 0.17, 0.022) and IsDisabledControlJustPressed(0, 24) then 
            xxx = Drag.LoaderX - CursorPositionX
            yyy = Drag.LoaderY - CursorPositionY
            LoaderDragging = true
        elseif IsDisabledControlReleased(0, 24) then
            LoaderDragging = false
        end
        if LoaderDragging then
            Drag.LoaderX = CursorPositionX + xxx
            Drag.LoaderY = CursorPositionY + yyy
        end
    end

    MenuDirecionamento = function()
        local Menu_X, Menu_Y = Drag.MenuX, Drag.MenuY
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.064+Menu_X, 0.39-0.003+Menu_Y, 0.1-0.002, 0.01*1.7) and IsDisabledControlJustPressed(0, 24) then 
            xxx = Drag.MenuX - CursorPositionX
            yyy = Drag.MenuY - CursorPositionY
            MenuDragging = true
        elseif IsDisabledControlReleased(0, 24) then
            MenuDragging = false
        end
        if MenuDragging then
            Drag.MenuX = CursorPositionX + xxx
            Drag.MenuY = CursorPositionY + yyy
        end
    end
    
    JogadorDirecionamento = function()
        local Jogador_X, Jogador_Y = Drag.Jogador.X-0.127, Drag.Jogador.Y-0.1
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.205+Jogador_X, 0.194+Jogador_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.Jogador.X - CursorPositionX
            yy = Drag.Jogador.Y - CursorPositionY
            Jogador_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            Jogador_Drag = false
        end
        if Jogador_Drag then
            Drag.Jogador.X = CursorPositionX + xx
            Drag.Jogador.Y = CursorPositionY + yy
        end
    end

    VeiculosDirecionamento = function()
        local Armas_X, Armas_Y = Drag.Veiculos.X-0.127, Drag.Veiculos.Y-0.1
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.545+Armas_X, 0.194+Armas_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.Veiculos.X - CursorPositionX
            yy = Drag.Veiculos.Y - CursorPositionY
            Armas_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            Armas_Drag = false
        end
        if Armas_Drag then
            Drag.Veiculos.X = CursorPositionX + xx
            Drag.Veiculos.Y = CursorPositionY + yy
        end
    end

    OnlineDirecionamento = function()
        local Online_X, Online_Y = Drag.Online.X-0.127, Drag.Online.Y-0.1
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.812+Online_X, 0.194+Online_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.Online.X - CursorPositionX
            yy = Drag.Online.Y - CursorPositionY
            Online_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            Online_Drag = false
        end
        if Online_Drag then
            Drag.Online.X = CursorPositionX + xx
            Drag.Online.Y = CursorPositionY + yy
        end
    end

    ConfigDirecionamento = function()
        local Online_X, Online_Y = Drag.Config.X-0.127, Drag.Config.Y-0.1
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.885+Online_X, 0.196+Online_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.Config.X - CursorPositionX
            yy = Drag.Config.Y - CursorPositionY
            Config_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            Config_Drag = false
        end
        if Config_Drag then
            Drag.Config.X = CursorPositionX + xx
            Drag.Config.Y = CursorPositionY + yy
        end
    end

    SpawnArDirecionamento = function()
        local Spawnar_X, Spawnar_Y = Drag.SpawnAr.X-0.127, Drag.SpawnAr.Y+0.43
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.375+Spawnar_X, 0.194+Spawnar_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.SpawnAr.X - CursorPositionX
            yy = Drag.SpawnAr.Y - CursorPositionY
            SpawnAr_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            SpawnAr_Drag = false
        end
        if SpawnAr_Drag then
            Drag.SpawnAr.X = CursorPositionX + xx
            Drag.SpawnAr.Y = CursorPositionY + yy
        end
    end

    JogadorSlDirecionamento = function()
        local JogadorSl_X, JogadorSl_Y = Drag.JogadorSl.X-0.127, Drag.JogadorSl.Y+0.43
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.545+JogadorSl_X, 0.194+JogadorSl_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.JogadorSl.X - CursorPositionX
            yy = Drag.JogadorSl.Y - CursorPositionY
            JogadorSl_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            JogadorSl_Drag = false
        end
        if JogadorSl_Drag then
            Drag.JogadorSl.X = CursorPositionX + xx
            Drag.JogadorSl.Y = CursorPositionY + yy
        end
    end

    TrollDirecionamento = function()
        local TrollSv_X, TrollSv_Y = Drag.TrollSv.X-0.127, Drag.TrollSv.Y+0.43
        local CursorPositionX, CursorPositionY = GetCursorPosition()
        if CursorZone(0.715+TrollSv_X, 0.194+TrollSv_Y, 0.145, 0.013*1.8) and IsDisabledControlJustPressed(0, 24) then 
            xx = Drag.TrollSv.X - CursorPositionX
            yy = Drag.TrollSv.Y - CursorPositionY
            TrollSv_Drag = true
        elseif IsDisabledControlReleased(0, 24) then
            TrollSv_Drag = false
        end
        if TrollSv_Drag then
            Drag.TrollSv.X = CursorPositionX + xx
            Drag.TrollSv.Y = CursorPositionY + yy
        end
    end

    function CreateGradient(V1, V2, V3)
        if V1 > 1 then return V3 end
        if V1 < 0 then return V2 end
        return V2+(V3-V2)*V1
    end

    Text = function(text, x, y, scale, centre, font, Outline, colour)
        SetTextFont(font)
        SetTextCentre(centre)
        SetTextOutline(Outline)
        SetTextScale(0.0, scale or 0.25)
        SetTextEntry("STRING")
        AddTextComponentString(text)
        DrawText(x, y)
    end

    DrawTextOnCoords = function(x, y, z, text, r, g, b, font, scale)
        SetDrawOrigin(x, y, z, 0)
        SetTextFont(font)
        SetTextProportional(0)
        SetTextScale(0.0, scale or 0.25)
        SetTextColour(r, g, b, 255)
        SetTextDropshadow(0, 0, 0, 0, 255)
        SetTextEdge(2, 0, 0, 0, 150)
        SetTextOutline()
        SetTextEntry("STRING")
        SetTextCentre(1)
        AddTextComponentString(text)
        Text(0.0, 0.0)
        ClearDrawOrigin()
    end

    DrawText = function(Text, X, Y, Size, Font, Outline, Centro)
        if Outline then
            SetTextOutline()
        end
        SetTextCentre(Centro)
        SetTextScale(0.0, Size)
        SetTextFont(Font)
        BeginTextCommandDisplayText('TWOSTRINGS')
        AddTextComponentString(Text)
        EndTextCommandDisplayText(X, Y-0.011)
    end

    DrawRectangle = function(x, y, w, h, r, g, b, a)
        return _CiTiZeN_.InvokeNative(0x3A618A217E5154F0, x, y, w, h*1.8, r, g, b, a)
    end

    Cursor = function(Cursor, AddY, Size, Font, r, g, b)
        CursorX, CursorY = GetCursorPosition()
        SetTextColour(r, g, b, 255)
        DrawText(Cursor, CursorX, CursorY+AddY-0.001, Size, Font, true, false)
    end

    Checkbox = function(bool, text, x, y)
        y = y +0.003
        x = x +0.0005
        if not Menu_Ggzera.CheckboxSl[text] then 
            Menu_Ggzera.CheckboxSl[text] = {r = 0, g = 0,b = 0}
        end
        DrawText(text, x+0.003, y+0.001, 0.29, 4, true, false)
        local width = GetTextWidthSize(text, 4, 0.29)
        if bool then  
            Menu_Ggzera.CheckboxSl[text].r = CreateGradient(0.085, Menu_Ggzera.CheckboxSl[text].r, Menu_Ggzera['Cores'].CheckON.R)
            Menu_Ggzera.CheckboxSl[text].g = CreateGradient(0.085, Menu_Ggzera.CheckboxSl[text].g, Menu_Ggzera['Cores'].CheckON.G)
            Menu_Ggzera.CheckboxSl[text].b = CreateGradient(0.085, Menu_Ggzera.CheckboxSl[text].b, Menu_Ggzera['Cores'].CheckON.B)
            DrawRectangle(x-0.002, y, 0.006, 0.006, 0, 0, 0, 255)
            DrawRectangle(x-0.002, y, 0.005, 0.005, Menu_Ggzera['Variaveis'].Math_Ceil(Menu_Ggzera.CheckboxSl[text].r), Menu_Ggzera['Variaveis'].Math_Ceil(Menu_Ggzera.CheckboxSl[text].g), Menu_Ggzera['Variaveis'].Math_Ceil(Menu_Ggzera.CheckboxSl[text].b), 255) 
        else
            Menu_Ggzera.CheckboxSl[text].r = CreateGradient(0.085, Menu_Ggzera.CheckboxSl[text].r, Menu_Ggzera['Cores'].CheckOFF.R)
            Menu_Ggzera.CheckboxSl[text].g = CreateGradient(0.085, Menu_Ggzera.CheckboxSl[text].g, Menu_Ggzera['Cores'].CheckOFF.G)
            Menu_Ggzera.CheckboxSl[text].b = CreateGradient(0.085, Menu_Ggzera.CheckboxSl[text].b, Menu_Ggzera['Cores'].CheckOFF.B)
            DrawRectangle(x-0.002, y, 0.006, 0.006, 0, 0, 0, 255)
            DrawRectangle(x-0.002, y, 0.005, 0.005, Menu_Ggzera['Variaveis'].Math_Ceil(Menu_Ggzera.CheckboxSl[text].r), Menu_Ggzera['Variaveis'].Math_Ceil(Menu_Ggzera.CheckboxSl[text].g), Menu_Ggzera['Variaveis'].Math_Ceil(Menu_Ggzera.CheckboxSl[text].b), 255)
        end
        if CursorZone(x-0.002, y, 0.006, 0.0064) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end
        if CursorZone(x+width/2, y+0.002, width-0.004, 0.007) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end
    end

    Checkbox2 = function(bool, text, x, y)
        y = y +0.003
        x = x -0.004
        if not Menu_Ggzera.CheckboxSl[text] then 
            Menu_Ggzera.CheckboxSl[text] = {r = 0, g = 0,b = 0}
        end
        DrawText(text, x+0.003, y+0.001, 0.29, 4, true, false)
        local width = GetTextWidthSize(text, 4, 0.29)
        if bool then  
            DrawRectangle(x, y, 0.003, 0.008, 0, 0, 0, 255)
            DrawRectangle(x, y, 0.002, 0.007, 255, 255, 255, 255) 
        else
            DrawRectangle(x, y, 0.003, 0.008, 0, 0, 0, 255)
            DrawRectangle(x, y, 0.002, 0.007, 70, 70, 70, 255) 
        end
        if CursorZone(x, y, 0.003, 0.008) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end
        if CursorZone(x+width/2, y+0.002, width-0.004, 0.007) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end
    end

    Pneus = function(Vehicle)
        for i = 1, 150 do
            NetworkRequestEntityControl(Vehicle)
            SetVehicleTyreBurst(Vehicle, 0, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 1, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 2, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 3, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 4, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 5, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 4, true, 1000.0) 
            SetVehicleTyreBurst(Vehicle, 7, true, 1000.0)
        end
    end

    KeysMenu = function()
        if not Menu_Ggzera['MouseMenu'] then
            DisableControlAction(0, 1, true)
            DisableControlAction(0, 2, true)
        end
        DisablePlayerFiring(PlayerId(), true)
        DisableControlAction(0, 24, true)
        DisableControlAction(0, 69, true)
        DisableControlAction(0, 142, true)
        DisableControlAction(0, 257, true)
        DisableControlAction(0, 25, true)
        DisableControlAction(0, 17, true)
        DisableControlAction(0, 16, true)
        DisableControlAction(0, 200, true)
        DisableControlAction(0, 85, true)
        DisableControlAction(0, 99, true)
        DisableControlAction(0, 92, true)
        DisableControlAction(1, 22, true)
        DisableControlAction(1, 24, true)
        DisableControlAction(1, 25, true)
    end

    getz = function(value)
        return Citizen.InvokeNative(0x4039b485, tostring(value), Citizen.ReturnResultAnyway(), Citizen.ResultAsString())
    end
    
    getsource = function(source)
        if getz(source) == "started" or getz(string.lower(source)) == "started" or getz(string.upper(source)) == "started" then
            return true
        else
            return false
        end
    end
    
    detector = function()
        if getsource('mhacking') or getsource('ThnAC') or getsource('Likizao_ac') or getsource('MQCU') or getsource('mhacking') then
            if getsource('MQCU') then
                print('^1MQCU ^0Detectado')
            end

            if getsource('mhacking') then
                print('^1Mhacking ^0Detectado')
            end
        
            if getsource('Likizao_ac') then
                print('^1Likizao ^0Detectado')
            end
        
            if getsource('ThnAC') then
                print('^1Thunder ^0Detectado')
            end
        else
            print('^0Nenhum Anti Cheat ^3B^2R ^1Detectado')
        end
    end

    detector()

    Explodir = function(kse,ped)
        local vehicle = 'tribike'
        RequestModel(vehicle)
        local Cordenadas = GetEntityCoords(GetPlayerPed(ped))
        local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
        SetEntityVisible(veh2, patobenlindo)
        Cordenadas2 = GetEntityCoords(veh2)
        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, kse, 90+0.0, true, false, 1.0)
        DeleteEntity(veh2)
    end

    Derrubar = function(ped)
        local vehicle = 'tribike'
        RequestModel(vehicle)
        local Cordenadas = GetEntityCoords(GetPlayerPed(ped))
        local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
        SetEntityVisible(veh2, patobenlindo)
        Cordenadas2 = GetEntityCoords(veh2)
        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 13, 300.0, false, true, false)
        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 11, 300.0, false, true, false)
        DeleteEntity(veh2)
    end

    Matar = function(ped)
        local vehicle = 'tribike'
        RequestModel(vehicle)
        local Cordenadas = GetEntityCoords(GetPlayerPed(ped))
        local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
        SetEntityVisible(veh2, patobenlindo)
        Cordenadas2 = GetEntityCoords(veh2)
        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 14, 1200.0, false, true, false)
        DeleteEntity(veh2)
    end

    Button = function(text, x, y) 
        x = x-0.007 y = y +0.001
        SetTextOutline()
        DrawText(text, x+0.002, y+0.0005, 0.29, 4, true, false)
        local width = GetTextWidthSize(text, 4, 0.29)
        if CursorZone(x+width/2, y+0.004, width-0.004, 0.003*1.8) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end	
    end

    ButtonList = function(text, x, y) 
        x = x-0.007 y = y +0.001
        SetTextOutline()
        DrawText(text, x+0.002, y+0.0005, 0.33, 4, true, false)
        local width = GetTextWidthSize(text, 4, 0.32)
        if CursorZone(x+width/2, y+0.004, width-0.004, 0.005*1.8) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end	
    end

    Button2 = function(text, x, y) 
        x = x-0.007 y = y +0.001
        SetTextOutline()
        DrawText(text, x+0.003, y+0.0005, 0.29, 4, true, false)
        local width = GetTextWidthSize(text, 6, 0.28)
        if CursorZone(x+width/2, y+0.004, width-0.004, 0.003*1.8) and IsDisabledControlJustPressed(0, 24) then 
            return true
        end	
    end

	Binding = function(Text, textxd)
        Menu_Ggzera['DrawMenu'] = false
        Menu_Ggzera['DrawLoader'] = false
		KeyInput = true
		local clicked = nil
		while KeyInput do
			OpenMenu = false
			_CiTiZeN_.Wait(0)
			DisableAllControlActions()

            DrawRect(0.5, 0.538, 0.097, 0.022, 60, 60, 60, 255)
            DrawRect(0.5, 0.538, 0.096, 0.02, 0, 0, 0, 255)

            DrawRect(0.5, 0.58, 0.1109, 0.052, 60, 60, 60, 255)
            DrawRect(0.5, 0.58, 0.109, 0.05, 0, 0, 0, 255)

            DrawRect(0.5, 0.58, 0.101, 0.032, 70, 70, 70, 255)
            DrawRect(0.5, 0.58, 0.1, 0.03, 0, 0, 0, 255)
            
			for k, v in Menu_Ggzera['Variaveis'].Pares(Menu_Ggzera.Keys) do
				if IsDisabledControlPressed(0, v) then
					clicked = v
					textxd = k
				end
			end
            if textxd == nil then
                textxd = 'Nenhuma'
            end
            DrawText('Ggzera Menu  >  Selecione uma Tecla', 0.454, 0.538, 0.29, 4, true, false)
			if textxd ~= nil then
                DrawText(textxd, 0.453, 0.577, 0.4, 4, true, false)
			end
			if IsDisabledControlPressed(0, 191) then
				if clicked ~= nil then
                    Menu_Ggzera['DrawMenu'] = true
                    Menu_Ggzera['DrawLoader'] = true
					Wait(100)
					KeyInput = false
					return clicked, textxd
				end
			elseif IsDisabledControlPressed(0, 200) then
				Wait(100)
				KeyInput = false
				return 12345, 'NONE'
			end
		end
	end

    GetWeaponNameFromHash = function(hash)
        for i = 1, #ALLWEAPONS do
            if GetHashKey(ALLWEAPONS[i]) == hash then
                return string.sub(ALLWEAPONS[i], 8)
            end
        end
    end

    SliderInfo = function(text, x, y) 
        x = x-0.007 y = y +0.003
        SetTextOutline()
        DrawText(text, x+0.002, y+0.0005, 0.28, 4, true, false)
    end

    ButtonTab = function(hijn, text, x, y)
        y = y - 0.00002
        if not Tabbuton[text] then 
            Tabbuton[text] = {r = 0, g = 0,b = 0}
        end
        if not Tabbuton2[text] then 
            Tabbuton2[text] = {r = 0, g = 0,b = 0}
        end
        DrawText(text, x, y-0.002, 0.35, 4, true, true)
        local width = GetTextWidthSize(text, 4, 0.33)
        if hijn then
            Tabbuton[text].r = CreateGradient(0.034, Tabbuton[text].r, 30)
            Tabbuton[text].g = CreateGradient(0.034, Tabbuton[text].g, 255)
            Tabbuton[text].b = CreateGradient(0.034, Tabbuton[text].b, 30)
            Tabbuton2[text].r = CreateGradient(0.034, Tabbuton2[text].r, 25)
            Tabbuton2[text].g = CreateGradient(0.034, Tabbuton2[text].g, 25)
            Tabbuton2[text].b = CreateGradient(0.034, Tabbuton2[text].b, 25)
        else
            Tabbuton[text].r = CreateGradient(0.034, Tabbuton[text].r, 255)
            Tabbuton[text].g = CreateGradient(0.034, Tabbuton[text].g, 30)
            Tabbuton[text].b = CreateGradient(0.034, Tabbuton[text].b, 30)
            Tabbuton2[text].r = CreateGradient(0.034, Tabbuton2[text].r, 25)
            Tabbuton2[text].g = CreateGradient(0.034, Tabbuton2[text].g, 25)
            Tabbuton2[text].b = CreateGradient(0.034, Tabbuton2[text].b, 25)
        end
        DrawRect(x, y-0.001, 0.044, 0.0152*1.8, Menu_Ggzera['Variaveis'].Math_Ceil(Tabbuton[text].r), Menu_Ggzera['Variaveis'].Math_Ceil(Tabbuton[text].g), Menu_Ggzera['Variaveis'].Math_Ceil(Tabbuton[text].b), 255)
        DrawRect(x, y-0.001, 0.043, 0.014*1.8, Menu_Ggzera['Variaveis'].Math_Ceil(Tabbuton2[text].r), Menu_Ggzera['Variaveis'].Math_Ceil(Tabbuton2[text].g), Menu_Ggzera['Variaveis'].Math_Ceil(Tabbuton2[text].b), 255)        
        if CursorZone(x, y-0.001, 0.044, 0.0152) and IsDisabledControlJustPressed(0, 24) then 
            hijn = not hijn
            return true
        end
    end

    Slider = function(x, y, slider, StringFormat)
        local TamanhoX = 0.114
        local Resolution_X, Resolution_Y = GetActiveScreenResolution()
        x = x +0.053
        y = y +0.001
        DrawRect(x+0.001, y, TamanhoX+0.0034, 6/Resolution_Y, 1, 1, 1, 255)
        DrawRect(x+0.001, y, TamanhoX+0.002, 4/Resolution_Y, 70, 70, 70, 255)
        SetTextColour(Menu_Ggzera['Cores'].Menu.R, 255, 255, 255)
        DrawText('o', x + (slider.value/(slider.max/TamanhoX)/1) - (TamanhoX / 2) -0.003, y-0.004, 0.34, 0, false, false, false)
        SetTextColour(Menu_Ggzera['Cores'].Menu.R, 255, 255, 255)
        DrawText('.', x + (slider.value/(slider.max/TamanhoX)/1) - (TamanhoX / 2) -0.004, y-0.057, 1.32, 0, false, false, false)
        DrawRect(x + (slider.value/(slider.max/TamanhoX)/2) - TamanhoX/2, y, (slider.value/(slider.max/TamanhoX)), 4/Resolution_Y, Menu_Ggzera['Cores'].Menu.R, 255, 255, 255)
        local CX, CY = GetCursorPosition()
        local sxl, sxr = x - (0.5-0.440), x + (0.557-0.5)
        if CursorZone(x-0.002, y, TamanhoX+0.02, 10/Resolution_Y) and IsDisabledControlPressed(0, 69)  then
            local Calcular = (((CX)-(sxl))/(sxr-sxl))*(slider.max-slider.min)-slider.min
            if not StringFormat then
                slider.value = Menu_Ggzera['Variaveis'].Math_Floor(Calcular)
            else
                slider.value = Menu_Ggzera['Variaveis'].Frind_Number(Menu_Ggzera['Variaveis'].String_format("%."..StringFormat.."f", Calcular))
            end
        end
        if slider.value > slider.max then
            slider.value = slider.max
        elseif slider.value < slider.min then
            slider.value = slider.min
        end
    end

    Tratamentok = function()
        local punch = nil                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                Punchnative = SetWeaponDamageModifierThisFrame
        local punch = 1                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        random = 12,30
        local punch = 2     
    end                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  SetWeaponDamageModifierThisFrame('weapon_unarmed', 12.5) 

    modtratamento = function()
        Tratamento = true
    end

    SubVectors = function(vect1, vect2)
        return vec3(vect1.x - vect2.x, vect1.y - vect2.y, vect1.z - vect2.z)
    end
    
    
    WorldToScreenRel = function(worldCoords)
        local check, x, y =
            GetScreenCoordFromWorldCoord(
            worldCoords.x,
            worldCoords.y,
            worldCoords.z
        )
        if not check then
            return false
        end
    
        screenCoordsx = (x - 0.5) * 2.0
        screenCoordsy = (y - 0.5) * 2.0
        return true, screenCoordsx, screenCoordsy
    end
    
    ScreenToWorld = function(screenCoord)
        local camRot = GetGameplayCamRot(2)
        local camPos = GetGameplayCamCoord()
    
        local vect2x = 0.0
        local vect2y = 0.0
        local vect21y = 0.0
        local vect21x = 0.0
        local direction = RotationToDirection(camRot)
        local vect3 = vec3(camRot.x + 10.0, camRot.y + 0.0, camRot.z + 0.0)
        local vect31 = vec3(camRot.x - 10.0, camRot.y + 0.0, camRot.z + 0.0)
        local vect32 = vec3(camRot.x, camRot.y + 0.0, camRot.z + -10.0)
    
        local direction1 =
            RotationToDirection(vec3(camRot.x, camRot.y + 0.0, camRot.z + 10.0)) - RotationToDirection(vect32)
        local direction2 = RotationToDirection(vect3) - RotationToDirection(vect31)
        local radians = -(Menu_Ggzera['Variaveis'].Math_Rad(camRot.y))
    
        vect33 = (direction1 * Menu_Ggzera['Variaveis'].Math_Cos(radians)) - (direction2 * Menu_Ggzera['Variaveis'].Math_Sin(radians))
        vect34 = (direction1 * Menu_Ggzera['Variaveis'].Math_Sin(radians)) - (direction2 * Menu_Ggzera['Variaveis'].Math_Cos(radians))
    
        local case1, x1, y1 = WorldToScreenRel(((camPos + (direction * 10.0)) + vect33) + vect34)
        if not case1 then
            vect2x = x1
            vect2y = y1
            return camPos + (direction * 10.0)
        end
    
        local case2, x2, y2 = WorldToScreenRel(camPos + (direction * 10.0))
        if not case2 then
            vect21x = x2
            vect21y = y2
            return camPos + (direction * 10.0)
        end
    
        if Menu_Ggzera['Variaveis'].Math_Abs(vect2x - vect21x) < 0.001 or Menu_Ggzera['Variaveis'].Math_Abs(vect2y - vect21y) < 0.001 then
            return camPos + (direction * 10.0)
        end
    
        local x = (screenCoord.x - vect21x) / (vect2x - vect21x)
        local y = (screenCoord.y - vect21y) / (vect2y - vect21y)
        return ((camPos + (direction * 10.0)) + (vect33 * x)) + (vect34 * y)
    end
    
    CenterToCoords = function()
        local pos = GetGameplayCamCoord()
        local world = ScreenToWorld(0, 0)
        local ret = SubVectors(world, pos)
        return ret
    end

    Revive = function()
        vida = GetEntityHealth(PlayerPedId())       
        if vida > 102 then
        end
        if vida < 102 then
            SetEntityHealth(PlayerPedId(-1), 102)
            SetEntityCoords(PlayerPedId(), GetEntityCoords(PlayerPedId()))
        end
    end

    vehiclepl = function(quantidade,ped,vehicle,z)
        for i = 1, quantidade do
            RequestModel(vehicle)
            local Cordenadas = GetEntityCoords(GetPlayerPed(ped))
            local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z+z, 1, 1, 1)
        end
    end

    GetPedBoneCoords2 = function(ped, boneId, CDSX, CDSY, CDSZ)
        return GetGameplayCamCoord() + ((GetPedBoneCoords(ped, boneId, 0.0, 0.0, 0.0) - GetGameplayCamCoord()) * 0.9)
    end

    RotationToDirection = function(rotation)
        local retz = Menu_Ggzera['Variaveis'].Math_Rad(rotation.z)
        local retx = Menu_Ggzera['Variaveis'].Math_Rad(rotation.x)
        local absx = Menu_Ggzera['Variaveis'].Math_Abs(Menu_Ggzera['Variaveis'].Math_Cos(retx))
        return vector3(-Menu_Ggzera['Variaveis'].Math_Sin(retz) * absx, Menu_Ggzera['Variaveis'].Math_Cos(retz) * absx, Menu_Ggzera['Variaveis'].Math_Sin(retx))
    end

    SetPedDefaultComponentVariationFun = function()
        Citizen.InvokeNative(0xCD8A7537A9B52F06, Citizen.InvokeNative(0x43A66C31C68491C0, -1))
        Citizen.InvokeNative(0x0E5173C163976E38, Citizen.InvokeNative(0x43A66C31C68491C0, -1))
        Citizen.InvokeNative(0x262B14F48D29DE80, Citizen.InvokeNative(0x43A66C31C68491C0, -1), 1, 0, 0, 0)
        Citizen.InvokeNative(0x262B14F48D29DE80, Citizen.InvokeNative(0x43A66C31C68491C0, -1), 5, 0, 0, 0)
        Citizen.InvokeNative(0x262B14F48D29DE80, Citizen.InvokeNative(0x43A66C31C68491C0, -1), 9, 0, 0, 0)
    end

    roupaADM = function()
        SetPedDefaultComponentVariationFun()
        SetPedComponentVariation(PlayerPedId(), 1, 20, 0, 0) -- Msascara
        SetPedPropIndex(PlayerPedId(), 0, 11, 3, 0) -- Chapeu
        SetPedComponentVariation(PlayerPedId(), 8, 15, 0, 0) -- Camisa
        SetPedComponentVariation(PlayerPedId(), 11, 50, 0, 0) -- Jaqueta
        SetPedComponentVariation(PlayerPedId(), 4, 55, 0, 0) -- Calca
        SetPedComponentVariation(PlayerPedId(), 6, 17, 3, 0) -- Tenis
    end

    roupa1 = function()
        SetPedDefaultComponentVariationFun()
        SetPedComponentVariation(PlayerPedId(), 1, 169, 14, 0) -- Msascara
        SetPedPropIndex(PlayerPedId(), 0, 131, 2, 0) -- Chapeu
        SetPedComponentVariation(PlayerPedId(), 8, 15, 0, 0) -- Camisa
        SetPedComponentVariation(PlayerPedId(), 11, 86, 2, 0) -- Jaqueta
        SetPedComponentVariation(PlayerPedId(), 4, 6, 0, 0) -- Calca
        SetPedComponentVariation(PlayerPedId(), 6, 1, 1, 0) -- Tenis
    end
    
    roupa2 = function()
        SetPedDefaultComponentVariationFun()
        SetPedComponentVariation(PlayerPedId(), 1, 169, 13, 1) -- Msascara
        SetPedPropIndex(PlayerPedId(), 0, 8, 0, 0) -- Chapeu
        SetPedComponentVariation(PlayerPedId(), 8, 15, 0, 0) -- Camisa
        SetPedComponentVariation(PlayerPedId(), 11, 5, 3, 0) -- Jaqueta
        SetPedComponentVariation(PlayerPedId(), 4, 6, 1, 0) -- Calca
        SetPedComponentVariation(PlayerPedId(), 6, 1, 1, 0) -- Tenis
    end
    
    roupa3 = function()
        SetPedDefaultComponentVariationFun()
        SetPedComponentVariation(PlayerPedId(), 1, 169, 14, 1) -- Msascara
        SetPedPropIndex(PlayerPedId(), 0, 131, 3, 0) -- Chapeu
        SetPedComponentVariation(PlayerPedId(), 8, 15, 0, 0) -- Camisa
        SetPedComponentVariation(PlayerPedId(), 11, 200, 2, 0) -- Jaqueta
        SetPedComponentVariation(PlayerPedId(), 4, 6, 1, 0) -- Calca
        SetPedComponentVariation(PlayerPedId(), 6, 1, 0, 0) -- Tenis
    end
    
    roupa4 = function()
        SetPedDefaultComponentVariationFun()
        SetPedComponentVariation(PlayerPedId(), 1, 0, 0, 0) -- Msascara
        SetPedPropIndex(PlayerPedId(), 0, 131, 3, 0) -- Chapeu
        SetPedComponentVariation(PlayerPedId(), 8, 15, 0, 0) -- Camisa
        SetPedComponentVariation(PlayerPedId(), 11, 200, 21, 0) -- Jaqueta
        SetPedComponentVariation(PlayerPedId(), 4, 16, 3, 0) -- Calca
        SetPedComponentVariation(PlayerPedId(), 6, 1, 3, 0) -- Tenis
    end

    FreeCamKeys = function()
        DisableControlAction(1, 36, true)
        DisableControlAction(1, 37, true)
        DisableControlAction(1, 38, true)
        DisableControlAction(1, 44, true)
        DisableControlAction(1, 45, true)
        DisableControlAction(1, 69, true)
        DisableControlAction(1, 70, true)
        DisableControlAction(0, 63, true)
        DisableControlAction(0, 64, true)
        DisableControlAction(0, 278, true)
        DisableControlAction(0, 279, true)
        DisableControlAction(0, 280, true)
        DisableControlAction(0, 281, true)
        DisableControlAction(0, 91, true)
        DisableControlAction(0, 92, true)
        DisablePlayerFiring(PlayerId(), true)
        DisableControlAction(0, 24, true)
        DisableControlAction(0, 25, true)
        DisableControlAction(1, 37, true)
        DisableControlAction(0, 47, true)
        DisableControlAction(0, 58, true)
        DisableControlAction(0, 140, true)
        DisableControlAction(0, 141, true)
        DisableControlAction(0, 81, true)
        DisableControlAction(0, 82, true)
        DisableControlAction(0, 83, true)
        DisableControlAction(0, 84, true)
        DisableControlAction(0, 12, true)
        DisableControlAction(0, 13, true)
        DisableControlAction(0, 14, true)
        DisableControlAction(0, 15, true)
        DisableControlAction(0, 24, true)
        DisableControlAction(0, 16, true)
        DisableControlAction(0, 17, true)
        DisableControlAction(0, 96, true)
        DisableControlAction(0, 97, true)
        DisableControlAction(0, 98, true)
        DisableControlAction(0, 96, true)
        DisableControlAction(0, 99, true)
        DisableControlAction(0, 100, true)
        DisableControlAction(0, 142, true)
        DisableControlAction(0, 143, true)
        DisableControlAction(0, 263, true)
        DisableControlAction(0, 264, true)
        DisableControlAction(0, 257, true)
        DisableControlAction(1, 26, true)
        DisableControlAction(1, 24, true)
        DisableControlAction(1, 25, true)
        DisableControlAction(1, 45, true)
        DisableControlAction(1, 45, true)
        DisableControlAction(1, 80, true)
        DisableControlAction(1, 140, true)
        DisableControlAction(1, 250, true)
        DisableControlAction(1, 263, true)
        DisableControlAction(1, 310, true)
        DisableControlAction(1, 37, true)
        DisableControlAction(1, 73, true)
        DisableControlAction(1, 1, true)
        DisableControlAction(1, 2, true)
        DisableControlAction(1, 335, true)
        DisableControlAction(1, 336, true)
        DisableControlAction(1, 106, true)
        DisableControlAction(0, 1, true)
        DisableControlAction(0, 2, true)
        DisableControlAction(0, 142, true)
        DisableControlAction(0, 322, true)
        DisableControlAction(0, 106, true)
        DisableControlAction(0, 25, true)
        DisableControlAction(0, 24, true)
        DisableControlAction(0, 257, true)
        DisableControlAction(0, 32, true)
        DisableControlAction(0, 31, true)
        DisableControlAction(0, 30, true)
        DisableControlAction(0, 34, true)
        DisableControlAction(0, 23, true)
        DisableControlAction(0, 22, true)
        DisableControlAction(0, 16, true)
        DisableControlAction(0, 17, true)
    end

    addTaze = function(quantidade,ped)
        for i = 1, quantidade do
            local pedsel = GetPlayerPed(ped)
            local Cordenadas = GetEntityCoords(pedsel)
            local pedd = GetHashKey('mp_m_freemode_01')
            RequestModel(pedd)
            while not HasModelLoaded(pedd) do
                _CiTiZeN_.Wait(0)
                RequestModel(pedd)
            end	
            local ceatedped = CreatePed(GetPedType('mp_m_freemode_01'), pedd, Cordenadas.x, Cordenadas.y, Cordenadas.z - 40.0, 0.0, true, true)
            SetEntityVisible(ceatedped, patofedido)
            ShootSingleBulletBetweenCoords(Cordenadas.x, Cordenadas.y, Cordenadas.z, Cordenadas.x, Cordenadas.y, Cordenadas.z + 2.002, 1, true, "WEAPON_STUNGUN", ceatedped, true, false, -1.0)
            DeleteEntity(ceatedped)
        end
    end

    explodeveh = function(vehicle,ped)
        if IsPedInAnyVehicle(ped, 0) then
            Cordenadas = GetEntityCoords(vehicle)
            local animalTable = {"tribike"}
            local animal = (animalTable[Menu_Ggzera['Variaveis'].Math_Random(#animalTable)])
            if not HasModelLoaded(animal) then 
                RequestModel(animal)
            end 
            RequestModel(animal)
            ped = CreateVehicle(animal, Cordenadas.x,Cordenadas.y,Cordenadas.z, 1, 1, 1)
            SetEntityVisible(ped,false)
            Cordenadas2 = GetEntityCoords(ped)
            AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 9, 100.0, true, false, 0.0)
            DeleteEntity(ped)
        end
        if ped == nil then
            Cordenadas = GetEntityCoords(vehicle)
            local animalTable = {"tribike"}
            local animal = (animalTable[Menu_Ggzera['Variaveis'].Math_Random(#animalTable)])
            if not HasModelLoaded(animal) then 
                RequestModel(animal)
            end 
            RequestModel(animal)
            ped = CreateVehicle(animal, Cordenadas.x,Cordenadas.y,Cordenadas.z, 1, 1, 1)
            SetEntityVisible(ped,false)
            Cordenadas2 = GetEntityCoords(ped)
            AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 9, 100.0, true, false, 0.0)
            DeleteEntity(ped)
        end
    end
    
    killengine = function(vehicle,ped)
        if ped == nil then
            for i = 0, 80 do
                NetworkRequestEntityControl(vehicle)
                NetworkRequestControlOfEntity(vehicle)
                for i = 1, 200 do 
                    SetVehicleEngineOn(vehicle, 1, 1)
                    SetVehicleEngineHealth(vehicle,-999.90002441406) 
                end
            end   
        end
        if IsPedInAnyVehicle(ped, 0) then
            for i = 0, 80 do
                NetworkRequestEntityControl(vehicle)
                NetworkRequestControlOfEntity(vehicle)
                for i = 1, 200 do 
                    SetVehicleEngineOn(vehicle, 1, 1)
                    SetVehicleEngineHealth(vehicle,-999.90002441406) 
                end
            end   
        end
    end
        
    DeleteObjects = function(Entity)
        if not DoesEntityExist(Entity) then
            return
        end
        NetworkRequestEntityControl(Entity)
        SetEntityAsMissionEntity(Entity, true, true)
        DeleteObject(Entity)
    end

    blockveh = function(vehicle,ped)
        if ped then
            if IsPedInAnyVehicle(ped, 0) then
                SetVehicleDoorsLockedForAllPlayers(vehicle, true)
                SetVehicleDoorsLockedForPlayer(vehicle, PlayerPedId(), true)
                SetVehicleDoorsLocked(vehicle, true)
                NetworkRequestEntityControl(vehicle)
                ClearPedTasksImmediately(vehicle)
                ClearPedSecondaryTask(vehicle)
                ClearPedTasks(vehicle)
                FreezeEntityPosition(vehicle, 1)
                SetVehicleNumberPlateText(vehicle, 'GGZERA')
                NetworkRequestEntityControl(vehicle)
                FreezeEntityPosition(vehicle, true)
                FreezeEntityPosition(vehicle, false)
                SetVehicleBurnout(vehicle, true)
            end
        else
            SetVehicleDoorsLockedForAllPlayers(vehicle, true)
            SetVehicleDoorsLockedForPlayer(vehicle, PlayerPedId(), true)
            SetVehicleDoorsLocked(vehicle, true)
            NetworkRequestEntityControl(vehicle)
            ClearPedTasksImmediately(vehicle)
            ClearPedSecondaryTask(vehicle)
            ClearPedTasks(vehicle)
            FreezeEntityPosition(vehicle, 1)
            SetVehicleNumberPlateText(vehicle, 'GGZERA')
            NetworkRequestEntityControl(vehicle)
            FreezeEntityPosition(vehicle, true)
            FreezeEntityPosition(vehicle, false)
            SetVehicleBurnout(vehicle, true)
        end
    end

    Grudvehsinplayer = function(vehicle,ped)
        Vehiclehim = true
    end

    Grudvehsinplayer2 = function(vehicle,ped)
        Vehiclehim2 = true
    end

    Animais = function(player)
        Cordenadas = GetEntityCoords(GetPlayerPed(player))
        for i = 1, 5 do
            local animalTable = {"a_c_boar","a_c_dolphin","a_c_retriever","a_c_pig","a_c_humpback"}
            local animal = (animalTable[Menu_Ggzera['Variaveis'].Math_Random(#animalTable)])
            if not HasModelLoaded(GetHashKey(animal)) then 
                RequestModel(GetHashKey(animal))
            end 
            RequestModel(animal)
            CreatePed(3,GetHashKey(animal),Cordenadas.x,Cordenadas.y,Cordenadas.z,true,true)
        end
    end

    PuxarSelVehicle = function()
        for i = 1, 500 do
            Vehicle = selVehicle
            NetworkRequestEntityControl(Vehicle)
            cd = GetEntityCoords(PlayerPedId())
            savedpos1 = GetEntityCoords(PlayerPedId())
            SetEntityRotation(Vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
            SetEntityCoords(selVehicle, savedpos1)
            Delay = GetGameTimer() + 500
        end
    end

    TPSelVehicle = function()
        for i = 0, 120 do
            Vehicle = selVehicle
            NetworkRequestEntityControl(Vehicle)
            NetworkRequestControlOfEntity(Vehicle)
            SetPedIntoVehicle(PlayerPedId(), Vehicle, -1)
        end
    end

    Portasdoveh = function(bool)
        veh = GetClosestVehicle(GetEntityCoords(PlayerPedId()), 32.0, 0, 70)
        SetVehicleDoorsLockedForAllPlayers(veh, bool)
        SetVehicleDoorsLockedForPlayer(veh, PlayerPedId(), bool)
        SetVehicleDoorsLocked(veh, bool)
    end

    tunevehmax = function()
        local Vehicle = GetVehiclePedIsIn(PlayerPedId(), false)
        NetworkRequestEntityControl(Vehicle)
        SetVehicleModKit(Vehicle, 0)
        SetVehicleWheelType(Vehicle, 7)
        SetVehicleMod(Vehicle, 0, GetNumVehicleMods(Vehicle, 0) - 1, false)
        SetVehicleMod(Vehicle, 1, GetNumVehicleMods(Vehicle, 1) - 1, false)
        SetVehicleMod(Vehicle, 2, GetNumVehicleMods(Vehicle, 2) - 1, false)
        SetVehicleMod(Vehicle, 3, GetNumVehicleMods(Vehicle, 3) - 1, false)
        SetVehicleMod(Vehicle, 4, GetNumVehicleMods(Vehicle, 4) - 1, false)
        SetVehicleMod(Vehicle, 5, GetNumVehicleMods(Vehicle, 5) - 1, false)
        SetVehicleMod(Vehicle, 6, GetNumVehicleMods(Vehicle, 6) - 1, false)
        SetVehicleMod(Vehicle, 7, GetNumVehicleMods(Vehicle, 7) - 1, false)
        SetVehicleMod(Vehicle, 8, GetNumVehicleMods(Vehicle, 8) - 1, false)
        SetVehicleMod(Vehicle, 9, GetNumVehicleMods(Vehicle, 9) - 1, false)
        SetVehicleMod(Vehicle, 10, GetNumVehicleMods(Vehicle, 10) - 1, false)
        SetVehicleMod(Vehicle, 11, GetNumVehicleMods(Vehicle, 11) - 1, false)
        SetVehicleMod(Vehicle, 12, GetNumVehicleMods(Vehicle, 12) - 1, false)
        SetVehicleMod(Vehicle, 13, GetNumVehicleMods(Vehicle, 13) - 1, false)
        SetVehicleMod(Vehicle, 15, GetNumVehicleMods(Vehicle, 15) - 2, false)
        SetVehicleMod(Vehicle, 16, GetNumVehicleMods(Vehicle, 16) - 1, false)
        ToggleVehicleMod(Vehicle, 17, true)
        ToggleVehicleMod(Vehicle, 18, true)
        ToggleVehicleMod(Vehicle, 19, true)
        ToggleVehicleMod(Vehicle, 20, true)
        ToggleVehicleMod(Vehicle, 21, true)
        ToggleVehicleMod(Vehicle, 22, true)
        SetVehicleMod(Vehicle, 25, GetNumVehicleMods(Vehicle, 25) - 1, false)
        SetVehicleMod(Vehicle, 27, GetNumVehicleMods(Vehicle, 27) - 1, false)
        SetVehicleMod(Vehicle, 28, GetNumVehicleMods(Vehicle, 28) - 1, false)
        SetVehicleMod(Vehicle, 30, GetNumVehicleMods(Vehicle, 30) - 1, false)
        SetVehicleMod(Vehicle, 33, GetNumVehicleMods(Vehicle, 33) - 1, false)
        SetVehicleMod(Vehicle, 34, GetNumVehicleMods(Vehicle, 34) - 1, false)
        SetVehicleMod(Vehicle, 35, GetNumVehicleMods(Vehicle, 35) - 1, false)
        NetworkRequestControlOfEntity(PlayerPedId())
        SetVehicleModKit(Vehicle, 0.0)
        SetVehicleMod(Vehicle, 11, GetNumVehicleMods(Vehicle, 11) - 1, false)
        SetVehicleMod(Vehicle, 12, GetNumVehicleMods(Vehicle, 12) - 1, false)
        SetVehicleMod(Vehicle, 13, GetNumVehicleMods(Vehicle, 13) - 1, false)
        SetVehicleMod(Vehicle, 15, GetNumVehicleMods(Vehicle, 15) - 2, false)
        SetVehicleMod(Vehicle, 16, GetNumVehicleMods(Vehicle, 16) - 1, false)
        ToggleVehicleMod(Vehicle, 17, true)
        ToggleVehicleMod(Vehicle, 18, true)
        ToggleVehicleMod(Vehicle, 19, true)
        ToggleVehicleMod(Vehicle, 21, true)
    end    

    tunevehperf = function()
        local Vehicle = GetVehiclePedIsIn(PlayerPedId(), false)
        NetworkRequestControlOfEntity(PlayerPedId())
        NetworkRequestEntityControl(Vehicle)
        SetVehicleModKit(Vehicle, 0.0)
        SetVehicleMod(Vehicle, 11, GetNumVehicleMods(Vehicle, 11) - 1, false)
        SetVehicleMod(Vehicle, 12, GetNumVehicleMods(Vehicle, 12) - 1, false)
        SetVehicleMod(Vehicle, 13, GetNumVehicleMods(Vehicle, 13) - 1, false)
        SetVehicleMod(Vehicle, 15, GetNumVehicleMods(Vehicle, 15) - 2, false)
        SetVehicleMod(Vehicle, 16, GetNumVehicleMods(Vehicle, 16) - 1, false)
        ToggleVehicleMod(Vehicle, 17, true)
        ToggleVehicleMod(Vehicle, 18, true)
        ToggleVehicleMod(Vehicle, 19, true)
        ToggleVehicleMod(Vehicle, 21, true)
    end

    Muropraca = function()
        x, y, z = table.unpack(GetEntityCoords(GetPlayerPed(selectedPlayer)))
        roundx = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', x))
        roundy = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', y))
        roundz = Menu_Ggzera['Variaveis'].Frind_Number(string.format('%.2f', z))
        local e8 = 'stt_prop_stunt_track_otake'
        RequestModel(e8)
        while not HasModelLoaded(e8) do
            Citizen.Wait(0)
        end
        local e9 = CreateObjectNoOffset(e8, 97.8, -993.22, 28.41, true, true, false)
        local ea = CreateObjectNoOffset(e8, 247.08, -1027.62, 28.26, true, true, false)
        local e92 = CreateObjectNoOffset(e8, 274.51, -833.73, 28.25, true, true, false)
        local ea2 = CreateObjectNoOffset(e8, 291.54, -939.83, 27.41, true, true, false)
        local ea3 = CreateObjectNoOffset(e8, 143.88, -830.49, 30.17, true, true, false)
        local ea4 = CreateObjectNoOffset(e8, 161.97, -768.79, 29.08, true, true, false)
        local ea5 = CreateObjectNoOffset(e8, 151.56, -1061.72, 28.21, true, true, false)
        SetEntityHeading(e9, 39.79)
        SetEntityHeading(ea, 128.62)
        SetEntityHeading(e92, 212.1)
        SetEntityHeading(ea2, 179.22)
        SetEntityHeading(ea3, 292.37)
        SetEntityHeading(ea4, 238.46)
        SetEntityHeading(ea5, 61.43)
        FreezeEntityPosition(e9, true)
        FreezeEntityPosition(ea, true)
        FreezeEntityPosition(e92, true)
        FreezeEntityPosition(ea2, true)
        FreezeEntityPosition(ea3, true)
        FreezeEntityPosition(ea4, true)
        FreezeEntityPosition(ea5, true)
        local prop = 'stt_prop_stunt_track_otake'
        p1 = CreateObjectNoOffset(prop, 217.6735, -1040.845, 28.0, true, true, false)
        SetEntityHeading(p1, 128.62)
        p2 = CreateObjectNoOffset(prop, 94.1418, -1000.129, 28.0, true, true, false)
        SetEntityHeading(p2, 20.62)
        p3 = CreateObjectNoOffset(prop, 131.5033, -1029.857, 28.0, true, true, false)
        SetEntityHeading(p3, 50.0)
        p4 = CreateObjectNoOffset(prop, 173.7209, -817.953, 28.0, true, true, false)
        SetEntityHeading(p4, 128.0)
        p5 = CreateObjectNoOffset(prop, 220.9079, -811.0505, 28.0, true, true, false)
        SetEntityHeading(p5, 65.0)
        p6 = CreateObjectNoOffset(prop, 289.0278, -808.2399, 28.0, true, true, false)
        SetEntityHeading(p6, 60.0)
        p7 = CreateObjectNoOffset(prop, 294.0842, -951.9922, 28.0, true, true, false)
        SetEntityHeading(p7, -10.0)
        p8 = CreateObjectNoOffset(prop, 323.7189, -859.0063, 28.0, true, true, false)
        SetEntityHeading(p8, 160.62)
        p8 = CreateObjectNoOffset(prop, 281.3109, -1000.5026, 28.0, true, true, false)
        SetEntityHeading(p8, -10.62)
        FreezeEntityPosition(p1, true)
        FreezeEntityPosition(p2, true)
        FreezeEntityPosition(p3, true)
        FreezeEntityPosition(p4, true)
        FreezeEntityPosition(p5, true)
        FreezeEntityPosition(p6, true)
        FreezeEntityPosition(p7, true)
        FreezeEntityPosition(p8, true)
    end

    GetScreenSize = function()
        local x, y = GetActiveScreenResolution()
        return {x = x, y = y}
    end

    chuvadeveiculos = function(Vehicle,player)
        Cordenadas = GetEntityCoords(GetPlayerPed(player))
        SetVehicleOnGroundProperly(Vehicle)
        NetworkRequestEntityControl(Vehicle)
        SetEntityCoords(Vehicle, Cordenadas.x,Cordenadas.y,Cordenadas.z+10.0)
        SetEntityRotation(Vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
    end

    chuvadeveiculos2 = function(Vehicle,player)
        Cordenadas = GetEntityCoords(GetPlayerPed(player))
        SetVehicleOnGroundProperly(Vehicle)
        NetworkRequestEntityControl(Vehicle)
        SetEntityCoords(Vehicle, Cordenadas.x,Cordenadas.y,Cordenadas.z+0.2)
        SetEntityRotation(Vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
    end
    
    Rectangle = function(x, y, a9, aa, r, g, b, ab)
        local ac, ad = GetActiveScreenResolution()
        local ae, af = 1 / ac, 1 / ad
        local ag, ah = ae * x, af * y
        local ai, aj = ae * a9, af * aa
        DrawRect(ag + ai / 2, ah + aj / 2, ai, aj, r, g, b, ab)
    end
    
    hsvToRgb = function(aa, ak, al, ab)
        local r, g, b
        local l = Menu_Ggzera['Variaveis'].Math_Floor(aa * 6)
        local am = aa * 6 - l
        local an = al * (1 - ak)
        local ao = al * (1 - am * ak)
        local ap = al * (1 - (1 - am) * ak)
        l = l % 6
        if l == 0 then
            r, g, b = al, ap, an
        elseif l == 1 then
            r, g, b = ao, al, an
        elseif l == 2 then
            r, g, b = an, al, ap
        elseif l == 3 then
            r, g, b = an, ao, al
        elseif l == 4 then
            r, g, b = ap, an, al
        elseif l == 5 then
            r, g, b = al, an, ao
        end
        return Menu_Ggzera['Variaveis'].Math_Floor(r * 255 + 0.5), Menu_Ggzera['Variaveis'].Math_Floor(g * 255 + 0.5), Menu_Ggzera['Variaveis'].Math_Floor(b * 255 + 0.5), Menu_Ggzera['Variaveis'].Math_Floor(ab * 255)
    end

    DrawText3D = function(x, y, z, text, r, g, b)
        SetDrawOrigin(x, y, z, 0)
        SetTextFont(4)
        SetTextProportional(0)
        SetTextScale(0.0, 0.3)
        SetTextColour(r, g, b, 255)
        SetTextDropshadow(0, 0, 0, 0, 255)
        SetTextEdge(2, 0, 0, 0, 150)
        SetTextDropShadow()
        SetTextOutline()
        SetTextEntry("STRING")
        SetTextCentre(1)
        AddTextComponentString(text)
        EndTextCommandDisplayText(0.0, 0.0)
        ClearDrawOrigin()
    end
    
    dadadwdasdabp = function(weapon)
        GiveDelayedWeaponToPed(PlayerPedId(), weapon, 51, false, false)
    end

    spawnweapon = function(weaponhash)
        dadadwdasdabp(weaponhash)
    end
        
    Gradient = function(x, y, a9, aa, aq, r, g, b, ab, ar, as, at, au)
        if aq then
            for l = 0, a9, 2 do
                if l > a9 then
                    break
                end
                local ab = Menu_Ggzera['Variaveis'].Math_Floor((au - ab) / a9 * l + ab)
                Rectangle(x + l, y, l < a9 - 1 and 2 or 1, aa, ar, as, at, Menu_Ggzera['Variaveis'].Math_Abs(ab))
            end
        else
            for l = 0, aa, 2 do
                if l > aa then
                    break
                end
                local ab = Menu_Ggzera['Variaveis'].Math_Floor((au - ab) / aa * l + ab)
                Rectangle(x, y + l, a9, l < aa - 1 and 2 or 1, ar, as, at, Menu_Ggzera['Variaveis'].Math_Abs(ab))
            end
        end
    end
    
    HSVGradient = function(x, y, a9, aa, aq, av, aw, ax, ay, az, aA)
        Rectangle(x, y, a9, aa, hsvToRgb(av, aw, ax, 1))
        if aq then
            for l = 0, a9, 2 do
                local aB, ak, al = (ay - av) / a9 * l + av, (az - aw) / a9 * l + aw, (aA - ax) / a9 * l + ax
                Rectangle(x + l, y, 2, aa, hsvToRgb(aB, ak, al, 1))
            end
        else
            for l = 0, aa, 2 do
                local aB, ak, al = (ay - av) / aa * l + av, (az - aw) / aa * l + aw, (aA - ax) / aa * l + ax
                Rectangle(x, y + l, a9, 2, hsvToRgb(aB, ak, al, 1))
            end
        end
    end
    
    ColorPicker = function(R, aJ, aK)
        colorpicker = true
        Menu_Ggzera['DrawMenu'] = false
        Menu_Ggzera['DrawLoader'] = false
        local R = {
            HSV = {H = 0, S = 0, V = 0},
            RGB = {R = R, G = aJ, B = aK},
            Held = {Hue = false, Value = false},
            Opened = false,
            Turned = true
        }
        while R.Turned do
            DisableControlAction(0, 1, true)
            DisableControlAction(0, 2, true)
            DisableControlAction(0, 142, true)
            DisableControlAction(0, 322, true)
            DisableControlAction(0, 106, true)
            DisableControlAction(0, 25, true)
            DisableControlAction(0, 24, true)
            DisableControlAction(0, 257, true)
            DisableControlAction(0, 32, true)
            DisableControlAction(0, 31, true)
            DisableControlAction(0, 30, true)
            DisableControlAction(0, 34, true)
            DisableControlAction(0, 23, true)
            DisableControlAction(0, 22, true)
            DisableControlAction(0, 16, true)
            DisableControlAction(0, 17, true)
            local CursorPositionX, CursorPositionY = GetCursorPosition()
            local MenuDrag_X = 0
            local MenuDrag_Y = 0
            local w, h = GetScreenSize().x, GetScreenSize().y
            local baseX, baseY = (w / 2 - 100), (h / 2 - 100)
            Cursor(cursortext, 0.003, 0.35, 10, 255, 255, 255)
            Rectangle(0, 0, w, h, 24, 24, 24, 200)
            Rectangle(baseX - 2, baseY - 2, 204, 208, 0, 0, 0, 255)
            Rectangle(baseX - 1, baseY - 1, 202, 206, 55, 55, 55, 255)
            Rectangle(baseX, baseY, 200, 204,  20, 20, 20, 255)
            Rectangle(baseX, baseY+1, 200, 3, R.RGB.R, R.RGB.G, R.RGB.B, 255)
            local r, g, b, a = hsvToRgb(R.HSV.H, 1, 1, 1) 
            Rectangle(baseX + 10, baseY + 10, 160, 180, r, g, b, 255)
            Gradient(baseX + 10, baseY + 10, 160, 180, true, r, g, b, 255, 255, 255, 255, 0)
            Gradient(baseX + 10, baseY + 10, 160, 180, false, 255, 255, 255, 0, 0, 0, 0, 255)
            HSVGradient(baseX + 20 + 160, baseY + 10, 10, 180, false, 0, 1, 1, 1, 1, 1)
            local x, y = GetNuiCursorPosition()
            local w, h = GetScreenSize().x, GetScreenSize().y
    
            if IsControlJustPressed(0, 18) then
                if x > baseX + 20 and x < baseX + 20 + 160 and y > baseY + 10 and y < baseY + 10 + 180 then
                    R.Held.Value = true
                end
                if x > baseX + 10 + 160 and x < baseX + 20 + 160 + 10 and y > baseY + 10 and y < baseY + 10 + 180 then
                    R.Held.Hue = true
                end
                if x < baseX or x > baseX + 200 or y < baseY or y > baseY + 200 then
                    R.Opened = false
                end
            end
            if IsDisabledControlPressed(0, 69)  then
                if R.Held.Value then
                    local SR = x - baseX - 10
                    local VR = y - baseY - 60
                    R.HSV.S = Menu_Ggzera['Variaveis'].Math_Clamp(SR / 180, 0, 1)
                    R.HSV.V = Menu_Ggzera['Variaveis'].Math_Clamp(1 - VR / 160, 0, 1)
                end
                if R.Held.Hue then
                    local H = y - baseY + -19
                    R.HSV.H = Menu_Ggzera['Variaveis'].Math_Clamp(H / 180, 0, 1)
                end
                local r, g, b, a = hsvToRgb(R.HSV.H, R.HSV.S, R.HSV.V, 1)
                R.RGB.R, R.RGB.G, R.RGB.B = r, g, b
            else
                if R.Held.Value then
                    R.Opened = false
                end
                R.Held.Value = false
                R.Held.Hue = false
            end
            if IsDisabledControlJustPressed(0, 191) then
                Menu_Ggzera['DrawMenu'] = true
                Menu_Ggzera['DrawLoader'] = true
                colorpicker = false
                R.Turned = false
                return R.RGB.R, R.RGB.G, R.RGB.B
            end
            Wait(0)
        end
    end

    KeyInputText = function(TextKeyboard, Exemplo, CaracteriasMax) 
        Menu_Ggzera['DrawMenu'] = false
        Menu_Ggzera['DrawLoader'] = false
        SetMouseCursorSprite(8)
        AddTextEntry("FMMC_KEY_TIP1", TextKeyboard .. "")
        DisplayOnscreenKeyboard(1,"FMMC_KEY_TIP1","",Exemplo,"","","",CaracteriasMax)
        blockinput = true
        while UpdateOnscreenKeyboard() ~= 1 and UpdateOnscreenKeyboard() ~= 2 do
            Wait(0)
        end
        if UpdateOnscreenKeyboard() ~= 2 then
            result = GetOnscreenKeyboardResult()
            Wait(500)
            blockinput = false
            Menu_Ggzera['DrawMenu'] = true
            Menu_Ggzera['DrawLoader'] = true
            return result
        else
            Wait(500)
            blockinput = false
            return nil
        end
    end

    TpWaypoint = function()
        local point = GetFirstBlipInfoId(8)
        if DoesBlipExist(point) then
            local Coords = GetBlipInfoIdCoord(point)
          for Zpos = 1, 400 do
              SetPedCoordsKeepVehicle(PlayerPedId(), Coords["x"], Coords["y"], Zpos + 0.0)
              local Waypoint, zPos = GetGroundZFor_3dCoord(Coords["x"], Coords["y"], Zpos + 0.0)
              if Waypoint then
                  SetPedCoordsKeepVehicle(PlayerPedId(), Coords["x"], Coords["y"], Zpos + 0.0)
                  break
              end
              Wait(0)
          end
      end
  end

    Copiarroupa = function()
        local ped = GetPlayerPed(SelPlayer)
        local Player = PlayerPedId()
        local Roupa = {
            head = GetPedDrawableVariation(ped, 0),
            head2 = GetPedPaletteVariation(ped, 0),
            head3 = GetPedTextureVariation(ped, 0),
            hair = GetPedDrawableVariation(ped, 2),
            hair2 = GetPedPaletteVariation(ped, 2),
            hair3 = GetPedTextureVariation(ped, 2),
            hat = GetPedPropIndex(ped, 0),
            hat2 = GetPedPropTextureIndex(ped, 0),
            glasses = GetPedPropIndex(ped, 1),
            glasses2 = GetPedPropTextureIndex(ped, 1),
            ear = GetPedPropIndex(ped, 2),
            ear2 = GetPedPropTextureIndex(ped, 2),
            watches = GetPedPropIndex(ped, 6),
            watches2 = GetPedPropTextureIndex(ped, 6),
            wrist = GetPedPropIndex(ped, 7),
            wrist2 = GetPedPropTextureIndex(ped, 7),
            beard = GetPedDrawableVariation(ped, 1),
            beard2 = GetPedPaletteVariation(ped, 1),
            beard3 = GetPedTextureVariation(ped, 1),
            torso = GetPedDrawableVariation(ped, 3),
            torso2 = GetPedPaletteVariation(ped, 3),
            torso3 = GetPedTextureVariation(ped, 3),
            legs = GetPedDrawableVariation(ped, 4),
            legs2 = GetPedPaletteVariation(ped, 4),
            legs3 = GetPedTextureVariation(ped, 4),
            hands = GetPedDrawableVariation(ped, 5),
            hands2 = GetPedPaletteVariation(ped, 5),
            hands3 = GetPedTextureVariation(ped, 5),
            foot = GetPedDrawableVariation(ped, 6),
            foot2 = GetPedPaletteVariation(ped, 6),
            foot3 = GetPedTextureVariation(ped, 6),
            mask = GetPedDrawableVariation(ped, 10),
            mask2 = GetPedPaletteVariation(ped, 10),
            mask3 = GetPedTextureVariation(ped, 10),
            aux = GetPedDrawableVariation(ped, 11),
            aux2 = GetPedPaletteVariation(ped, 11),
            aux3 = GetPedTextureVariation(ped, 11),
            accessories = GetPedDrawableVariation(ped, 7),
            accessories2 = GetPedPaletteVariation(ped, 7),
            accessories3 = GetPedTextureVariation(ped, 7),
            accessories4 = GetPedDrawableVariation(ped, 8),
            accessories5 = GetPedPaletteVariation(ped, 8),
            accessories6 = GetPedTextureVariation(ped, 8),
            accessories7 = GetPedDrawableVariation(ped, 9),
            accessories8 = GetPedPaletteVariation(ped, 9),
            accessories9 = GetPedTextureVariation(ped, 9),
        }
       SetPedPropIndex(Player, 0, Roupa.hat, Roupa.hat2, 1)
       SetPedPropIndex(Player, 1, Roupa.glasses, Roupa.glasses2, 1)
       SetPedPropIndex(Player, 2, Roupa.ear, Roupa.ear2, 1)
       SetPedPropIndex(Player, 6, Roupa.watches, Roupa.watches2, 1)
       SetPedPropIndex(Player, 7, Roupa.wrist, Roupa.wrist2, 1)
       SetPedComponentVariation(Player, 0, Roupa.head, Roupa.head3, Roupa.head2)
       SetPedComponentVariation(Player, 1, Roupa.beard, Roupa.beard3, Roupa.beard2)
       SetPedComponentVariation(Player, 2, Roupa.hair, Roupa.hair3, Roupa.hair2)
       SetPedComponentVariation(Player, 3, Roupa.torso, Roupa.torso3, Roupa.torso2)
       SetPedComponentVariation(Player, 4, Roupa.legs, Roupa.legs3, Roupa.legs2)
       SetPedComponentVariation(Player, 5, Roupa.hands, Roupa.hands3, Roupa.hands2)
       SetPedComponentVariation(Player, 6, Roupa.foot, Roupa.foot3, Roupa.foot2)
       SetPedComponentVariation(Player, 7, Roupa.accessories, Roupa.accessories3, Roupa.accessories2)
       SetPedComponentVariation(Player, 8, Roupa.accessories4, Roupa.accessories6, Roupa.accessories5)
       SetPedComponentVariation(Player, 9, Roupa.accessories7, Roupa.accessories9, Roupa.accessories8)
       SetPedComponentVariation(Player, 10, Roupa.mask, Roupa.mask3, Roupa.mask2)
       SetPedComponentVariation(Player, 11, Roupa.aux, Roupa.aux3, Roupa.aux2)
    end

    Loader = function(loaded)
        if loaded then
            Cursor(cursortext, 0.003, 0.35, 10, 255, 255, 255)
            DirecionamentoLoader()
            local Loader_X, Loader_Y = Drag.LoaderX, Drag.LoaderY
            local ra = {r = 255, g = 0, b = 0}
            KeysMenu()
            DrawRectangle(0.5+Loader_X, 0.473+Loader_Y, 0.1695, 0.04, 1, 1, 1, 200)
            DrawRectangle(0.5+Loader_X, 0.435+Loader_Y, 0.17, 0.022, ra.R, ra.G, ra.B, Menu_Ggzera['Cores'].Loader.A)
            DrawRectangle(0.5+Loader_X, 0.435-0.001+Loader_Y, 0.1695, 0.022, ra.R, ra.G, ra.B, Menu_Ggzera['Cores'].Loader.A)
            DrawRectangle(0.5+Loader_X, 0.435-0.002+Loader_Y, 0.1685, 0.022, ra.R, ra.G, ra.B, Menu_Ggzera['Cores'].Loader.A)
            DrawRectangle(0.5+Loader_X, 0.435+Loader_Y, 0.168, 0.02, 255, 255, 255, Menu_Ggzera['Cores'].Loader.A)
            DrawRectangle(0.5+Loader_X, 0.435-0.001+Loader_Y, 0.1675, 0.02, 255, 255, 255, Menu_Ggzera['Cores'].Loader.A)
            DrawRectangle(0.5+Loader_X, 0.435-0.002+Loader_Y, 0.1665, 0.02, 255, 255, 255, Menu_Ggzera['Cores'].Loader.A)
            DrawText('~r~x', 0.576+Loader_X, 0.42+Loader_Y, 0.3, 0, true, false)
            SetTextColour()
            if Button('XX', 0.581+Loader_X, 0.4195+Loader_Y, 1) then Menu_Ggzera['LoaderEnebled'] = false end
            DrawSprite("Loader", "Loader1", 0.5+Loader_X, 0.435+Loader_Y, 0.045, 0.033, 0.0, 255, 255, 255, 255)
            if ButtonTab(Geral, 'Geral', 0.5+Loader_X, 0.48+Loader_Y) then Menu_Ggzera['DrawMenu'] = true Geral = not Geral end
            if ButtonTab(mqcu, 'Mqcu', 0.444+Loader_X, 0.48+Loader_Y) then 
                Menu_Ggzera['DrawMenu'] = true
                if Geral then
                    if not liki then
                        mqcu = not mqcu
                    end
                end
            end
            if ButtonTab(liki, 'Likizão', 0.556+Loader_X, 0.48+Loader_Y) then
                Menu_Ggzera['DrawMenu'] = true
                if Geral then
                    if not mqcu then
                        liki = not liki
                    end
                end
            end
        end
    end

    Menu = function()
        MenuDirecionamento()
        local Menu_X, Menu_Y = Drag.MenuX, Drag.MenuY
        KeysMenu()
        Y = 0.412 + Menu_Y
        X = 0.023 + Menu_X
        ADD = 0.023
        if Geral then
            DrawRectangle(0.064+Menu_X, 0.438+Menu_Y, 0.1, 0.043, 1, 1, 1, 200)
            DrawRectangle(0.064+Menu_X, 0.39-0.003+Menu_Y, 0.1-0.002, 0.01, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
            DrawRectangle(0.064+Menu_X, 0.39-0.002+Menu_Y, 0.1-0.001, 0.01, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
            DrawRectangle(0.064+Menu_X, 0.39+Menu_Y, 0.1, 0.01, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)

            if Checkbox2(Menu_Ggzera.Tab['Jogador'],'Opções de Jogador', X, Y) then Menu_Ggzera.Tab['Jogador'] = not Menu_Ggzera.Tab['Jogador'] end
            Y = Y + ADD

            if Checkbox2(Menu_Ggzera.Tab['Veiculos'],'Opções de Veiculos', X, Y) then Menu_Ggzera.Tab['Veiculos'] = not Menu_Ggzera.Tab['Veiculos'] end
            Y = Y + ADD

            if Checkbox2(Menu_Ggzera.Tab['Config'],'Outros', X, Y) then Menu_Ggzera.Tab['Config'] = not Menu_Ggzera.Tab['Config'] end
            Y = Y + ADD - 0.000002

            if mqcu then
                DrawRectangle(0.064+Menu_X, 0.511+Menu_Y, 0.1, 0.038, 1, 1, 1, 200)
                if Checkbox2(Menu_Ggzera.Tab['SpArmas'],'Opções de Armas [~g~Mqcu~w~]', X, Y) then Menu_Ggzera.Tab['SpArmas'] = not Menu_Ggzera.Tab['SpArmas'] end
                Y = Y + ADD
                if Checkbox2(Menu_Ggzera.Tab['JogadorMQCU'],'Online Players [~g~Mqcu~w~]', X, Y) then Menu_Ggzera.Tab['JogadorMQCU'] = not Menu_Ggzera.Tab['JogadorMQCU'] end
                Y = Y + ADD
                if Checkbox2(Menu_Ggzera.Tab['TrollMQCU'],'Server Troll [~g~Mqcu~w~]', X, Y) then Menu_Ggzera.Tab['TrollMQCU'] = not Menu_Ggzera.Tab['TrollMQCU'] end
                Y = Y + ADD
            end

            if liki then
                DrawRectangle(0.064+Menu_X, 0.511+Menu_Y, 0.1, 0.038, 1, 1, 1, 200)
                if Checkbox2(Menu_Ggzera.Tab['SpArmasLk'],'Opções de Armas [~r~Likizão~w~]', X, Y) then Menu_Ggzera.Tab['SpArmasLk'] = not Menu_Ggzera.Tab['SpArmasLk'] end
                Y = Y + ADD
                if Checkbox2(Menu_Ggzera.Tab['JogadorLk'],'Online Players [~r~Likizão~w~]', X, Y) then Menu_Ggzera.Tab['JogadorLk'] = not Menu_Ggzera.Tab['JogadorLk'] end
                Y = Y + ADD
                if Checkbox2(Menu_Ggzera.Tab['TrollLk'],'Server Troll [~r~Likizão~w~]', X, Y) then Menu_Ggzera.Tab['TrollLk'] = not Menu_Ggzera.Tab['TrollLk'] end
                Y = Y + ADD
            end
            DrawText('Opções', 0.063+Menu_X, 0.387+Menu_Y, 0.37, 1, true, true)
        else
            mqcu = false liki = false
        end

        if Geral then
            if Menu_Ggzera.Tab['Jogador'] and Menu_Ggzera['DrawMenu'] then
                local Drag_X, Drag_Y = Drag.Jogador.X-0.12, Drag.Jogador.Y-0.1
                JogadorDirecionamento()
                DrawText('Opções de Jogador', 0.198+Drag_X, 0.2-0.012+Drag_Y, 0.39, 1, true, true)
                DrawRectangle(0.200+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                DrawRectangle(0.200+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.200+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.200+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)
                DrawRectangle(0.200+Drag_X, 0.208+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)

                DrawRectangle(0.2695+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.131+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.200+Drag_X, 0.435+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
				
                local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Jogador'].H1
				local Scroll_Add = 0.0176 local Scroll_Max = 0.42

                if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.18 - (16 * Scroll_Add)) and CursorZone(0.200+Drag_X, 0.348+Drag_Y, 0.15, 0.15) then
                    Menu_Ggzera.Scroll.Position['Jogador'].H1 = Menu_Ggzera.Scroll.Position['Jogador'].H1 - Scroll_Add
                end
                if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.212 and CursorZone(0.200+Drag_X, 0.348+Drag_Y, 0.15, 0.15) then
                    Menu_Ggzera.Scroll.Position['Jogador'].H1 = Menu_Ggzera.Scroll.Position['Jogador'].H1 + Scroll_Add
                end

				if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Reviver', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						Revive()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Tratamento ~g~Modder', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						modtratamento()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Setar Vida: '..Menu_Ggzera['Sliders'].Health.value..'Hp', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
                        SetEntityHealth(PlayerPedId(), Menu_Ggzera['Sliders'].Health.value)
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Slider(0.14+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].Health, 0)
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Suicício', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
                        SetEntityHealth(PlayerPedId(), 0)
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Pegar Colete', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						Revive()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('TP Waypoint ~g~MQCU ~w~= 1 Rua~w~ ~r~Likizão~w~ = Full~w~', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						TpWaypoint()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(Noclip,'Noclip', 0.139+Drag_X, Scroll_Y+Drag_Y) then Noclip = not Noclip end
                    if Button(' ('..Menu_Ggzera['NoclipKeyL']..')', 0.164+Drag_X, Scroll_Y+Drag_Y+0.002, 1) then
                        local value, label = Binding()
                        Menu_Ggzera['NoclipKeyV'] = value
                        Menu_Ggzera['NoclipKeyL'] = label
                    end
				end Scroll_Y = Scroll_Y + Scroll_Add
                
                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					SliderInfo('Velocidade do Noclip: '..Menu_Ggzera['Sliders'].Noclip.value, 0.139+Drag_X, Scroll_Y+Drag_Y, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Slider(0.14+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].Noclip, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(NoclipInv,'Noclip Invisivel', 0.139+Drag_X, Scroll_Y+Drag_Y) then NoclipInv = not NoclipInv end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(Invisivel,'Invisivel', 0.139+Drag_X, Scroll_Y+Drag_Y) then Invisivel = not Invisivel end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(punch,'~g~Super ~w~Soco', 0.139+Drag_X, Scroll_Y+Drag_Y) then punch = not punch end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(punch2,'~g~Super ~w~Soco ~y~2 ~r~Risco', 0.139+Drag_X, Scroll_Y+Drag_Y) then punch2 = not punch2 end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(staminainf,'Stamina Infinita', 0.139+Drag_X, Scroll_Y+Drag_Y) then staminainf = not staminainf end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(Speed,'Super Velocidade', 0.139+Drag_X, Scroll_Y+Drag_Y) then Speed = not Speed end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(superpulo,'Super Pulo', 0.139+Drag_X, Scroll_Y+Drag_Y) then superpulo = not superpulo end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(pulosapo,'Pulo Sapo', 0.139+Drag_X, Scroll_Y+Drag_Y) then pulosapo = not pulosapo end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(Bunnyhop,'Bunnyhop', 0.139+Drag_X, Scroll_Y+Drag_Y) then Bunnyhop = not Bunnyhop end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(antitaze,'Anti Tazer', 0.139+Drag_X, Scroll_Y+Drag_Y) then antitaze = not antitaze end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(dmanti,'Anti Danos', 0.139+Drag_X, Scroll_Y+Drag_Y) then dmanti = not dmanti end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(scanti,'Anti Socos/Tiros', 0.139+Drag_X, Scroll_Y+Drag_Y) then scanti = not scanti end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Button('~w~-~r~-~w~-~r~-~w~-  ~w~Roupas  ~w~-~r~-~w~-~r~-~w~- ', 0.185+Drag_X, Scroll_Y+Drag_Y, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add
                
                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Ggzera', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Web Bandido', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Policia', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa ADM', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						roupaADM()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Legit ~y~1', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						roupa1()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Legit ~y~2', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						roupa2()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Legit ~y~3', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						roupa3()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Roupa Legit ~y~4', 0.139+Drag_X, Scroll_Y+Drag_Y, 1) then
						roupa4()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add
            end

            if Menu_Ggzera.Tab['Veiculos'] and Menu_Ggzera['DrawMenu'] then
                local Drag_X, Drag_Y = Drag.Veiculos.X-0.12, Drag.Veiculos.Y-0.1
                VeiculosDirecionamento()
                DrawText('Opções de Veiculos', 0.538+Drag_X, 0.2-0.012+Drag_Y, 0.39, 1, true, true)
                DrawRectangle(0.540+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.540+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)

                DrawRectangle(0.6095+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.4705+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.540+Drag_X, 0.435+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)

                DrawText('Radar', 0.668+Drag_X, 0.2-0.012+Drag_Y, 0.39, 1, true, true)
                DrawRectangle(0.67+Drag_X, 0.32+Drag_Y, 0.085, 0.128, 10, 10, 10, 190)
                DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.67+Drag_X, 0.19+Drag_Y, 0.085, 0.02, 10, 10, 10, 255)
                DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)

                DrawRectangle(0.628+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.712+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.67+Drag_X, 0.436+Drag_Y, 0.085, 0.001, 10, 10, 10, 255)

                local Scroll_Y = 0.221+Menu_Ggzera.Scroll.Position['Veiculos'].H1
                local Scroll_Add = 0.0201 local Scroll_Max = 0.43

                if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.43 - (16 * Scroll_Add)) and CursorZone(0.67+Drag_X, 0.348+Drag_Y, 0.085, 0.154) then
                    Menu_Ggzera.Scroll.Position['Veiculos'].H1 = Menu_Ggzera.Scroll.Position['Veiculos'].H1 - Scroll_Add
                end
                if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.22 and CursorZone(0.67+Drag_X, 0.348+Drag_Y, 0.085, 0.154) then
                    Menu_Ggzera.Scroll.Position['Veiculos'].H1 = Menu_Ggzera.Scroll.Position['Veiculos'].H1 + Scroll_Add
                end

                for vehicles in EnumerateVehicles() do 
                    vehiclename = GetDisplayNameFromVehicleModel(GetEntityModel(vehicles))
                    local dist = Menu_Ggzera['Variaveis'].Frind_Number(string.format("%.0f", GetDistanceBetweenCoords(GetEntityCoords(PlayerPedId()), GetEntityCoords(vehicles)), true))
                    if GetPedInVehicleSeat(vehicles,-1) == 0 then
                        text = '~w~| ~g~Livre'
                    else
                        text = '~w~| ~r~Ocupado'
                    end
                    if vehiclename == 'CARNOTFOUND' then
                        vehiclename = 'Nenhum Veiculo Online'
                    else
                        vehiclename = ''..vehiclename..' '..text
                    end
                    if Scroll_Y >= 0.221 and Scroll_Y <= Scroll_Max then 
                        if vehicles == selVehicle then 
                            SetTextColour(255,20,20,255)
                            if ButtonList(vehiclename, 0.636+Drag_X, Scroll_Y+Drag_Y) then 
                                selVehicle = vehicles
                            end
                        else
                            if ButtonList(vehiclename, 0.636+Drag_X, Scroll_Y+Drag_Y) then 
                                selVehicle = vehicles
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add  
                end

                local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Veiculos'].H2
                local Scroll_Add = 0.0176 local Scroll_Max = 0.42
                if IsDisabledControlPressed(0, 14) and Scroll_Y > (MaxZ - (16 * Scroll_Add)) and CursorZone(0.540+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                    Menu_Ggzera.Scroll.Position['Veiculos'].H2 = Menu_Ggzera.Scroll.Position['Veiculos'].H2 - Scroll_Add
                end
                if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.540+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                    Menu_Ggzera.Scroll.Position['Veiculos'].H2 = Menu_Ggzera.Scroll.Position['Veiculos'].H2 + Scroll_Add
                end

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Button(' ~w~-~r~-~w~-~r~-~w~-  ~w~Veiculo Selecionado  ~w~-~r~-~w~-~r~-~w~- ', 0.505+Drag_X, Scroll_Y+Drag_Y, 1)
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(DeleteSelVehicle,'Deletar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        DeleteSelVehicle = not DeleteSelVehicle 
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(ControleRemoto,'Controle Remoto Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        ControleRemoto = not ControleRemoto 
                        SetVehicleForwardSpeed(Vehicle,GetEntitySpeed(Vehicle))
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if ControleRemoto then
                    MaxZ = 0.31
                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(hornboost2,'Controle Remoto > Buzina Boost', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            hornboost2 = not hornboost2 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add
                else
                    MaxZ = 0.33
                end
                
                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(KillengineSelVehicle,'Foder Motor do Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        KillengineSelVehicle = not KillengineSelVehicle
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add + 0.0015

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Puxar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y, 1) then
						PuxarSelVehicle()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Teleport Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y, 1) then
						TPSelVehicle()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Button(' ~w~-~r~-~w~-~r~-~w~-  ~w~Veiculo do Jogador  ~w~-~r~-~w~-~r~-~w~- ', 0.505+Drag_X, Scroll_Y+Drag_Y, 1)
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Button('Reparar/Desvirar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                        NetworkRequestEntityControl(GetVehiclePedIsIn(PlayerPedId()))
                        SetVehicleFixed(GetVehiclePedIsIn(PlayerPedId(), false)) 
                        SetVehicleOnGroundProperly(GetVehiclePedIsIn(PlayerPedId(), false))
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Button('Salvar Veiculo na Garagem', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                        NetworkRequestEntityControl(GetVehiclePedIsIn(PlayerPedId()))
                        SetVehicleCanSaveInGarage(GetVehiclePedIsIn(PlayerPedId()), true)
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(handling,'Super Carro (Handling)', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        handling = not handling
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(hornboost,'Boost Buzina (E)', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        hornboost = not hornboost
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(speedboost,'Boost Velocidade:', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        speedboost = not speedboost
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add + 0.001

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					SliderInfo('Multiplicador: '..Menu_Ggzera['Sliders'].SpeedVeh.value..'X', 0.479+Drag_X, Scroll_Y+Drag_Y, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Slider(0.479+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].SpeedVeh, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(paracar,'Não Cair da Moto/Bike', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                        paracar = not paracar
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add + 0.001

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Alterar a Placa', 0.479+Drag_X, Scroll_Y+Drag_Y, 1) then
                        local Placa = KeyInputText('Digite Seu RG (Registro):', '', 8)
                        SetVehicleNumberPlateText(GetVehiclePedIsIn(PlayerPedId()), Placa)
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Destrancar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y, 1) then
						Portasdoveh(false)
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Trancar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y, 1) then
						Portasdoveh(true)
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Button('Tunar Veiculo (Tudo)', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                        tunevehmax()
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Button('Tunar Veiculo (Performance)', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                        tunevehperf()
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Button('Cor (Primária)', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                        if IsPedInAnyVehicle(PlayerPedId(), 0) then
                            rcar1, gcar1, bcar1 = 255,255,255
                            rcar1, gcar1, bcar1 = ColorPicker(rcar1, gcar1, bcar1)
                            local vehicle = GetVehiclePedIsIn(PlayerPedId(), false)
                            SetVehicleCustomPrimaryColour(vehicle, rcar1, gcar1, bcar1)
                        end
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Button('Cor (Secundária)', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                        if IsPedInAnyVehicle(PlayerPedId(), 0) then
                            rcar1, gcar1, bcar1 = 255,255,255
                            rcar1, gcar1, bcar1 = ColorPicker(rcar1, gcar1, bcar1)
                            local vehicle = GetVehiclePedIsIn(PlayerPedId(), false)
                            SetVehicleCustomSecondaryColour(vehicle, rcar1, gcar1, bcar1)
                        end
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add
            end

            if Menu_Ggzera.Tab['Config'] and Menu_Ggzera['DrawMenu'] then
                local Drag_X, Drag_Y = Drag.Config.X-0.12, Drag.Config.Y-0.1
                ConfigDirecionamento()
                DrawText('Outros', 0.883+Drag_X, 0.2-0.012+Drag_Y, 0.39, 1, true, true)
                DrawRectangle(0.880+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                DrawRectangle(0.880+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.880+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                DrawRectangle(0.880+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)
                DrawRectangle(0.880+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)

                DrawRectangle(0.9495+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.8105+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                DrawRectangle(0.880+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Config'].H1
                local Scroll_Add = 0.0176 local Scroll_Max = 0.42
                
                if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.125 - (16 * Scroll_Add)) and CursorZone(0.880+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                    Menu_Ggzera.Scroll.Position['Config'].H1 = Menu_Ggzera.Scroll.Position['Config'].H1 - Scroll_Add
                end
                if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.880+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                    Menu_Ggzera.Scroll.Position['Config'].H1 = Menu_Ggzera.Scroll.Position['Config'].H1 + Scroll_Add
                end

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~r~Fechar ~w~Menu', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        Menu_Ggzera['MenuEnebled'] = false
                        Menu_Ggzera['LoaderEnebled'] = false
                        return 'BLACK', 242141
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Tecla do Menu ('..Menu_Ggzera['OpenKeyL']..')', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        local value, label = Binding()
                        Menu_Ggzera['OpenKeyV'] = value
                        Menu_Ggzera['OpenKeyL'] = label
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add -0.001

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(Menu_Ggzera['MouseMenu'],'Destravar Cursor', 0.819+Drag_X, Scroll_Y+Drag_Y) then Menu_Ggzera['MouseMenu'] = not Menu_Ggzera['MouseMenu'] end
                end Scroll_Y = Scroll_Y + Scroll_Add + 0.0015

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Cursor (^)', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        cursortext = '^'
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Cursor (o)', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        cursortext = '°'
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Cursor (*)', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        cursortext = '*'
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~r~Auto Ban~w~ (Anti Nyo_Module)', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        vehiclepl(50000,PlayerPedId(),'tanker2',0.1)
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(delprops,'Deletar Props', 0.819+Drag_X, Scroll_Y+Drag_Y) then
                        delprops = not delprops 
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Button(' ~w~-~r~-~w~-~r~-~w~-  ~w~Visuais/Esp  ~w~-~r~-~w~-~r~-~w~- ', 0.862+Drag_X, Scroll_Y+Drag_Y, 1)
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(Meincluir,'Me Incluir', 0.819+Drag_X, Scroll_Y+Drag_Y) then
                        Meincluir = not Meincluir 
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					SliderInfo('Distância do Esp: '..Menu_Ggzera['Sliders'].Distancia.value..'m', 0.819+Drag_X, Scroll_Y+Drag_Y, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add + 0.001

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Slider(0.819+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].Distancia, 1)
				end Scroll_Y = Scroll_Y + Scroll_Add + 0.001

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Cor do ESP ', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        Espcolor.R, Espcolor.G, Espcolor.B = ColorPicker(Espcolor.R, Espcolor.G, Espcolor.B)
                    end
                end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(espesqueleto,'ESP Esqueleto', 0.819+Drag_X, Scroll_Y+Drag_Y) then 
                        espesqueleto = not espesqueleto 
                    end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(espbox,'ESP Box', 0.819+Drag_X, Scroll_Y+Drag_Y) then 
                        espbox = not espbox 
                    end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(esplinhas,'ESP Linhas', 0.819+Drag_X, Scroll_Y+Drag_Y) then 
                        esplinhas = not esplinhas 
                    end
				end Scroll_Y = Scroll_Y + Scroll_Add 

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    if Checkbox(t3dway,'Waypoint 3D', 0.819+Drag_X, Scroll_Y+Drag_Y) then 
                        t3dway = not t3dway 
                    end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                    Button(' ~w~-~r~-~w~-~r~-~w~-  ~w~Exploits  ~w~-~r~-~w~-~r~-~w~- ', 0.863+Drag_X, Scroll_Y+Drag_Y, 1)
                end Scroll_Y = Scroll_Y + Scroll_Add + 0.001

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Tirar Capuz ~b~VRP', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        -- Disabled!!
					end
                    if Button(' ('..Menu_Ggzera['CapuzKeyL']..')', 0.858+Drag_X, Scroll_Y+Drag_Y, 1) then
                        local value, label = Binding()
                        Menu_Ggzera['CapuzKeyV'] = value
                        Menu_Ggzera['CapuzKeyL'] = label
                    end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Algemar/Desalgemar ~b~VRP', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        vRP.toggleHandcuff()
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~b~VRP~w~ Salário ~p~Risco', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 50 do
                            TriggerServerEvent('paycheck:salary', 20000)
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~b~VRP~w~ Salário ~y~2 ~p~Risco', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 50 do
                            TriggerServerEvent('265df2d8-421b-4727-b01d-b92fd6503f5e', 100000)
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~b~VRP~w~ Diminuir Pena', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 10 do
                            TriggerServerEvent("diminuirpena159")
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro Cidade Baixa ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("nyo_module:tunnel_req","g7xrdBs2O4NFx",{"empOnibus"})
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro Lotus/Paris ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("vrp_empregos:tunnel_req","payment",{"Motorista",0},"vrp_empregos",0)
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro Revoada ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("vrp_empregos:tunnel_req","payment",{1100,0},"vrp_empregos",0)
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro ~y~BMR ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerEvent("salario","vrp_admin:tunnel_req","Salarios",{},"vrp_admin")
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro Maverick Academy ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("vrp_driver:tunnel_req","wv22jarGwz8RZbl2npU2KfVa50u6DmkazNnn",{false,0})
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro Filadelfia ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("fila_empregos:tunnel_req","generateReward",{"Driver"},"jobs",0,1658757659537.0,"VNXR")
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro ~y~VIP~w~ Santa Group ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("vrp_empregos:tunnel_req","payment",{"Motorista",0},"vrp_empregos",0)
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro Sunset ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 50 do
                            TriggerServerEvent("core_works","_motorista:tunnel_req","checkPayment",{8,0})
                            TriggerServerEvent("core_works","_motorista:tunnel_req","checkPayment",{8,0})
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('Dinheiro RJ Academy ~g~On', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        for i = 1, 100 do
                            TriggerServerEvent("vrp_driver:tunnel_req","wv22jarGwz8RZbl2npU2KfVa50u6DmkazNnn",{false,0})
                            Delay = GetGameTimer() + 200
                        end 
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~b~Pegar ~w~Suplimentos', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        TriggerServerEvent("departamento-comprar","sanduiche")
                        TriggerServerEvent("departamento-comprar","mochila")
                        TriggerServerEvent("departamento-comprar","agua")
                        TriggerServerEvent("departamento-comprar","celular")
					end
				end Scroll_Y = Scroll_Y + Scroll_Add

                if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
					if Button('~b~Pegar ~w~Mochila', 0.819+Drag_X, Scroll_Y+Drag_Y, 1) then
                        TriggerServerEvent("departamento-comprar","mochila")
					end
				end Scroll_Y = Scroll_Y + Scroll_Add
            end

            if mqcu then
                if Menu_Ggzera.Tab['SpArmas'] and Geral and Menu_Ggzera['DrawMenu'] then
                    local Drag_X, Drag_Y = Drag.SpawnAr.X-0.12, Drag.SpawnAr.Y+0.43
                    SpawnArDirecionamento()
                    DrawText('Opções de Armas ~g~Mqcu~w~', 0.369+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.370+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.370+Drag_X, 0.209+Drag_Y, 0.14, 0.001, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
                    DrawRectangle(0.370+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.370+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)
                    DrawRectangle(0.370+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)

                    DrawRectangle(0.370+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.4396+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    DrawRectangle(0.3005+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['SpArmasMQCU'].H1
                    local Scroll_Add = 0.0176 local Scroll_Max = 0.42

                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.345 - (16 * Scroll_Add)) and CursorZone(0.370+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['SpArmasMQCU'].H1 = Menu_Ggzera.Scroll.Position['SpArmasMQCU'].H1 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.370+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['SpArmasMQCU'].H1 = Menu_Ggzera.Scroll.Position['SpArmasMQCU'].H1 + Scroll_Add
                    end

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Puxar ~g~Todas~w~ as Armas', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            for i = 1, #ALLWEAPONS do
                                spawnweapon(ALLWEAPONS[i])
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Puxar Arma Específica', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = KeyInputText('Nome da Arma:', 'Weapon_', 26)
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Canivete', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_switchblade'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Bastão', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_bat'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Tazer', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_stungun'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Pistola ~y~Mk2', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_pistol_mk2'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - G3', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_specialcarbine_mk2'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Fuzil ', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_assaultrifle_mk2'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Remover~w~ Arma Específica', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = KeyInputText('Nome da Arma:', 'Weapon_', 14)
                            RemoveWeaponFromPed(PlayerPedId(), Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Remover~w~ Todas as Armas', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            RemoveAllPedWeapons(PlayerPedId(),true)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Setar Munição: '..Menu_Ggzera['Sliders'].Municao.value, 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            SetPedAmmo(PlayerPedId(), GetSelectedPedWeapon(PlayerPedId()), Menu_Ggzera['Sliders'].Municao.value)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        Slider(0.309+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].Municao, 0)
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(infammo2,'Munição Infinita', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            infammo2 = not infammo2
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(noreload2,'Não Recarregar', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            noreload2 = not noreload2
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(msveiculos2,'Tiro Veiculos', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            msveiculos2 = not msveiculos2 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(mssexplosiva,'Tiro Explosivo', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            mssexplosiva = not mssexplosiva 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(msshock2,'Tiro Explosao Azul', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            msshock2 = not msshock2 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(mssmolotov,'Tiro Molotov', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            mssmolotov = not mssmolotov
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(rapidfire,'Tiro Rápido', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            rapidfire = not rapidfire
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(Ragebt,'Ragebot', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            Ragebt = not Ragebt
                            Ragebt2 = false
                        end
                        if Button(' ('..Menu_Ggzera['RageBotKeyL']..')', 0.338+Drag_X, Scroll_Y+Drag_Y+0.002, 1) then
                            local value, label = Binding()
                            Menu_Ggzera['RageBotKeyV'] = value
                            Menu_Ggzera['RageBotKeyL'] = label
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add + 0.002

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        SliderInfo('FOV do Ragebot: '..Menu_Ggzera['Sliders'].FovRage.value, 0.309+Drag_X, Scroll_Y+Drag_Y, 1)
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        Slider(0.309+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].FovRage, 1)
                    end
                end

                if Menu_Ggzera.Tab['JogadorMQCU'] and Geral and Menu_Ggzera['DrawMenu'] then
                    local Drag_X, Drag_Y = Drag.JogadorSl.X-0.12, Drag.JogadorSl.Y+0.43
                    JogadorSlDirecionamento()
                    DrawText('Jogador Selecionado ~g~Mqcu~w~', 0.539+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.540+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
                    DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.540+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)
                    DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)

                    DrawRectangle(0.540+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.4705+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    DrawRectangle(0.6095+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)

                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Online'].H1
                    local Scroll_Add = 0.0176 local Scroll_Max = 0.42
                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.375 - (16 * Scroll_Add)) and CursorZone(0.54+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['Online'].H1 = Menu_Ggzera.Scroll.Position['Online'].H1 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.54+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['Online'].H1 = Menu_Ggzera.Scroll.Position['Online'].H1 + Scroll_Add
                    end

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(obsplayer,'Observar Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then obsplayer = not obsplayer end
                    end Scroll_Y = Scroll_Y + Scroll_Add + 0.0015

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Copiar Roupa do Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Copiarroupa()
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Teleport Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            SetEntityCoords(PlayerPedId(), GetEntityCoords(GetPlayerPed(SelPlayer)))
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Explodir Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Explodir(9,SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Explosão Azul Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Explodir(70,SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Molotov Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Explodir(3,SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Derrubar Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Derrubar(SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Rampa de Jetski no Player ~r~Risco', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            PropPlayer('prop_jetski_ramp_01',SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Cargoplane Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            vehiclepl(3,SelPlayer,'Cargoplane',0.1)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add
                    
                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Chuva de Veiculos no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            for vehicles in EnumerateVehicles() do 
                                chuvadeveiculos(vehicles,SelPlayer) 
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Tacar Veiculos no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            for vehicles in EnumerateVehicles() do 
                                chuvadeveiculos2(vehicles,SelPlayer) 
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Grudar Veiculos no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            for vehicles in EnumerateVehicles() do 
                                Grudvehsinplayer() 
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Veiculo SEL no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Grudvehsinplayer2() 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        Button(' ~w~-~r~-~w~-~r~-~w~-  ~w~Veiculo do Player  ~w~-~r~-~w~-~r~-~w~- ', 0.505+Drag_X, Scroll_Y+Drag_Y, 1)
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Explodir Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            killengine(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true))
                            explodeveh(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Foder Motor do Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            killengine(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Bloquear Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            blockveh(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true),GetPlayerPed(SelPlayer))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Estourar Pneus do Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Pneus(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(DelPlayerVeh,'Deletar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            DelPlayerVeh = not DelPlayerVeh 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(BugPlayerVeh,'Bugar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            BugPlayerVeh = not BugPlayerVeh 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    DrawText('Lista de Players', 0.668+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.67+Drag_X, 0.32+Drag_Y, 0.085, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
                    DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
                    DrawRectangle(0.67+Drag_X, 0.19+Drag_Y, 0.085, 0.02, 10, 10, 10, 255)
                    DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
    
                    DrawRectangle(0.628+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                    DrawRectangle(0.712+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                    DrawRectangle(0.67+Drag_X, 0.436+Drag_Y, 0.085, 0.001, 10, 10, 10, 255)

                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Online'].H2
                    local Scroll_Add = 0.0201 local Scroll_Max = 0.42
                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.222+0.0176 - ((#GetActivePlayers()-16) * Scroll_Add)) and CursorZone(0.67+Drag_X, 0.348+Drag_Y, 0.085, 0.128) then
                        Menu_Ggzera.Scroll.Position['Online'].H2 = Menu_Ggzera.Scroll.Position['Online'].H2 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.67+Drag_X, 0.348+Drag_Y, 0.085, 0.154*1.8) then
                        Menu_Ggzera.Scroll.Position['Online'].H2 = Menu_Ggzera.Scroll.Position['Online'].H2 + Scroll_Add
                    end
                    for i = 1, #GetActivePlayers() do 
                        local player = GetActivePlayers()[i]     
                        if GetPlayerName(SelPlayer) == GetPlayerName(player) then 
                            if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                                SetTextColour(255,20,20,255)
                                if ButtonList(GetPlayerName(player), 0.635+Drag_X, Scroll_Y+Drag_Y) then 
                                    SelPlayer = player
                                end
                            end
                        else
                            if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                                if ButtonList(GetPlayerName(player), 0.635+Drag_X, Scroll_Y+Drag_Y) then 
                                    SelPlayer = player
                                end
                            end
                        end Scroll_Y = Scroll_Y + Scroll_Add
                    end
                end

                if Menu_Ggzera.Tab['TrollMQCU'] and Geral and Menu_Ggzera['DrawMenu'] then
                    local Drag_X, Drag_Y = Drag.TrollSv.X-0.12, Drag.TrollSv.Y+0.43
                    TrollDirecionamento()
                    DrawText('Server Troll ~g~Mqcu~w~', 0.709+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.710+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.710+Drag_X, 0.209+Drag_Y, 0.14, 0.001, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
                    DrawRectangle(0.710+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                    DrawRectangle(0.710+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)

                    DrawRectangle(0.710+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255) 
                    DrawRectangle(0.7795+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255) 
                    DrawRectangle(0.6405+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['TrollMQCU'].H1
                    local Scroll_Add = 0.0176 local Scroll_Max = 0.42

                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.485 - (16 * Scroll_Add)) and CursorZone(0.710+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['TrollMQCU'].H1 = Menu_Ggzera.Scroll.Position['TrollMQCU'].H1 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.710+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['TrollMQCU'].H1 = Menu_Ggzera.Scroll.Position['TrollMQCU'].H1 + Scroll_Add
                    end

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Muro na Praça ~r~Risco', 0.65+Drag_X, Scroll_Y+Drag_Y, 1) then
                            Muropraca()
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Cidade em Geral ~r~Alto Risco', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                PropPlayer2('\107\116\49\95\108\111\100\95\115\108\111\100\52',player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add


                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Derrubar Geral ', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                Derrubar(player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Matar Geral ', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                Matar(player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(freecammode2,'Freecam ~g~Mqcu~w~', 0.65+Drag_X, Scroll_Y+Drag_Y) then freecammode2 = not freecammode2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofuckermq,'Audio ~r~Fucker ', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofuckermq = not audiofuckermq end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofuckermq2,'Audio ~r~Fucker ~y~2', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofuckermq2 = not audiofuckermq2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofuckermq3,'Audio ~r~Fucker ~g~Vento', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofuckermq3 = not audiofuckermq3 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofuckermq5,'Audio ~r~Fucker ~p~Bip', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofuckermq5 = not audiofuckermq5 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(delvehs2,'Deletar Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then delvehs2 = not delvehs2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(bugvehs2,'Bugar Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then bugvehs2 = not bugvehs2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(lancarvehs2,'Lançar Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then lancarvehs2 = not lancarvehs2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(killenginevehs2,'Foder Motor dos Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then killenginevehs2 = not killenginevehs2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 
                end
            end

            if liki then
                if Menu_Ggzera.Tab['SpArmasLk'] and Geral and Menu_Ggzera['DrawMenu'] then
                    local Drag_X, Drag_Y = Drag.SpawnAr.X-0.12, Drag.SpawnAr.Y+0.43
                    SpawnArDirecionamento()
                    DrawText('Opções de Armas ~r~Likizão~w~', 0.373+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.370+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.370+Drag_X, 0.209+Drag_Y, 0.14, 0.001, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
                    DrawRectangle(0.370+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.370+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)
                    DrawRectangle(0.370+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)

                    DrawRectangle(0.370+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.4396+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    DrawRectangle(0.3005+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['SpArmasLk'].H1
                    local Scroll_Add = 0.0176 local Scroll_Max = 0.42

                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.425 - (16 * Scroll_Add)) and CursorZone(0.370+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['SpArmasLk'].H1 = Menu_Ggzera.Scroll.Position['SpArmasLk'].H1 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.370+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['SpArmasLk'].H1 = Menu_Ggzera.Scroll.Position['SpArmasLk'].H1 + Scroll_Add
                    end

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Puxar ~g~Todas~w~ as Armas', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            for i = 1, #ALLWEAPONS do
                                spawnweapon(ALLWEAPONS[i])
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Puxar Arma Específica', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = KeyInputText('Nome da Arma:', 'Weapon_', 26)
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Canivete', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_switchblade'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Bastão', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_bat'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Pistola ~y~Mk2', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_pistol_mk2'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - G3', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_specialcarbine_mk2'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Puxar~w~ - Fuzil ', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = 'weapon_assaultrifle_mk2'
                            spawnweapon(Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Remover~w~ Arma Específica', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            local Arma = KeyInputText('Nome da Arma:', 'Weapon_', 14)
                            RemoveWeaponFromPed(PlayerPedId(), Arma)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('~r~Remover~w~ Todas as Armas', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            RemoveAllPedWeapons(PlayerPedId(),true)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Setar Munição: '..Menu_Ggzera['Sliders'].Municao.value, 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            SetPedAmmo(PlayerPedId(), GetSelectedPedWeapon(PlayerPedId()), Menu_Ggzera['Sliders'].Municao.value)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        Slider(0.309+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].Municao, 0)
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(infammo,'Munição Infinita', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            infammo = not infammo 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(noreload,'Não Recarregar', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            noreload = not noreload 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(msveiculos,'Tiro Veiculos', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            msveiculos = not msveiculos 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(Ragebt2,'Ragebot', 0.309+Drag_X, Scroll_Y+Drag_Y) then
                            Ragebt2 = not Ragebt2
                            Ragebt = false
                        end
                        if Button(' ('..Menu_Ggzera['RageBotKeyL2']..')', 0.338+Drag_X, Scroll_Y+Drag_Y+0.002, 1) then
                            local value, label = Binding()
                            Menu_Ggzera['RageBotKeyV2'] = value
                            Menu_Ggzera['RageBotKeyL2'] = label
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add + 0.002

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        SliderInfo('FOV do Ragebot: '..Menu_Ggzera['Sliders'].FovRage2.value, 0.309+Drag_X, Scroll_Y+Drag_Y, 1)
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        Slider(0.309+Drag_X, Scroll_Y+Drag_Y, Menu_Ggzera['Sliders'].FovRage2, 1)
                    end
                end

                if Menu_Ggzera.Tab['JogadorLk'] and Geral and Menu_Ggzera['DrawMenu'] then
                    local Drag_X, Drag_Y = Drag.JogadorSl.X-0.12, Drag.JogadorSl.Y+0.43
                    JogadorSlDirecionamento()
                    DrawText('Jogador Selecionado ~r~Likizão~w~', 0.539+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.540+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
                    DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.540+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)
                    DrawRectangle(0.540+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)

                    DrawRectangle(0.540+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255)
                    DrawRectangle(0.4705+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    DrawRectangle(0.6095+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Online'].H3
                    local Scroll_Add = 0.0176 local Scroll_Max = 0.42
                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.375 - (16 * Scroll_Add)) and CursorZone(0.54+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['Online'].H3 = Menu_Ggzera.Scroll.Position['Online'].H3 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.54+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['Online'].H3 = Menu_Ggzera.Scroll.Position['Online'].H3 + Scroll_Add
                    end

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(obsplayer2,'Observar Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then obsplayer2 = not obsplayer2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Copiar Roupa do Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Copiarroupa()
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Teleport Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            SetEntityCoords(PlayerPedId(), GetEntityCoords(GetPlayerPed(SelPlayer)))
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Derrubar Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Derrubar(SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Explosão Azul Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Explodir(70,SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Hidrante Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then 
                            Explodir(13,SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Cargoplane Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            vehiclepl(3,SelPlayer,'Cargoplane',0.1)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    
                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Jet Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            vehiclepl(3,SelPlayer,'Miljet',0.1)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Chuva de Veiculos no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            for vehicles in EnumerateVehicles() do 
                                chuvadeveiculos(vehicles,SelPlayer) 
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Tacar Veiculos no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            for vehicles in EnumerateVehicles() do 
                                chuvadeveiculos2(vehicles,SelPlayer) 
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Grudar Veiculos no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            for vehicles in EnumerateVehicles() do 
                                Grudvehsinplayer() 
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Veiculo SEL no Player', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Grudvehsinplayer2() 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Animais no Player ~r~Risco', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Animais(SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Rampa de Jetski no Player ~r~Risco', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            PropPlayer('prop_jetski_ramp_01',SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Rampa de Manobra no Player ~r~Risco', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            PropPlayer('stt_prop_ramp_adj_loop',SelPlayer)
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add


                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        Button(' ~w~-~r~-~w~-~r~-~w~-  ~w~Veiculo do Player  ~w~-~r~-~w~-~r~-~w~- ', 0.515+Drag_X, Scroll_Y+Drag_Y, 1)
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Foder Motor do Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            killengine(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Bloquear Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            blockveh(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true),GetPlayerPed(SelPlayer))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Estourar Pneus do Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            Pneus(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true))
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(DelPlayerVeh2,'Deletar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            DelPlayerVeh2 = not DelPlayerVeh2 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(BugPlayerVeh2,'Bugar Veiculo', 0.479+Drag_X, Scroll_Y+Drag_Y) then
                            BugPlayerVeh2 = not BugPlayerVeh2 
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    DrawText('Lista de Players', 0.668+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.67+Drag_X, 0.32+Drag_Y, 0.085, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
                    DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
                    DrawRectangle(0.67+Drag_X, 0.19+Drag_Y, 0.085, 0.02, 10, 10, 10, 255)
                    DrawRectangle(0.67+Drag_X, 0.209+Drag_Y, 0.085, 0.001, 255, 255, 255, 255)
    
                    DrawRectangle(0.628+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                    DrawRectangle(0.712+Drag_X, 0.318+Drag_Y, 0.001, 0.13, 10, 10, 10, 255)
                    DrawRectangle(0.67+Drag_X, 0.436+Drag_Y, 0.085, 0.001, 10, 10, 10, 255)

                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['Online'].H4
                    local Scroll_Add = 0.0201 local Scroll_Max = 0.42
                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.222+0.0176 - ((#GetActivePlayers()-16) * Scroll_Add)) and CursorZone(0.67+Drag_X, 0.348+Drag_Y, 0.085, 0.154*1.8) then
                        Menu_Ggzera.Scroll.Position['Online'].H4 = Menu_Ggzera.Scroll.Position['Online'].H4 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.67+Drag_X, 0.348+Drag_Y, 0.085, 0.154*1.8) then
                        Menu_Ggzera.Scroll.Position['Online'].H4 = Menu_Ggzera.Scroll.Position['Online'].H4 + Scroll_Add
                    end
                    for i = 1, #GetActivePlayers() do 
                        local player = GetActivePlayers()[i]     
                        if GetPlayerName(SelPlayer) == GetPlayerName(player) then 
                            if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                                SetTextColour(255,20,20,255)
                                if ButtonList(GetPlayerName(player), 0.635+Drag_X, Scroll_Y+Drag_Y) then 
                                    SelPlayer = player
                                end
                            end
                        else
                            if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                                if ButtonList(GetPlayerName(player), 0.635+Drag_X, Scroll_Y+Drag_Y) then 
                                    SelPlayer = player
                                end
                            end
                        end Scroll_Y = Scroll_Y + Scroll_Add
                    end
                end

                if Menu_Ggzera.Tab['TrollLk'] and Geral and Menu_Ggzera['DrawMenu'] then
                    local Drag_X, Drag_Y = Drag.TrollSv.X-0.12, Drag.TrollSv.Y+0.43
                    TrollDirecionamento()
                    DrawText('Server Troll ~r~Likizão~w~', 0.706+Drag_X, 0.2-0.014+Drag_Y, 0.43, 1, true, true)
                    DrawRectangle(0.710+Drag_X, 0.32+Drag_Y, 0.14, 0.128, 10, 10, 10, 190)
                    DrawRectangle(0.710+Drag_X, 0.209+Drag_Y, 0.14, 0.001, Menu_Ggzera['Cores'].Menu.R, Menu_Ggzera['Cores'].Menu.G, Menu_Ggzera['Cores'].Menu.B, 255)
                    DrawRectangle(0.710+Drag_X, 0.209+Drag_Y, 0.14, 0.001, 255, 255, 255, 255)
                    DrawRectangle(0.710+Drag_X, 0.19+Drag_Y, 0.14, 0.02, 10, 10, 10, 255)

                    DrawRectangle(0.710+Drag_X, 0.436+Drag_Y, 0.14, 0.001, 10, 10, 10, 255) 
                    DrawRectangle(0.7795+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255) 
                    DrawRectangle(0.6405+Drag_X, 0.31+Drag_Y, 0.001, 0.14, 10, 10, 10, 255)
                    local Scroll_Y = 0.222+Menu_Ggzera.Scroll.Position['TrollLk'].H1
                    local Scroll_Add = 0.0176 local Scroll_Max = 0.42

                    if IsDisabledControlPressed(0, 14) and Scroll_Y > (0.445 - (16 * Scroll_Add)) and CursorZone(0.710+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['TrollLk'].H1 = Menu_Ggzera.Scroll.Position['TrollLk'].H1 - Scroll_Add
                    end
                    if IsDisabledControlJustPressed(0, 15) and Scroll_Y < 0.222 and CursorZone(0.710+Drag_X, 0.32+Drag_Y, 0.14, 0.128) then
                        Menu_Ggzera.Scroll.Position['TrollLk'].H1 = Menu_Ggzera.Scroll.Position['TrollLk'].H1 + Scroll_Add
                    end

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Muro na Praça', 0.65+Drag_X, Scroll_Y+Drag_Y, 1) then
                            Muropraca()
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Cidade em Geral ~r~Risco', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                PropPlayer2('\107\116\49\95\108\111\100\95\115\108\111\100\52',player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Rampa de Jetski em Geral ~r~Risco', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                PropPlayer('prop_jetski_ramp_01',player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Rampa de Manobra em Geral ~r~Risco', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                PropPlayer('stt_prop_ramp_adj_loop',player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Jato em Geral ~r~Risco', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                PropPlayer('prop_med_jet_01',player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Derrubar Geral ', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                Derrubar(player)
                            end
                        end                    
                    end Scroll_Y = Scroll_Y + Scroll_Add

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Button('Matar Geral', 0.65+Drag_X, Scroll_Y+Drag_Y) then
                            for k, player in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                                Matar(player)
                            end
                        end
                    end Scroll_Y = Scroll_Y + Scroll_Add + 0.001

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(freecammode,'Freecam ~r~Likizão~w~', 0.65+Drag_X, Scroll_Y+Drag_Y) then freecammode = not freecammode end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofucker,'Audio ~r~Fucker ', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofucker = not audiofucker end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofucker2,'Audio ~r~Fucker ~y~2', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofucker2 = not audiofucker2 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(audiofucker3,'Audio ~r~Fucker ~g~Vento', 0.65+Drag_X, Scroll_Y+Drag_Y) then audiofucker3 = not audiofucker3 end
                    end Scroll_Y = Scroll_Y + Scroll_Add 
                    
                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(delvehs,'Deletar Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then delvehs = not delvehs end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(offmotors,'Desligar Motor dos Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then offmotors = not offmotors end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(bugvehs,'Bugar Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then bugvehs = not bugvehs end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(lancarvehs,'Lançar Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then lancarvehs = not lancarvehs end
                    end Scroll_Y = Scroll_Y + Scroll_Add 

                    if Scroll_Y >= 0.222 and Scroll_Y <= Scroll_Max then 
                        if Checkbox(killenginevehs,'Foder Motor dos Veiculos', 0.65+Drag_X, Scroll_Y+Drag_Y) then killenginevehs = not killenginevehs end
                    end Scroll_Y = Scroll_Y + Scroll_Add 
                end
            end
        end
    end

    while Menu_Ggzera['LoaderEnebled'] do
		_CiTiZeN_.Wait(0)
		local value, label = Binding()
		Menu_Ggzera['OpenKeyV'] = value
		Menu_Ggzera['OpenKeyL'] = label
		break;
	end

    _CiTiZeN_.CreateThread(function() while Menu_Ggzera['FreecamEnebled'] do Wait(0)
            if rapidfire and not Menu_Ggzera['DrawMenu'] then
                DisablePlayerFiring(
                    PlayerPedId(),
                    true
                )
                if IsDisabledControlPressed(0, 24) then
                    local _, weapon =
                        GetCurrentPedWeapon(
                        PlayerPedId()
                    )
                    local wepent =
                        GetCurrentPedWeaponEntityIndex(
                        PlayerPedId()
                    )
                    local camDir = CenterToCoords()
                    local camPos = GetGameplayCamCoord()
                    local launchPos = GetEntityCoords(wepent)
                    local targetPos = camPos + (camDir * 200.0)
        
                    ShootSingleBulletBetweenCoords(
                        launchPos,
                        targetPos,
                        5,
                        1,
                        weapon,
                        PlayerPedId(),
                        true,
                        true,
                        24000.0
                    )
                    ShootSingleBulletBetweenCoords(
                        launchPos,
                        targetPos,
                        5,
                        1,
                        weapon,
                        PlayerPedId(),
                        true,
                        true,
                        24000.0
                    )
                end
            end

            if Ragebt then
                RequestStreamedTextureDict('mpmissmarkers256', 1)
                DrawSprite("mpmissmarkers256","corona_shade",0.5,0.5, Menu_Ggzera['Sliders'].FovRage.value/30.0, Menu_Ggzera['Sliders'].FovRage.value/30.0 * 1.8 ,0.0,0,0,0,90)
                if IsDisabledControlPressed(0, Menu_Ggzera['RageBotKeyV']) then
                    for k, Players in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                    Peds = GetPlayerPed(Players)
                    Posicao = GetEntityCoords(Peds)
                    R = Peds                       
                    local x, y, z = table.unpack(GetEntityCoords(Peds))
                    local _, _x, _y = GetScreenCoordFromWorldCoord(x, y, z)
                    local x1, y1, z1 = table.unpack(GetEntityCoords(Peds))
                    local FOV = Menu_Ggzera['Sliders'].FovRage.value/30.0
                    if Peds ~= PlayerPedId() and IsEntityOnScreen(Peds) then
                        if (_x > 0.5 - FOV / 2 and _x < 0.5 + FOV / 2 and _y > 0.5 - FOV / 2 and _y < 0.5 + FOV / 2) then
                                ShootSingleBulletBetweenCoords(x1, y1, z1+0.02, x1, y1, z1, 60.0, true, GetSelectedPedWeapon(PlayerPedId()), PlayerPedId(), true, false, 2000.0)									
                            end
                        end				
                    end
                end
            end


            if Ragebt2 then
                RequestStreamedTextureDict('mpmissmarkers256', 1)
                DrawSprite("mpmissmarkers256","corona_shade",0.5,0.5, Menu_Ggzera['Sliders'].FovRage2.value/30.0, Menu_Ggzera['Sliders'].FovRage2.value/30.0 * 1.8 ,0.0,0,0,0,90)
                if IsDisabledControlPressed(0, Menu_Ggzera['RageBotKeyV2']) then
                    for k, Players in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                    Peds = GetPlayerPed(Players)
                    Posicao = GetEntityCoords(Peds)
                    R = Peds                       
                    local x, y, z = table.unpack(GetEntityCoords(Peds))
                    local _, _x, _y = GetScreenCoordFromWorldCoord(x, y, z)
                    local x1, y1, z1 = table.unpack(GetEntityCoords(Peds))
                    local FOV = Menu_Ggzera['Sliders'].FovRage2.value/30.0
                    if Peds ~= PlayerPedId() then
                        if (_x > 0.5 - FOV / 2 and _x < 0.5 + FOV / 2 and _y > 0.5 - FOV / 2 and _y < 0.5 + FOV / 2) then
                                ShootSingleBulletBetweenCoords(x1, y1, z1+0.02, x1, y1, z1, 60.0, true, GetSelectedPedWeapon(PlayerPedId()), PlayerPedId(), true, false, 2000.0)									
                            end
                        end				
                    end
                end
            end

            if msveiculos then
                local a, pos = GetPedLastWeaponImpactCoord(PlayerPedId())
                    if a then
                        for vehicle in EnumerateVehicles() do
                        SetVehicleOnGroundProperly(vehicle)
                        NetworkRequestEntityControl(vehicle)
                        SetEntityCoords(vehicle, pos)
                        SetEntityRotation(vehicle, GetGameplayCamRot(2), 2, 1)
                        SetVehicleForwardSpeed(vehicle, 40.0)
                    end
                end
            end

            if msveiculos2 then
                local a, pos = GetPedLastWeaponImpactCoord(PlayerPedId())
                    if a then
                        for vehicle in EnumerateVehicles() do
                        SetVehicleOnGroundProperly(vehicle)
                        NetworkRequestEntityControl(vehicle)
                        SetEntityCoords(vehicle, pos)
                        SetEntityRotation(vehicle, GetGameplayCamRot(2), 2, 1)
                        SetVehicleForwardSpeed(vehicle, 40.0)
                    end
                end
            end

            if msshock then
                local a, Cordenadas = GetPedLastWeaponImpactCoord(PlayerPedId())
                if a then
                    local vehicle = 'tribike'
                    RequestModel(vehicle)
                    local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                    SetEntityVisible(veh2, patobenlindo)
                    Cordenadas2 = GetEntityCoords(veh2)
                    AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 70, 100.0, true, false, 0.0)
                    DeleteEntity(veh2)
                end
            end    

            if msshock2 then
                local a, Cordenadas = GetPedLastWeaponImpactCoord(PlayerPedId())
                if a then
                    local vehicle = 'tribike'
                    RequestModel(vehicle)
                    local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                    SetEntityVisible(veh2, patobenlindo)
                    Cordenadas2 = GetEntityCoords(veh2)
                    AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 70, 100.0, true, false, 0.0)
                    DeleteEntity(veh2)
                end
            end    

            if mssmolotov then
                local a, Cordenadas = GetPedLastWeaponImpactCoord(PlayerPedId())
                if a then
                    local vehicle = 'tribike'
                    RequestModel(vehicle)
                    local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                    SetEntityVisible(veh2, patobenlindo)
                    Cordenadas2 = GetEntityCoords(veh2)
                    AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 3, 100.0, true, false, 0.0)
                    DeleteEntity(veh2)
                end
            end    

            if LSmssmolotov then
                local a, Cordenadas = GetPedLastWeaponImpactCoord(PlayerPedId())
                if a then
                    local vehicle = 'tribike'
                    RequestModel(vehicle)
                    local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                    SetEntityVisible(veh2, patobenlindo)
                    Cordenadas2 = GetEntityCoords(veh2)
                    AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 3, 100.0, true, false, 0.0)
                    DeleteEntity(veh2)
                end
            end    

            if mssexplosiva then
                local a, Cordenadas = GetPedLastWeaponImpactCoord(PlayerPedId())
                if a then
                    local vehicle = 'tribike'
                    RequestModel(vehicle)
                    local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                    SetEntityVisible(veh2, patobenlindo)
                    Cordenadas2 = GetEntityCoords(veh2)
                    AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 7, 100.0, true, false, 0.0)
                    DeleteEntity(veh2)
                end
            end    

            if msHidrante then
                local a, Cordenadas = GetPedLastWeaponImpactCoord(PlayerPedId())
                if a then
                    local vehicle = 'tribike'
                    RequestModel(vehicle)
                    local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                    SetEntityVisible(veh2, patobenlindo)
                    Cordenadas2 = GetEntityCoords(veh2)
                    AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 13, 100.0, true, false, 0.0)
                    DeleteEntity(veh2)
                end
            end    
        
            if espinfo then
                for k, v in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                    local player = GetPlayerPed(v)
                    if Meincluir then
                        er = nil
                    else
                        er = PlayerPedId()
                    end
                    Checkadmin = ''
                    if GetDistanceBetweenCoords(GetEntityCoords(PlayerPedId()), GetEntityCoords(player), true) < Menu_Ggzera['Sliders'].Distancia.value and player ~= er then
                        local playerX, playerY, playerZ = table.unpack(GetEntityCoords(player))
                        local position = GetEntityCoords(player)
                        local xx = Menu_Ggzera['Variaveis'].Frind_Number(string.format("%.2f", playerX))
                        local yy = Menu_Ggzera['Variaveis'].Frind_Number(string.format("%.2f", playerY))
                        local zz = Menu_Ggzera['Variaveis'].Frind_Number(string.format("%.2f", playerZ))
                        local pos = {x = xx, y = yy, z = zz}
                        local _, WeaponHash = GetCurrentPedWeapon(player, 1)
                        local Weapon = GetWeaponNameFromHash(WeaponHash)
                        if Weapon == "UNARMED" then Weapon = "Desarmado" end
                        if arminhas then
                            textweapon = '~s~Arma:~w~ '..Weapon..''
                        else
                            textweapon = ''
                        end
                        local text = '( '..GetPlayerServerId(v)..' | '..GetPlayerName(v)..' )~n~'..Checkadmin..''..textweapon
                        DrawText3D(position.x, position.y, position.z+0.8, text, Espcolor.R, Espcolor.G, Espcolor.B)
                    end
                end
            end

            if espbox then
                for p in EnumeratePeds() do
                    local X, Y = GetActiveScreenResolution()
                    local c = GetEntityCoords(p)
                    if Meincluir then 
                        me = p
                        mr = IsPedAPlayer(p)
                    else
                        mr = p
                        me = p ~= PlayerPedId() 
                    end
                    local d = GetDistanceBetweenCoords(GetFinalRenderedCamCoord(), c.x, c.y, c.z, true) * (1.1 - (0))
                    if IsEntityOnScreen(p) then
                    if d < Menu_Ggzera['Sliders'].Distancia.value then
                    if me and mr and not IsEntityDead(p) and not colorpicker then 
                        SetDrawOrigin(c.x, c.y, c.z, 0)
                        DrawRect(0.0, 0.0, (1075.2/X)/d, (2376/Y)/d, 0, 0, 0, 150)
                    if HasEntityClearLosToEntity(PlayerPedId(), p, 19) then 
                        local r, g, b = Espcolor.R, Espcolor.G, Espcolor.B
                        DrawRect((-537.6/X)/d, 0.0, (3/X),((2379)/Y)/d, 0, 0, 0, 255)
                        DrawRect((537.6/X)/d, 0.0, (3/X),((2379)/Y)/d, 0, 0, 0, 255)
                        DrawRect(0.0, (-1187/Y)/d, ((1078.2)/X)/d, (3/Y), 0, 0, 0, 255)
                        DrawRect(0.0, (1187/Y)/d, ((1078.2)/X)/d, (3/Y), 0, 0, 0, 255)
                        DrawRect((-537.6/X)/d, 0.0, (1/X), (2376/Y)/d, r, g, b, 255)
                        DrawRect((537.6/X)/d, 0.0, (1/X), (2376/Y)/d, r, g, b, 255)
                        DrawRect(0.0, (-1187/Y)/d, (1076.2/X)/d, (1/Y), r, g, b, 255)
                        DrawRect(0.0, (1187/Y)/d, (1076.2/X)/d, (1/Y), r, g, b, 255)
                    else
                        local r, g, b = Espcolor.R, Espcolor.G, Espcolor.B
                        DrawRect((-537.6/X)/d, 0.0, (3/X),((2379)/Y)/d, 0, 0, 0, 255)
                        DrawRect((537.6/X)/d, 0.0, (3/X),((2379)/Y)/d, 0, 0, 0, 255)
                        DrawRect(0.0, (-1187/Y)/d, ((1078.2)/X)/d, (3/Y), 0, 0, 0, 255)
                        DrawRect(0.0, (1187/Y)/d, ((1078.2)/X)/d, (3/Y), 0, 0, 0, 255)
                        DrawRect((-537.6/X)/d, 0.0, (1/X), (2376/Y)/d, r, g, b, 255)
                        DrawRect((537.6/X)/d, 0.0, (1/X), (2376/Y)/d, r, g, b, 255)
                        DrawRect(0.0, (-1187/Y)/d, (1076.2/X)/d, (1/Y), r, g, b, 255)
                        DrawRect(0.0, (1187/Y)/d, (1076.2/X)/d, (1/Y), r, g, b, 255)	
                    end
                else
                    local r, g, b = Espcolor.R, Espcolor.G, Espcolor.B
                    DrawRect((-537.6/X)/d, 0.0, (3/X),((2379)/Y)/d, 0, 0, 0, 255)
                    DrawRect((537.6/X)/d, 0.0, (3/X),((2379)/Y)/d, 0, 0, 0, 255)
                    DrawRect(0.0, (-1187/Y)/d, ((1078.2)/X)/d, (3/Y), 0, 0, 0, 255)
                    DrawRect(0.0, (1187/Y)/d, ((1078.2)/X)/d, (3/Y), 0, 0, 0, 255)
                    DrawRect((-537.6/X)/d, 0.0, (1/X), (2376/Y)/d, r, g, b, 255)
                    DrawRect((537.6/X)/d, 0.0, (1/X), (2376/Y)/d, r, g, b, 255)
                    DrawRect(0.0, (-1187/Y)/d, (1076.2/X)/d, (1/Y), r, g, b, 255)
                    DrawRect(0.0, (1187/Y)/d, (1076.2/X)/d, (1/Y), r, g, b, 255)					
                end
                    ClearDrawOrigin()
                end
                end
            end
        end

            if espesqueleto then
                for k, v in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do
                    local ped = GetPlayerPed(v)
                    local Pped = PlayerPedId()
                    if Meincluir then
                        er = nil
                    else
                        er = PlayerPedId()
                    end
                    if GetDistanceBetweenCoords(GetEntityCoords(PlayerPedId()), GetEntityCoords(ped), true) < Menu_Ggzera['Sliders'].Distancia.value and ped ~= er then
                        DrawLine(GetPedBoneCoords2(ped, 31086, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 39317, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 39317, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 11816, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 11816, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 16335, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 11816, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 46078, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 16335, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 52301, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 46078, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 14201, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 46078, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 14201, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 39317, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 40269, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 39317, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 45509, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 40269, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 28252, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 45509, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 61163, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 28252, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 57005, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                        DrawLine(GetPedBoneCoords2(ped, 61163, 0.0, 0.0, 0.0), GetPedBoneCoords2(ped, 18905, 0.0, 0.0, 0.0), Espcolor.R, Espcolor.G, Espcolor.B, 255)
                    end
                end 
            end

            if esplinhas then
                local Players = GetActivePlayers()
                local playerCoords = GetEntityCoords(PlayerPedId())
                for i = 1, #Players do
                    if i == PlayerId() then i = i + 1 end
                    local targetCoords = GetEntityCoords(GetPlayerPed(Players[i]))
                    DrawLine(playerCoords, targetCoords, 0, 0, 255, 255)
                end
            end

            if t3dway then
                local waypointblip = GetFirstBlipInfoId(8)
                if DoesBlipExist(waypointblip) then
                    local Cordenadas = GetBlipInfoIdCoord(waypointblip)
                    DrawMarker(28, Cordenadas, 0.0, 0.0, 0.0, 0.0, 180.0, 0.0, 1.0, 1.0, 1000.0, 171, 60, 230, 255, true, true, 2, nil, nil, false)
                end
            end

            if blips then
                for k, v in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    local entity = GetPlayerPed(v)
                    local blip = AddBlipForEntity(entity)
                    if not IsEntityVisible(entity) then
                        blipcolor = 75
                    else
                        blipcolor = 0
                    end
                    SetBlipAsFriendly(blip, true)
                    SetBlipSprite(blip, 1)
                    SetBlipColour(blip, blipcolor)
                    SetBlipNameToPlayerName(blip, v)
                    if GetEntityHealth(entity) < 101 then
                        SetBlipSprite(blip, 1)
                        SetBlipColour(blip, blipcolor)
                    end
                end
            elseif not blips then
                for k, v in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    local entity = GetPlayerPed(v)
                    local blip = GetBlipFromEntity(entity)
                    if DoesBlipExist(blip) then
                        RemoveBlip(_CiTiZeN_.PointerValueIntInitialized(blip))
                    end
                end
            end

            if infammo then
                SetPedInfiniteAmmoClip(PlayerPedId(), true)
            else
                SetPedInfiniteAmmoClip(PlayerPedId(), false)
            end

            if infammo2 then
                SetPedInfiniteAmmoClip(PlayerPedId(), true)
            else
                SetPedInfiniteAmmoClip(PlayerPedId(), false)
            end

            if noreload then
                if IsPedShooting(PlayerPedId()) then
                    PedSkipNextReloading(PlayerPedId())
                    MakePedReload(PlayerPedId())
                end
            end

            if noreload2 then
                if IsPedShooting(PlayerPedId()) then
                    PedSkipNextReloading(PlayerPedId())
                    MakePedReload(PlayerPedId())
                end
            end

            if ControleRemoto then
                FreezeEntityPosition(PlayerPedId(), true)
                SetVehicleEngineOn(selVehicle, true, true, true)
                Camera = Camera
                if not Camera ~= nil then
                    Camera = CreateCam("DEFAULT_SCRIPTED_Camera", 1)
                end
                RenderScriptCams(1, 0, 0, 1, 1)
                SetCamActive(Camera, true)
                local Cordenadas = GetEntityCoords(selVehicle)
                SetCamCoord(Camera, Cordenadas.x, Cordenadas.y, Cordenadas.z + 3)
                SetCamRot(cam, GetEntityRotation(selVehicle), 2)
                while DoesCamExist(Camera) do
                    _CiTiZeN_.Wait(0)
                    if not ControleRemoto then
                        SetVehicleEngineOn(selVehicle, false, false, false)
                        DestroyCam(camrc, false)
                        RenderScriptCams(false, false, 0, 1, 0)
                        FreezeEntityPosition(PlayerPedId(), false)
                        SetFocusEntity(PlayerPedId())
                        break
                    end
                    if IsDisabledControlPressed(0, 129) and not IsDisabledControlPressed(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 9, 1)
                    end
                    if IsDisabledControlJustReleased(0, 129) or IsDisabledControlJustReleased(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 6, 2500)
                    end
                    if IsDisabledControlPressed(0, 130) and not IsDisabledControlPressed(0, 129) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 22, 1)
                    end
                    if IsDisabledControlPressed(0, 89) and IsDisabledControlPressed(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 13, 1)
                    end
                    if IsDisabledControlPressed(0, 90) and IsDisabledControlPressed(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 14, 1)
                    end
                    if IsDisabledControlPressed(0, 129) and IsDisabledControlPressed(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 30, 100)
                    end
                    if IsDisabledControlPressed(0, 89) and IsDisabledControlPressed(0, 129) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 7, 1)
                    end
                    if IsDisabledControlPressed(0, 90) and IsDisabledControlPressed(0, 129) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 8, 1)
                    end
                    if IsDisabledControlPressed(0, 89) and not IsDisabledControlPressed(0, 129) and not IsDisabledControlPressed(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 4, 1)
                    end
                    if IsDisabledControlPressed(0, 90) and not IsDisabledControlPressed(0, 129) and not IsDisabledControlPressed(0, 130) then
                        TaskVehicleTempAction(PlayerPedId(), selVehicle, 5, 1)
                    end
                    if hornboost2 then
                        local Vehicle = selVehicle
                        if IsDisabledControlPressed(0, 38) then
                            SetVehicleBoostActive(Vehicle, true)
                            SetVehicleForwardSpeed(Vehicle,GetEntitySpeed(Vehicle) + 2)
                            Timer = GetGameTimer() + 1000
                        end
                    end
                    local x, y, z = table.unpack(GetCamCoord(Camera))
                    AttachCamToEntity(Camera, selVehicle, 0.0, -9.5, 1.8, true)
                    SetFocusArea(GetCamCoord(Camera).x, GetCamCoord(Camera).y, GetCamCoord(Camera).z, 0.0, 0.0, 0.0)
                    SetCamRot(Camera, GetEntityRotation(selVehicle), 2)
                end
            end

            if paracar then
                SetPedCanBeKnockedOffVehicle(PlayerPedId(), true)
            else
                SetPedCanBeKnockedOffVehicle(PlayerPedId(), false)
            end

            if hornboost then
                local Vehicle = GetVehiclePedIsIn(PlayerPedId(), false)
                if IsDisabledControlPressed(0, 38) then
                    SetVehicleBoostActive(Vehicle, true)
                    SetVehicleForwardSpeed(Vehicle,GetEntitySpeed(Vehicle) + 2)
                    Timer = GetGameTimer() + 1000
                end
            end

            if handling then
                if IsPedInAnyVehicle(PlayerPedId(), true) then
                    SetVehicleGravityAmount(GetVehiclePedIsIn(PlayerPedId(), false), 5.0*5)
                end
            else
                if IsPedInAnyVehicle(PlayerPedId(), true) then
                    SetVehicleGravityAmount(GetVehiclePedIsIn(PlayerPedId(), false), 9.8)
                end
            end

            if speedboost then
                SetVehicleEnginePowerMultiplier(GetVehiclePedIsIn(PlayerPedId(), false),Menu_Ggzera['Variaveis'].Math_Abs(20 *Menu_Ggzera['Sliders'].SpeedVeh.value) / 5.0)
            else
                SetVehicleEnginePowerMultiplier(GetVehiclePedIsIn(PlayerPedId(), false),GetEntitySpeed(GetVehiclePedIsIn(PlayerPedId(), false)))
            end
        
            if not Menu_Ggzera['DrawMenu'] then
                if freecammode then
                    if not Menu_Ggzera['DrawMenu'] then
                        local Camera = CreateCam('DEFAULT_SCRIPTED_Camera', 1)
                        RenderScriptCams(true, true, 700, 1, 1)
                        SetCamActive(Camera, true)
                        SetCamCoord(Camera, GetGameplayCamCoord())
                        local CDSRotX = GetGameplayCamRot(2).x
                        local CDSRotY = GetGameplayCamRot(2).y
                        local CDSRotZ = GetGameplayCamRot(2).z
                        while DoesCamExist(Camera) do
                            Wait(0)
                            FreeCamKeys()
                            local FreecamModes = freecam.modes[freecam.mode]
                            local Camera_rot = GetCamRot(Camera, 2)
                            local Cordenadas = GetCamCoord(Camera)
                            local adjustedRotation = {
                                x = (Menu_Ggzera['Variaveis'].Math_Pi / 180) * GetCamRot(Camera, 0).x,
                                y = (Menu_Ggzera['Variaveis'].Math_Pi / 180) * GetCamRot(Camera, 0).y,
                                z = (Menu_Ggzera['Variaveis'].Math_Pi / 180) * GetCamRot(Camera, 0).z
                            }
                            local direction = {
                                x = -Menu_Ggzera['Variaveis'].Math_Sin(adjustedRotation.z) *
                                    Menu_Ggzera['Variaveis'].Math_Abs(Menu_Ggzera['Variaveis'].Math_Cos(adjustedRotation.x)),
                                y = Menu_Ggzera['Variaveis'].Math_Cos(adjustedRotation.z) *
                                    Menu_Ggzera['Variaveis'].Math_Abs(Menu_Ggzera['Variaveis'].Math_Cos(adjustedRotation.x)),
                                z = Menu_Ggzera['Variaveis'].Math_Sin(adjustedRotation.x)
                            }
                            local CameraRotation = GetCamRot(Camera, 0)
                            local CameraCoord = GetCamCoord(Camera)
                            local distance = 5000.0
                            local destination = {
                                x = CameraCoord.x + direction.x * distance,
                                y = CameraCoord.y + direction.y * distance,
                                z = CameraCoord.z + direction.z * distance
                            }
                            local a, b, Cordenadas, d, entity =
                                GetShapeTestResult(
                                StartShapeTestRay(
                                    CameraCoord.x,
                                    CameraCoord.y,
                                    CameraCoord.z,
                                    destination.x,
                                    destination.y,
                                    destination.z,
                                    -1,
                                    -1,
                                    1
                                )
                            )
                            SetCamFov(Camera, 15.0*5)
                            -------------------------------------------------------------------------------------------------------------------------------------------------
                            if not freecammode then
                                DestroyCam(Camera, false)
                                ClearTimecycleModifier()
                                RenderScriptCams(false, true, 700, 1, 0)
                                FreezeEntityPosition(PlayerPedId(), false)
                                SetFocusEntity(PlayerPedId())
                                break
                            end
                            if not Menu_Ggzera['DrawMenu'] then
                                local playerPed = PlayerPedId()
                                local playerRot = GetEntityRotation(playerPed, 2)
                                local rotX = playerRot.x
                                local rotY = playerRot.y
                                local rotZ = playerRot.z
                                CDSRotX = CDSRotX - (GetDisabledControlNormal(1, 2) * 6.0)
                                CDSRotZ = CDSRotZ - (GetDisabledControlNormal(1, 1) * 6.0)
                                if (CDSRotX > 90.0) then
                                    CDSRotX = 90.0
                                elseif (CDSRotX < -90.0) then
                                    CDSRotX = -90.0
                                end
                                if (CDSRotY > 90.0) then
                                    CDSRotY = 90.0
                                elseif (CDSRotY < -90.0) then
                                    CDSRotY = -90.0
                                end
                                if (CDSRotZ > 360.0) then
                                    CDSRotZ = CDSRotZ - 360.0
                                elseif (CDSRotZ < -360.0) then
                                    CDSRotZ = CDSRotZ + 360.0
                                end
                                local x, y, z = table.unpack(GetCamCoord(Camera))
                                local Vector = vector3(x, y, z)
                                local vecX, vecY, vecZ = GetCamMatrix(Camera)
                                local CurrentSpeed = 0.6
                                if IsDisabledControlPressed(1, 36) then
                                    CurrentSpeed = CurrentSpeed / 15
                                end
                                if IsDisabledControlPressed(1, 21) then
                                    CurrentSpeed = CurrentSpeed * 3
                                end
                                if IsDisabledControlPressed(1, 32) then
                                    SetCamCoord(
                                        Camera,
                                        GetCamCoord(Camera) + (RotationToDirection(GetCamRot(Camera, 2)) * (CurrentSpeed))
                                    )
                                elseif IsDisabledControlPressed(1, 33) then
                                    SetCamCoord(
                                        Camera,
                                        GetCamCoord(Camera) - (RotationToDirection(GetCamRot(Camera, 2)) * (CurrentSpeed))
                                    )
                                elseif IsDisabledControlPressed(1, 22) then
                                    SetCamCoord(Camera, x, y, z + (CurrentSpeed))
                                elseif IsDisabledControlPressed(1, 73) then
                                    SetCamCoord(Camera, x, y, z - (CurrentSpeed))
                                elseif IsDisabledControlPressed(1, 34) then
                                    Vector = Vector - vecX * (CurrentSpeed)
                                    SetCamCoord(Camera, Vector, y, z)
                                elseif IsDisabledControlPressed(1, 9) then
                                    Vector = Vector + vecX * (CurrentSpeed)
                                    SetCamCoord(Camera, Vector, y, z)
                                end
                                local cx, cy, cz =
                                    string.format('%.' .. 1 .. 'f', Cordenadas.x),
                                    string.format('%.' .. 1 .. 'f', Cordenadas.y),
                                    string.format('%.' .. 1 .. 'f', Cordenadas.z)
                                local resX, resY = GetActiveScreenResolution()
                                if FreecamModes == 'Olhar em Volta' then
                                    DisableControlAction(0, 32, true) -- W
                                    DisableControlAction(0, 31, true) -- S
                                    DisableControlAction(0, 30, true) -- D
                                    DisableControlAction(0, 34, true) -- A
                                    DisableControlAction(0, 71, true) -- W
                                    DisableControlAction(0, 72, true) -- S
                                    DisableControlAction(0, 63, true) -- D
                                    DisableControlAction(0, 64, true) -- A
                                    if IsDisabledControlJustPressed(0, 69) then
                                        if Cordenadas ~= vector3(0, 0, 0) then
                                        end
                                    end
                                end

                                DrawRect(0.5, 0.5, 0.009, 3/resY, 0, 0, 0, 255)
                                DrawRect(0.5, 0.5, 3/resX, 0.009*GetAspectRatio(), 0, 0, 0, 255)
                                DrawRect(0.5, 0.5, 0.008, 1/resY, 255, 255, 255, 255)
                                DrawRect(0.5, 0.5, 1/resX, 0.008*GetAspectRatio(), 255, 255, 255, 255)

                                if FreecamModes == 'Colocar Veiculos' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(1, 69) then 
                                            for vehicle in EnumerateVehicles() do
                                                SetVehicleOnGroundProperly(vehicle)
                                                NetworkRequestEntityControl(vehicle)
                                                SetEntityCoords(vehicle, Cordenadas)
                                                SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                            end
                                        end
                                    end
                                end

                                if FreecamModes == 'Chuva de Veiculos' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(1, 69) then 
                                            for vehicle in EnumerateVehicles() do
                                                SetVehicleOnGroundProperly(vehicle)
                                                NetworkRequestEntityControl(vehicle)
                                                SetEntityCoords(vehicle, Cordenadas.x,Cordenadas.y,Cordenadas.z+10.0)
                                                SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                            end
                                        end
                                    end
                                end

                                if FreecamModes == 'Teleport' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(1, 69) then 
                                            SetEntityCoords(PlayerPedId(), Cordenadas.x,Cordenadas.y,Cordenadas.z+0.5)
                                            SetEntityRotation(PlayerPedId(), GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                        end
                                    end
                                end

                                if FreecamModes == 'Explosão Azul' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            local vehicle = 'tribike'
                                            RequestModel(vehicle)
                                            local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                                            SetEntityVisible(veh2, patobenlindo)
                                            Cordenadas2 = GetEntityCoords(veh2)
                                            AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 70, 100.0, true, false, 0.0)
                                            DeleteEntity(veh2)
                                        end
                                    end
                                end

                                if FreecamModes == 'Hidrante' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            local vehicle = 'tribike'
                                            RequestModel(vehicle)
                                            local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                                            SetEntityVisible(veh2, patobenlindo)
                                            Cordenadas2 = GetEntityCoords(veh2)
                                            AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 13, 100.0, true, false, 0.0)
                                            DeleteEntity(veh2)
                                        end
                                    end
                                end

                                if FreecamModes == 'Rampa Spawner' then
                                    if Cordenadas ~= vector3(0, 0, 0) then 
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            local smallprops = {"stt_prop_ramp_adj_loop","stt_prop_ramp_multi_loop_rb","stt_prop_ramp_jump_xxl"}
                                            local animalTable = {"a_c_boar"}
                                            local animal = (animalTable[Menu_Ggzera['Variaveis'].Math_Random(#animalTable)])
                                            if not HasModelLoaded(animal) then 
                                                RequestModel(animal)
                                            end 
                                            RequestModel(animal)
                                            ped = CreatePed(3,animal,Cordenadas.x,Cordenadas.y,Cordenadas.z,true,true)
                                            SetEntityVisible(ped,false)
                                            Cordenadas2 = GetEntityCoords(ped)
                                            local Prop = (smallprops[Menu_Ggzera['Variaveis'].Math_Random(#smallprops)])
                                            CreateObjectNoOffset(Prop,Cordenadas2.x,Cordenadas2.y,Cordenadas2.z,true,true,true)
                                            FreezeEntityPosition(Prop, true)
                                            DeleteEntity(ped)
                                        end
                                    end
                                end

                                if FreecamModes == 'Animal Spawner' then
                                    if Cordenadas ~= vector3(0, 0, 0) then 
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            local animalTable = {"a_c_boar","a_c_dolphin","a_c_retriever","a_c_pig","a_c_humpback"}
                                            local animal = (animalTable[Menu_Ggzera['Variaveis'].Math_Random(#animalTable)])
                                            if not HasModelLoaded(GetHashKey(animal)) then 
                                                RequestModel(GetHashKey(animal))
                                            end 
                                            RequestModel(animal)
                                            CreatePed(3,GetHashKey(animal),Cordenadas.x,Cordenadas.y,Cordenadas.z,true,true)
                                        end
                                    end
                                end

                                if FreecamModes == 'Aviao Spawner' then
                                    if Cordenadas ~= vector3(0, 0, 0) then 
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            local wd = {'MilJet','Jet'}
                                            local wa = (wd[Menu_Ggzera['Variaveis'].Math_Random(#wd)])
                                            RequestModel(wa)
                                            while not HasModelLoaded(wa) do
                                                Wait(0)
                                            end
                                            local Vehicle = CreateVehicle(wa, Cordenadas.x, Cordenadas.y, Cordenadas.z, 0.0, true, false)
                                            SetVehicleEngineOn(Vehicle, true, true, true)
                                            SetEntityRotation(Vehicle, GetCamRot(cam, 2), 0.0, 0.0, 0.0, true)
                                        end
                                    end
                                end

                                if FreecamModes == 'Lançar Veiculos' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            for vehicle in EnumerateVehicles() do
                                                SetVehicleOnGroundProperly(vehicle)
                                                NetworkRequestEntityControl(vehicle)
                                                SetEntityCoords(vehicle, Cordenadas)
                                                SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                                SetVehicleForwardSpeed(vehicle, 50.0)
                                            end
                                        end
                                    end
                                end

                                if FreecamModes == 'Chuva de Veiculos' then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                        if IsDisabledControlJustPressed(0, 69) then 
                                            for vehicle in EnumerateVehicles() do
                                                SetVehicleOnGroundProperly(vehicle)
                                                NetworkRequestEntityControl(vehicle)
                                                SetEntityCoords(vehicle, Cordenadas.x, Cordenadas.y, Cordenadas.z+7.0)
                                                SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                            end
                                        end
                                    end
                                end
                                FreeCamKeys()
                                local rX, rY = GetActiveScreenResolution()
                                DrawRectangle(0.5, 0.89, 0.1514, 0.019, 255, 255, 255, 255)
                                DrawRectangle(0.5, 0.89, 0.15, 0.018, 0, 0, 0, 255)
                                SetTextColour(255, 255, 255, 255)
                                DrawText('~r~[~w~Ggzera Menu~r~]~w~ ~s~Freecam Mode: ~w~' ..FreecamModes, 0.428, 0.889,0.33,4,true, false)
                                if IsDisabledControlJustPressed(1, 14) then
                                    freecam.mode = freecam.mode + 1
                                    if freecam.mode > #freecam.modes then
                                        freecam.mode = 1
                                    end
                                end
                                if IsDisabledControlJustPressed(1, 15) then
                                    freecam.mode = freecam.mode - 1
                                    if freecam.mode < 1 then
                                        freecam.mode = #freecam.modes
                                    end
                                end
                                SetFocusPosAndVel(
                                    GetCamCoord(Camera).x,
                                    GetCamCoord(Camera).y,
                                    GetCamCoord(Camera).z,
                                    0.0,
                                    0.0,
                                    0.0
                                )
                                SetCamRot(Camera, CDSRotX, CDSRotY, CDSRotZ, 2)
                                SetCamRot(Camera, CDSRotX, CDSRotY, CDSRotZ, 2)
                            end
                        end
                    end
                end
            end
            if freecammode2 then
                if not Menu_Ggzera['DrawMenu'] then
                    local Camera = CreateCam('DEFAULT_SCRIPTED_Camera', 1)
                    RenderScriptCams(true, true, 700, 1, 1)
                    SetCamActive(Camera, true)
                    SetCamCoord(Camera, GetGameplayCamCoord())
                    local CDSRotX = GetGameplayCamRot(2).x
                    local CDSRotY = GetGameplayCamRot(2).y
                    local CDSRotZ = GetGameplayCamRot(2).z
                    while DoesCamExist(Camera) do
                        Wait(0)
                        FreeCamKeys()
                        local FreecamModes = freecam2.modes2[freecam2.mode2]
                        local Camera_rot = GetCamRot(Camera, 2)
                        local Cordenadas = GetCamCoord(Camera)
                        local adjustedRotation = {x = (Menu_Ggzera['Variaveis'].Math_Pi / 180) * GetCamRot(Camera, 0).x,y = (Menu_Ggzera['Variaveis'].Math_Pi / 180) * GetCamRot(Camera, 0).y,z = (Menu_Ggzera['Variaveis'].Math_Pi / 180) * GetCamRot(Camera, 0).z}
                        local direction = {
                            x = -Menu_Ggzera['Variaveis'].Math_Sin(adjustedRotation.z) *
                                Menu_Ggzera['Variaveis'].Math_Abs(Menu_Ggzera['Variaveis'].Math_Cos(adjustedRotation.x)),
                            y = Menu_Ggzera['Variaveis'].Math_Cos(adjustedRotation.z) *
                                Menu_Ggzera['Variaveis'].Math_Abs(Menu_Ggzera['Variaveis'].Math_Cos(adjustedRotation.x)),
                            z = Menu_Ggzera['Variaveis'].Math_Sin(adjustedRotation.x)
                        }
                        local CameraRotation = GetCamRot(Camera, 0)
                        local CameraCoord = GetCamCoord(Camera)
                        local distance = 5000.0
                        local destination = {
                            x = CameraCoord.x + direction.x * distance,
                            y = CameraCoord.y + direction.y * distance,
                            z = CameraCoord.z + direction.z * distance
                        }
                        local a, b, Cordenadas, d, entity =
                            GetShapeTestResult(
                            StartShapeTestRay(
                                CameraCoord.x,
                                CameraCoord.y,
                                CameraCoord.z,
                                destination.x,
                                destination.y,
                                destination.z,
                                -1,
                                -1,
                                1
                            )
                        )
                        SetCamFov(Camera, 15.0*5)
                        -------------------------------------------------------------------------------------------------------------------------------------------------
                        if not freecammode2 then
                            DestroyCam(Camera, false)
                            ClearTimecycleModifier()
                            RenderScriptCams(false, true, 700, 1, 0)
                            FreezeEntityPosition(PlayerPedId(), false)
                            SetFocusEntity(PlayerPedId())
                            break
                        end
                        if not Menu_Ggzera['DrawMenu'] then
                            local playerPed = PlayerPedId()
                            local playerRot = GetEntityRotation(playerPed, 2)
                            local rotX = playerRot.x
                            local rotY = playerRot.y
                            local rotZ = playerRot.z
                            CDSRotX = CDSRotX - (GetDisabledControlNormal(1, 2) * 6.0)
                            CDSRotZ = CDSRotZ - (GetDisabledControlNormal(1, 1) * 6.0)
                            if (CDSRotX > 90.0) then
                                CDSRotX = 90.0
                            elseif (CDSRotX < -90.0) then
                                CDSRotX = -90.0
                            end
                            if (CDSRotY > 90.0) then
                                CDSRotY = 90.0
                            elseif (CDSRotY < -90.0) then
                                CDSRotY = -90.0
                            end
                            if (CDSRotZ > 360.0) then
                                CDSRotZ = CDSRotZ - 360.0
                            elseif (CDSRotZ < -360.0) then
                                CDSRotZ = CDSRotZ + 360.0
                            end
                            local x, y, z = table.unpack(GetCamCoord(Camera))
                            local Vector = vector3(x, y, z)
                            local vecX, vecY, vecZ = GetCamMatrix(Camera)
                            local CurrentSpeed = 0.6
                            if IsDisabledControlPressed(1, 36) then
                                CurrentSpeed = CurrentSpeed / 15
                            end
                            if IsDisabledControlPressed(1, 21) then
                                CurrentSpeed = CurrentSpeed * 3
                            end
                            if IsDisabledControlPressed(1, 32) then
                                SetCamCoord(
                                    Camera,
                                    GetCamCoord(Camera) + (RotationToDirection(GetCamRot(Camera, 2)) * (CurrentSpeed))
                                )
                            elseif IsDisabledControlPressed(1, 33) then
                                SetCamCoord(
                                    Camera,
                                    GetCamCoord(Camera) - (RotationToDirection(GetCamRot(Camera, 2)) * (CurrentSpeed))
                                )
                            elseif IsDisabledControlPressed(1, 22) then
                                SetCamCoord(Camera, x, y, z + (CurrentSpeed))
                            elseif IsDisabledControlPressed(1, 73) then
                                SetCamCoord(Camera, x, y, z - (CurrentSpeed))
                            elseif IsDisabledControlPressed(1, 34) then
                                Vector = Vector - vecX * (CurrentSpeed)
                                SetCamCoord(Camera, Vector, y, z)
                            elseif IsDisabledControlPressed(1, 9) then
                                Vector = Vector + vecX * (CurrentSpeed)
                                SetCamCoord(Camera, Vector, y, z)
                            end
                            local cx, cy, cz =
                                string.format('%.' .. 1 .. 'f', Cordenadas.x),
                                string.format('%.' .. 1 .. 'f', Cordenadas.y),
                                string.format('%.' .. 1 .. 'f', Cordenadas.z)
                            local resX, resY = GetActiveScreenResolution()
                            if FreecamModes == 'Olhar em Volta' then
                                if IsDisabledControlJustPressed(0, 69) then
                                    if Cordenadas ~= vector3(0, 0, 0) then
                                    end
                                end
                            end

                            DrawRect(0.5, 0.5, 0.009, 3/resY, 0, 0, 0, 255)
                            DrawRect(0.5, 0.5, 3/resX, 0.009*GetAspectRatio(), 0, 0, 0, 255)
                            DrawRect(0.5, 0.5, 0.008, 1/resY, 255, 255, 255, 255)
                            DrawRect(0.5, 0.5, 1/resX, 0.008*GetAspectRatio(), 255, 255, 255, 255)

                            if FreecamModes == 'Colocar Veiculos' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(1, 69) then 
                                        for vehicle in EnumerateVehicles() do
                                            SetVehicleOnGroundProperly(vehicle)
                                            NetworkRequestEntityControl(vehicle)
                                            SetEntityCoords(vehicle, Cordenadas)
                                            SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                        end
                                    end
                                end
                            end

                            if FreecamModes == 'Chuva de Veiculos' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(1, 69) then 
                                        for vehicle in EnumerateVehicles() do
                                            SetVehicleOnGroundProperly(vehicle)
                                            NetworkRequestEntityControl(vehicle)
                                            SetEntityCoords(vehicle, Cordenadas.x,Cordenadas.y,Cordenadas.z+10.0)
                                            SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                        end
                                    end
                                end
                            end

                            if FreecamModes == 'Teleport' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(1, 69) then 
                                        SetEntityCoords(PlayerPedId(), Cordenadas.x,Cordenadas.y,Cordenadas.z+0.5)
                                        SetEntityRotation(PlayerPedId(), GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                    end
                                end
                            end

                            if FreecamModes == 'Explodir' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(0, 69) then 
                                        local vehicle = 'tribike'
                                        RequestModel(vehicle)
                                        local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                                        SetEntityVisible(veh2, patobenlindo)
                                        Cordenadas2 = GetEntityCoords(veh2)
                                        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 9, 100.0, true, false, 0.0)
                                        DeleteEntity(veh2)
                                    end
                                end
                            end

                            if FreecamModes == 'Explosão Azul' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(0, 69) then 
                                        local vehicle = 'tribike'
                                        RequestModel(vehicle)
                                        local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                                        SetEntityVisible(veh2, patobenlindo)
                                        Cordenadas2 = GetEntityCoords(veh2)
                                        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 70, 100.0, true, false, 0.0)
                                        DeleteEntity(veh2)
                                    end
                                end
                            end

                            if FreecamModes == 'Hidrante' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(0, 69) then 
                                        local vehicle = 'tribike'
                                        RequestModel(vehicle)
                                        local veh2 = CreateVehicle((vehicle), Cordenadas.x, Cordenadas.y, Cordenadas.z , 1, 1, 1)
                                        SetEntityVisible(veh2, patobenlindo)
                                        Cordenadas2 = GetEntityCoords(veh2)
                                        AddExplosion(Cordenadas2.x, Cordenadas2.y, Cordenadas2.z, 13, 100.0, true, false, 0.0)
                                        DeleteEntity(veh2)
                                    end
                                end
                            end

                            if FreecamModes == 'Lançar Veiculos' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(0, 69) then 
                                        for vehicle in EnumerateVehicles() do
                                            SetVehicleOnGroundProperly(vehicle)
                                            NetworkRequestEntityControl(vehicle)
                                            SetEntityCoords(vehicle, Cordenadas)
                                            SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                            SetVehicleForwardSpeed(vehicle, 50.0)
                                        end
                                    end
                                end
                            end

                            if FreecamModes == 'Chuva de Veiculos' then
                                if Cordenadas ~= vector3(0, 0, 0) then
                                    if IsDisabledControlJustPressed(0, 69) then 
                                        for vehicle in EnumerateVehicles() do
                                            SetVehicleOnGroundProperly(vehicle)
                                            NetworkRequestEntityControl(vehicle)
                                            SetEntityCoords(vehicle, Cordenadas.x, Cordenadas.y, Cordenadas.z+7.0)
                                            SetEntityRotation(vehicle, GetCamRot(Camera, 2), 0.0, GetCamRot(Camera, 2), 0.0, true)
                                        end
                                    end
                                end
                            end

                            if FreecamModes == 'Cargoplane Spawner' then
                                if Cordenadas ~= vector3(0, 0, 0) then 
                                    if IsDisabledControlJustPressed(0, 69) then 
                                        local wd = {'Cargoplane'}
                                        local wa = (wd[Menu_Ggzera['Variaveis'].Math_Random(#wd)])
                                        RequestModel(wa)
                                        while not HasModelLoaded(wa) do
                                            Wait(0)
                                        end
                                        local Vehicle = CreateVehicle(wa, Cordenadas.x, Cordenadas.y, Cordenadas.z, 0.0, true, false)
                                        SetVehicleEngineOn(Vehicle, true, true, true)
                                        SetEntityRotation(Vehicle, GetCamRot(cam, 2), 0.0, 0.0, 0.0, true)
                                        SetVehicleForwardSpeed(Vehicle, 1.0)
                                    end
                                end
                            end

                            FreeCamKeys()
                            DrawRectangle(0.5, 0.89, 0.1524, 0.019, 255, 255, 255, 255)
                            DrawRectangle(0.5, 0.89, 0.151, 0.018, 0, 0, 0, 255)
                            SetTextColour(255, 255, 255, 255)
                            DrawText('~r~[~w~Ggzera Menu~r~]~w~ ~s~Freecam Mode: ~w~' ..FreecamModes, 0.428, 0.889,0.33,4,true, false)
                            if IsDisabledControlJustPressed(1, 14) then
                                freecam2.mode2 = freecam2.mode2 + 1
                                if freecam2.mode2 > #freecam2.modes2 then
                                    freecam2.mode2 = 1
                                end
                            end
                            if IsDisabledControlJustPressed(1, 15) then
                                freecam2.mode2 = freecam2.mode2 - 1
                                if freecam2.mode2 < 1 then
                                    freecam2.mode2 = #freecam2.modes2
                                end
                            end
                            SetFocusPosAndVel(GetCamCoord(Camera).x,GetCamCoord(Camera).y,GetCamCoord(Camera).z,0.0,0.0,0.0)
                            SetCamRot(Camera, CDSRotX, CDSRotY, CDSRotZ, 2)
                            SetCamRot(Camera, CDSRotX, CDSRotY, CDSRotZ, 2)
                        end
                    end
                end
            end
        end
    end)

    _CiTiZeN_.CreateThread(function() while Menu_Ggzera['MenuEnebled'] do Wait(0)
            if punch then
                Bypass = nil
                Tratamentok()
                if Bypas then
                    EnableAllControlActions(Bypass)     
                end
                Bypass = {Weapon = {'Weapon_Unarmed'}}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           SetWeaponDamageModifierThisFrame('weapon_unarmed', 12.5)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       
            end

            if DelPlayerVeh then
                vehicle = GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true)
                if DoesEntityExist(vehicle) then
                    NetworkRequestEntityControl(vehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    DeleteVehicle(vehicle)
                    DeleteEntity(vehicle)
                end
            end

            if DelPlayerVeh2 then
                vehicle = GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true)
                if DoesEntityExist(vehicle) then
                    NetworkRequestEntityControl(vehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    DeleteVehicle(vehicle)
                    DeleteEntity(vehicle)
                end
            end

            if BugPlayerVeh then
                vehicle = GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true)
                if DoesEntityExist(vehicle) then
                    NetworkRequestEntityControl(vehicle)
                    local Cordenadas = GetEntityCoords(PlayerPedId())
                    ApplyForceToEntity(vehicle, 3, Cordenadas, 0.0, 0.0, 0.0, 0, 0, 1, 1, 0, 1)
                end
            end

            if BugPlayerVeh2 then
                vehicle = GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true)
                if DoesEntityExist(vehicle) then
                    NetworkRequestEntityControl(vehicle)
                    local Cordenadas = GetEntityCoords(PlayerPedId())
                    ApplyForceToEntity(vehicle, 3, Cordenadas, 0.0, 0.0, 0.0, 0, 0, 1, 1, 0, 1)
                end
            end

            if DeleteSelVehicle then
                vehicle = selVehicle
                if DoesEntityExist(vehicle) then
                    NetworkRequestEntityControl(vehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    DeleteVehicle(vehicle)
                    DeleteEntity(vehicle)
                end
            end

            if DeleteSelVehicle2 then
                vehicle = selVehicle
                if DoesEntityExist(vehicle) then
                    NetworkRequestEntityControl(vehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    DeleteVehicle(vehicle)
                    DeleteEntity(vehicle)
                end
            end

            if KillengineSelVehicle then
                if selVehicle then
                    NetworkRequestEntityControl(selVehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    SetVehicleEngineOn(selVehicle, 1, 1)
                    SetVehicleEngineHealth(selVehicle,-999.90002441406) 
                end
            end

            if bugvehs then
                for vehicle in EnumerateVehicles() do
                    if DoesEntityExist(vehicle) then
                        NetworkRequestEntityControl(vehicle)
                        local Cordenadas = GetEntityCoords(PlayerPedId())
                        ApplyForceToEntity(vehicle, 3, Cordenadas, 0.0, 0.0, 0.0, 0, 0, 1, 1, 0, 1)
                    end
                end
            end

            if Vehiclehim then
                cordenadas = GetEntityCoords(GetPlayerPed(SelPlayer))
                for vehicle in EnumerateVehicles() do	
                    NetworkRequestEntityControl(vehicle)
                    SetEntityCoords(vehicle,cordenadas.x,cordenadas.y,cordenadas.z) 
                    SetEntityCoordsNoOffset(vehicle,cordenadas.x,cordenadas.y,cordenadas.z, true, true, true)
                end
            end

            if Vehiclehim2 then
                cordenadas = GetEntityCoords(GetPlayerPed(SelPlayer))
                vehicle = selVehicle
                NetworkRequestEntityControl(vehicle)
                SetEntityCoords(vehicle,cordenadas.x,cordenadas.y,cordenadas.z) 
                SetEntityCoordsNoOffset(vehicle,cordenadas.x,cordenadas.y,cordenadas.z, true, true, true)
            end

            if bugvehs2 then
                for vehicle in EnumerateVehicles() do
                    if DoesEntityExist(vehicle) then
                        NetworkRequestEntityControl(vehicle)
                        local Cordenadas = GetEntityCoords(PlayerPedId())
                        ApplyForceToEntity(vehicle, 3, Cordenadas, 0.0, 0.0, 0.0, 0, 0, 1, 1, 0, 1)
                    end
                end
            end

            if lancarvehs then
                for vehicle in EnumerateVehicles() do
                    if DoesEntityExist(vehicle) then
                        NetworkRequestEntityControl(vehicle)
                        local Cordenadas = GetEntityCoords(PlayerPedId())
                        ApplyForceToEntity(vehicle, 3, Cordenadas, 0.0, 0.0, 0.0, 0, 0, 1, 1, 0, 1)
                    end
                end
            end
            
            if lancarvehs2 then
                for vehicle in EnumerateVehicles() do
                    if DoesEntityExist(vehicle) then
                        NetworkRequestEntityControl(vehicle)
                        local Cordenadas = GetEntityCoords(PlayerPedId())
                        ApplyForceToEntity(vehicle, 3, Cordenadas, 0.0, 0.0, 0.0, 0, 0, 1, 1, 0, 1)
                    end
                end
            end
            
            if killenginevehs then
                for vehicle in EnumerateVehicles() do
                    if DoesEntityExist(vehicle) then
                        NetworkRequestEntityControl(vehicle)
                        SetVehicleEngineOn(vehicle, 1, 1)
                        SetVehicleEngineOn(vehicle, 1, 1)
                        SetVehicleEngineHealth(vehicle,-999.90002441406) 
                    end
                end
            end

            if killenginevehs2 then
                for vehicle in EnumerateVehicles() do
                    if DoesEntityExist(vehicle) then
                        NetworkRequestEntityControl(vehicle)
                        SetVehicleEngineOn(vehicle, 1, 1)
                        SetVehicleEngineOn(vehicle, 1, 1)
                        SetVehicleEngineHealth(vehicle,-999.90002441406) 
                    end
                end
            end

            if delprops then
                for objects in EnumerateObjects() do
                    DeleteObjects(objects)
                end
            end

            if audiofucker4 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySoundFromCoord(-1, 'DESPAWN', GetEntityCoords(GetPlayerPed(i)), 'BARRY_01_SOUNDSET', true, 10.0, true)
                end
            end

            if audiofucker then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Enemy_Capture_Start', 'GTAO_Magnate_Yacht_Attack_Soundset', true)
                    PlaySound(-1, 'Enemy_Deliver', 'HUD_FRONTEND_MP_COLLECTABLE_SOUNDS', true)
                    PlaySound(-1, 'Enemy_Capture_Start', 'GTAO_Magnate_Yacht_Attack_Soundset', true)
                    PlaySound(-1, 'Change_Station_Loud', 'Radio_Soundset', true)
                    PlaySound(-1, 'GOLF_EAGLE', 'HUD_AWARDS', true)
                    PlaySound(-1, 'Blip_Pickup', 'GTAO_Magnate_Boss_Modes_Soundset', true)
                end
            end

            if audiofucker2 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Bomb_Disarmed', 'GTAO_Speed_Convoy_Soundset', true)
                    PlaySound(-1, 'Change_Station_Loud', 'Radio_Soundset', true)
                    PlaySound(-1, 'GOLF_EAGLE', 'HUD_AWARDS', true) 
                    PlaySound(-1, 'Blip_Pickup', 'GTAO_Magnate_Boss_Modes_Soundset', true)
                end
            end

            if audiofucker3 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Whoosh_1s_L_to_R', 'MP_LOBBY_SOUNDS', true)
                end
            end

            if audiofuckermq4 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySoundFromCoord(-1, 'DESPAWN', GetEntityCoords(GetPlayerPed(i)), 'BARRY_01_SOUNDSET', true, 10.0, true)
                end
            end

            if audiofuckermq5 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Bomb_Disarmed', 'GTAO_Speed_Convoy_Soundset', true)
                end
            end

            if audiofuckermq then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Enemy_Capture_Start', 'GTAO_Magnate_Yacht_Attack_Soundset', true)
                    PlaySound(-1, 'Enemy_Deliver', 'HUD_FRONTEND_MP_COLLECTABLE_SOUNDS', true)
                    PlaySound(-1, 'Enemy_Capture_Start', 'GTAO_Magnate_Yacht_Attack_Soundset', true)
                    PlaySound(-1, 'Change_Station_Loud', 'Radio_Soundset', true)
                    PlaySound(-1, 'GOLF_EAGLE', 'HUD_AWARDS', true)
                    PlaySound(-1, 'Blip_Pickup', 'GTAO_Magnate_Boss_Modes_Soundset', true)

                    PlaySoundFromCoord(-1, 'Enemy_Capture_Start', GetEntityCoords(GetPlayerPed(i)), 'GTAO_Magnate_Yacht_Attack_Soundset', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'Enemy_Deliver', GetEntityCoords(GetPlayerPed(i)), 'HUD_FRONTEND_MP_COLLECTABLE_SOUNDS', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'Enemy_Capture_Start', GetEntityCoords(GetPlayerPed(i)), 'GTAO_Magnate_Yacht_Attack_Soundset', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'Blip_Pickup', GetEntityCoords(GetPlayerPed(i)), 'GTAO_Magnate_Boss_Modes_Soundset', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'GOLF_EAGLE', GetEntityCoords(GetPlayerPed(i)), 'HUD_AWARDS', true, 100.0, true)
                end
            end

            if audiofuckermq2 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Bomb_Disarmed', 'GTAO_Speed_Convoy_Soundset', true)
                    PlaySound(-1, 'Change_Station_Loud', 'Radio_Soundset', true)
                    PlaySound(-1, 'GOLF_EAGLE', 'HUD_AWARDS', true) 
                    PlaySound(-1, 'Blip_Pickup', 'GTAO_Magnate_Boss_Modes_Soundset', true)

                    PlaySoundFromCoord(-1, 'Bomb_Disarmed', GetEntityCoords(GetPlayerPed(i)), 'GTAO_Speed_Convoy_Soundset', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'Change_Station_Loud', GetEntityCoords(GetPlayerPed(i)), 'Radio_Soundset', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'GOLF_EAGLE', GetEntityCoords(GetPlayerPed(i)), 'HUD_AWARDS', true, 100.0, true)
                    PlaySoundFromCoord(-1, 'Blip_Pickup', GetEntityCoords(GetPlayerPed(i)), 'GTAO_Magnate_Boss_Modes_Soundset', true, 100.0, true)
                end
            end

            if audiofuckermq3 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Whoosh_1s_L_to_R', 'MP_LOBBY_SOUNDS', true)
                    PlaySoundFromCoord(-1, 'Whoosh_1s_L_to_R', GetEntityCoords(GetPlayerPed(i)), 'MP_LOBBY_SOUNDS', true, 100.0, true)
                end
            end

            if audiofuckermq5 then
                for k, i in Menu_Ggzera['Variaveis'].Pares(GetActivePlayers()) do 
                    PlaySound(-1, 'Bomb_Disarmed', 'GTAO_Speed_Convoy_Soundset', true)
                    PlaySoundFromCoord(-1, 'Bomb_Disarmed', GetEntityCoords(GetPlayerPed(i)), 'GTAO_Speed_Convoy_Soundset', true, 100.0, true)
                end
            end

            if delvehs then
                for vehicle in EnumerateVehicles() do
                    NetworkRequestControlOfEntity(vehicle)
                    NetworkRequestEntityControl(vehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    DeleteVehicle(vehicle)
                    DeleteEntity(vehicle)
                end
            end

            if delvehs2 then
                for vehicle in EnumerateVehicles() do
                    NetworkRequestControlOfEntity(vehicle)
                    NetworkRequestEntityControl(vehicle)
                    SetEntityAsMissionEntity(vehicle, true, true)
                    DeleteVehicle(vehicle)
                    DeleteEntity(vehicle)
                end
            end

            if punch2 then
                Bypass = nil
                Tratamentok()
                if Bypas then
                    EnableAllControlActions(Bypass)     
                end
                Bypass = {Weapon = {'Weapon_Unarmed'}}                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     SetWeaponDamageModifierThisFrame('weapon_unarmed', 600.5)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      
            end

            if staminainf then
                ResetPlayerStamina(PlayerPedId())
            end

            if Invisivel then
                SetEntityAlpha(GetVehiclePedIsIn(PlayerPedId()), 0)
                SetEntityAlpha(PlayerPedId(), 0)
            else
                ResetEntityAlpha(PlayerPedId())
                ResetEntityAlpha(GetVehiclePedIsIn(PlayerPedId()))
            end

            if Tratamento then 
                life = GetEntityHealth(PlayerPedId()) 
                if life < 399 and (JumpDelay or 0) < GetGameTimer() then 
                    JumpDelay = GetGameTimer() + 150
                    SetEntityHealth(PlayerPedId(), life+1)
                end
            end

            if Speed then
                if IsDisabledControlPressed(0, 21) then
                    if IsPedRagdoll(PlayerPedId()) then
                    else
                        SetEntityVelocity(PlayerPedId(), GetOffsetFromEntityInWorldCoords(PlayerPedId(), 0.0, 15.0*2, GetEntityVelocity(PlayerPedId())[3]) - GetEntityCoords(PlayerPedId()))
                    end
                end
            end

            if obsplayer2 then
                _CiTiZeN_.CreateThread(function()
                    local Camerat = Camerat
                    if not Camerat ~= nil then
                        Camerat = CreateCam("DEFAULT_SCRIPTED_Camera", 1)
                    end
                    RenderScriptCams(1, 0, 0, 1, 1)
                    SetCamActive(Camerat, true)
                    local Cordenadas = GetEntityCoords(GetPlayerPed(SelPlayer))
                    SetCamCoord(Camerat, Cordenadas.x, Cordenadas.y, Cordenadas.z + 3)
                    while DoesCamExist(Camerat) do
                        _CiTiZeN_.Wait(0)
                        if not obsplayer then
                            DestroyCam(Camerat, false)
                            ClearTimecycleModifier()
                            RenderScriptCams(false, false, 0, 1, 0)
                            SetFocusEntity(PlayerPedId())
                            break
                        end
                        local playerPed = GetPlayerPed(SelPlayer)
                        local playerRot = GetEntityRotation(playerPed, 2)
                        local x, y, z = table.unpack(GetCamCoord(Camerat))
                        local x2, y2, z2 = table.unpack(GetPedBoneCoords(playerPed, 31086, 0.0, 0.0, 0.0))
                        SetCamCoord(Camerat, x2+1.5, y2+1.5, z2+0.5)
                        if not Displayed then
                            SetFocusArea(GetCamCoord(Camerat).x, GetCamCoord(Camerat).y, GetCamCoord(Camerat).z,0.0,0.0,0.0)
                            SetCamRot(Camerat, GetGameplayCamRot(2), 2)
                        end
                    end
                end)
            end

            if obsplayer then
                _CiTiZeN_.CreateThread(function()
                    local Camerat = Camerat
                    if not Camerat ~= nil then
                        Camerat = CreateCam("DEFAULT_SCRIPTED_Camera", 1)
                    end
                    RenderScriptCams(1, 0, 0, 1, 1)
                    SetCamActive(Camerat, true)
                    local Cordenadas = GetEntityCoords(GetPlayerPed(SelPlayer))
                    SetCamCoord(Camerat, Cordenadas.x, Cordenadas.y, Cordenadas.z + 3)
                    while DoesCamExist(Camerat) do
                        _CiTiZeN_.Wait(0)
                        if not obsplayer then
                            DestroyCam(Camerat, false)
                            ClearTimecycleModifier()
                            RenderScriptCams(false, false, 0, 1, 0)
                            SetFocusEntity(PlayerPedId())
                            break
                        end
                        local playerPed = GetPlayerPed(SelPlayer)
                        local playerRot = GetEntityRotation(playerPed, 2)
                        local x, y, z = table.unpack(GetCamCoord(Camerat))
                        local x2, y2, z2 = table.unpack(GetPedBoneCoords(playerPed, 31086, 0.0, 0.0, 0.0))
                        SetCamCoord(Camerat, x2+1.5, y2+1.5, z2+0.5)
                        if not Displayed then
                            SetFocusArea(GetCamCoord(Camerat).x, GetCamCoord(Camerat).y, GetCamCoord(Camerat).z,0.0,0.0,0.0)
                            SetCamRot(Camerat, GetGameplayCamRot(2), 2)
                        end
                    end
                end)
            end

            if pulosapo then
                SetPedCanRagdoll(PlayerPedId(), false)
                if IsDisabledControlJustPressed(0, 22) then
                    ApplyForceToEntity(PlayerPedId(), 3, 0.0, 0.0, 30.0, 0.0, 0.0, 0.0, 0, 0, 0, 1, 1, 1)
                end
                SetBeastModeActive(PlayerId())
            end

            if superpulo then
                SetPedCanRagdoll(PlayerPedId(), false)
                if IsDisabledControlJustPressed(0, 22) then
                    ApplyForceToEntity(PlayerPedId(), 3, 0.0, 0.0, 30.0, 0.0, 0.0, 0.0, 0, 0, 0, 1, 1, 1)
                end
            end
    
            if Bunnyhop then
                if IsDisabledControlPressed(1, 22) and (JumpDelay or 0) < GetGameTimer() then 
                    JumpDelay = GetGameTimer() + 133
                    TaskJump(PlayerPedId(), true)
                end
            end
    
            if scanti then
                SetEntityProofs(PlayerPedId(), 1, 0, 0, 0, 1, 0, 0, 0)
                SetEntityProofs(PlayerPedId(), 0, 0, 0, 0, 1, 0, 0, 0)
            else
                SetEntityProofs(PlayerPedId(), 0, 0, 0, 0, 0, 0, 0, 0)
            end

            if dmanti then
                SetEntityCanBeDamaged(PlayerPedId(), not dmanti)
            end

            if antitaze then
                SetPedMinGroundTimeForStungun(PlayerPedId(), 0)
            elseif not antitaze then
                SetPedMinGroundTimeForStungun(PlayerPedId(), 3600)
            end
            
            if Noclip then
                local PedCD = GetEntityCoords(PlayerPedId())
                local SpeedNoclip = Menu_Ggzera['Sliders'].Noclip.value/8
                local PlayerCam = GetGameplayCamRot(0)
                local vehicleecheck = IsPedInAnyVehicle(PlayerPedId(), 0)
                if NoclipInv then
                    SetEntityAlpha(GetVehiclePedIsIn(PlayerPedId()), 0)
                    SetEntityAlpha(PlayerPedId(), 0)
                else
                    ResetEntityAlpha(PlayerPedId())
                    ResetEntityAlpha(GetVehiclePedIsIn(PlayerPedId()))
                end
                if not vehicleecheck then
                    if IsDisabledControlPressed(0, 21) then
                        SpeedNoclip = SpeedNoclip * 3
                    elseif IsDisabledControlPressed(0, 36) then
                        SpeedNoclip = SpeedNoclip / 3
                    end
                    local Frente, Certo = RotationCam(PlayerCam) * vector3(0.0, 1.0, 0.0), RotationCam(PlayerCam) * vector3(1.0, 0.0, 0.0)
                    if IsDisabledControlPressed(0, 32) then
                        PedCD = PedCD + Frente * SpeedNoclip
                    end
                    if IsDisabledControlPressed(0, 33) then
                        PedCD = PedCD + Frente * - SpeedNoclip
                    end
                    if IsDisabledControlPressed(0, 30) then
                        PedCD = PedCD + Certo * SpeedNoclip
                    end
                    if IsDisabledControlPressed(0, 34) then
                        PedCD = PedCD + Certo * - SpeedNoclip
                    end
                    SetEntityCoordsNoOffset(PlayerPedId(), PedCD.x, PedCD.y, PedCD.z, true, true, true)
                    local Cordenadas = vector3(PlayerCam.x - GetDisabledControlNormal(0, 2) * 10,
                    PlayerCam.y, PlayerCam.z - GetDisabledControlNormal(0, 1) * 10)
                    SetEntityRotation(PlayerPedId(), Cordenadas, 0)
                else
                    local VehicleCD = GetEntityCoords(GetVehiclePedIsIn(PlayerPedId()))
                    local SpeedNoclip = Menu_Ggzera['Sliders'].Noclip.value/8
                    local PlayerCam = GetGameplayCamRot(0)
                    DisableControlAction(0, 85, true)
                    DisableControlAction(0, 38, true)
                    if IsDisabledControlPressed(0, 21) then
                        SpeedNoclip = SpeedNoclip * 3
                    elseif IsDisabledControlPressed(0, 36) then
                        SpeedNoclip = SpeedNoclip / 3
                    end
                    local Frente, Certo = RotationCam(PlayerCam) * vector3(0.0, 1.0, 0.0), RotationCam(PlayerCam) * vector3(1.0, 0.0, 0.0)
                    if IsDisabledControlPressed(0, 32) then 
                        VehicleCD = VehicleCD + Frente * SpeedNoclip 
                    end
                    if IsDisabledControlPressed(0, 33) then 
                        VehicleCD = VehicleCD + Frente * - SpeedNoclip 
                    end
                    if IsDisabledControlPressed(0, 30) then 
                        VehicleCD = VehicleCD + Certo * SpeedNoclip 
                    end
                    if IsDisabledControlPressed(0, 34) then 
                        VehicleCD = VehicleCD + Certo * - SpeedNoclip 
                    end
                    SetEntityCoordsNoOffset(GetVehiclePedIsIn(PlayerPedId()), VehicleCD.x, VehicleCD.y, VehicleCD.z, true, true, true)
                    local Cordenadas = vector3(PlayerCam.x -GetDisabledControlNormal(0, 2) * 10, PlayerCam.y,
                    PlayerCam.z - GetDisabledControlNormal(0, 1) * 10)
                    SetEntityRotation(GetVehiclePedIsIn(PlayerPedId()), Cordenadas, 0)
                end
            end

            if IsControlJustPressed(1, Menu_Ggzera['NoclipKeyV']) then
                Noclip = not Noclip
            end

            if Desligarmotor then
                SetVehicleEngineOn(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true), 0, 0)
            else
                SetVehicleEngineOn(GetVehiclePedIsIn(GetPlayerPed(SelPlayer), true), 1, 1)
            end

            if offmotors then
                for vehicles in EnumerateVehicles() do 
                    SetVehicleEngineOn(vehicles, 0, 0)
                end
            end

            if offmotors2 then
                for vehicles in EnumerateVehicles() do 
                    SetVehicleEngineOn(vehicles, 0, 0)
                end
            end

            if IsControlJustPressed(1, 288) and Menu_Ggzera['DrawMenu'] then
                Menu_Ggzera.Tab['Jogador'] = true
                Menu_Ggzera.Tab['Veiculos'] = true
                Menu_Ggzera.Tab['Veiculos'] = true
                Menu_Ggzera.Tab['Online'] = true
                Menu_Ggzera.Tab['Config'] = true
                if liki then
                    Menu_Ggzera.Tab['SpArmasLk'] = true
                    Menu_Ggzera.Tab['JogadorLk'] = true
                    Menu_Ggzera.Tab['TrollLk'] = true
                else
                end
                if mqcu then
                    Menu_Ggzera.Tab['SpArmas'] = true
                    Menu_Ggzera.Tab['JogadorMQCU'] = true
                    Menu_Ggzera.Tab['TrollMQCU'] = true
                else
                end
            end
            if IsControlJustPressed(1, Menu_Ggzera['OpenKeyV']) then
                Menu_Ggzera['DrawMenu'] = not Menu_Ggzera['DrawMenu']
                Menu_Ggzera['DrawLoader'] = not Menu_Ggzera['DrawLoader']
            end
            if Menu_Ggzera['DrawMenu'] then
                Menu()
                Cursor(cursortext, 0.003, 0.35, 10, 255, 255, 255)
            end
        end
    end)

    _CiTiZeN_.CreateThread(function() while Menu_Ggzera['LoaderEnebled'] do Wait(0)
            if Menu_Ggzera['DrawLoader'] then
                Loader(true)
                Cursor(cursortext, 0.003, 0.35, 10, 255, 255, 255)
            else
                Loader(false)
            end
        end
    end)
end)
