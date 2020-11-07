---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 23aab4561e8127c67be4d9f751b250bc3fb6d1a0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772663"
---
# <span data-ttu-id="14afe-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="14afe-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="14afe-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="14afe-102">SYNOPSIS</span></span>
<span data-ttu-id="14afe-103">Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="14afe-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="14afe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="14afe-104">SYNTAX</span></span>

### <span data-ttu-id="14afe-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="14afe-105">StringParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14afe-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="14afe-106">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14afe-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="14afe-107">ObjectParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14afe-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="14afe-108">DESCRIPTION</span></span>
<span data-ttu-id="14afe-109">Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="14afe-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="14afe-110">Por exemplo, a hierarquização da nuvem e as políticas de hierarquização na nuvem podem ser alteradas a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="14afe-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="14afe-111">Vários aspectos de um ponto de extremidade do servidor, como o caminho local, não podem ser alterados após a criação do ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="14afe-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="14afe-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="14afe-112">EXAMPLES</span></span>

### <span data-ttu-id="14afe-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="14afe-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="14afe-114">Este exemplo executa duas ações, ele define uma nova política de camada de nuvem no ponto de extremidade do servidor especificado, que direciona o servidor a hierarquizar todos os arquivos que não foram acessados nos últimos 30 dias e também desabilita o modo de transferência de dados offline, que foi habilitado inicialmente nesse ponto de extremidade do servidor durante a criação.</span><span class="sxs-lookup"><span data-stu-id="14afe-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="14afe-115">A transferência de dados offline é usada como parte da interoperabilidade com serviços de migração em massa, como a caixa dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="14afe-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="14afe-116">OS</span><span class="sxs-lookup"><span data-stu-id="14afe-116">PARAMETERS</span></span>

### <span data-ttu-id="14afe-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="14afe-117">-AsJob</span></span>
<span data-ttu-id="14afe-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="14afe-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="14afe-119">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="14afe-119">-CloudTiering</span></span>
<span data-ttu-id="14afe-120">Parâmetro de hierarquização na nuvem</span><span class="sxs-lookup"><span data-stu-id="14afe-120">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="14afe-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14afe-121">-DefaultProfile</span></span>
<span data-ttu-id="14afe-122">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="14afe-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14afe-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="14afe-123">-InputObject</span></span>
<span data-ttu-id="14afe-124">Objeto de objeto de sincronização, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="14afe-124">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="14afe-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="14afe-125">-Name</span></span>
<span data-ttu-id="14afe-126">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="14afe-126">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="14afe-127">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="14afe-127">-OfflineDataTransfer</span></span>
<span data-ttu-id="14afe-128">Parâmetro de dados propagados na nuvem</span><span class="sxs-lookup"><span data-stu-id="14afe-128">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="14afe-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14afe-129">-ResourceGroupName</span></span>
<span data-ttu-id="14afe-130">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="14afe-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="14afe-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14afe-131">-ResourceId</span></span>
<span data-ttu-id="14afe-132">ID do recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="14afe-132">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="14afe-133">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="14afe-133">-StorageSyncServiceName</span></span>
<span data-ttu-id="14afe-134">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="14afe-134">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="14afe-135">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="14afe-135">-SyncGroupName</span></span>
<span data-ttu-id="14afe-136">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="14afe-136">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="14afe-137">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="14afe-137">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="14afe-138">O parâmetro arquivos de camada com mais de dias</span><span class="sxs-lookup"><span data-stu-id="14afe-138">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="14afe-139">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="14afe-139">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="14afe-140">Parâmetro de porcentagem do espaço livre no volume</span><span class="sxs-lookup"><span data-stu-id="14afe-140">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="14afe-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="14afe-141">-Confirm</span></span>
<span data-ttu-id="14afe-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14afe-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14afe-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14afe-143">-WhatIf</span></span>
<span data-ttu-id="14afe-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="14afe-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14afe-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="14afe-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14afe-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14afe-146">CommonParameters</span></span>
<span data-ttu-id="14afe-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14afe-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14afe-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14afe-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14afe-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="14afe-149">INPUTS</span></span>

### <span data-ttu-id="14afe-150">System. String</span><span class="sxs-lookup"><span data-stu-id="14afe-150">System.String</span></span>

### <span data-ttu-id="14afe-151">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="14afe-151">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="14afe-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="14afe-152">OUTPUTS</span></span>

### <span data-ttu-id="14afe-153">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="14afe-153">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="14afe-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="14afe-154">NOTES</span></span>

## <span data-ttu-id="14afe-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="14afe-155">RELATED LINKS</span></span>