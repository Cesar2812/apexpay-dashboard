#REPORTEDELABORATORIO04(INDIVIDUAL)
**Curso:**ControldeVersionesparaDesarrollo FullStack
**Docente:**Ing. LuisFlores--

###1.IdentificacióndelDesarrollador
***NombreCompleto:**[CesarJoseCerdaMaldonado]
***UsuariodeGitHub:**@[Cesar2812]
***FechadeEntrega:**[28/5/2026]--

###2.Hito1:ImplementacióndeSeguridadPerimetral(.gitignore)
1.**Estructura delarchivo`.gitignore`consolidadalocalmente:**
```text
    # Secretos locales de ApexPay
    .env
    .env.local
    # Temporales de compilacion y dependencias generadas por el script
    node_modules/
    dist/
    *.log
```

2.**PruebadeInmunidaddeCredenciales:***Peguelasalidacompletadelcomando`gitstatus`dondesedemuestre
queelarchivo`.env`quecreolocalmenteestotalmenteignoradoporelsoftwaredecontroldeversiones:*
```text
    Ignored files:
    (use "git add -f <file>..." to include in what will be committed)
            .env
            app-compilation.log
            node_modules/
```--
###3.Hito2:ResolucióndelaColisióndeInterfaces(MergeConflictSolo)
1.**Discrepancia TécnicaInicial:***Describabrevemente(máximo3líneas)quécausóelrechazoinicialdelpush
localfrentealcambioremotodelainterfazwebdeGitHubyquémarcadoresinyectóGitenelarchivoREADME
.md:*
_Respuesta:_ 
    El conflicto fue ocacionado por cambios realizados en la misma linea de codigo del mismo archivo, al querer 
    fusionar los cambios del local al remoto lanzo un error de desincronizacion y luego, se fusiono la rama remota con la local
    y se mostro el conflicto los marcadores inyectados fueron <<<<HEAD que es el codigo de mi rama actual y el codigo de la rama entrante que ocaciona el conflicto

2.**ResultadoConsolidadodeConsenso:***PegarelbloquefinaldelREADME.mddondeconvivelaconfiguración
híbridaresueltademaneramanual:*
```markdown
    # Tema Del Proyecto: Hibrido
```-- 

###4.Hito3:MitigacióndeExposicióndeInfraestructura(gitrevert)
1.**HistóricodelHistorialClínicodeProducción(GitLog):***Pegarlasalidadelcomando`gitlog--oneline
n4`delaramaprincipalejecutadoensu máquinalocal,quemuestrelasecuenciatransparentedelcommitde
exposiciónaccidentalderedseguidodelcommitdecontra-medidaautomática(`revert`):*
```text
    6cabafc (HEAD -> main, origin/main, origin/HEAD) Merge pull request #2 from Cesar2812/feat/footer
    1d06dec (origin/feat/footer, feat/footer) fix: incorporar politicas de privacidad de footer
    41762fa Merge pull request #1 from Cesar2812/feat/menu-principal
    ada9dd9 (origin/feat/menu-principal, feat/menu-principal) fix: ajustar menu de navegacion segun auditoria interna
    f0f4909 feat: estructurar pie de pagina corporativo
    c0059f9 feat: estructurar el menu principal de navegacion
    bb7147c Revert "feat: modulo de pruebas de red expuestas"
    db9a863 feat: modulo de pruebas de red expuestas
    3e91ca6 merge: conciliar conflicto de temas en solitario
    29a1258 feat: configurar tema claro localmente
    364dc95 feat: configurar tema oscuro de forma remota
    0631312 chore:inicializar codigo base de ApexPay y configurar gitignore
    6dbe584 Initial commit
```
2.**AnálisisdeResilienciaOrganizacional:***Expliquedeformadetalladaporquéelcomando`gitreset--hard`
seconsideraunaprácticadealtopeligrocorporativoenramascentralespúblicascompartidasenGitHub.
¿Cómoayuda`gitrevert`asalvaguardarlaestabilidaddelequipodedesarrollo?*
_Respuesta:_
    Desde una perspectiva de resiliencia organizacional y estabilidad colaborativa, git reset --hard representa una operación destructiva que puede comprometer la integridad del repositorio, interrumpir el trabajo del equipo y provocar pérdida crítica de información cuando se usa en ramas públicas compartidas.

    Por el contrario, git revert constituye una práctica segura y alineada con principios modernos de ingeniería colaborativa, ya que permite corregir errores preservando el historial, la trazabilidad y la estabilidad operativa del ecosistema de desarrollo.


###5.Hito4:EnlacesdeGobernanzaySolicitudesdeIntegración
*ColoquelasdireccionesURLcompletasdelassolicitudesdeintegración(PR)fusionadasensurepositoriode
GitHub:*
***PullRequestdeMenú(`feat/menu-principal`):**`https://github.com/Cesar2812/apexpay-dashboard/pull/1`
***PullRequestdeFooter(`feat/footer`):**`https://github.com/Cesar2812/apexpay-dashboard/pull/2`