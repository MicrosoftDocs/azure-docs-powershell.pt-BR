---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: BF5E3E1A-14B6-4630-8168-628057009D5E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 284d1601746254b2e10fdfe042e5882e94ca1bd9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946352"
---
# Get-AzureEnvironment

## Sinopse
Obtém ambientes do Azure

## SYNTAX

```
Get-AzureEnvironment [-Name <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureEnvironment** Obtém os ambientes do Azure que estão disponíveis para o Windows PowerShell.

Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.
Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.
Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

O cmdlet **Get-AzureEnvironment** Obtém ambientes do seu arquivo de dados de assinatura, e não do Azure.
Se o arquivo de dados de assinatura estiver desatualizado, execute o cmdlet **Add-AzureAccount** ou **Import-PublishSettingsFile** para atualizá-lo.

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: obter todos os ambientes
```
PS C:\> Get-AzureEnvironment

EnvironmentName               ServiceEndpoint               ResourceManagerEndpoint       PublishSettingsFileUrl
---------------               ---------------               -----------------------       ----------------------

AzureCloud                    https://management.core.wi... https://management.azure.com/ https://go.microsoft.com/fw... 
AzureChinaCloud               https://management.core.ch... https://not-supported-serv... https://go.microsoft.com/fw...
```

Esse comando obtém todos os ambientes que estão disponíveis para o Windows PowerShell.

### Exemplo 2: obter um ambiente por nome
```
PS C:\> Get-AzureEnvironment -Name AzureCloud

Name                          : AzureCloud

PublishSettingsFileUrl        : https://go.microsoft.com/fwlink/?LinkID=301775

ServiceEndpoint               : https://management.core.windows.net/

ResourceManagerEndpoint       : https://management.azure.com/

ManagementPortalUrl           : https://go.microsoft.com/fwlink/?LinkId=254433

ActiveDirectoryEndpoint       : https://login.windows.net/

ActiveDirectoryCommonTenantId : common

StorageEndpointSuffix         : core.windows.net

StorageBlobEndpointFormat     : {0}://{1}.blob.core.windows.net/

StorageQueueEndpointFormat    : {0}://{1}.queue.core.windows.net/

StorageTableEndpointFormat    : {0}://{1}.table.core.windows.net/

GalleryEndpoint               : https://gallery.azure.com/
```

Este exemplo obtém o ambiente AzureCloud.

### Exemplo 3: obter todas as propriedades de todos os ambientes
```
PS C:\> Get-AzureEnvironment | ForEach-Object {Get-AzureEnvironment -Name $_.EnvironmentName}
```

Esse comando obtém todas as propriedades de todos os ambientes.

O comando usa o cmdlet **Get-AzureEnvironment** para obter todos os ambientes do Azure para esta conta.
Em seguida, ele usa o cmdlet **ForEach-Object** para executar um comando **Get-AzureEnvironment** com o parâmetro **Name** em cada ambiente.
O valor do parâmetro **Name** é a propriedade **environmentname** de cada ambiente.

Sem parâmetros, **Get-AzureEnvironment** obtém apenas as propriedades selecionadas de um ambiente.

## OS

### -Nome
Obtém apenas o ambiente especificado.
Digite o nome do ambiente.
O valor do parâmetro diferencia maiúsculas de minúsculas.
Caracteres curinga não são permitidos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Perfil
Especifica o perfil do Azure do qual este cmdlet lê. Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### System. Management. Automation. PSCustomObject
Por padrão, **Get-AzureEnvironment** retorna um objeto personalizado.

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment
Quando você executa **Get-AzureEnvironment** com o parâmetro **Name** , ele retorna um objeto  **WindowsAzureEnvironment** .

## INFORMA

## LINKS RELACIONADOS

[Add-AzureAccount](./Add-AzureAccount.md)

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzurePublishSettingsFile](./Get-AzurePublishSettingsFile.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)

[Set-AzureEnvironment](./Set-AzureEnvironment.md)


