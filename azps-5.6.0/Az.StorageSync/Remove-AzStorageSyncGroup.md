---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: 38c6d45c4e49f86d3aacc2774942d15ddd50941e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888141"
---
# <span data-ttu-id="8e696-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8e696-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="8e696-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e696-102">SYNOPSIS</span></span>
<span data-ttu-id="8e696-103">Este comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="8e696-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="8e696-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="8e696-104">SYNTAX</span></span>

### <span data-ttu-id="8e696-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8e696-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8e696-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e696-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e696-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e696-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e696-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="8e696-108">DESCRIPTION</span></span>
<span data-ttu-id="8e696-109">Este comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="8e696-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="8e696-110">Um grupo de sincronização só pode ser removido quando todos os pontos de extremidade contidos são excluídos primeiro.</span><span class="sxs-lookup"><span data-stu-id="8e696-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="8e696-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8e696-111">EXAMPLES</span></span>

### <span data-ttu-id="8e696-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="8e696-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="8e696-113">Este comando removerá o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="8e696-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="8e696-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="8e696-114">PARAMETERS</span></span>

### <span data-ttu-id="8e696-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e696-115">-AsJob</span></span>
<span data-ttu-id="8e696-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8e696-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e696-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e696-117">-DefaultProfile</span></span>
<span data-ttu-id="8e696-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8e696-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8e696-119">-Force</span><span class="sxs-lookup"><span data-stu-id="8e696-119">-Force</span></span>
<span data-ttu-id="8e696-120">Supply -Force para ignorar a confirmação deste comando.</span><span class="sxs-lookup"><span data-stu-id="8e696-120">Supply -Force to skip confirmation of this command.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8e696-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8e696-121">-InputObject</span></span>
<span data-ttu-id="8e696-122">Objeto de entrada SyncGroup</span><span class="sxs-lookup"><span data-stu-id="8e696-122">SyncGroup Input Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8e696-123">-Name</span><span class="sxs-lookup"><span data-stu-id="8e696-123">-Name</span></span>
<span data-ttu-id="8e696-124">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="8e696-124">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: SyncGroupName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8e696-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8e696-125">-PassThru</span></span>
<span data-ttu-id="8e696-126">Em execução normal, esse cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="8e696-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="8e696-127">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8e696-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="8e696-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e696-128">-ResourceGroupName</span></span>
<span data-ttu-id="8e696-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="8e696-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="8e696-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8e696-130">-ResourceId</span></span>
<span data-ttu-id="8e696-131">ID do Recurso SyncGroup</span><span class="sxs-lookup"><span data-stu-id="8e696-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="8e696-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="8e696-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="8e696-133">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="8e696-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="8e696-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e696-134">-Confirm</span></span>
<span data-ttu-id="8e696-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e696-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e696-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e696-136">-WhatIf</span></span>
<span data-ttu-id="8e696-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="8e696-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8e696-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8e696-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e696-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e696-139">CommonParameters</span></span>
<span data-ttu-id="8e696-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e696-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e696-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8e696-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e696-142">INPUTS</span><span class="sxs-lookup"><span data-stu-id="8e696-142">INPUTS</span></span>

### <span data-ttu-id="8e696-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="8e696-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="8e696-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8e696-144">System.String</span></span>

### <span data-ttu-id="8e696-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="8e696-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="8e696-146">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="8e696-146">OUTPUTS</span></span>

### <span data-ttu-id="8e696-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="8e696-147">System.Object</span></span>
## <span data-ttu-id="8e696-148">NOTES</span><span class="sxs-lookup"><span data-stu-id="8e696-148">NOTES</span></span>

## <span data-ttu-id="8e696-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8e696-149">RELATED LINKS</span></span>
