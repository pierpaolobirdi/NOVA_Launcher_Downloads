- The publish scripts store no credential: on the owner's self-hosted runner Git Credential Manager kept the workflow's
  `x-access-token` login as his github.com account, and other programs that read private repositories got an account chooser.
  `push_retry.sh` (sourced by every publish script before its first git command) empties `credential.helper` and forbids prompts.
