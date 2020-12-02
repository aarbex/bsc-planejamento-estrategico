
<template>
    <q-layout class="bg-light-grey window-height window-width row justify-center items-center">
       <q-parallax
      src="../assets/bg.png"
    >
    <q-header elevated class="bg-brown-13">
      <q-toolbar>
        <q-toolbar-title>
          BSC - Planejamento Estratégico
        </q-toolbar-title>
      </q-toolbar>
    </q-header>
       <div class="column">
        <div class="row">
        <q-card square bordered class="q-pa-xl shadow-1">
            <h5 class="text-h5 text-black q-my-md">Login</h5>
          <q-card-section>
            <q-form class="q-gutter-md">
              <q-input square filled v-model="email" type="email" label="email" />
              <q-input square filled v-model="password" :type="isPwd ? 'password' : 'text'" label="password">
              <template v-slot:append>
          <q-icon
            :name="isPwd ? 'visibility_off' : 'visibility'"
            class="cursor-pointer"
            @click="isPwd = !isPwd"
          />
        </template>
              </q-input>
            </q-form>
          </q-card-section>
          <q-card-actions class="q-px-md">
            <q-btn unelevated color="brown-13" size="lg" class="full-width" label="Login" />
          </q-card-actions>
        </q-card>
      </div>
    </div>
       </q-parallax>
    <q-dialog v-model="cookies">
      <q-card>
        <q-card-section>
          <div class="text-h6">Uso de Cookies</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
          Este site usa cookies e dados pessoais de acordo com os nossos Termos de Uso e Política de Privacidade e, ao continuar navegando neste site, você declara estar ciente dessas condições.
        </q-card-section>

        <q-card-actions align="right" class="text-primary">
          <q-btn flat label="Termos de Uso e Política de Privacidade" @click="termos = true" color="brown-13" />
          <q-btn flat label="Aceitar" v-close-popup color="brown-13"/>
        </q-card-actions>
      </q-card>
    </q-dialog>

    <q-dialog v-model="termos" persistent transition-show="scale" transition-hide="scale">
      <q-card style="width: 600px">
        <q-card-section>
          <div class="text-h6">Termos de Uso e Política de Privacidade</div>
        </q-card-section>

        <q-card-section class="q-pt-none">
