---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890004"
---
# <span data-ttu-id="550d1-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="550d1-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="550d1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="550d1-102">SYNOPSIS</span></span>
<span data-ttu-id="550d1-103">Remove um recurso de acesso ao disco.</span><span class="sxs-lookup"><span data-stu-id="550d1-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="550d1-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="550d1-104">SYNTAX</span></span>

### <span data-ttu-id="550d1-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="550d1-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="550d1-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="550d1-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="550d1-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="550d1-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="550d1-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="550d1-108">DESCRIPTION</span></span>
<span data-ttu-id="550d1-109">O cmdlet **Remove-AzDiskAccess** remove um recurso de acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="550d1-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="550d1-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="550d1-110">EXAMPLES</span></span>

### <span data-ttu-id="550d1-111">Exemplo 1: remover o acesso ao disco usando o conjunto de parâmetros padrão</span><span class="sxs-lookup"><span data-stu-id="550d1-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="550d1-112">Este comando remove o acesso ao disco chamado "DiskAccess01" no grupo de recursos "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="550d1-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="550d1-113">Exemplo 2: Remover o Acesso ao Disco usando a ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="550d1-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="550d1-114">Este comando remove o acesso ao disco pela ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="550d1-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="550d1-115">Exemplo 3: remover o acesso ao disco usando o objeto Input</span><span class="sxs-lookup"><span data-stu-id="550d1-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="550d1-116">Este comando remove o acesso ao disco por InputObject</span><span class="sxs-lookup"><span data-stu-id="550d1-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="550d1-117">Exemplo 4: remover o acesso ao disco canalização do objeto input</span><span class="sxs-lookup"><span data-stu-id="550d1-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="550d1-118">Este comando remove o acesso ao disco canalização do InputObject</span><span class="sxs-lookup"><span data-stu-id="550d1-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="550d1-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="550d1-119">PARAMETERS</span></span>

### <span data-ttu-id="550d1-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="550d1-120">-AsJob</span></span>
<span data-ttu-id="550d1-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="550d1-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="550d1-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="550d1-122">-DefaultProfile</span></span>
<span data-ttu-id="550d1-123">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="550d1-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="550d1-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="550d1-124">-InputObject</span></span>
<span data-ttu-id="550d1-125">Objeto De Acesso ao Disco do PowerShell</span><span class="sxs-lookup"><span data-stu-id="550d1-125">PowerShell Disk Access Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess
Parameter Sets: InputObjectParameterSet
Aliases: DiskAccess

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="550d1-126">-Name</span><span class="sxs-lookup"><span data-stu-id="550d1-126">-Name</span></span>
<span data-ttu-id="550d1-127">Especifica o nome de um acesso em disco.</span><span class="sxs-lookup"><span data-stu-id="550d1-127">Specifies the name of a disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases: DiskAccessName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550d1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="550d1-128">-ResourceGroupName</span></span>
<span data-ttu-id="550d1-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="550d1-129">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550d1-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="550d1-130">-ResourceId</span></span>
<span data-ttu-id="550d1-131">ID do recurso para o acesso ao disco.</span><span class="sxs-lookup"><span data-stu-id="550d1-131">Resource ID for your disk access.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIDParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="550d1-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="550d1-132">-Confirm</span></span>
<span data-ttu-id="550d1-133">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="550d1-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="550d1-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="550d1-134">-WhatIf</span></span>
<span data-ttu-id="550d1-135">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="550d1-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="550d1-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="550d1-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="550d1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="550d1-137">CommonParameters</span></span>
<span data-ttu-id="550d1-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="550d1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="550d1-139">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="550d1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="550d1-140">INPUTS</span><span class="sxs-lookup"><span data-stu-id="550d1-140">INPUTS</span></span>

### <span data-ttu-id="550d1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="550d1-141">System.String</span></span>

### <span data-ttu-id="550d1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="550d1-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="550d1-143">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="550d1-143">OUTPUTS</span></span>

### <span data-ttu-id="550d1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="550d1-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="550d1-145">NOTES</span><span class="sxs-lookup"><span data-stu-id="550d1-145">NOTES</span></span>

## <span data-ttu-id="550d1-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="550d1-146">RELATED LINKS</span></span>
