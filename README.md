<style>
.p {
  font-family: "Times New Roman", Times, serif;
  
}

</style>
# WaveFit2.4

Wavefit 2.4 é uma aplicção destinada a ajuste de aparelho auditivo, este projeto foi desenvolvido utilizando wpf como o front de todo o sistema e o 
backend  foi utilizado a linguagem C#.
A funcionalizadade principal do wavefit2.4 á ajustar aparelho auditivo de acordo com o audiograma.


Árvore das pastas que se relacionam
<pre>
  <code>
WaveFit2/
├── Dll/
│   ├── Audion4/
│   │   ├── Audion4.dll
│   │   ├── Audion4.h
│   │   └── Audion4.lib
│   ├── Audion6/
│   │   ├── Audion6.dll
│   │   ├── Audion6.h
│   │   └── Audion6.lib
│   ├── Audion8/
│   │   ├── Audion8.dll
│   │   ├── Audion8.h
│   │   └── Audion8.lib
│   ├── Complementary HI/
│   │   ├── ACSWIT32.DLL
│   │   ├── COM_HOOK.EXE
│   │   ├── DSXXX.dll
│   │   ├── FTChipID.dll
│   │   ├── FTD2XX.dll
│   │   ├── GRTI.dll
│   │   ├── hidapi.dll
│   │   ├── HIP32225.DLL
│   │   ├── HIP32302.dll
│   │   ├── HIP32401.dll
│   │   ├── Hiprowin.d
│   │   ├── Hiprowin.e
│   │   ├── Hiprowin.f
│   │   ├── Hiprowin.i
│   │   ├── Hiprowin.nl
│   │   ├── Hiprowin.uk
│   │   ├── MCard32.dll
│   │   ├── MLRuntime.dll
│   │   ├── msvcr100.dll
│   │   ├── nl_threewire.dll
│   │   ├── RTI_TargetCalc.dll
│   │   ├── Swboxw32.dll
│   │   ├── Swboxwin.dll
│   ├── SpinNR/
│   │   ├── SpinNR.dll
│   │   ├── SpinNR.h
│   │   └── SpinNR.lib
├── Home/
│   ├── View/
│   │   ├── HomeUserControl.xaml
│   │   ├── HomeUserControl.xaml.cs
│   │   ├── WhiteNoiseWindow.xaml
│   │   └── WhiteNoiseWindow.xaml.cs
│   ├── ViewModel/
│   │   └── HomeViewModel.cs
├── Image/
│   ├── AparelhoAuditivoLogo.png
│   ├── Fonteonefit.png
│   ├── Logo.png
│   └── orelha.png
├── Migrations/
│   ├── 202405151810448_AddLocation_Place.cs
│   ├── 202405151810448_AddLocation_Place.Designer.cs
│   ├── 202405151810448_AddLocation_Place.resx
│   ├── 202405211841054_AddHealthCenter_Audiometer.cs
│   ├── 202405211841054_AddHealthCenter_Audiometer.Designer.cs
│   ├── 202405211841054_AddHealthCenter_Audiometer.resx
│   ├── 202405231715257_HearingAidReceptor.cs
│   ├── 202405231715257_HearingAidReceptor.Designer.cs
│   ├── 202405231715257_HearingAidReceptor.resx
│   └── Configuration.cs
├── obj/
│   ├── WaveFit2.csproj.EntityFrameworkCore.targets
│   ├── WaveFit2.EntityFrameworkCore.targets
│   ├── Debug/
│       ├── .NETFramework,Version=v4.8.AssemblyAttributes.cs
│       ├── App.g.cs
│       ├── App.g.i.cs
│       ├── DesignTimeResolveAssemblyReferences.cache
│       ├── DesignTimeResolveAssemblyReferencesInput.cache
│       ├── GeneratedInternalTypeHelper.g.cs
│       ├── GeneratedInternalTypeHelper.g.i.cs
│       ├── MainWindow.g.i.cs
│       ├── WaveFit2.csproj.AssemblyReference.cache
│       ├── WaveFit2.csproj.CopyComplete
│       ├── WaveFit2.csproj.CoreCompileInputs.cache
│       ├── WaveFit2.csproj.FileListAbsolute.txt
│       ├── WaveFit2.csproj.GenerateResource.cache
│       ├── WaveFit2.exe
│       ├── WaveFit2.g.resources
│       ├── WaveFit2.Migrations.AddHealthCenter_Audiometer.resources
│       └── WaveFit2_MarkupCompile.cache
├── Properties/
│   ├── AssemblyInfo.cs
├── Resources/
│   ├── AudiometrySymbols/
│   │   ├── LA.png
│   │   ├── LAMask.png
│   │   ├── LAMaskNoAnswer.png
│   │   ├── LANoAnswer.png
│   │   ├── LL.png
│   │   ├── LLMask.png
│   │   ├── LLMaskNoAnswer.png
│   │   ├── LLNoAnswer.png
│   │   ├── LV.png
│   │   ├── LVMaksNoAnswer.png
│   │   ├── LVMasak.png
│   │   ├── LVNoAnswer.png
│   │   ├── RA.png
│   │   ├── RAMask.png
│   │   ├── RAMaskNoAnswer.png
│   │   ├── RANoAnswer.png
│   │   ├── RL.png
│   │   ├── RLMask.png
│   │   ├── RLMaskNoAnswer.png
│   │   ├── RLNoAnswer.png
│   │   ├── RVA.png
│   │   ├── RVAMask.png
│   │   ├── RVAMaskNoAnswer.png
│   │   ├── RVANoAnswer.png
│   │   ├── RVO.png
│   │   ├── RVOMaksNoAnswer.png
│   │   ├── RVOMask.png
│   │   ├── RVONoAnswer.png
│   ├── MicModel/
│   │   └── APT-D Sonion 6295.txt
│   ├── Profiles/
│   │   ├── arctic-fox.png
│   │   ├── bear.png
│   │   ├── cat.png
│   │   ├── chicken.png
│   │   ├── dog.png
│   │   ├── koala.png
│   │   ├── panda.png
│   │   ├── sea-lion.png
│   │   └── sloth.png
│   ├── RecModel/
│   │   ├── BVA321.txt
│   │   ├── BVA530.txt
│   │   └── OSPL90.txt
├── Settings/
│   ├── Class/
│   │   ├── ByteToImageConverter.cs
│   │   └── CombinedData.cs
│   ├── View/
│   │   ├── EditProfileUserControl.xaml
│   │   ├── EditProfileUserControl.xaml.cs
│   │   ├── HealthCenterForms.xaml
│   │   ├── HealthCenterForms.xaml.cs
│   │   ├── HealthCenterUserControl.xaml
│   │   ├── HealthCenterUserControl.xaml.cs
│   │   ├── SettingsUserControl.xaml
│   │   ├── SettingsUserControl.xaml.cs
│   │   ├── UsersDatagridUserControl.xaml
│   │   └── UsersDatagridUserControl.xaml.cs
│   ├── ViewModel/
│   │   ├── HealthCenterSettingViewModel.cs
│   │   └── SettingsViewModel.cs
├── Validation/
│   ├── ValidationPassword.cs
│   └── ValidationRegister.cs
├── App.config
├── MainWindow.xaml
├── MainWindow.xaml.cs
├── WaveFit2.csproj
└── Program.cs
  </code>
    </pre>

