---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 00B8AB6D-02E0-45B5-AB69-49FC69246A34
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb66f34cea13ac95cac47738e7cec214a6a10103
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 07/18/2020
ms.locfileid: "93945583"
---
# Get-AzureSiteRecoveryRecoveryPlanFile

## Sinopse
Baixa um plano do Azure site Recovery no formato XML.

## SYNTAX

### ByRPObject (padrão)
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -RecoveryPlan <ASRRecoveryPlan>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### ById
```
Get-AzureSiteRecoveryRecoveryPlanFile -Path <String> -Id <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **Get-AzureSiteRecoveryRecoveryPlanFile** baixa um plano do Azure site Recovery no formato XML.
Você pode usar esse arquivo para atualizar o plano de recuperação e depois carregá-lo no servidor de recuperação de site.

Um plano de recuperação reúne máquinas virtuais em um grupo para fins de failover e recuperação.

## EXEMPLOS

### Exemplo 1: obter um arquivo de plano de recuperação
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan 
PS C:\> Get-AzureSiteRecoveryRecoveryPlanFile -RecoveryPlan $RecoveryPlan -Path "C:\Users\Contoso\Desktop\RecoveryPlan.xml"
```

Esse comando usa o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** para obter o plano de recuperação e, em seguida, armazena-o na variável $RecoveryPlan.

O segundo comando usa o cmdlet **GetAzureSiteRecoveryRecoveryPlanFile** para obter o arquivo XML de plano de recuperação do site no $RecoveryPlan.
O comando armazena o arquivo XML no caminho especificado.

## OS

### -ID
Especifica a ID do plano de recuperação a ser obtido.

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Caminho
Especifica o caminho completo para armazenar o arquivo XML do plano de recuperação.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -RecoveryPlan
Especifica um objeto **ASRRecoveryPlan** do qual obter o plano de recuperação.
Para obter um objeto **ASRRecoveryPlan** , use o cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

## EXIBE

## INFORMA

## LINKS RELACIONADOS

[Get-AzureSiteRecoveryRecoveryPlan](./Get-AzureSiteRecoveryRecoveryPlan.md)


