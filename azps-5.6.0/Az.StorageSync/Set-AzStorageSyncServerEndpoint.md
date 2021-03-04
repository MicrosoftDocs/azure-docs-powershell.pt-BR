---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 65df82b189442a32738e445a1b48093c18816bbc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888136"
---
# <span data-ttu-id="d2f0e-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2f0e-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="d2f0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f0e-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f0e-103">Este comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="d2f0e-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d2f0e-104">SYNTAX</span></span>

### <span data-ttu-id="d2f0e-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d2f0e-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f0e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2f0e-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2f0e-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d2f0e-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [LocalCacheMode] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2f0e-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d2f0e-108">DESCRIPTION</span></span>
<span data-ttu-id="d2f0e-109">Este comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="d2f0e-110">Por exemplo, as políticas de camada de nuvem e de camadas de nuvem podem ser alteradas a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="d2f0e-111">Vários aspectos de um ponto de extremidade do servidor, como o caminho local, não podem ser alterados após a criação do ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="d2f0e-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d2f0e-112">EXAMPLES</span></span>

### <span data-ttu-id="d2f0e-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d2f0e-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="d2f0e-114">Este exemplo executa duas ações, ela define uma nova política de camada de nuvem no ponto de extremidade do servidor especificado, que direciona o servidor para hierarcar todos os arquivos que não foram acessados nos últimos 30 dias e também desabilita o modo de transferência de dados offline, que foi inicialmente habilitado neste ponto de extremidade do servidor durante a criação.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="d2f0e-115">A transferência de dados offline é usada como parte da interoperabilidade com serviços de migração em massa, como a Caixa de Dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="d2f0e-116">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d2f0e-116">PARAMETERS</span></span>

### <span data-ttu-id="d2f0e-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d2f0e-117">-AsJob</span></span>
<span data-ttu-id="d2f0e-118">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="d2f0e-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d2f0e-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="d2f0e-119">-CloudTiering</span></span>
<span data-ttu-id="d2f0e-120">Parâmetro Cloud Tiering</span><span class="sxs-lookup"><span data-stu-id="d2f0e-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="d2f0e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f0e-121">-DefaultProfile</span></span>
<span data-ttu-id="d2f0e-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2f0e-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d2f0e-123">-InputObject</span></span>
<span data-ttu-id="d2f0e-124">Objeto SyncGroup, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-124">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint
Parameter Sets: ObjectParameterSet
Aliases: RegisteredServer

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f0e-125">-Name</span><span class="sxs-lookup"><span data-stu-id="d2f0e-125">-Name</span></span>
<span data-ttu-id="d2f0e-126">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-126">Name of the ServerEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ServerEndpointName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f0e-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="d2f0e-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="d2f0e-128">Parâmetro de dados de sementes na nuvem</span><span class="sxs-lookup"><span data-stu-id="d2f0e-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="d2f0e-129">-localCacheMode</span><span class="sxs-lookup"><span data-stu-id="d2f0e-129">-localCacheMode</span></span>
<span data-ttu-id="d2f0e-130">Parâmetro do modo de cache local</span><span class="sxs-lookup"><span data-stu-id="d2f0e-130">Local cache mode Parameter</span></span>

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

### <span data-ttu-id="d2f0e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f0e-131">-ResourceGroupName</span></span>
<span data-ttu-id="d2f0e-132">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="d2f0e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d2f0e-133">-ResourceId</span></span>
<span data-ttu-id="d2f0e-134">ID do Recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2f0e-134">ServerEndpoint Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f0e-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="d2f0e-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="d2f0e-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="d2f0e-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="d2f0e-137">-SyncGroupName</span></span>
<span data-ttu-id="d2f0e-138">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="d2f0e-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="d2f0e-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="d2f0e-140">Parâmetro Tier Files Older Than Days</span><span class="sxs-lookup"><span data-stu-id="d2f0e-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="d2f0e-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="d2f0e-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="d2f0e-142">Parâmetro De porcentagem de espaço livre de volume</span><span class="sxs-lookup"><span data-stu-id="d2f0e-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="d2f0e-143">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d2f0e-143">-Confirm</span></span>
<span data-ttu-id="d2f0e-144">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f0e-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2f0e-145">-WhatIf</span></span>
<span data-ttu-id="d2f0e-146">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2f0e-147">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-147">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2f0e-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f0e-148">CommonParameters</span></span>
<span data-ttu-id="d2f0e-149">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2f0e-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f0e-150">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2f0e-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f0e-151">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d2f0e-151">INPUTS</span></span>

### <span data-ttu-id="d2f0e-152">System.String</span><span class="sxs-lookup"><span data-stu-id="d2f0e-152">System.String</span></span>

### <span data-ttu-id="d2f0e-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2f0e-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="d2f0e-154">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d2f0e-154">OUTPUTS</span></span>

### <span data-ttu-id="d2f0e-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d2f0e-155">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="d2f0e-156">NOTES</span><span class="sxs-lookup"><span data-stu-id="d2f0e-156">NOTES</span></span>

## <span data-ttu-id="d2f0e-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d2f0e-157">RELATED LINKS</span></span>
