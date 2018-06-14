---
title: Instalar e configurar o Azure PowerShell | Microsoft Docs
description: Como instalar e configurar o Azure PowerShell para o primeiro uso.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/27/2018
ms.openlocfilehash: c9a2f7b87654de5a50d8e0f06fefc6d362532aaf
ms.sourcegitcommit: c98e3a21037ebd82936828bcb544eed902b24212
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/08/2018
ms.locfileid: "34854368"
---
# <a name="install-and-configure-azure-powershell"></a>Instalar e configurar o PowerShell do Azure

Instalar o Azure PowerShell na Galeria do PowerShell é o método preferencial de instalação.

## <a name="step-1-install-powershellget"></a>Etapa 1: Instalar o PowerShellGet

Instalar os itens da Galeria do PowerShell requer o módulo PowerShellGet. Verifique se que você tem a versão apropriada do PowerShellGet e outros requisitos do sistema. Execute o seguinte comando para ver se você tem o PowerShellGet instalado em seu sistema.

```powershell
Get-Module -Name PowerShellGet -ListAvailable | Select-Object -Property Name,Version,Path
```

Você deverá ver algo semelhante à seguinte saída:

```Output
Name          Version Path
----          ------- ----
Name          Version Path
----          ------- ----
PowerShellGet 1.6.0   C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.6.0\PowerShellGet.psd1
PowerShellGet 1.0.0.1 C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PowerShellGet.psd1
```

Você precisa do PowerShellGet versão 1.1.2.0 ou superior. Para atualizar o PowerShellGet, use o seguinte comando:

```powershell
Install-Module PowerShellGet -Force
```

