# DCLPRCOPT
Présentation de l'utilisation de Declare Processing Options (DCLPRCOPT)
Declare Processing Options (DCLPRCOPT)

The DCLPRCOPT command allows you to control the behavior of the CL compiler and do so from a source statement within the procedure or program being compiled. No longer do we have to remember what activation group to specify on the CRTBNDCL or, when binding to a *SRVPGM, use CRTCLMOD and then CRTPGM in order to reference a *SRVPGM or *BNDDIR. We can specify these, and more, on the DCLPRCOPT command within the source we are compiling. This capability to store compile options within the CL source is similar to ILE RPG's H-spec capability and ILE COBOL's PROCESS statement.

 

While DCLPRCOPT in V5R4 only supported the parameter Subroutine stack depth (SUBRSTACK), V6R1 supports the specification of Log commands (LOG), Allow RTVCLSRC (ALWRTVSRC), Text (TEXT), User profile (USRPRF), Authority (AUT), Sort sequence (SRTSEQ), Language ID (LANGID), Storage model (STGMDL), Default activation group (DFTACTGRP), Activation group (ACTGRP), Bind service program (BNDSRVPGM), and Binding directory (BNDDIR). This capability should greatly reduce the frequency of errors due to compile option mistakes, mistakes that can sometimes lead to very long problem determination procedures as many developers tend to look first at the source of a problem program, not the attributes of the program.

 

Here's an example of using DCLPRCOPT to specify that binding directory MYBNDDIR in library MYLIB is to be used when resolving procedure calls:

 

DCLPRCOPT BNDDIR(MYLIB/MYBNDDIR)
- See more at: http://www.mcpressonline.com/programming/cl/v6r1-cl-the-story-continues.html#sthash.seVLDrqV.dpuf
