---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 4581cfea88982eee4144730b92662374ec0a5790
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598487"
---
# New-AzStorageSyncServerEndpoint

## Sinopse
Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado. Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização.

## SYNTAX

### Objectparameterset (padrão)
```
New-AzStorageSyncServerEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StringParameterSet
```
New-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -ServerResourceId <String> -ServerLocalPath <String> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ParentStringParameterSet
```
New-AzStorageSyncServerEndpoint [-ParentResourceId] <String> -Name <String> -ServerResourceId <String>
 -ServerLocalPath <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer]
 [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## DESCRITIVO
Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado. Isso permite que o caminho especificado no servidor comece a sincronizar os arquivos com outros pontos de extremidade no grupo de sincronização. Se houver arquivos em outros pontos de extremidade no grupo de sincronização e esse local recém-adicionado também contiver arquivos, um processo de reconciliação tentará determinar se os arquivos são, na verdade, os mesmos nas mesmas pastas que em outros pontos de extremidade. Os namespaces serão mesclados e a reconciliação ajudará a evitar arquivos de conflito. Se houver arquivos em outros pontos de extremidade do servidor, muitas vezes é melhor começar com um local vazio neste servidor, de modo que os arquivos da nuvem sejam inseridos no servidor em um processo automático chamado recuperação rápida de desastres. Os metadados de namespace serão sincronizados primeiro, e o fluxo de dados de cada arquivo será baixado. Se um arquivo for solicitado por um usuário ou aplicativo fora da ordem de download, esse arquivo será cancelado com prioridade para atender à solicitação de acesso. Opcionalmente, você pode usar a hierarquização na nuvem nesse ponto de extremidade do servidor para determinar se esse ponto de extremidade deve se tornar um cache do conjunto completo de arquivos da nuvem. Se a camada de nuvem for usada, o download do conteúdo do arquivo será interrompido no ponto definido pelas políticas de camada de nuvem que você pode definir.

## EXEMPLOS

### Exemplo 1
```powershell
PS C:\> $RegisteredServer = Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
PS C:\> New-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName" -ServerResourceId $RegisteredServer.ResourceId -ServerLocalPath "myServerLocalPath" -CloudTiering -OfflineDataTransfer -OfflineDataTransferShareName "myOfflineDataTransferShareName" -TierFilesOlderThanDays "myTierFilesOlderThanDays"
```

Esse comando cria um novo ponto de extremidade de servidor em um servidor registrado e o insere em um grupo de sincronização. Dessa forma, ele faz parte de uma topologia de outros pontos de extremidade, e os metadados e o conteúdo do arquivo serão iniciados imediatamente na sincronização entre todos os locais mencionados como pontos de extremidade no grupo de sincronização.

## OS

### -AsJob
Executar o cmdlet em segundo plano

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

### -OfflineDataTransfer
Parâmetro de dados propagados na nuvem

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

### -OfflineDataTransferShareName
Parâmetro de URI do compartilhamento de arquivo de dados propagados na nuvem

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

### -CloudTiering
Parâmetro de hierarquização na nuvem

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

### -DefaultProfile
As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Nome
Nome do ServerEndpoint.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServerEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ParentObject
Objeto de objeto de sincronização, normalmente passado pelo parâmetro.

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ParentResourceId
ID do recurso pai do pool de sincronização

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Nome do grupo de recursos.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerLocalPath
Parâmetro de caminho local do servidor

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerResourceId
ID do recurso de RegisteredServer

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageSyncServiceName
Nome do StorageSyncService.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SyncGroupName
Nome do The Sync.

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TierFilesOlderThanDays
O parâmetro arquivos de camada com mais de dias

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VolumeFreeSpacePercent
Parâmetro de porcentagem do espaço livre no volume

```yaml
Type: System.Nullable`1[System.Int32]
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

### Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup

### System. String

## EXIBE

### Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint

## INFORMA

## LINKS RELACIONADOS