<b>POLÍTICA DE PRIVACIDADE – LLIÈGE TECNOLOGIA<br/><br/></b>
A LLIÈGE é uma empresa que foi constituída, com o propósito de desenvolver, integrar e comercializar com qualidade, soluções e serviços de tecnologia da informação e geotecnologias. A sede da empresa situa-se na Rua Olga Batista, 160, Parque Nova Jandira, Jandira, SP. Aqui representada pelo seu CEO, Wibson Fernando de Paula, a empresa compromete-se a proteger os dados pessoais dos seus Clientes e Visitantes em suas diversas plataformas.
Ao acessar e usar os sites da Web, os Usuários se comprometem a cumprir e se vincular a esta Política de Privacidade que pode ser alterada ou atualizada a qualquer momento, sem aviso prévio. Qualquer modificação ou atualização será publicada online no Website. Essa Política de Privacidade se aplica a quaisquer dados tratados pela LLIÈGE, conforme o Art. 5º, inciso X da Lei Geral de Proteção de Dados (lei nº 13.709, de 14 de agosto de 2018.). Nesse sentido, recomendamos que nossa política de privacidade seja regularmente consultada pelo usuário, de forma a estar sempre atualizado.<br/>
<b><br/>CAPÍTULO I<br/></b>
A natureza dos dados pessoais recolhidos pela LLIÈGE
A LLIÈGE recolhe e processa os dados que são fornecidos voluntariamente pelos Usuários para acessar ou utilizar o Website, bem como os dados relativos às preferências dos Usuários em relação aos Usuários e ao tráfego (tais como os endereços IP).
A finalidade deste processamento de dados é permitir aos Usuários acessar o Website e utilizá-lo, melhorar os serviços colocando cookies nos dispositivos dos Usuários, manter a nossa relação com o cliente e estabelecer um diálogo através do Live Chat, para fornecer um serviço adaptado às necessidades dos Usuários e informá-los sobre os nossos produtos e ofertas de serviços, realizar tarefas relacionadas com a solicitação de vendas, em particular através do envio de newsletters, telefonemas, para a elaboração de estatísticas (vendas, para a venda, aluguel ou troca dos seus arquivos de solicitação a atualização dos seus arquivos de solicitação,) quantitativas e qualitativas, atualização de dados, gestão dos direitos de acesso, retificação e oposição e a gestão das opiniões das pessoas sobre os produtos e serviços.
A LLIÈGE nunca recolherá ou processará dados pessoais direta ou indiretamente relacionados a raça, situação de saúde, orientação sexual, convicções políticas ou filosóficas ou crenças religiosas, considerados sensíveis pela Lei nº 13.709/2018, a Lei Geral de Proteção de Dados.
<b><br/><br/>CAPÍTULO II<br/></b>
Dados que não sejam de natureza pessoal
Os dados de tráfego são gerados quando os dispositivos dos Usuários se conectam à Internet e, isoladamente, não são suficientes para identificá-los. A LLIÈGE pode coletar os seguintes dados: a origem da conexão, o tipo e a versão do navegador de Internet que o Usuário está usando, a duração da conexão, etc. Estes dados podem ser utilizados para fins estatísticos, para analisar o tráfego e melhorar os websites. Os dados de tráfego são sempre processados de forma anônima.
A LLIÈGE coloca cookies nos dispositivos dos Usuários. Cookies são pequenos arquivos que contêm, por exemplo, dados de tráfego e preferências dos Usuários.
Os cookies colocados pela LLIÈGE têm a seguinte finalidade: "Autenticação do Usuário", registar as visitas dos Usuários e a sua origem e oferecer um Live Chat.
A LLIÈGE utiliza o serviço Google Analytics (fornecido pela Google Inc.) como meio de medir o alcance da audiência para recolher os seguintes dados: a origem das ligações (fornecedores de acesso), tipo e versão do browser utilizado, o idioma do browser, duração da ligação, endereço IP, etc e armazenar cookies nos dispositivos dos Usuários para executar estratégias de alcance da audiência. Para mais informações, o Cliente ou Usuários podem consultar o seguinte site: www.google.com/intl/fr/policies/privacy/.
Alguns parceiros da LLIÈGE podem assim depositar cookies nos terminais dos Usuários: Google Analytics para os fins acima especificados, bem como para o Live Chat, Pixel (Facebook) e Google Adwords para remarketing.
Cookies são necessários para navegar nos sites e devem, portanto, ser aceitos pelos usuários. Os Usuários podem configurar o seu browser para desativar os cookies ou avisá-los antes de aceitarem um cookie nos websites que visitam. No entanto, se os Usuários desativarem os cookies, eles podem não ser capazes de usar todas as partes dos sites.
Os cookies são válidos por um período de doze (12) meses. A LLIÈGE poderá solicitar a renovação do consentimento após este período ou efetuar de modo automático.
<b><br/><br/>CAPÍTULO III<br/></b>
Tratamento dos dados pessoais dos Usuários
A LLIÈGE recolhe e processa os dados pessoais dos Usuários de forma transparente e lícita que respeita os direitos dos Usuários e a Lei nº 13.709, de 14 de agosto de 2018.
A LLIÈGE é a entidade responsável pelo tratamento dos dados pessoais recolhidos via digital pela plataforma. A empresa não garante a segurança de nenhum outro tipo de canal para recolhimento de dados além do supracitado.
Os dados coletados estão diretamente relacionados ao fluxo do sistema, sendo exigíveis para seu uso regular e demais cadastros associados a seus fins de execução de políticas públicas, conforme Art. 7º, III, da Lei Geral de Proteção de Dados
A manipulação dos dados inseridos na plataforma é de total responsabilidade da PREFEITURA DA ESTÂNCIA TURÍSTICA DE IBIUNA, que passa a ser a proprietária para formular políticas públicas e garantir a sua privacidade total.
A LLIÈGE exerce a sua responsabilidade em segurança dos dados informados pelas vias digitais através de suas próprias plataformas, não garantindo a segurança em qualquer outra via que não seja essa.
<b><br/><br/>CAPÍTULO IV<br/></b>
Tratamento dos dados pessoais dos Menores de Idade
A LLIÈGE não transmite de forma alguma para nenhum fim dados relacionados a menores de idade.
Qualquer compartilhamento realizado pela PREFEITURA DA ESTÂNCIA TURISTICA DE IBIUNA de dados de menores é de exclusiva responsabilidade da própria, independente do fim aplicado.
A LLIÈGE atende ao disposto no Art. 14, § 1º da Lei Geral de Proteção de Dados, apenas recolhendo dados de menores com o consentimento do responsável legal pelo menor.
<b><br/><br/>CAPÍTULO V<br/></b>
Armazenamento dos dados pessoais dos Usuários
Os dados pessoais fornecidos pelos Usuários são hospedados por Matrix Data Center e Google, cujos servidores estão localizados respectivamente em São Paulo (SP) no Brasil e San José nos Estados Unidos. Veja aqui a política de privacidade e termos de uso da Matrix Data Center: https://
A LLIÈGE esforça-se por evitar qualquer interferência com os dados pessoais dos Usuários, tais como perda, desvio, intrusão, divulgação não autorizada, alteração ou destruição de dados pessoais.
Qualquer informação fornecida pelos usuários será coletada e guardada de acordo com os mais rígidos padrões de segurança e confiabilidade.
Os dados pessoais recolhidos através da plataforma serão utilizados apenas para o devido exercício das políticas públicas pela PREFEITURA MUNICIPAL DA ESTÂNCIA TURÍSTICA DE IBIUNA, segundo o Art. 11. e inciso II da Lei n° 13.709/2018.
<b><br/><br/>CAPÍTULO VI<br/></b>
Dos Prazos<br/>
Os dados pessoais tratados pela LLIÈGE serão apagados no prazo máximo de três anos após a data do último contato do usuário com os serviços, ou resultante de uma solicitação de prospecção/Usuário, na sequência de uma anulação da newsletter ou em ligação com a comunidade LLIÈGE.
<b><br/><br/>CAPÍTULO VII<br/></b>
Transferência de dados pessoais dos Usuários<br/>
A LLIÈGE é autorizada pelo usuário a transferir dados pessoais para a sua filial LLIÈGE (localizada em São Paulo).
A LLIÈGE é autorizada pelo usuário a transferir dados pessoais dos Usuários se tal for exigido por lei ou ordem judicial.
A LLIÈGE pode também partilhar informações de dados anonimizados para possíveis parceiros. Tais informações não identificam os Usuários individualmente. Qualquer transferência de dados será garantida pela Autoridade Nacional de Proteção de Dados (ANPD) após sua instauração, e comunicada a mesma. Em nenhuma hipótese este compartilhamento configurará ganho financeiro para LLIÈGE, sendo sua comercialização descartada e fora das boas práticas da empresa, que apenas o fará para os fins acima citados.
Demais movimentações de dados recolhidos pela plataforma são de exclusiva responsabilidade da PREFEITURA DA ESTÂNCIA TURÍSTICA DE IBIUNA, que deverá observar as vias legais de Proteção de Dados para o seu compartilhamento com foco na execução das diversas políticas públicas.
<b><br/><br/>CAPÍTULO VIII<br/></b>
Exercício dos Direitos dos Usuários<br/>
Os Usuários têm direitos de acesso, modificação e retificação, e oposição ao processamento e portabilidade.
Os Usuários podem solicitar a eliminação dos dados pessoais recolhidos ou tratados pela LLIÈGE a qualquer tempo.
Os usuários podem informar-se a qualquer tempo de como seus dados estão sendo tratados e de possíveis movimentações.
Os Usuários podem exercer estes direitos escrevendo à LLIÈGE para o endereço postal: Avenida Angélica, 321, Conjunto 191, Santa Cecília, São Paulo, CEP 01228-000 ou enviando e-mail para lliege@lliege.com.br.
Desde a presente anuência com essa Política de Privacidade, está o usuário sujeito a suas cláusulas.
        </q-card-section>

        <q-card-actions align="right" class="bg-white text-teal">
          <q-btn flat label="OK" color="brown-13" v-close-popup />
        </q-card-actions>
      </q-card>
    </q-dialog>
    </q-layout>
</template>

<script>
export default {
  name: 'Login',
  data () {
    return {
      email: '',
      password: '',
      cookies: true,
      termos: false,
      isPwd: true
    }
  }
}
</script>
<style lang="stylus">

</style>
