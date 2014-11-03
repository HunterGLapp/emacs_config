;;set background color
(load-theme 'tango-dark)

(add-to-list 'auto-mode-alist '("\\.latex\\'" . latex-mode))
;; show the time
(display-time)

;; syntax highlighting
(global-font-lock-mode 1)

;; stop scrolling at EOF
(setq next-line-add-newlines nil)

;; haskell indentation. There are other choices
(add-hook 'haskell-mode-hook 'turn-on-haskell-indentation)

;; prety Haskell (use with caution)
;;(setq haskell-font-lock-symbols t)

;; start with scratch buffer
(setq inhibit-startup-message t)

;; get rid of ~ files
(setq make-backup-files nil)

;; line numbers
(require 'linum)

(global-linum-mode)

(defcustom linum-disabled-modes-list '(eshell-mode wl-summary-mode compilation-mode org-mode text-mode dired-mode doc-view-mode)
  "* List of modes disabled when global linum mode is on"
  :type '(repeat (sexp :tag "Major mode"))
  :tag " Major modes where linum is disabled: "
  :group 'linum
  )
(defcustom linum-disable-starred-buffers 't
  "* Disable buffers that have stars in them like *Gnu Emacs*"
  :type 'boolean
  :group 'linum)

(defun linum-on ()
  "* When linum is running globally, disable line number in modes defined in `linum-disabled-modes-list'. Changed by linum-off. Also turns off numbering in starred modes like *scratch*"

  (unless (or (minibufferp) (member major-mode linum-disabled-modes-list)
              (and linum-disable-starred-buffers (string-match "*" (buffer-name)))
              )
    (linum-mode 1)))

(provide 'setup-linum)

(set-mouse-color "black")

(switch-to-buffer-other-window "*scratch*")
(shell)
(shrink-window 10)

(auto-save-mode 0)

(tool-bar-mode -1)

 ;; Set transparency of emacs
 (defun transparency (value)
   "Sets the transparency of the frame window. 0=transparent/100=opaque"
   (interactive "nTransparency Value 0 - 100 opaque:")
   (set-frame-parameter (selected-frame) 'alpha value))

(transparency 100)

(custom-set-variables
 ;; custom-set-variables was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 '(TeX-PDF-mode t)
 '(TeX-source-correlate-method (quote synctex))
 '(TeX-source-correlate-mode t)
 '(TeX-source-correlate-start-server t)
 '(TeX-view-program-list (quote (("Okular" "okular -unique %o#src:%n%b"))))
 '(TeX-view-program-selection (quote ((output-pdf "Okular"))))
 '(doc-view-continuous t)
 '(doc-view-ghostscript-options (quote ("-dSAFER" "-dNOPAUSE" "-sDEVICE=png16m" "-dTextAlphaBits=4" "-dBATCH" "-dGraphicsAlphaBits=8" "-dQUIET" "-dDOINTERPOLATE" "-dNOPROMPT" "-dAlignToPixels=0" "-dMaxBitMap=5000000000" "-dNOTRANSPARENCY")))
 '(doc-view-image-width 1000)
 '(doc-view-resolution 100000))
(custom-set-faces
 ;; custom-set-faces was added by Custom.
 ;; If you edit it by hand, you could mess it up, so be careful.
 ;; Your init file should contain only one such instance.
 ;; If there is more than one, they won't work right.
 )

(setq TeX-PDF-mode t)
