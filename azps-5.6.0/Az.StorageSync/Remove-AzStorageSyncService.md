---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/remove-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Remove-AzStorageSyncService.md
ms.openlocfilehash: 648ef711d030f7600863d286df24cfdf1d2f7927
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888138"
---
# <span data-ttu-id="a5d23-101">Remove-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a5d23-101">Remove-AzStorageSyncService</span></span>

## <span data-ttu-id="a5d23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5d23-102">SYNOPSIS</span></span>
<span data-ttu-id="a5d23-103">Este comando excluirá o serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="a5d23-103">This command will delete the specified storage sync service.</span></span>

## <span data-ttu-id="a5d23-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="a5d23-104">SYNTAX</span></span>

### <span data-ttu-id="a5d23-105">StringParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="a5d23-105">StringParameterSet (Default)</span></span>
```
Remove-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d23-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d23-106">InputObjectParameterSet</span></span>
```
Remove-AzStorageSyncService [-InputObject] <PSStorageSyncService> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5d23-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a5d23-107">ResourceIdParameterSet</span></span>
```
Remove-AzStorageSyncService [-ResourceId] <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5d23-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="a5d23-108">DESCRIPTION</span></span>
<span data-ttu-id="a5d23-109">Este comando excluirá o serviço de sincronização de armazenamento especificado.</span><span class="sxs-lookup"><span data-stu-id="a5d23-109">This command will delete the specified storage sync service.</span></span> <span data-ttu-id="a5d23-110">Um serviço de sincronização de armazenamento só pode ser removido quando todos os grupos de sincronização contidos e servidores registrados são excluídos primeiro.</span><span class="sxs-lookup"><span data-stu-id="a5d23-110">A storage sync service can only be removed when all of the contained sync groups and registered servers are deleted first.</span></span>

## <span data-ttu-id="a5d23-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a5d23-111">EXAMPLES</span></span>

### <span data-ttu-id="a5d23-112">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a5d23-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStorageSyncService -Force -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="a5d23-113">Este comando removerá o serviço de sincronização de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="a5d23-113">This command will remove the storage sync service.</span></span>

## <span data-ttu-id="a5d23-114">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="a5d23-114">PARAMETERS</span></span>

### <span data-ttu-id="a5d23-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5d23-115">-AsJob</span></span>
<span data-ttu-id="a5d23-116">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="a5d23-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a5d23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5d23-117">-DefaultProfile</span></span>
<span data-ttu-id="a5d23-118">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a5d23-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5d23-119">-Force</span><span class="sxs-lookup"><span data-stu-id="a5d23-119">-Force</span></span>
<span data-ttu-id="a5d23-120">Supply -Force para ignorar a confirmação deste comando.</span><span class="sxs-lookup"><span data-stu-id="a5d23-120">Supply -Force to skip confirmation of this command.</span></span>

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

### <span data-ttu-id="a5d23-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5d23-121">-InputObject</span></span>
<span data-ttu-id="a5d23-122">Objeto de entrada StorageSyncService, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="a5d23-122">StorageSyncService Input Object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5d23-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a5d23-123">-Name</span></span>
<span data-ttu-id="a5d23-124">Nome do StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="a5d23-124">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5d23-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5d23-125">-PassThru</span></span>
<span data-ttu-id="a5d23-126">Em execução normal, esse cmdlet não retorna nenhum valor sobre o sucesso.</span><span class="sxs-lookup"><span data-stu-id="a5d23-126">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="a5d23-127">Se você fornecer o parâmetro PassThru, o cmdlet gravará um valor no pipeline após a execução bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="a5d23-127">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="a5d23-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5d23-128">-ResourceGroupName</span></span>
<span data-ttu-id="a5d23-129">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="a5d23-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="a5d23-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5d23-130">-ResourceId</span></span>
<span data-ttu-id="a5d23-131">ID do Recurso StorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a5d23-131">StorageSyncService Resource Id</span></span>

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

### <span data-ttu-id="a5d23-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a5d23-132">-Confirm</span></span>
<span data-ttu-id="a5d23-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5d23-133">Prompts for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5d23-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5d23-134">-WhatIf</span></span>
<span data-ttu-id="a5d23-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="a5d23-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5d23-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a5d23-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5d23-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5d23-137">CommonParameters</span></span>
<span data-ttu-id="a5d23-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5d23-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5d23-139">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5d23-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5d23-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="a5d23-140">INPUTS</span></span>

### <span data-ttu-id="a5d23-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="a5d23-141">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="a5d23-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a5d23-142">System.String</span></span>

### <span data-ttu-id="a5d23-143">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a5d23-143">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a5d23-144">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="a5d23-144">OUTPUTS</span></span>

### <span data-ttu-id="a5d23-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="a5d23-145">System.Object</span></span>
## <span data-ttu-id="a5d23-146">NOTES</span><span class="sxs-lookup"><span data-stu-id="a5d23-146">NOTES</span></span>

## <span data-ttu-id="a5d23-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a5d23-147">RELATED LINKS</span></span>
