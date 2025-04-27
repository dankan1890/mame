ifeq ($(OS), Windows_NT)
  WINLIBS = iupole iupfiledlg
endif

TARGETS := iup iupcd iupcontrols iupgl iupglcontrols iup_plot iup_mglplot iup_scintilla iupim iupimglib $(WINLIBS) iupweb iuptuio ledc iupview iupvled iuplua5 iupluaconsole iupluascripter
TARGETS := $(filter-out $(EXCLUDE_TARGETS), $(TARGETS))
OTHERDEPENDENCIES := iupgtk iupmot

.PHONY: do_all $(TARGETS) $(OTHERDEPENDENCIES)
do_all: $(TARGETS)

iup iupgtk iupmot:
	@$(MAKE) --no-print-directory -C ./src/ $@
iupcd:
	@$(MAKE) --no-print-directory -C ./srccd/
iupcontrols:
	@$(MAKE) --no-print-directory -C ./srccontrols/
iup_plot:
	@$(MAKE) --no-print-directory -C ./srcplot/
iup_mglplot:
	@$(MAKE) --no-print-directory -C ./srcmglplot/
iup_scintilla:
	@$(MAKE) --no-print-directory -C ./srcscintilla/
iupgl:
	@$(MAKE) --no-print-directory -C ./srcgl/
iupglcontrols:
	@$(MAKE) --no-print-directory -C ./srcglcontrols/
iupim:
	@$(MAKE) --no-print-directory -C ./srcim/
iupole:
	@$(MAKE) --no-print-directory -C ./srcole/
iupfiledlg:
	@$(MAKE) --no-print-directory -C ./srcfiledlg/
iupweb:
	@$(MAKE) --no-print-directory -C ./srcweb/
iuptuio:
	@$(MAKE) --no-print-directory -C ./srctuio/
iupimglib:
	@$(MAKE) --no-print-directory -C ./srcimglib/
iuplua5:
	@$(MAKE) --no-print-directory -C ./srclua5/
iupluaconsole:
	@$(MAKE) --no-print-directory -C ./srcluaconsole/
iupluascripter:
	@$(MAKE) --no-print-directory -C ./srcluascripter/
ledc:
	@$(MAKE) --no-print-directory -C ./srcledc/
iupview: iupcontrols iup
	@$(MAKE) --no-print-directory -C ./srcview/
iupvled: iupcontrols iup
	@$(MAKE) --no-print-directory -C ./srcvled/
