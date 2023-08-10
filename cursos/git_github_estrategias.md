  <html>
    <table>
        <tbody>
            <tr><td>O que são e como utilizar <strong>issues</strong></td></tr>
            <tr><td>Que as issues podem ser utilizadas para vários propósitos
            <ul>
                <li>Reportar problemas</li>
                <li>Sugerir melhorias</li>
                <li>Solicitar novas funcionalidades</li>
                <li>Organizar qualquer coisa que faça sentido para o projeto</li>
                <li>e outros</li>
            </ul>
            </td></tr>
            <tr><td>O que são <strong>pull requests</strong></td></tr>
            <tr><td>Como unir vários commits em um, utilizando o comando <strong>git rebase -i</strong></td></tr>
            <tr><td>Como enviar e como revisar um pull request no GitHub</td></tr>
            <tr><td>
                Controle avançado de conflitos
                <ul>
                    <li>Que o comando git <strong>cherry-pick</strong> pode trazer um commit específico para a branch atual</li>
                    <li>Como encontrar o commit em que determinada alteração foi aplicada, utilizando o <strong>git bisect</strong></li>
                    <li>Como encontrar o responsável por determinanda linha ou bloco de código, utilizando o <strong>git blame</strong></li>
                    <li>Que jamais devemos apontar um culpado por determinado bug. Uma equipe deve ser unida e se ajudar</li>
                    <li>Que o comando <strong>git show {hash}</strong>  mostra todas as alterações aplicadas pelo commit com o hash informado.</li>
                </ul>
            </td></tr>
            <tr><td>
            Estratégias de branching
            <ul>
                <li>Que é uma convensão bem seguida que a branch <strong>master</strong> tenha apenas os commits prontos para ir para produção</li>
                <li>Que não é interessante realizar trabalho e commitar diretamente na branch <strong>master</strong></li>
                <li>Como remover uma branch</li>
                <ul>
                    <li><strong>git branch -d {nome_branch}</strong> remove uma branch que já tem seu trabalho unido à branch atual</li>
                    <li><strong>git branch -D {nome_branch}</strong> remove uma branch mesmo que os commits desta branch ainda não estejam na branch atual, ou seja, força a remoção;</li>
                </ul>
                <li>Um pouco do processo chamado de <strong>Git Flow</strong></li>
                <ul>   
                    <li>Entendemos que o estado do código representado pela branch <strong>master</strong> deve ser o mesmo que estará em produção</li>
                    <li>Vimos que deve haber uma branch de desenvolvimento (comument chamado de <strong>develop</strong>), onde todas as funcionalidades e correções devem ser muito bem testada antes de ir para produção <strong> master</strong></li>
                    <li>Vimos que cada funcionalidade deve ser feita em uma branch separada, e que é comum que esta branch tenha <strong>feature/</strong> como prefixo</li>
                    <li>Aprendemos também que bugs normalmente são corrigidos em <strong>hotfix/</strong></li>
                    <li>Além disso, branches específicas para cada release são criadas para realizar os testes e correções de bugs específicos</li>
                </ul>
            </ul>
            </td></tr>
            <tr><td>
            Ferramentas visuais
                <ul>
                    <li>Existem ferramentas visuais que podem nos auxiliar com o trabalho com o Git;</li>
                    <li>O <strong>Git Cola</strong> foi uma das primeiras ferramentas visuais multiplataforma. Embora não seja a mais complexa ou visualmente atraente, é bem completa e pode nos ajudar bastante</li>
                    <li>O <strong>Git Desktop</strong> pode ser interessante para gerenciar os projetos do GitHub de forma mais ágil e facilitada, sem a necessidade de acessar o site;</li>
                    <li>O <strong>GitKraken</strong> é uma ferramenta extremamente completa, que nos auxilia inclusive com a implementação do <strong>Git Flow</strong></li>
                </ul>
            </td></tr>
            <tr><td>
                Hooks e dploy com Git
                <ul>
                    <li>Que o Git trabalha com eventos e os chama de <strong>hooks;</strong></li>
                    <li>Que podemos definir códigos a serem executados quando determinado evento (hook) ocorrer</li>
                    <li>A criar hooks dentro da pasta <strong>.git/hooks</strong>, utilizando <strong>Shell Script</strong></li>
                    <li>Que o nome do arquivo indica em qual hook (evento) ele será executado;</li>
                    <li>Que, com hooks, podemos executar os testes automatizados do nosso código, ou até mesmo colocar uma aplicação em produção</li>
                </ul>
            </td></tr>
        </tbody>
    </table>     
 </html>