<h2>Estrutura de Diretórios e Arquivos</h2>

<b>
  
<h2>Diretório Raiz (WaveFit2/)</h2>

<h4>App.Config</h4>
 <p><i>
     Arquivo de configuração da aplicação que define configurações globais, como strings de conexão com o banco de dados.
   </i></p>

</b>

<h4>MainWindow.xaml</h4>
  <p><i>
     Arquivo XAML que define a interface gráfica principal da aplicação.
  </i></p>

</b>

<h4>MainWindow.xaml.cs</h4>
  <p><i>
    Código-behind para MainWindow.xaml, contendo a lógica de interação da interface principal.
  </i></p>
  
</b>

<h4>WaveFit2.csproj</h4> 
<p><i>
  Arquivo de projeto do .NET que define a estrutura do projeto, incluindo dependências e configurações de build.
</i></p>

</b>

<h4>Program.cs</h4> 
<p><i>
  Ponto de entrada principal da aplicação.
</i></p>

<b>
<h2>dll/</h2>

<b>

<p> 
  Diretório que contém várias bibliotecas dinâmicas (DLLs) necessárias para o funcionamento do software. Cada subdiretório contém bibliotecas específicas.
</p>

</b>

<h4>Audion4/, Audion6/, Audion8/</h4>
<p>
  Contêm bibliotecas específicas de áudio e seus arquivos de cabeçalho e de link.
</p>

</b>

<h4>Complementary HI/</h4>
<p>
  Contém diversas bibliotecas de suporte e ferramentas auxiliares.
</p>

</b>

<h2>Home/</h2>
<p>Contém arquivos relacionados à tela inicial da aplicação.</p>
</b>
<h4>View/</h4>
<p>
  Contém arquivos XAML para a interface do usuário.
</p>

</b>

<h4>HomeUserControl.xaml</h4>
<p>
  Define a interface da tela inicial.
</p>

</b>

<h4>WhiteNoiseWindow.xaml</h4>
<p>
  Interface para a janela de ruído branco.
</p>

</b>

<h4>WhiteNoiseWindow.xaml.cs</h4>
<p>
  Código-behind para a janela de ruído branco.
</p>

<h4>ViewModel</h4>
<p>
  Contém arquivos que implementam a lógica de apresentação para a tela inicial.
</p>
<h4>HomeViewModel.cs</h4>
<p>
  Lógica de apresentação para a tela inicial.
</p>

<b>
  
<h2>Image/</h2>
<p> 
  Diretório para armazenar recursos de imagem utilizados na aplicação.
</p>

</b>

