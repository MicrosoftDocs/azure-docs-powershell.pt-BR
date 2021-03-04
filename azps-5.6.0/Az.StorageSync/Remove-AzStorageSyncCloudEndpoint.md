---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 451df6b0608ece9888b1525388784dcee1aac334
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888145"
---
# <span data-ttu-id="9031b-101">Remove-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9031b-101">Remove-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="9031b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9031b-102">SYNOPSIS</span></span>
<span data-ttu-id="9031b-103">Este comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9031b-103">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="9031b-104">Sem pelo menos um ponto de extremidade de nuvem, nenhum outro ponto de extremidade de servidor neste grupo de sincronização pode sincronizar.</span><span class="sxs-lookup"><span data-stu-id="9031b-104">Without at least one cloud endpoint, no other server endpoints in this sync group can sync.</span></span>

## <span data-ttu-id="9031b-105">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="9031b-105">SYNTAX</span></span>

### <span data-ttu-id="9031b-106">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9031b-106">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9031b-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9031b-107">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-InputObject] <PSCloudEndpoint> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9031b-108">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9031b-108">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncCloudEndpoint [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9031b-109">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="9031b-109">DESCRIPTION</span></span>
<span data-ttu-id="9031b-110">Este comando excluirá o ponto de extremidade de nuvem especificado de um grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9031b-110">This command will delete the specified cloud endpoint from a sync group.</span></span> <span data-ttu-id="9031b-111">O arquivo do Azure compartilha as referências do ponto de extremidade da nuvem permanece intocada por esse processo.</span><span class="sxs-lookup"><span data-stu-id="9031b-111">The Azure file share the cloud endpoint references remains untouched by this process.</span></span> <span data-ttu-id="9031b-112">Este comando destina-se apenas ao descomissionamento.</span><span class="sxs-lookup"><span data-stu-id="9031b-112">This command is only intended for decommissioning.</span></span> <span data-ttu-id="9031b-113">Remover um ponto de extremidade de nuvem é uma operação destrutiva.</span><span class="sxs-lookup"><span data-stu-id="9031b-113">Removing a cloud endpoint is a destructive operation.</span></span> <span data-ttu-id="9031b-114">Os pontos de extremidade do servidor não podem sincronizar sem pelo menos um ponto de extremidade de nuvem presente.</span><span class="sxs-lookup"><span data-stu-id="9031b-114">Server endpoints cannot sync without at least one cloud endpoint present.</span></span> <span data-ttu-id="9031b-115">Essa operação não deve ser executada para resolver problemas de sincronização.</span><span class="sxs-lookup"><span data-stu-id="9031b-115">This operation should not be performed to solve sync issues.</span></span> <span data-ttu-id="9031b-116">Se esse compartilhamento de arquivos do Azure for adicionado novamente ao mesmo grupo de sincronização, como um ponto de extremidade de nuvem, ele poderá levar a arquivos de conflito e outras consequências não intencionais.</span><span class="sxs-lookup"><span data-stu-id="9031b-116">If this Azure file share is added again to the same sync group, as a cloud endpoint, it can lead to conflict files and other unintended consequences.</span></span>

## <span data-ttu-id="9031b-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="9031b-117">EXAMPLES</span></span>

### <span data-ttu-id="9031b-118">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="9031b-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncCloudEndpoint -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName"
```

<span data-ttu-id="9031b-119">Este comando removerá o ponto de extremidade da nuvem.</span><span class="sxs-lookup"><span data-stu-id="9031b-119">This command will remove the cloud endpoint.</span></span>

## <span data-ttu-id="9031b-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="9031b-120">PARAMETERS</span></span>

### <span data-ttu-id="9031b-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9031b-121">-AsJob</span></span>
<span data-ttu-id="9031b-122">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="9031b-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9031b-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9031b-123">-DefaultProfile</span></span>
<span data-ttu-id="9031b-124">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9031b-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9031b-125">-Force</span><span class="sxs-lookup"><span data-stu-id="9031b-125">-Force</span></span>
<span data-ttu-id="9031b-126">Supply -Force para ignorar a confirmação deste comando.</span><span class="sxs-lookup"><span data-stu-id="9031b-126">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="9031b-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9031b-127">-InputObject</span></span>
<span data-ttu-id="9031b-128">Objeto de entrada CloudEndpoint, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="9031b-128">CloudEndpoint Input Object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="9031b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="9031b-129">-Name</span></span>
<span data-ttu-id="9031b-130">Nome do CloudEndpoint.</span><span class="sxs-lookup"><span data-stu-id="9031b-130">Name of the CloudEndpoint.</span></span>

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

### <span data-ttu-id="9031b-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9031b-131">-PassThru</span></span>
<span data-ttu-id="9031b-132">Em execução normal, esse cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="9031b-132">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="9031b-133">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="9031b-133">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="9031b-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9031b-134">-ResourceGroupName</span></span>
<span data-ttu-id="9031b-135">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="9031b-135">Resource Group Name.</span></span>

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

### <span data-ttu-id="9031b-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9031b-136">-ResourceId</span></span>
<span data-ttu-id="9031b-137">ID do Recurso CloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9031b-137">CloudEndpoint Resource Id</span></span>

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

### <span data-ttu-id="9031b-138">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="9031b-138">-StorageSyncServiceName</span></span>
<span data-ttu-id="9031b-139">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="9031b-139">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="9031b-140">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="9031b-140">-SyncGroupName</span></span>
<span data-ttu-id="9031b-141">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="9031b-141">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="9031b-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9031b-142">-Confirm</span></span>
<span data-ttu-id="9031b-143">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9031b-143">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9031b-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9031b-144">-WhatIf</span></span>
<span data-ttu-id="9031b-145">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="9031b-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9031b-146">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="9031b-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9031b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9031b-147">CommonParameters</span></span>
<span data-ttu-id="9031b-148">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9031b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9031b-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9031b-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9031b-150">INPUTS</span><span class="sxs-lookup"><span data-stu-id="9031b-150">INPUTS</span></span>

### <span data-ttu-id="9031b-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="9031b-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

### <span data-ttu-id="9031b-152">System.String</span><span class="sxs-lookup"><span data-stu-id="9031b-152">System.String</span></span>

## <span data-ttu-id="9031b-153">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="9031b-153">OUTPUTS</span></span>

### <span data-ttu-id="9031b-154">System.Object</span><span class="sxs-lookup"><span data-stu-id="9031b-154">System.Object</span></span>
## <span data-ttu-id="9031b-155">NOTES</span><span class="sxs-lookup"><span data-stu-id="9031b-155">NOTES</span></span>

## <span data-ttu-id="9031b-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9031b-156">RELATED LINKS</span></span>
