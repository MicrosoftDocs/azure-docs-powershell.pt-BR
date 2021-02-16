---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: dad4af4f954fae03a68728de928614a81eed5e5a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113924"
---
# <span data-ttu-id="2864a-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2864a-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="2864a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2864a-102">SYNOPSIS</span></span>
<span data-ttu-id="2864a-103">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="2864a-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="2864a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2864a-104">SYNTAX</span></span>

### <span data-ttu-id="2864a-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="2864a-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2864a-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="2864a-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2864a-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2864a-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2864a-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="2864a-108">DESCRIPTION</span></span>
<span data-ttu-id="2864a-109">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="2864a-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="2864a-110">Um grupo de sincronização só pode ser removido quando todos os pontos de extremidade contidos são excluídos primeiro.</span><span class="sxs-lookup"><span data-stu-id="2864a-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="2864a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="2864a-111">EXAMPLES</span></span>

### <span data-ttu-id="2864a-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="2864a-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="2864a-113">Esse comando removerá o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="2864a-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="2864a-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2864a-114">PARAMETERS</span></span>

### <span data-ttu-id="2864a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2864a-115">-AsJob</span></span>
<span data-ttu-id="2864a-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="2864a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2864a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2864a-117">-DefaultProfile</span></span>
<span data-ttu-id="2864a-118">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="2864a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2864a-119">-Forçar</span><span class="sxs-lookup"><span data-stu-id="2864a-119">-Force</span></span>
<span data-ttu-id="2864a-120">Supply -Force to skip confirmation of this command.</span><span class="sxs-lookup"><span data-stu-id="2864a-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="2864a-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2864a-121">-InputObject</span></span>
<span data-ttu-id="2864a-122">Objeto de entrada SyncGroup</span><span class="sxs-lookup"><span data-stu-id="2864a-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="2864a-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="2864a-123">-Name</span></span>
<span data-ttu-id="2864a-124">Nome do SyncGroup.</span><span class="sxs-lookup"><span data-stu-id="2864a-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="2864a-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2864a-125">-PassThru</span></span>
<span data-ttu-id="2864a-126">Em execução normal, este cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="2864a-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="2864a-127">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="2864a-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="2864a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2864a-128">-ResourceGroupName</span></span>
<span data-ttu-id="2864a-129">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2864a-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="2864a-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2864a-130">-ResourceId</span></span>
<span data-ttu-id="2864a-131">ID de Recurso do SyncGroup</span><span class="sxs-lookup"><span data-stu-id="2864a-131">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="2864a-132">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="2864a-132">-StorageSyncServiceName</span></span>
<span data-ttu-id="2864a-133">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="2864a-133">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="2864a-134">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="2864a-134">-Confirm</span></span>
<span data-ttu-id="2864a-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2864a-135">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2864a-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2864a-136">-WhatIf</span></span>
<span data-ttu-id="2864a-137">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="2864a-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2864a-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="2864a-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2864a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2864a-139">CommonParameters</span></span>
<span data-ttu-id="2864a-140">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2864a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2864a-141">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2864a-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2864a-142">Entradas</span><span class="sxs-lookup"><span data-stu-id="2864a-142">INPUTS</span></span>

### <span data-ttu-id="2864a-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="2864a-143">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="2864a-144">System.String</span><span class="sxs-lookup"><span data-stu-id="2864a-144">System.String</span></span>

### <span data-ttu-id="2864a-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="2864a-145">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="2864a-146">Saídas</span><span class="sxs-lookup"><span data-stu-id="2864a-146">OUTPUTS</span></span>

### <span data-ttu-id="2864a-147">System.Object</span><span class="sxs-lookup"><span data-stu-id="2864a-147">System.Object</span></span>
## <span data-ttu-id="2864a-148">Notas</span><span class="sxs-lookup"><span data-stu-id="2864a-148">NOTES</span></span>

## <span data-ttu-id="2864a-149">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2864a-149">RELATED LINKS</span></span>
