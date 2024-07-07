# scoreboard-redesinged


Config = {}


-- SPRACHE EINSTELLEN -- SETTING THE LANGUAGE
Config.Locale = 'de'

Config.RPNames = true -- Set to "true" if you want RP Names

Config.Translations = {
    ['de'] = {
        ['no_perms'] = 'Sie müssen Administrator sein, um diesen Befehl auszuführen!',
        ['updated_default'] = 'Ihre Anzeigetafel wurde auf das Standarddesign aktualisiert!',
        ['saved_custom'] = 'Sie haben Ihr benutzerdefiniertes Farbthema gespeichert!',
        ['event_uploaded'] = 'Veranstaltung erfolgreich hochgeladen!',
        ['event_removed'] = 'Ereignis erfolgreich entfernt!',
    },
    ['en'] = {
        ['no_perms'] = 'You have to be admin to execute this command!',
        ['updated_default'] = 'Updated your scoreboard to the default theme!',
        ['saved_custom'] = 'You saved your custom color theme!',
        ['event_uploaded'] = 'Event uploaded successfully!',
        ['event_removed'] = 'Event removed successfully!',
    },
    ['es'] = {
        ['no_perms'] = '¡Debes de ser admin para usar este comando!',
        ['updated_default'] = '¡Has actualizado al tema predeterminado!',
        ['saved_custom'] = '¡Has guardado tu tema!',
        ['event_uploaded'] = '¡Has subido el evento!',
        ['event_removed'] = '¡Has eliminado el evento!',
    },
--     ['LANGUAGE'] = {
--         ['no_perms'] = 'YOUR TEXT',
--         ['updated_default'] = 'YOUR TEXT',
--         ['saved_custom'] = 'YOUR TEXT',
--         ['event_uploaded'] = 'YOUR TEXT',
--         ['event_removed'] = 'YOUR TEXT',
--     },
}

-- CHANGE NOTIFICATION SETTINGS -- BENACHRICHTIGUNGSEINSTELLUNGEN ÄNDERN

Config.Notification = function(action)
    TriggerEvent('esx:showNotification', Config.Translations[Config.Locale][action])
    -- TriggerEvent('CUSTOM:CUSTOM', Config.Translations[Config.Locale][action])
end

-- JOBS IM SCOREBOARD EINSTELLEN -- POSTING JOBS IN THE SCOREBOARD

Config.Business = {
    ['LAPD'] = {
        Job = 'police',
        Description = 'To protect and to serve.',
        Status = {
            Service = {'Available', 'Busy', 'Out of service'},
            Defcons = {'Defcon 1', 'Defcon 2', 'Defcon 3', 'Defcon 4', 'Defcon 5'},
        }
    },
    ['LAMD'] = {
        Job = 'ambulance',
        Description = 'Dedicated to safing lifes.',
        Status = {
            Service = {'Available', 'Busy', 'Out of service'},
            Defcons = {'Ambulances', 'In Hospital', 'None'},
        }
    },
    ['California Customs'] = {
        Job = 'mechanic',
        Description = 'Modify your vehicles as your liking.',
        Status = {
            Service = {'Available', 'Busy', 'Out of service'},
            Tunning = {'In LS', 'In PT', 'In SS'},
        }
    },
    -- ['CUSTOM JOB'] = {
    --     Job = 'CUSTOM',
    --     Description = 'YOUR DESCRIPTION',
    --     Status = {
    --         Service = {'Available', 'Busy', 'Out of service'},
    --         Tunning = {'CUSTOM', 'CUSTOM', 'CUSTOM'}, OR  Defcons = {'CUSTOM', 'CUSTOM', 'None'},
    --     }
    -- },
}

Config.Robberies = {
    ['BANK'] = {
        Job = 'police',
        Description = "Break into the bank's facilities stealthily, or enter like in the movies.",
        Min = 1,
    },
    ['CASINO'] = {
        Job = 'police',
        Description = "Enter the casino to rob the safe, but be careful, the cameras are always watching you.",
        Min = 2,
    },
    -- ['CUSTOM'] = {
    --     Job = 'JOBNAME',
    --     Description = "DESCRIPTION",
    --     Min = TIME,
    -- },
}
