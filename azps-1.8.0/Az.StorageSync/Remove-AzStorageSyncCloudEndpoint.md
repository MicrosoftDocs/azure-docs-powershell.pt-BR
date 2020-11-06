---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 2d9ad2417041f39ea43f48813310869f1ea7f353
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598482"
---
# <span data-ttu-id="1695b-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1695b-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="1695b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1695b-102">SYNOPSIS</span></span>
<span data-ttu-id="1695b-103">Esse comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1695b-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="1695b-104">Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade do servidor neste grupo de sincronização pode sincronizar.</span><span class="sxs-lookup"><span data-stu-id="1695b-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="1695b-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1695b-105">SYNTAX</span></span>

### <span data-ttu-id="1695b-106">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1695b-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1695b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1695b-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1695b-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1695b-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1695b-109">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1695b-109">DESCRIPTION</span></span>
<span data-ttu-id="1695b-110">Esse comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1695b-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="1695b-111">O compartilhamento de arquivo do Azure as referências de ponto de extremidade de nuvem permanecem intocadas por esse processo.</span><span class="sxs-lookup"><span data-stu-id="1695b-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="1695b-112">Este comando destina-se apenas a descomissionamento.</span><span class="sxs-lookup"><span data-stu-id="1695b-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="1695b-113">A remoção de um ponto de extremidade de nuvem é uma operação destrutiva.</span><span class="sxs-lookup"><span data-stu-id="1695b-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="1695b-114">Os pontos de extremidade do servidor não podem ser sincronizados sem haver pelo menos um ponto de extremidade de nuvem.</span><span class="sxs-lookup"><span data-stu-id="1695b-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="1695b-115">Esta operação não deve ser realizada para solucionar problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="1695b-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="1695b-116">Se esse compartilhamento de arquivos do Azure for adicionado novamente ao mesmo grupo de sincronização, como um ponto de extremidade de nuvem, ele poderá levar a arquivos conflitantes e a outras conseqüências indesejadas.</span><span class="sxs-lookup"><span data-stu-id="1695b-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="1695b-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1695b-117">EXAMPLES</span></span>

### <span data-ttu-id="1695b-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1695b-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="1695b-119">Esse comando removerá o ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="1695b-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="1695b-120">OS</span><span class="sxs-lookup"><span data-stu-id="1695b-120">PARAMETERS</span></span>

### <span data-ttu-id="1695b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1695b-121">-AsJob</span></span>
<span data-ttu-id="1695b-122">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="1695b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1695b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1695b-123">-DefaultProfile</span></span>
<span data-ttu-id="1695b-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1695b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1695b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="1695b-125">-Force</span></span>
<span data-ttu-id="1695b-126">Supply-Force para ignorar a confirmação desse comando.</span><span class="sxs-lookup"><span data-stu-id="1695b-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="1695b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1695b-127">-InputObject</span></span>
<span data-ttu-id="1695b-128">Objeto de entrada CloudEndpoint, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1695b-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1695b-129">-Nome</span><span class="sxs-lookup"><span data-stu-id="1695b-129">-Name</span></span>
<span data-ttu-id="1695b-130">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="1695b-130">Name of the CloudEndpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1695b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1695b-131">-PassThru</span></span>
<span data-ttu-id="1695b-132">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="1695b-132">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1695b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1695b-133">-ResourceGroupName</span></span>
<span data-ttu-id="1695b-134">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1695b-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="1695b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1695b-135">-ResourceId</span></span>
<span data-ttu-id="1695b-136">ID do recurso CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1695b-136">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="1695b-137">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="1695b-137">-StorageSyncServiceName</span></span>
<span data-ttu-id="1695b-138">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="1695b-138">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1695b-139">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="1695b-139">-SyncGroupName</span></span>
<span data-ttu-id="1695b-140">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="1695b-140">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1695b-141">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1695b-141">-Confirm</span></span>
<span data-ttu-id="1695b-142">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1695b-142">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1695b-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1695b-143">-WhatIf</span></span>
<span data-ttu-id="1695b-144">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1695b-144">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1695b-145">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1695b-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1695b-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1695b-146">CommonParameters</span></span>
<span data-ttu-id="1695b-147">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1695b-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1695b-148">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1695b-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1695b-149">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1695b-149">INPUTS</span></span>

### <span data-ttu-id="1695b-150">Microsoft. Azure. Commands. StorageSync. Models. PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="1695b-150">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="1695b-151">System. String</span><span class="sxs-lookup"><span data-stu-id="1695b-151">System.String</span></span>

## <span data-ttu-id="1695b-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1695b-152">OUTPUTS</span></span>

### <span data-ttu-id="1695b-153">System. Object</span><span class="sxs-lookup"><span data-stu-id="1695b-153">System.Object</span></span>
## <span data-ttu-id="1695b-154">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1695b-154">NOTES</span></span>

## <span data-ttu-id="1695b-155">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1695b-155">RELATED LINKS</span></span>
