---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E771D1F2-A06B-44BB-AAFF-9459DC6303E6
online version: ''
schema: 2.0.0
ms.openlocfilehash: 273edfe08e4d2476cd4c1baa2967a829ec1bbcc2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945448"
---
# Select-AzureStorSimpleResource

## Sinopse
Define um recurso como o recurso atual.

## SYNTAX

```
Select-AzureStorSimpleResource -ResourceName <String> [-RegistrationKey <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Select-AzureStorSimpleResource** define um recurso como o recurso atual.
Depois de selecionar um recurso, outros cmdlets se aplicam ao contexto do recurso.

## EXEMPLOS

### Exemplo 1: selecionar um recurso pela primeira vez
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa" -RegistrationKey "<your registration key>"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Esse comando seleciona o recurso chamado Contoso64-Tsqa como o contexto atual.
Neste exemplo, o computador não tinha esse contexto inicializado anteriormente e, portanto, você deve especificar um valor para o parâmetro *RegistrationKey* .

### Exemplo 2: tentativa de selecionar um recurso
```
This command gets the current context for this computer by using the **Get-AzureStorSimpleResourceContext** cmdlet. The current selected resource is Contoso64-Tsqa. This is consistent with the previous example. 
PS C:\>Get-AzureStorSimpleResourceContext
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa 

This command attempts to reset the resource to be Contoso02-Resource. For this example, this resource has not been previously selected. The registration key is not saved or included in the command. The command cannot select the resource. 
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso02-Resource"
Select-AzureStorSimpleResource : Could not find the persisted secret. Please use Select-AzureStorSimpleResource and
provide the Registration key once again.
```

### Exemplo 3: selecionar um recurso selecionado anteriormente
```
PS C:\>Select-AzureStorSimpleResource -ResourceName "Contoso64-Tsqa"
ResourceId           ResourceName
----------           ------------
1909806764156522689  Contoso64-Tsqa
```

Esse comando seleciona o recurso chamado Contoso64-Tsqa como o contexto atual.
Neste exemplo, esse contexto foi selecionado anteriormente e, portanto, você não precisa especificar um valor para o parâmetro *RegistrationKey* .

## OS

### -Perfil
Especifica um perfil do Azure.

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

### -RegistrationKey
Especifica uma chave de registro.
Especifique uma chave na primeira vez em que você selecionar um recurso.
Depois que esse cmdlet seleciona o recurso atual, os cmdlets usam essa chave, conforme necessário.
Para obter mais informações, consulte [obter a chave de registro de serviço](https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx)  ( https://msdn.microsoft.com/en-us/library/azure/dn772346.aspx) na Microsoft Developer Network.

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

### -ResourceName
Especifica o nome do recurso a ser selecionado como o recurso atual.

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

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### Nenhuma

## EXIBE

### StorSimpleResourceContext
Esse cmdlet retorna um objeto **StorSimpleResourceContext** que contém detalhes do contexto do recurso.

## INFORMA

## LINKS RELACIONADOS

[Get-AzureStorSimpleResource](./Get-AzureStorSimpleResource.md)

[Get-AzureStorSimpleResourceContext](./Get-AzureStorSimpleResourceContext.md)


