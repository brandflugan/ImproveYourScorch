# ImproveYourScorch
Fire Invulnerability / Scorch timer with stack counter and animation for WeaAuras Classic

## Import the following Lua Table:
```lua
{
    ["authorOptions"] = {
    },
    ["yOffset"] = -121.46722412109,
    ["anchorPoint"] = "CENTER",
    ["cooldownSwipe"] = true,
    ["cooldownEdge"] = false,
    ["actions"] = {
        ["start"] = {
        },
        ["init"] = {
        },
        ["finish"] = {
        },
    },
    ["triggers"] = {
        [1] = {
            ["trigger"] = {
                ["rem"] = "30",
                ["useStacks"] = false,
                ["auranames"] = {
                    [1] = "Fire Vulnerability",
                },
                ["totalOperator"] = ">",
                ["unit"] = "target",
                ["stacks"] = "5",
                ["debuffType"] = "HARMFUL",
                ["showClones"] = true,
                ["useName"] = true,
                ["stacksOperator"] = "==",
                ["subeventSuffix"] = "_CAST_START",
                ["useTotal"] = false,
                ["event"] = "Health",
                ["spellIds"] = {
                },
                ["total"] = "6",
                ["names"] = {
                },
                ["type"] = "aura2",
                ["subeventPrefix"] = "SPELL",
                ["useRem"] = false,
            },
            ["untrigger"] = {
            },
        },
        ["activeTriggerMode"] = -10,
    },
    ["internalVersion"] = 37,
    ["keepAspectRatio"] = false,
    ["animation"] = {
        ["start"] = {
            ["type"] = "none",
            ["easeStrength"] = 3,
            ["duration_type"] = "seconds",
            ["easeType"] = "none",
        },
        ["main"] = {
            ["colorR"] = 1,
            ["scalex"] = 1,
            ["colorB"] = 1,
            ["colorG"] = 1,
            ["type"] = "custom",
            ["easeType"] = "easeOutIn",
            ["duration"] = "1",
            ["use_color"] = true,
            ["alpha"] = 0,
            ["duration_type"] = "seconds",
            ["y"] = 0,
            ["x"] = 0,
            ["colorType"] = "pulseHSV",
            ["colorA"] = 1,
            ["colorFunc"] = "    function(progress, r1, g1, b1, a1, r2, g2, b2, a2)\\n      local angle = (progress * 2 * math.pi) - (math.pi / 2)\\n      local newProgress = ((math.sin(angle) + 1)/2);\\n      return WeakAuras.GetHSVTransition(newProgress, r1, g1, b1, a1, r2, g2, b2, a2)\\n    end\\n  ",
            ["easeStrength"] = 3,
            ["rotate"] = 0,
            ["scaley"] = 1,
        },
        ["finish"] = {
            ["type"] = "none",
            ["easeStrength"] = 3,
            ["duration_type"] = "seconds",
            ["easeType"] = "none",
        },
    },
    ["desaturate"] = false,
    ["subRegions"] = {
        [1] = {
            ["text_shadowXOffset"] = 0,
            ["text_text_format_s_format"] = "none",
            ["text_text"] = "%s",
            ["text_shadowColor"] = {
                [1] = 0,
                [2] = 0,
                [3] = 0,
                [4] = 1,
            },
            ["text_selfPoint"] = "AUTO",
            ["text_automaticWidth"] = "Auto",
            ["text_fixedWidth"] = 64,
            ["anchorYOffset"] = 0,
            ["text_justify"] = "CENTER",
            ["rotateText"] = "NONE",
            ["type"] = "subtext",
            ["text_color"] = {
                [1] = 1,
                [2] = 1,
                [3] = 1,
                [4] = 1,
            },
            ["text_font"] = "Friz Quadrata TT",
            ["text_shadowYOffset"] = 0,
            ["text_wordWrap"] = "WordWrap",
            ["text_visible"] = true,
            ["text_anchorPoint"] = "INNER_BOTTOMRIGHT",
            ["text_fontSize"] = 12,
            ["anchorXOffset"] = 0,
            ["text_fontType"] = "OUTLINE",
        },
        [2] = {
            ["glowFrequency"] = 0.25,
            ["type"] = "subglow",
            ["useGlowColor"] = false,
            ["glowType"] = "buttonOverlay",
            ["glowLength"] = 10,
            ["glowYOffset"] = 0,
            ["glowColor"] = {
                [1] = 1,
                [2] = 1,
                [3] = 1,
                [4] = 1,
            },
            ["glowXOffset"] = 0,
            ["glow"] = false,
            ["glowScale"] = 1,
            ["glowThickness"] = 1,
            ["glowLines"] = 8,
            ["glowBorder"] = false,
        },
    },
    ["height"] = 63.999355316162,
    ["load"] = {
        ["spec"] = {
            ["multi"] = {
            },
        },
        ["class"] = {
            ["multi"] = {
            },
        },
        ["size"] = {
            ["multi"] = {
            },
        },
    },
    ["regionType"] = "icon",
    ["desc"] = "Fire Invulnerability / Scorch timer with stack counter and animation for WeaAuras Classic\\n\\nBy Brandflugan @ github",
    ["selfPoint"] = "CENTER",
    ["width"] = 63.999980926514,
    ["frameStrata"] = 1,
    ["zoom"] = 0,
    ["auto"] = true,
    ["xOffset"] = 0.44482421875,
    ["id"] = "Improve Your Scorch",
    ["color"] = {
        [1] = 1,
        [2] = 1,
        [3] = 1,
        [4] = 1,
    },
    ["alpha"] = 1,
    ["anchorFrameType"] = "SCREEN",
    ["icon"] = true,
    ["uid"] = "1LCk0hflyty",
    ["inverse"] = false,
    ["cooldownTextDisabled"] = false,
    ["conditions"] = {
        [1] = {
            ["check"] = {
                ["trigger"] = 1,
                ["variable"] = "expirationTime",
                ["op"] = "<=",
                ["value"] = "6",
            },
            ["changes"] = {
                [1] = {
                    ["value"] = true,
                    ["property"] = "sub.2.glow",
                },
            },
        },
        [2] = {
            ["check"] = {
                ["trigger"] = 1,
                ["op"] = "<",
                ["value"] = "5",
                ["variable"] = "totalStacks",
            },
            ["changes"] = {
                [1] = {
                    ["value"] = true,
                    ["property"] = "desaturate",
                },
            },
        },
    },
    ["cooldown"] = true,
    ["config"] = {
    },
}
```
