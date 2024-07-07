# scoreboard-redesinged


Config = {}


-- SPRACHE EINSTELLEN -- SETTING THE LANGUAGE

     ['LANGUAGE'] = {
         ['no_perms'] = 'YOUR TEXT',
         ['updated_default'] = 'YOUR TEXT',
         ['saved_custom'] = 'YOUR TEXT',
         ['event_uploaded'] = 'YOUR TEXT',
         ['event_removed'] = 'YOUR TEXT',
     },


-- CHANGE NOTIFICATION SETTINGS -- BENACHRICHTIGUNGSEINSTELLUNGEN ÄNDERN

Config.Notification = function(action)
    TriggerEvent('CUSTOM:CUSTOM', Config.Translations[Config.Locale][action])
end

-- JOBS IM SCOREBOARD EINSTELLEN -- POSTING JOBS IN THE SCOREBOARD

     ['CUSTOM JOB'] = {
         Job = 'CUSTOM',
         Description = 'YOUR DESCRIPTION',
         Status = {
             Service = {'Available', 'Busy', 'Out of service'},
             Tunning = {'CUSTOM', 'CUSTOM', 'CUSTOM'}, OR  Defcons = {'CUSTOM', 'CUSTOM', 'None'},
        }
     },

-- CREATE ROBBERY EVENTS

     ['CUSTOM'] = {
         Job = 'JOBNAME',
         Description = "DESCRIPTION",
         Min = TIME,
     },

