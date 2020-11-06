---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncserverendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncServerEndpoint.md
ms.openlocfilehash: 03b4ea18bc40f8ddd3a2dc2605427013c45d7506
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598470"
---
# <span data-ttu-id="87e7f-101">Set-AzStorageSyncServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87e7f-101">Set-AzStorageSyncServerEndpoint</span></span>

## <span data-ttu-id="87e7f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="87e7f-102">SYNOPSIS</span></span>
<span data-ttu-id="87e7f-103">Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="87e7f-103">This command allows for changes on the adjustable parameters of a server endpoint.</span></span>

## <span data-ttu-id="87e7f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="87e7f-104">SYNTAX</span></span>

### <span data-ttu-id="87e7f-105">Objectparameterset (padrão)</span><span class="sxs-lookup"><span data-stu-id="87e7f-105">ObjectParameterSet (Default)</span></span>
```
Set-AzStorageSyncServerEndpoint [-InputObject] <PSServerEndpoint> [-CloudTiering]
 [-VolumeFreeSpacePercent <Int32>] [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>]
 [-OfflineDataTransferShareName <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="87e7f-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e7f-106">StringParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="87e7f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="87e7f-107">ResourceIdParameterSet</span></span>
```
Set-AzStorageSyncServerEndpoint [-ResourceId] <String> [-CloudTiering] [-VolumeFreeSpacePercent <Int32>]
 [-OfflineDataTransfer] [-TierFilesOlderThanDays <Int32>] [-OfflineDataTransferShareName <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="87e7f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="87e7f-108">DESCRIPTION</span></span>
<span data-ttu-id="87e7f-109">Esse comando permite alterações nos parâmetros ajustáveis de um ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="87e7f-109">This command allows for changes on the adjustable parameters of a server endpoint.</span></span> <span data-ttu-id="87e7f-110">Por exemplo, a hierarquização da nuvem e as políticas de hierarquização na nuvem podem ser alteradas a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="87e7f-110">For instance cloud tiering and cloud tiering policies can be changed at any time.</span></span> <span data-ttu-id="87e7f-111">Vários aspectos de um ponto de extremidade do servidor, como o caminho local, não podem ser alterados após a criação do ponto de extremidade do servidor.</span><span class="sxs-lookup"><span data-stu-id="87e7f-111">Several aspects of a server endpoint, such as the local path, cannot be changed after the server endpoint had been created.</span></span>

## <span data-ttu-id="87e7f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="87e7f-112">EXAMPLES</span></span>

### <span data-ttu-id="87e7f-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="87e7f-113">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncServerEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myServerEndpointName"  -TierFilesOlderThanDays 30 -OfflineDataTransfer -OfflineDataTransfer $false
```

<span data-ttu-id="87e7f-114">Este exemplo executa duas ações, ele define uma nova política de camada de nuvem no ponto de extremidade do servidor especificado, que direciona o servidor a hierarquizar todos os arquivos que não foram acessados nos últimos 30 dias e também desabilita o modo de transferência de dados offline, que foi habilitado inicialmente nesse ponto de extremidade do servidor durante a criação.</span><span class="sxs-lookup"><span data-stu-id="87e7f-114">This example performs two actions, it sets a new cloud tiering policy on the specified server endpoint, which directs the server to tier all files that have not been accessed in the past 30 days and it also disables the offline data transfer mode, which was initially enabled on this server endpoint during it's creation.</span></span> <span data-ttu-id="87e7f-115">A transferência de dados offline é usada como parte da interoperabilidade com serviços de migração em massa, como a caixa dados do Azure.</span><span class="sxs-lookup"><span data-stu-id="87e7f-115">Offline data transfer is used as part of interoperability with bulk migration services, such as Azure Data Box.</span></span>

## <span data-ttu-id="87e7f-116">OS</span><span class="sxs-lookup"><span data-stu-id="87e7f-116">PARAMETERS</span></span>

### <span data-ttu-id="87e7f-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87e7f-117">-AsJob</span></span>
<span data-ttu-id="87e7f-118">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="87e7f-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="87e7f-119">-OfflineDataTransfer</span><span class="sxs-lookup"><span data-stu-id="87e7f-119">-OfflineDataTransfer</span></span>
<span data-ttu-id="87e7f-120">Parâmetro de dados propagados na nuvem</span><span class="sxs-lookup"><span data-stu-id="87e7f-120">Cloud Seeded Data Parameter</span></span>

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

### <span data-ttu-id="87e7f-121">-OfflineDataTransferShareName</span><span class="sxs-lookup"><span data-stu-id="87e7f-121">-OfflineDataTransferShareName</span></span>
<span data-ttu-id="87e7f-122">Parâmetro de URI do compartilhamento de arquivo de dados propagados na nuvem</span><span class="sxs-lookup"><span data-stu-id="87e7f-122">Cloud Seeded Data File Share Uri Parameter</span></span>

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

### <span data-ttu-id="87e7f-123">-CloudTiering</span><span class="sxs-lookup"><span data-stu-id="87e7f-123">-CloudTiering</span></span>
<span data-ttu-id="87e7f-124">Parâmetro de hierarquização na nuvem</span><span class="sxs-lookup"><span data-stu-id="87e7f-124">Cloud Tiering Parameter</span></span>

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

### <span data-ttu-id="87e7f-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="87e7f-125">-DefaultProfile</span></span>
<span data-ttu-id="87e7f-126">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="87e7f-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="87e7f-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="87e7f-127">-InputObject</span></span>
<span data-ttu-id="87e7f-128">Objeto de objeto de sincronização, normalmente passado pelo parâmetro.</span><span class="sxs-lookup"><span data-stu-id="87e7f-128">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="87e7f-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="87e7f-129">-Name</span></span>
<span data-ttu-id="87e7f-130">Nome do ServerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="87e7f-130">Name of the ServerEndpoint.</span></span>

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

### <span data-ttu-id="87e7f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87e7f-131">-ResourceGroupName</span></span>
<span data-ttu-id="87e7f-132">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="87e7f-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="87e7f-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="87e7f-133">-ResourceId</span></span>
<span data-ttu-id="87e7f-134">ID do recurso ServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87e7f-134">ServerEndpoint Resource Id</span></span>

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

### <span data-ttu-id="87e7f-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="87e7f-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="87e7f-136">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="87e7f-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="87e7f-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="87e7f-137">-SyncGroupName</span></span>
<span data-ttu-id="87e7f-138">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="87e7f-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="87e7f-139">-TierFilesOlderThanDays</span><span class="sxs-lookup"><span data-stu-id="87e7f-139">-TierFilesOlderThanDays</span></span>
<span data-ttu-id="87e7f-140">O parâmetro arquivos de camada com mais de dias</span><span class="sxs-lookup"><span data-stu-id="87e7f-140">Tier Files Older Than Days Parameter</span></span>

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

### <span data-ttu-id="87e7f-141">-VolumeFreeSpacePercent</span><span class="sxs-lookup"><span data-stu-id="87e7f-141">-VolumeFreeSpacePercent</span></span>
<span data-ttu-id="87e7f-142">Parâmetro de porcentagem do espaço livre no volume</span><span class="sxs-lookup"><span data-stu-id="87e7f-142">Volume Free Space Percent Parameter</span></span>

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

### <span data-ttu-id="87e7f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87e7f-143">CommonParameters</span></span>
<span data-ttu-id="87e7f-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="87e7f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87e7f-145">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87e7f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87e7f-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="87e7f-146">INPUTS</span></span>

### <span data-ttu-id="87e7f-147">System. String</span><span class="sxs-lookup"><span data-stu-id="87e7f-147">System.String</span></span>

### <span data-ttu-id="87e7f-148">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87e7f-148">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="87e7f-149">EXIBE</span><span class="sxs-lookup"><span data-stu-id="87e7f-149">OUTPUTS</span></span>

### <span data-ttu-id="87e7f-150">Microsoft. Azure. Commands. StorageSync. Models. PSServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="87e7f-150">Microsoft.Azure.Commands.StorageSync.Models.PSServerEndpoint</span></span>

## <span data-ttu-id="87e7f-151">INFORMA</span><span class="sxs-lookup"><span data-stu-id="87e7f-151">NOTES</span></span>

## <span data-ttu-id="87e7f-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="87e7f-152">RELATED LINKS</span></span>