<h4>AparelhoAuditivoLogo.png, Fonteonefit.png, Logo.png, orelha.png</h4>
<p>
  Imagens utilizadas na interface do usuário.
</p>

</b>

<h2>Migrations/</h2>
  
<p>
  Contém arquivos relacionados às migrações do banco de dados.
</p>
<p><i>
  202405151810448_AddLocation_Place.cs 
  
  202405151810448_AddLocation_Place.Designer.cs
  
  202405151810448_AddLocation_Place.resx
</i></p>
  <p>
  Arquivos gerados pelo Entity Framework para adicionar a migração de localizações.
  </p>

</b>

<p><i>
  202405211841054_AddHealthCenter_Audiometer.cs
  
  202405211841054_AddHealthCenter_Audiometer.Designer.cs
  
  202405211841054_AddHealthCenter_Audiometer.resx:
 </i></p> 
 <p>
  Arquivos gerados pelo Entity Framework para adicionar a migração de centros de saúde.
 </p>

</b>

<p><i>
  202405231715257_HearingAidReceptor.cs
  202405231715257_HearingAidReceptor.Designer.cs
  202405231715257_HearingAidReceptor.resx:
</i></p> 
 <p>
  Arquivos gerados pelo Entity Framework para adicionar a migração de receptores de aparelhos auditivos.
 </p>

</b>

<h4>Configuration.cs</h4>
<p>
  Arquivo de configuração das migrações.
</p>

</b>

<h2>obj/</h2>
<p>
  Diretório gerado automaticamente que contém arquivos temporários de build e outros artefatos.
</p>
<p>
  WaveFit2.csproj.EntityFrameworkCore.targets
  
  WaveFit2.EntityFrameworkCore.targets: 
</p>
<p>  
  Arquivos de destino do Entity Framework Core.
</p>

</b>

<h2>Debug/</h2>
<p>
 Contém arquivos temporários de debug, caches e artefatos de compilação.
</p>

</b>

<h2>Properties/</h2>
<p>
 Contém configurações do projeto.
</p>

<p>
  AssemblyInfo.cs
  
  Contém informações de meta-dados sobre o assembly, como versão, título e descrição.
</p>

</b>

<h2>Resources/</h2>
<p>
 Diretório que contém vários recursos utilizados na aplicação, como símbolos de audiometria, modelos de microfone e perfis.
</p>
<h2>AudiometrySymbols/</h2>
<p>
    Contém imagens dos símbolos de audiometria.  
</p>

</b>

<h2>MicModel/</h2>
<p>
    Contém arquivos de texto com especificações de modelos de microfone.  
</p>

<h2>Profiles/</h2>
<p>
    Contém imagens de perfis de usuários. 
</p>

<h2>RecModel/</h2>
<p>
    Contém arquivos de texto com modelos de recepção.
</p>

<h2>Settings/</h2>
<p>
    Contém arquivos relacionados às configurações da aplicação.
</p>
<h2>Class/</h2>
<p>
  Contém classes auxiliares.
</p>
<h4>ByteToImageConverter.cs</h4>
<p>
  Classe que converte bytes em imagens.
</p>

<h4>CombinedData.cs</h4>
<p>
  Classe que combina dados de diferentes fontes.
</p>

<h2>View/</h2>
<p>
  Contém arquivos XAML para interfaces de configuração.
</p>
<h4>
EditProfileUserControl.xaml 
  
EditProfileUserControl.xaml.cs
</h4>
Interface e código-behind para edição de perfil.
</p>

<h4>
HealthCenterForms.xaml  
  
HealthCenterForms.xaml.cs
</h4>
Interface e código-behind para formulários de centro de saúde.
</p>

<h4>
HealthCenterUserControl.xaml
  
HealthCenterUserControl.xaml.cs
</h4>
Interface e código-behind para controle de usuário do centro de saúde.
</p>

<h4>
SettingsUserControl.xaml
  
SettingsUserControl.xaml.cs
</h4>
Interface e código-behind para controle de configurações.
</p>

<h4>
UsersDatagridUserControl.xaml
  
UsersDatagridUserControl.xaml.cs
</h4>
Interface e código-behind para controle de grade de dados de usuários.
</p>

<h2>ViewModel/</h2>
<p>Contém classes que implementam a lógica de apresentação para as configurações.</p>
<h4>
  HealthCenterSettingViewModel.cs
</h4>
<p>
  Lógica de apresentação para configurações do centro de saúde.
</p>

<h4>
  SettingsViewModel.cs
</h4>
<p>
  Lógica de apresentação para as configurações gerais.
</p>

<h2>Validation/</h2>

<p>Contém arquivos relacionados à validação de dados.</p>
<h4>ValidationPassword.cs</h4>
<p>Classe para validação de senhas</p>
<h4>ValidationRegister.cs</h4>
<p>
  Classe para validação de registros.
</p>
<p>
  Essa explicação detalha a função e o conteúdo de cada diretório e arquivo principal do projeto "WaveFit2".
</p>






