Se você não tiver o PowerShellGet instalado, consulte a seção [Como obter o PowerShellGet](#how-to-get-powershellget) deste artigo.

> [!NOTE]
> Usar o PowerShellGet requer uma Política de Execução que permite executar scripts. Para obter mais informações sobre a Política de Execução do PowerShell, consulte [Sobre as Políticas de Execução](/powershell/module/microsoft.powershell.core/about/about_execution_policies).

## <a name="step-2-install-azure-powershell"></a>Etapa 2: instalar o Azure PowerShell

Instalando o Azure PowerShell a partir da Galeria do PowerShell requer privilégios elevados. Execute o comando a seguir em uma sessão do PowerShell com privilégios elevados:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Por padrão, a Galeria do PowerShell não está configurada como um repositório Confiável para o PowerShellGet. Na primeira vez em que a PSGallery for utilizada, o prompt a seguir será exibido:

```Output
Untrusted repository

You are installing the modules from an untrusted repository. If you trust this repository, change
its InstallationPolicy value by running the Set-PSRepository cmdlet.

Are you sure you want to install the modules from 'PSGallery'?
[Y] Yes  [A] Yes to All  [N] No  [L] No to All  [S] Suspend  [?] Help (default is "N"): Y
```

Responda “Sim” ou “Sim para Todos” para continuar com a instalação.

> [!NOTE]
> Caso sua versão seja mais antiga que a 2.8.5.201 do NuGet, será necessário baixar e instalar a versão mais recente do NuGet.

O AzureRM é um módulo do pacote cumulativo de atualizações para os cmdlets do Azure Resource Manager. Ao instalar o módulo AzureRM, qualquer outro módulo do Azure PowerShell que não tiver sido instalado anteriormente será baixado usando a Galeria do PowerShell.

Um erro poderá ocorrer se a versão anterior do Azure PowerShell estiver instalada. Para resolver esse problema, consulte a seção [Atualizando para uma nova versão do Azure PowerShell](#update-azps) deste artigo.

## <a name="step-3-load-the-azurerm-module"></a>Etapa 3: Carregar o módulo AzureRM
Depois de instalar o módulo, você precisa carregá-lo em sua sessão do PowerShell. Isso deve ser feito em uma sessão normal (não elevada) do PowerShell. Os módulos são carregados usando o cmdlet `Import-Module` da seguinte maneira:

```powershell
Import-Module -Name AzureRM
```

## <a name="next-steps"></a>Próximas etapas

Para obter mais informações sobre como usar o Azure PowerShell, consulte os seguintes artigos:

* [Introdução ao Azure PowerShell](get-started-azureps.md)

## <a name="frequently-asked-questions"></a>Perguntas frequentes

### <a name="how-to-get-powershellget"></a>Como obter o PowerShellGet

|Versão do SO|Instalar instruções|
|---|---|
|Tenho o Windows 10 ou o Windows Server 2016|Compilado no Windows Management Framework (WMF) 5.0 incluído no SO|
|Desejo fazer uma atualização para o PowerShell 5|[Instalar a versão mais recente do WMF](https://www.microsoft.com/en-us/download/details.aspx?id=54616)|
|Estou executando uma versão do Windows com o PowerShell 3 ou 4|[Obter os módulos PackageManagement](http://go.microsoft.com/fwlink/?LinkID=746217)|

<a id="helpmechoose"></a>
### <a name="checking-the-version-of-azure-powershell"></a>Verificando a versão do Azure PowerShell

Embora recomendemos que você atualize para a última versão o mais cedo possível, várias versões do Azure PowerShell têm suporte. Para determinar a versão do Azure PowerShell instalada, execute `Get-Module AzureRM` na linha de comando.

```powershell
Get-Module AzureRM -ListAvailable | Select-Object -Property Name,Version,Path
```

### <a name="support-for-classic-deployment-methods"></a>Suporte para métodos de implantação clássicos

Se você tiver implantações que usam o modelo de implantação clássico, será possível instalar a versão de Gerenciamento de Serviços do Azure PowerShell. Para obter mais informações, veja [Instalar o módulo Gerenciamento de Serviços do Azure PowerShell](/powershell/azure/servicemanagement/install-azure-ps). Os módulos Azure e AzureRM compartilham dependências em comum. Caso você use ambos os módulos, Azure e AzureRM, instale a mesma versão de cada pacote.

### <a id="update-azps"></a>Atualizando para uma nova versão do Azure PowerShell

Se houver uma versão anterior do Azure PowerShell instalada que inclua o módulo de Gerenciamento de Serviços, o seguinte erro poderá ocorrer:

```Output
PackageManagement\Install-Package : A command with name 'Get-AzureStorageContainerAcl' is already
available on this system. This module 'Azure.Storage' may override the existing commands. If you
still want to install this module 'Azure.Storage', use -AllowClobber parameter.

At C:\Program Files\WindowsPowerShell\Modules\PowerShellGet\1.0.0.1\PSModule.psm1:1772 char:21
+ ...          $null = PackageManagement\Install-Package @PSBoundParameters
+                      ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    + CategoryInfo          : InvalidOperation: (Microsoft.Power....InstallPackage:InstallPackage) [Install-Package], Exception
    + FullyQualifiedErrorId : CommandAlreadyAvailable,Validate-ModuleCommandAlreadyAvailable,Microsoft.PowerShell.PackageManagement.Cmdlets.InstallPackage
```

Assim como indicado pela mensagem de erro, é necessário usar o parâmetro AllowClobber para instalar o módulo. Use o seguinte comando:

```powershell
# Install the Azure Resource Manager modules from the PowerShell Gallery
Install-Module -Name AzureRM -AllowClobber
```

Para saber mais, confira o tópico de ajuda para [Install-Module](https://msdn.microsoft.com/powershell/reference/5.1/PowerShellGet/install-module).

### <a name="installing-module-versions-side-by-side"></a>Instalando versões de módulo lado a lado

O método PowerShellGet de instalação é o único método que suporta a instalação de diversas versões. Por exemplo, é possível ter scripts escritos usando uma versão anterior do Azure PowerShell que você não tem tempo nem recursos para atualizar. Os comandos a seguir ilustram como instalar diversas versões do Azure PowerShell:

```powershell
Install-Module -Name AzureRM -RequiredVersion 3.7.0
Install-Module -Name AzureRM -RequiredVersion 1.2.9
```

somente uma versão do módulo pode ser carregada em uma sessão do PowerShell. Você deve abrir uma nova janela do PowerShell e usar `Import-Module` para importar uma versão específica dos cmdlets do AzureRM:

```powershell
Import-Module -Name AzureRM -RequiredVersion 1.2.9
```

> [!NOTE]
> A versão 2.1.0 e a versão 1.2.6 são as primeiras versões do módulo projetadas para ser instaladas e usadas lado a lado. Ao carregar uma versão anterior do Azure PowerShell, versões incompatíveis do módulo **AzureRM.Profile** serão carregadas. Desse modo, os cmdlets solicitarão que você faça logon sempre que um cmdlet for executado.

### <a name="other-installation-methods"></a>Outros métodos de instalação

Para obter informações sobre como instalar usando o Web Platform Installer ou o Pacote MSI, consulte [Outros métodos de instalação](other-install.md)
