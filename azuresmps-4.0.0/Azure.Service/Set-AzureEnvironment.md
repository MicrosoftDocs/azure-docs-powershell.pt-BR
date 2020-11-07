---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 1094497D-2CBE-41DF-9ED1-8E7D3F14B05A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 82bd806d35f36a07958f2bdeeeda42853cd453b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945967"
---
# Set-AzureEnvironment

## Sinopse
Altera as propriedades de um ambiente do Azure.

## SYNTAX

```
Set-AzureEnvironment -Name <String> [-PublishSettingsFileUrl <String>] [-ServiceEndpoint <String>]
 [-ManagementPortalUrl <String>] [-StorageEndpoint <String>] [-ActiveDirectoryEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-GalleryEndpoint <String>]
 [-ActiveDirectoryServiceEndpointResourceId <String>] [-GraphEndpoint <String>]
 [-AzureKeyVaultDnsSuffix <String>] [-AzureKeyVaultServiceEndpointResourceId <String>]
 [-TrafficManagerDnsSuffix <String>] [-SqlDatabaseDnsSuffix <String>] [-EnableAdfsAuthentication]
 [-AdTenant <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureEnvironment** altera as propriedades de um ambiente do Azure.
Ele retorna um objeto que representa o ambiente com seus novos valores de propriedade.
Use o parâmetro **Name** para identificar o ambiente e os outros parâmetros para alterar os valores da propriedade.
Você não pode usar **set-AzureEnvironment** para alterar o nome de um ambiente do Azure.

Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.
Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.
Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

Observação: não altere as propriedades dos ambientes AzureCloud ou AzureChinaCloud.
Use esse cmdlet para alterar os valores de ambientes privados que você criar.

## EXEMPLOS

### Exemplo 1: alterar as propriedades do ambiente
```
PS C:\> Set-AzureEnvironment -Name ContosoEnv -PublishSettingsFileUrl "https://contoso.com" -StorageEndpoint "contoso.com"
```

Esse comando altera os valores das propriedades **PublishSettingsFileUrl** e **StorageEndpoint** do ambiente ContosoEnv.

## OS

### -ActiveDirectoryEndpoint
Altera o ponto de extremidade da autenticação do Azure Active Directory para o valor especificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: AdEndpointUrl, ActiveDirectory, ActiveDirectoryAuthority

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ActiveDirectoryServiceEndpointResourceId
Especifica a ID do recurso de uma API de gerenciamento cujo acesso é gerenciado pelo Azure Active Directory.

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

### -AdTenant
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

### -AzureKeyVaultDnsSuffix
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

### -AzureKeyVaultServiceEndpointResourceId
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

### -EnableAdfsAuthentication
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: OnPremise

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GalleryEndpoint
Altera o ponto de extremidade da galeria do Gerenciador de recursos do Azure para o valor especificado.
O ponto de extremidade da galeria é o local dos modelos da Galeria de grupos de recursos.
Para obter mais informações sobre os grupos de recursos e modelos de galeria do Azure, consulte o tópico da ajuda para [Get-AzureResourceGroupGalleryTemplate](https://go.microsoft.com/fwlink/?LinkID=393052).

```yaml
Type: String
Parameter Sets: (All)
Aliases: Gallery, GalleryUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -GraphEndpoint
```yaml
Type: String
Parameter Sets: (All)
Aliases: Graph, GraphUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ManagementPortalUrl
Altera a URL do portal de gerenciamento do Azure para o valor especificado.

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

### -Nome
Identifica o ambiente que está sendo alterado.
Esse parâmetro é obrigatório.
O valor do parâmetro diferencia maiúsculas de minúsculas.
Caracteres curinga não são permitidos.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
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

### -PublishSettingsFileUrl
Altera a URL de arquivos de configurações de publicação no ambiente especificado.
Um arquivo de configurações de publicação do Azure é um arquivo XML que contém informações sobre a sua conta e um certificado de gerenciamento que permite que o Windows PowerShell entre em sua conta do Azure em seu nome.

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

### -ResourceManagerEndpoint
Altera o ponto de extremidade dos dados do Azure Resource Manager, incluindo dados sobre grupos de recursos associados à conta.
Para obter mais informações sobre o Azure Resource Manager, consulte [cmdlets do Azure Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e [uso do Windows PowerShell com o Gerenciador de recursos](https://go.microsoft.com/fwlink/?LinkID=394767) https://go.microsoft.com/fwlink/?LinkID=394767) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceManager, ResourceManagerUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceEndpoint
Altera a URL do ponto de extremidade do serviço do Azure no ambiente especificado.
O ponto de extremidade do serviço do Azure determina se o aplicativo é gerenciado pela plataforma global do Azure, Azure operado pela 21Vianet na China ou uma instalação particular do Azure.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ServiceManagement, ServiceManagementUrl

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SqlDatabaseDnsSuffix
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

### -StorageEndpoint
Altera o ponto de extremidade padrão dos serviços de armazenamento no ambiente especificado.

```yaml
Type: String
Parameter Sets: (All)
Aliases: StorageEndpointSuffix

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TrafficManagerDnsSuffix
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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma
Você pode canalizar a entrada para esse cmdlet pelo nome da propriedade, mas não por valor.

## EXIBE

### Microsoft. WindowsAzure. Commands. Utilities. Common. WindowsAzureEnvironment

## INFORMA

## LINKS RELACIONADOS

[Add-AzureEnvironment](./Add-AzureEnvironment.md)

[Get-AzureEnvironment](./Get-AzureEnvironment.md)

[Remove-AzureEnvironment](./Remove-AzureEnvironment.md)


