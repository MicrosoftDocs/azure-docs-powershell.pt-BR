---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/az.storagesync/remove-azstoragesyncgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncGroup.md
ms.openlocfilehash: f7c1f129d9a5f6f6bdd117597a2943567fb4001d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93598481"
---
# <span data-ttu-id="ae56f-101">Remove-AzStorageSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ae56f-101">Remove-AzStorageSyncGroup</span></span>

## <span data-ttu-id="ae56f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ae56f-102">SYNOPSIS</span></span>
<span data-ttu-id="ae56f-103">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="ae56f-103">This command will delete the specified sync group.</span></span>

## <span data-ttu-id="ae56f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ae56f-104">SYNTAX</span></span>

### <span data-ttu-id="ae56f-105">StringParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ae56f-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncGroup [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-Name] <String>
 [-Force] [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae56f-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae56f-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-InputObject] <PSSyncGroup> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae56f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae56f-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncGroup [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae56f-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ae56f-108">DESCRIPTION</span></span>
<span data-ttu-id="ae56f-109">Esse comando excluirá o grupo de sincronização especificado.</span><span class="sxs-lookup"><span data-stu-id="ae56f-109">This command will delete the specified sync group.</span></span> <span data-ttu-id="ae56f-110">Um grupo de sincronização só poderá ser removido quando todos os pontos de extremidade contidos forem excluídos primeiro.</span><span class="sxs-lookup"><span data-stu-id="ae56f-110">A sync group can only be removed when all of the contained endpoints are deleted first.</span></span>

## <span data-ttu-id="ae56f-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae56f-111">EXAMPLES</span></span>

### <span data-ttu-id="ae56f-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae56f-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncGroup -Force -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -Name "mySyncGroupName"
```

<span data-ttu-id="ae56f-113">Esse comando irá remover o grupo de sincronização.</span><span class="sxs-lookup"><span data-stu-id="ae56f-113">This command will remove the sync group.</span></span>

## <span data-ttu-id="ae56f-114">OS</span><span class="sxs-lookup"><span data-stu-id="ae56f-114">PARAMETERS</span></span>

### <span data-ttu-id="ae56f-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ae56f-115">-AsJob</span></span>
<span data-ttu-id="ae56f-116">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ae56f-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ae56f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae56f-117">-DefaultProfile</span></span>
<span data-ttu-id="ae56f-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae56f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae56f-119">-Force</span><span class="sxs-lookup"><span data-stu-id="ae56f-119">-Force</span></span>
<span data-ttu-id="ae56f-120">Supply-Force para ignorar a confirmação desse comando.</span><span class="sxs-lookup"><span data-stu-id="ae56f-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="ae56f-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ae56f-121">-InputObject</span></span>
<span data-ttu-id="ae56f-122">Objeto de entrada do objeto de sincronização</span><span class="sxs-lookup"><span data-stu-id="ae56f-122">SyncGroup Input Object</span></span>

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

### <span data-ttu-id="ae56f-123">-Nome</span><span class="sxs-lookup"><span data-stu-id="ae56f-123">-Name</span></span>
<span data-ttu-id="ae56f-124">Nome do The Sync.</span><span class="sxs-lookup"><span data-stu-id="ae56f-124">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="ae56f-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ae56f-125">-PassThru</span></span>
<span data-ttu-id="ae56f-126">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="ae56f-126">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="ae56f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae56f-127">-ResourceGroupName</span></span>
<span data-ttu-id="ae56f-128">Nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae56f-128">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae56f-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ae56f-129">-ResourceId</span></span>
<span data-ttu-id="ae56f-130">ID do recurso do pool de sincronização</span><span class="sxs-lookup"><span data-stu-id="ae56f-130">SyncGroup Resource Id</span></span>

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

### <span data-ttu-id="ae56f-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="ae56f-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="ae56f-132">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="ae56f-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="ae56f-133">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ae56f-133">-Confirm</span></span>
<span data-ttu-id="ae56f-134">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae56f-134">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae56f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae56f-135">-WhatIf</span></span>
<span data-ttu-id="ae56f-136">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ae56f-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ae56f-137">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ae56f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae56f-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae56f-138">CommonParameters</span></span>
<span data-ttu-id="ae56f-139">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae56f-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae56f-140">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae56f-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae56f-141">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ae56f-141">INPUTS</span></span>

### <span data-ttu-id="ae56f-142">Microsoft. Azure. Commands. StorageSync. Models. PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="ae56f-142">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="ae56f-143">System. String</span><span class="sxs-lookup"><span data-stu-id="ae56f-143">System.String</span></span>

### <span data-ttu-id="ae56f-144">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ae56f-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ae56f-145">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ae56f-145">OUTPUTS</span></span>

### <span data-ttu-id="ae56f-146">System. Object</span><span class="sxs-lookup"><span data-stu-id="ae56f-146">System.Object</span></span>
## <span data-ttu-id="ae56f-147">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ae56f-147">NOTES</span></span>

## <span data-ttu-id="ae56f-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae56f-148">RELATED LINKS</span></span>
