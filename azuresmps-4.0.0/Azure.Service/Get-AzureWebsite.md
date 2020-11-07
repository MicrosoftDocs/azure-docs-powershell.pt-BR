---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E4B1AA31-1185-4035-86E6-2BB2587285C6
online version: ''
schema: 2.0.0
ms.openlocfilehash: a8273613081ab6bab0c9c3481df90f5b680b3355
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93946274"
---
# Get-AzureWebsite

## Sinopse
Obtém os sites do Azure na assinatura atual.

## SYNTAX

```
Get-AzureWebsite [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureWebsite** Obtém informações sobre os sites do Azure na assinatura atual.

Por padrão, **Get-AzureWebsite** Obtém todos os websites do Azure na assinatura atual e retorna um objeto que fornece informações básicas sobre os sites.
Quando você usa o parâmetro *Name* , **Get-AzureWebsite** retorna um objeto com informações abrangentes, incluindo detalhes de configuração.

A assinatura atual é a assinatura designada como "atual". Para localizar a assinatura atual, use o parâmetro *atual* do cmdlet [Get-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397623) .
Para alterar a assinatura atual, use o cmdlet [Select-AzureSubscription](https://go.microsoft.com/fwlink/?LinkID=397628) .

Este tópico descreve o cmdlet na versão 0.8.10 do módulo do Microsoft Azure PowerShell.
Para obter a versão do módulo que você está usando, no console do PowerShell do Azure, digite `(Get-Module -Name Azure).Version` .

## EXEMPLOS

### Exemplo 1: obter todos os sites na assinatura
```
PS C:\> Get-AzureWebsite
```

Este comando obtém todos os websites do Azure na assinatura atual.

### Exemplo 2: obter um site por nome
```
PS C:\> Get-AzureWebsite -Name ContosoWeb
```

Esse comando obtém informações detalhadas sobre o site do Azure ContosoWeb, incluindo informações de configuração.
Quando você usa o parâmetro *Name* , **Get-AzureWebsite** retorna um objeto **SiteWithConfig** com informações estendidas sobre o site.

### Exemplo 3: obter informações detalhadas sobre todos os sites
```
PS C:\> Get-AzureWebsite | ForEach-Object {Get-AzureWebsite -Name $_.Name}
```

Este comando obtém informações detalhadas sobre todos os sites na assinatura.
Ele usa um comando **Get-AzureWebsite** para obter todos os sites e, em seguida, usa o cmdlet **ForEach-Object** para obter cada site por nome.

### Exemplo 4: obter informações sobre um slot de implantação
```
PS C:\> Get-AzureWebsite -Name ContosoWeb -Slot Staging
```

Esse comando obtém o slot de implantação de preparo do site do ContosoWeb.
Os slots de implantação permitem testar versões diferentes do seu site do Azure sem liberá-los para o público.

### Exemplo 5: obter instâncias de site
```
PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances

InstanceId
----------
2d8e712fb8f85d061c30fd793a534e6700a175f9a9ab12ca55cb3b0edfcc10ee
5834916b8cef49249b18187708223a33fbbc4352d33b48369f3166644bdd3445

PS C:\>(Get-AzureWebsite -Name ContosoWeb).Instances.Count
2
```

Os comandos neste exemplo usam a propriedade instances de um site do Azure para obter informações sobre instâncias de sites em execução no momento.
A propriedade **Instances** foi adicionada ao objeto **SiteWithConfig** na versão 0.8.3 do módulo do Azure.

O primeiro comando obtém as IDs de instância de todas as instâncias atualmente em execução de um site.
O segundo comando obtém o número de instâncias em execução do site.
Você pode usar a propriedade **Count** em qualquer matriz.

## OS

### -Nome
Obtém informações de configuração detalhadas sobre o site especificado.
Digite o nome de um site na assinatura.
Por padrão, **Get-AzureWebsite** Obtém todos os sites na assinatura atual.
O valor de *nome* não oferece suporte a caracteres curinga.

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
Especifica o perfil do Azure do qual este cmdlet lê.
Se você não especificar um perfil, esse cmdlet lerá do perfil padrão local.

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

### -Slot
Obtém o slot de implantação especificado do site.
Digite o nome do slot, como "preparação" ou "produção".
Para obter mais informações sobre slots de implantação, consulte implantação em estágios em sites do Microsoft Azure https://azure.microsoft.com/en-us/documentation/articles/web-sites-staged-publishing/ .
Para adicionar um slot de implantação a um site do Azure existente, use o cmdlet Set-AzureWebsite.

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

### Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. site
Por padrão, **Get-AzureWebsite** retorna uma matriz de objetos do **site** .

### Microsoft. WindowsAzure. Commands. Utilities. sites. Services. webentities. SiteWithConfig
Quando você usa o parâmetro *Name* , **Get-AzureWebsite** retorna um objeto **SiteWithConfig** .

## INFORMA

## LINKS RELACIONADOS

[New-AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Start-AzureWebsite](./Start-AzureWebsite.md)

[Parar-AzureWebsite](./Stop-AzureWebsite.md)

[Show-AzureWebsite](./Show-AzureWebsite.md)


