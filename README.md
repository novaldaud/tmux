# tmux
Konfigurasi Tmux-Linux
# split panes using | and -
bind | split-window -h
bind - split-window -v
unbind '"'
unbind %

# switch panes using Alt-arrow without prefix
bind -n M-Left select-pane -L
bind -n M-Right select-pane -R
bind -n M-Up select-pane -U
bind -n M-Down select-pane -D

# Enable mouse mode (tmux 2.1 and above)
set -g mouse on

# don't rename windows automatically
set-option -g allow-rename off

## COLORSCHEME: gruvbox dark
set-option -g status "on"

# default statusbar colors
set-option -g status-bg colour237 #bg1
set-option -g status-fg colour223 #fg1

# default window title colors
set-window-option -g window-status-bg colour214 #yellow
set-window-option -g window-status-fg colour237 #bg1

set-window-option -g window-status-activity-bg colour237 #bg1
set-window-option -g window-status-activity-fg colour248 #fg3

# active window title colors
set-window-option -g window-status-current-bg default
set-window-option -g window-status-current-fg colour237 #bg1

# pane border
# set -g pane-border-bg colour249
# set -g pane-border-fg colour238
# set-option -g pane-active-border-fg colour250 #fg2
# set-option -g pane-border-fg colour237 #bg1

set -g pane-border-bg colour235
set -g pane-border-fg colour238
set -g pane-active-border-bg colour236
set -g pane-active-border-fg colour214

# message infos
set-option -g message-bg colour239 #bg2
set-option -g message-fg colour223 #fg1

# writting commands inactive
set-option -g message-command-bg colour239 #fg3
set-option -g message-command-fg colour223 #bg1

# pane number display
set-option -g display-panes-active-colour colour250 #fg2
set-option -g display-panes-colour colour237 #bg1

# clock
set-window-option -g clock-mode-colour colour109 #blue

# bell
set-window-option -g window-status-bell-style fg=colour235,bg=colour167 #bg, red


## Theme settings mixed with colors (unfortunately, but there is no cleaner way)
set-option -g status-attr "none"
set-option -g status-justify "left"
set-option -g status-left-attr "none"
set-option -g status-left-length "80"
set-option -g status-right-attr "none"
set-option -g status-right-length "80"
set-window-option -g window-status-activity-attr "none"
set-window-option -g window-status-attr "none"
set-window-option -g window-status-separator ""

set-option -g status-left "#[fg=colour248, bg=colour241] #S #[fg=colour241, bg=colour237, nobold, noitalics, nounderscore]"
set-option -g status-right "#[fg=colour239, bg=colour237, nobold, nounderscore, noitalics]#[fg=colour246,bg=colour239] %Y-%m-%d  %H:%M #[fg=colour248, bg=colour239, nobold, noitalics, nounderscore]#[fg=colour237, bg=colour248] #h "

set-window-option -g window-status-current-format "#[fg=colour239, bg=colour248, :nobold, noitalics, nounderscore]#[fg=colour239, bg=colour214] #I #[fg=colour239, bg=colour214, bold] #W #[fg=colour214, bg=colour237, nobold, noitalics, nounderscore]"
set-window-option -g window-status-format "#[fg=colour237,bg=colour239,noitalics]#[fg=colour223,bg=colour239] #I #[fg=colour223, bg=colour239] #W #[fg=colour239, bg=colour237, noitalics]"
