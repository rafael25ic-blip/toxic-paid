local Players     = game:GetService("Players")
local RunService  = game:GetService("RunService")
local player      = Players.LocalPlayer
local backpack    = player:WaitForChild("Backpack")

spawn(function()
    while true do
        -- Intentamos encontrar UNA Tropical Shakes en el Backpack
        local shake = backpack:FindFirstChild("Tropical Shake")
        if not shake then
            warn("✅ Ya no quedan Tropical Shakes en el inventario.")
            break
        end

        -- Informar que la detectamos
        warn("🕹 Encontrada Tropical Shakes:", shake, "- equipando...")
        -- Equipa en Character
        shake.Parent = player.Character
        -- Esperar 1 frame para que realmente esté equipada
        RunService.Heartbeat:Wait()

        -- Activa la herramienta (la “bebe”)
        if shake.Activate then
            shake:Activate()
            warn("🍹 Activada Tropical Shakes:", shake)
        elseif mouse1click then
            mouse1click()
            warn("🍹 mouse1click() sobre Tropical Shakes")
        else
            warn("⚠️ No se pudo activar Tropical Shakes: no hay Activate() ni mouse1click()")
        end

        -- Pequeña pausa para que el servidor procese el consumo
        task.wait(0.1)
    end
end)
