---
external help file: Microsoft.WindowsAzure.Commands.Profile.dll-Help.xml
ms.assetid: 6185C6BA-460E-4EEA-B1EF-CD67629AA75E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51c20ef378cd2629ea96f236339a97172fb3038e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945950"
---
# Set-AzureSubscription

## Sinopse
Altera uma assinatura do Azure.

## SYNTAX

### UpdateSubscriptionByIdParameterSetName (padrão)
```
Set-AzureSubscription -SubscriptionId <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### UpdateSubscriptionByNameParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> [-Certificate <X509Certificate2>] [-ServiceEndpoint <String>]
 [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>] [-Context <AzureStorageContext>]
 [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### AddSubscriptionParameterSetName
```
Set-AzureSubscription -SubscriptionName <String> -SubscriptionId <String> -Certificate <X509Certificate2>
 [-ServiceEndpoint <String>] [-ResourceManagerEndpoint <String>] [-CurrentStorageAccountName <String>]
 [-Context <AzureStorageContext>] [-Environment <String>] [-PassThru] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureSubscription** estabelece e altera as propriedades de um objeto de assinatura do Azure.
Você pode usar esse cmdlet para trabalhar em uma assinatura do Azure que não seja a sua assinatura padrão ou alterar sua conta de armazenamento atual.
Para obter informações sobre as assinaturas atual e padrão, consulte o cmdlet **Select-AzureSubscription** .

Esse cmdlet opera em um objeto de assinatura do Azure, não na sua assinatura real do Azure.
Para criar e provisionar uma assinatura do Azure, acesse o [portal do Azure](https://azure.microsoft.com/) ( https://azure.microsoft.com/) .

Esse cmdlet altera os dados no arquivo de dados de assinatura que você cria quando usa o cmdlet **Add-AzureAccount** ou **Import-AzurePublishSettingsFile** para adicionar uma conta do Azure ao Windows PowerShell.

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: alterar um subscription1 existente
```
C:\PS> $thumbprint = <Thumbprint-2>
C:\PS> $differentCert = Get-Item cert:\\CurrentUser\My\$thumbprint 
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $differentCert
```

Este exemplo altera o certificado para a assinatura chamada ContosoEngineering.

### Exemplo 2: alterar o ponto de extremidade do serviço
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -ServiceEndpoint "https://management.core.contoso.com"
```

Esse comando adiciona ou altera um ponto de extremidade de serviço personalizado para a assinatura do ContosoEngineering.

### Exemplo 3: limpar valores de propriedade
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoEngineering -Certificate $null -ResourceManagerEndpoint $Null
```

Esse comando define os valores das propriedades Certificate e ResourceManagerEndpoint como NULL ($Null).
Isso limpa os valores dessas propriedades sem alterar outras configurações.

### Exemplo 4: usar um arquivo de dados de assinatura alternativo
```
C:\PS> Set-AzureSubscription -SubscriptionName ContosoFinance -SubscriptionDataFile C:\Azure\SubscriptionData.xml -CurrentStorageAccount ContosoStorage01
```

Esse comando altera a conta de armazenamento atual da assinatura do ContosoFinance para o ContosoStorage01.
O comando usa o parâmetro **SubscriptionDataFile** para alterar os dados no arquivo de dados de assinatura do C:\Azure\SubscriptionData.xml.
Por padrão, **set-AzureSubscription** usa o arquivo de dados de assinatura padrão em seu perfil de usuário móvel.

## OS

### -Certificado
```yaml
Type: X509Certificate2
Parameter Sets: UpdateSubscriptionByIdParameterSetName, UpdateSubscriptionByNameParameterSetName
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: X509Certificate2
Parameter Sets: AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Contexto
```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CurrentStorageAccountName
```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Ambiente
Especifica um ambiente do Azure.

Um ambiente do Azure uma implantação independente do Microsoft Azure, como o AzureCloud para global Azure e o AzureChinaCloud para Azure operado pela 21Vianet na China.
Você também pode criar ambientes do Azure locais usando o Azure Pack e os cmdlets do WAPack.
Para obter mais informações, consulte [Azure Pack](https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx)  ( https://www.microsoft.com/server-cloud/products/windows-azure-pack/default.aspx) .

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Retorna $True se o comando tiver êxito e $False se falhar.
Por padrão, esse cmdlet não retorna nenhuma saída.
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
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

### -ResourceManagerEndpoint
Especifica o ponto de extremidade dos dados do Azure Resource Manager, incluindo dados sobre grupos de recursos associados à conta.
Para obter mais informações sobre o Azure Resource Manager, consulte [cmdlets do Azure Resource Manager](https://go.microsoft.com/fwlink/?LinkID=394765)  ( https://go.microsoft.com/fwlink/?LinkID=394765) e [uso do Windows PowerShell com o Gerenciador de recursos](https://go.microsoft.com/fwlink/?LinkID=394767) https://go.microsoft.com/fwlink/?LinkID=394767) .

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

### -ServiceEndpoint
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

### -SubscriptionId
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByIdParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Subscriptionname
```yaml
Type: String
Parameter Sets: UpdateSubscriptionByNameParameterSetName, AddSubscriptionParameterSetName
Aliases: 

Required: True
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

### None ou System. Boolean
Quando você usa o parâmetro *PassThru* , esse cmdlet retorna um valor booliano.
Por padrão, esse cmdlet não retorna nenhuma saída.

## INFORMA

## LINKS RELACIONADOS

[Add-AzureAccount](./Add-AzureAccount.md)

[Get-AzureSubscription](./Get-AzureSubscription.md)

[Import-AzurePublishSettingsFile](./Import-AzurePublishSettingsFile.md)

[Remove-AzureSubscription](./Remove-AzureSubscription.md)

[Select-AzureSubscription](./Select-AzureSubscription.md)


