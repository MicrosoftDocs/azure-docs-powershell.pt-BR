---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: FCE4633A-4F75-4A23-B825-6AC62238658A
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryReplicationProtectedItem.md
ms.openlocfilehash: 2070a26a1bfdb41e5135479548f04bdbaced6884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429069"
---
# Set-AzureRmSiteRecoveryReplicationProtectedItem

## Sinopse
Define propriedades de recuperação, como a rede de destino e o tamanho da máquina virtual para um item protegido de replicação.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## SYNTAX

```
Set-AzureRmSiteRecoveryReplicationProtectedItem -ReplicationProtectedItem <ASRReplicationProtectedItem>
 [-Name <String>] [-Size <String>] [-PrimaryNic <String>] [-RecoveryNetworkId <String>]
 [-RecoveryNicSubnetName <String>] [-RecoveryNicStaticIPAddress <String>] [-NicSelectionType <String>]
 [-LicenseType <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
O cmdlet **set-AzureRmSiteRecoveryReplicationProtectedItem** define as propriedades de recuperação para um item protegido de replicação.

## EXEMPLOS

## OS

### -LicenseType
Especifica a seleção do tipo de licença para máquinas virtuais do Windows Server migradas por meio do benefício de uso híbrido.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NoLicenseType, WindowsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Especifica o nome da máquina virtual de recuperação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -NicSelectionType
Especifica as propriedades da NIC (placa de interface de rede) definidas por usuário ou definidas por padrão.
Você pode especificar não selecionado para voltar aos valores padrão.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: NotSelected, SelectedByUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryNic
Especifica a NIC da máquina virtual para a qual esse cmdlet define a propriedade de rede de recuperação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNetworkId
Especifica a ID da rede virtual do Azure para a qual esse cmdlet recupera o item protegido.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNicStaticIPAddress
Especifica o endereço IP estático que deve ser atribuído à NIC primária na recuperação.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -RecoveryNicSubnetName
Especifica o nome da sub-rede na rede virtual do Azure de recuperação para a qual esse cmdlet recupera o item protegido.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ReplicationProtectedItem
Especifica o item protegido de replicação do Azure site Recovery.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Tamanho
Especifica o tamanho da máquina virtual de recuperação.
O valor deve ser do conjunto de tamanhos com suporte nas máquinas virtuais do Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable. Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## SENSORES

### ASRReplicationProtectedItem
O parâmetro ' ReplicationProtectedItem ' aceita o valor do tipo ' ASRReplicationProtectedItem ' do pipeline

## EXIBE

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## INFORMA

## LINKS RELACIONADOS

[Get-AzureRmSiteRecoveryReplicationProtectedItem](./Get-AzureRmSiteRecoveryReplicationProtectedItem.md)

[New-AzureRmSiteRecoveryReplicationProtectedItem](./New-AzureRmSiteRecoveryReplicationProtectedItem.md)

[Remove-AzureRmSiteRecoveryReplicationProtectedItem](./Remove-AzureRmSiteRecoveryReplicationProtectedItem.md)
