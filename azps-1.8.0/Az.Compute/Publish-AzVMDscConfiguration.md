---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 7b8e770a37b7f196878d1650f20d08ee382f6008
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93601295"
---
# Publish-AzVMDscConfiguration

## Sinopse
Carrega um script DSC para o armazenamento de BLOBs do Azure.

## SYNTAX

### UploadArchive (padrão)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Createarchive
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Publish-AzVMDscConfiguration** carrega um script de configuração de estado desejado (DSC) no armazenamento de blob do Azure, que posteriormente pode ser aplicado às máquinas virtuais do Azure usando o cmdlet Set-AzVMDscExtension.

## EXEMPLOS

### Exemplo 1: criar um pacote. zip em carregá-lo para armazenamento do Azure
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

Esse comando cria um pacote. zip para o script fornecido e quaisquer módulos de recursos dependentes e o carrega no armazenamento do Azure.

### Exemplo 2: criar um pacote. zip e armazená-lo em um arquivo local
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

Esse comando cria um pacote. zip para o script fornecido e todos os módulos de recursos dependentes e os armazena no arquivo local que é chamado .\MyConfiguration.ps1.zip.

### Exemplo 3: adicionar configuração ao arquivo morto e, em seguida, carregá-lo para armazenamento
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

Esse comando adiciona uma configuração chamada Sample.ps1 ao arquivo morto de configuração para carregar no Azure Storage e ignora módulos de recursos dependentes.

### Exemplo 4: adicionar dados de configuração e configuração ao arquivo morto e, em seguida, carregá-los para armazenamento
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

Esse comando adiciona uma configuração chamada Sample.ps1 e dados de configuração chamados SampleData.psd1 para o arquivo morto de configuração para carregar no armazenamento do Azure.

### Exemplo 5: adicionar configuração, dados de configuração e conteúdo adicional ao arquivo morto e, em seguida, carregá-lo para armazenamento
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

Esse comando adiciona uma configuração chamada Sample.ps1, dados de configuração SampleData.psd1 e conteúdo adicional para o arquivamento de configuração para carregar no armazenamento do Azure.

## OS

### -AdditionalPath
Especifica o caminho de um arquivo ou diretório a ser incluído no arquivo de configuração.
Ele é baixado para a máquina virtual juntamente com a configuração.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Especifica o caminho de um arquivo. psd1 que especifica os dados para a configuração.
Isso é adicionado ao arquivo de configuração e, em seguida, passado para a função de configuração.
Ele é substituído pelo caminho de dados de configuração fornecido pelo cmdlet Set-AzVMDscExtension

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
Especifica o caminho de um arquivo que contém uma ou mais configurações.
O arquivo pode ser um arquivo de script do Windows PowerShell (. ps1) ou um arquivo de módulo do Windows PowerShell (. psm1).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Especifica o nome do contêiner de armazenamento do Azure no qual a configuração é carregada.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Força o comando a ser executado sem pedir confirmação do usuário.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -OutputArchivePath
Especifica o caminho de um arquivo. zip local no qual gravar o arquivo morto de configuração.
Quando esse parâmetro é usado, o script de configuração não é carregado no armazenamento do blob do Azure.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Especifica o nome do grupo de recursos que contém a conta de armazenamento.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Indica que esse cmdlet exclui dependências do recurso DSC do arquivo de configuração.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Especifica o nome da conta de armazenamento do Azure que é usado para carregar o script de configuração para o contêiner especificado pelo parâmetro *ContainerName* .

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Especifica o sufixo para o ponto de extremidade de armazenamento.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Confirme
Solicita confirmação antes de executar o cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Mostra o que aconteceria se o cmdlet fosse executado.
O cmdlet não é executado.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### System. String

### System. String []

## EXIBE

### System. String

## INFORMA

## LINKS RELACIONADOS

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


