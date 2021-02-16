---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzDiskAccess.md
ms.openlocfilehash: 4b67364f0d079c7cd5fbbdd89b1a84b4dc6fee0e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117851"
---
# <span data-ttu-id="8af49-101">Remove-AzDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8af49-101">Remove-AzDiskAccess</span></span>

## <span data-ttu-id="8af49-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8af49-102">SYNOPSIS</span></span>
<span data-ttu-id="8af49-103">Remove um recurso de acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="8af49-103">Removes a disk access resource.</span></span>

## <span data-ttu-id="8af49-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8af49-104">SYNTAX</span></span>

### <span data-ttu-id="8af49-105">DefaultParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="8af49-105">DefaultParameterSet (Default)</span></span>
```
Remove-AzDiskAccess [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af49-106">ResourceIDParameterSet</span><span class="sxs-lookup"><span data-stu-id="8af49-106">ResourceIDParameterSet</span></span>
```
Remove-AzDiskAccess [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8af49-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8af49-107">InputObjectParameterSet</span></span>
```
Remove-AzDiskAccess [-InputObject] <PSDiskAccess> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8af49-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="8af49-108">DESCRIPTION</span></span>
<span data-ttu-id="8af49-109">O **cmdlet Remove-AzDiskAccess** remove um recurso de acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="8af49-109">The **Remove-AzDiskAccess** cmdlet removes a disk access resource.</span></span>

## <span data-ttu-id="8af49-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="8af49-110">EXAMPLES</span></span>

### <span data-ttu-id="8af49-111">Exemplo 1: Remover Acesso a Disco usando o Conjunto de Parâmetros Padrão</span><span class="sxs-lookup"><span data-stu-id="8af49-111">Example 1: Remove Disk Access using Default Parameter Set</span></span>
```
PS C:\> Remove-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
```

<span data-ttu-id="8af49-112">Esse comando remove o acesso a disco chamado "DiskAccess01" no grupo de recursos "ResourceGroup01"</span><span class="sxs-lookup"><span data-stu-id="8af49-112">This command removes the disk access named "DiskAccess01" in resource group "ResourceGroup01"</span></span>

### <span data-ttu-id="8af49-113">Exemplo 2: Remover o Acesso a Disco usando a ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="8af49-113">Example 2: Remove Disk Access using Resource ID</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -ResourceId $myDiskAccess.id
```

<span data-ttu-id="8af49-114">Esse comando remove o acesso a disco por ID do Recurso</span><span class="sxs-lookup"><span data-stu-id="8af49-114">This command removes the disk access by Resource ID</span></span>

### <span data-ttu-id="8af49-115">Exemplo 3: Remover o Acesso a Disco usando o Objeto de Entrada</span><span class="sxs-lookup"><span data-stu-id="8af49-115">Example 3: Remove Disk Access using Input Object</span></span>
```
PS C:\> $myDiskAccess = Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01"
PS C:\> Remove-AzDiskAccess -InputObject $myDiskAccess
```

<span data-ttu-id="8af49-116">Este comando remove o acesso a disco por InputObject</span><span class="sxs-lookup"><span data-stu-id="8af49-116">This command removes the disk access by InputObject</span></span>

### <span data-ttu-id="8af49-117">Exemplo 4: remover o acesso ao disco por meio da canalização de objeto de entrada</span><span class="sxs-lookup"><span data-stu-id="8af49-117">Example 4: Remove Disk Access by piping Input Object</span></span>
```
PS C:\> Get-AzDiskAccess -ResourceGroupName "ResourceGroup01" -Name "DiskAccess01" | Remove-AzDiskAccess 
```

<span data-ttu-id="8af49-118">Este comando remove o acesso a disco por meio de uma canalização do InputObject</span><span class="sxs-lookup"><span data-stu-id="8af49-118">This command removes the disk access by piping the InputObject</span></span>

## <span data-ttu-id="8af49-119">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8af49-119">PARAMETERS</span></span>

### <span data-ttu-id="8af49-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8af49-120">-AsJob</span></span>
<span data-ttu-id="8af49-121">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="8af49-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8af49-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8af49-122">-DefaultProfile</span></span>
<span data-ttu-id="8af49-123">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8af49-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8af49-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8af49-124">-InputObject</span></span>
<span data-ttu-id="8af49-125">Objeto de Acesso a Disco do PowerShell</span><span class="sxs-lookup"><span data-stu-id="8af49-125">PowerShell Disk Access Object</span></span>

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

### <span data-ttu-id="8af49-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="8af49-126">-Name</span></span>
<span data-ttu-id="8af49-127">Especifica o nome de um acesso a disco.</span><span class="sxs-lookup"><span data-stu-id="8af49-127">Specifies the name of a disk access.</span></span>

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

### <span data-ttu-id="8af49-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8af49-128">-ResourceGroupName</span></span>
<span data-ttu-id="8af49-129">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8af49-129">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="8af49-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8af49-130">-ResourceId</span></span>
<span data-ttu-id="8af49-131">ID do recurso para seu acesso em disco.</span><span class="sxs-lookup"><span data-stu-id="8af49-131">Resource ID for your disk access.</span></span>

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

### <span data-ttu-id="8af49-132">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="8af49-132">-Confirm</span></span>
<span data-ttu-id="8af49-133">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8af49-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8af49-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8af49-134">-WhatIf</span></span>
<span data-ttu-id="8af49-135">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="8af49-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8af49-136">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="8af49-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8af49-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8af49-137">CommonParameters</span></span>
<span data-ttu-id="8af49-138">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8af49-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8af49-139">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8af49-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8af49-140">Entradas</span><span class="sxs-lookup"><span data-stu-id="8af49-140">INPUTS</span></span>

### <span data-ttu-id="8af49-141">System.String</span><span class="sxs-lookup"><span data-stu-id="8af49-141">System.String</span></span>

### <span data-ttu-id="8af49-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span><span class="sxs-lookup"><span data-stu-id="8af49-142">Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskAccess</span></span>

## <span data-ttu-id="8af49-143">Saídas</span><span class="sxs-lookup"><span data-stu-id="8af49-143">OUTPUTS</span></span>

### <span data-ttu-id="8af49-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="8af49-144">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="8af49-145">Notas</span><span class="sxs-lookup"><span data-stu-id="8af49-145">NOTES</span></span>

## <span data-ttu-id="8af49-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8af49-146">RELATED LINKS</span></span>
