---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azhostgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzHostGroup.md
ms.openlocfilehash: 17397d2bd1056b6e4280d560b2640abcacb1250a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93784926"
---
# <span data-ttu-id="62d6e-101">Remove-AzHostGroup</span><span class="sxs-lookup"><span data-stu-id="62d6e-101">Remove-AzHostGroup</span></span>

## <span data-ttu-id="62d6e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="62d6e-102">SYNOPSIS</span></span>
<span data-ttu-id="62d6e-103">Remove um grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="62d6e-103">Removes a host group.</span></span>

## <span data-ttu-id="62d6e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62d6e-104">SYNTAX</span></span>

### <span data-ttu-id="62d6e-105">Defaultparameter (padrão)</span><span class="sxs-lookup"><span data-stu-id="62d6e-105">DefaultParameter (Default)</span></span>
```
Remove-AzHostGroup [-ResourceGroupName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d6e-106">ResourceIdParameter</span><span class="sxs-lookup"><span data-stu-id="62d6e-106">ResourceIdParameter</span></span>
```
Remove-AzHostGroup [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="62d6e-107">ObjectParameter</span><span class="sxs-lookup"><span data-stu-id="62d6e-107">ObjectParameter</span></span>
```
Remove-AzHostGroup [-InputObject] <PSHostGroup> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62d6e-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="62d6e-108">DESCRIPTION</span></span>
<span data-ttu-id="62d6e-109">Este cmdlet excluirá um grupo de hosts</span><span class="sxs-lookup"><span data-stu-id="62d6e-109">This cmdlet will delete a Host group</span></span>

## <span data-ttu-id="62d6e-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="62d6e-110">EXAMPLES</span></span>

### <span data-ttu-id="62d6e-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="62d6e-111">Example 1</span></span>
```
PS C:\> Get-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName | Remove-AzHostGroup
```

<span data-ttu-id="62d6e-112">Esse comando obtém e remove o grupo host fornecido.</span><span class="sxs-lookup"><span data-stu-id="62d6e-112">This command gets and removes the given host group.</span></span>

### <span data-ttu-id="62d6e-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="62d6e-113">Example 2</span></span>
```
PS C:\> Remove-AzHostGroup -ResourceGroupName $resourceGroupName -HostGroupName $hostGroupName
```

<span data-ttu-id="62d6e-114">Esse comando Remove o grupo de hosts fornecido.</span><span class="sxs-lookup"><span data-stu-id="62d6e-114">This command removes the given host group.</span></span>

## <span data-ttu-id="62d6e-115">OS</span><span class="sxs-lookup"><span data-stu-id="62d6e-115">PARAMETERS</span></span>

### <span data-ttu-id="62d6e-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="62d6e-116">-AsJob</span></span>
<span data-ttu-id="62d6e-117">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="62d6e-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="62d6e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d6e-118">-DefaultProfile</span></span>
<span data-ttu-id="62d6e-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="62d6e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62d6e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="62d6e-120">-InputObject</span></span>
<span data-ttu-id="62d6e-121">O objeto local do grupo host.</span><span class="sxs-lookup"><span data-stu-id="62d6e-121">The local object of the host group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup
Parameter Sets: ObjectParameter
Aliases: HostGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d6e-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="62d6e-122">-Name</span></span>
<span data-ttu-id="62d6e-123">O nome do grupo de hosts.</span><span class="sxs-lookup"><span data-stu-id="62d6e-123">The name of the host group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases: HostGroupName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d6e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d6e-124">-ResourceGroupName</span></span>
<span data-ttu-id="62d6e-125">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="62d6e-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DefaultParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d6e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62d6e-126">-ResourceId</span></span>
<span data-ttu-id="62d6e-127">A ID do recurso.</span><span class="sxs-lookup"><span data-stu-id="62d6e-127">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameter
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62d6e-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="62d6e-128">-Confirm</span></span>
<span data-ttu-id="62d6e-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62d6e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62d6e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62d6e-130">-WhatIf</span></span>
<span data-ttu-id="62d6e-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="62d6e-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62d6e-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="62d6e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62d6e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d6e-133">CommonParameters</span></span>
<span data-ttu-id="62d6e-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62d6e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d6e-135">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="62d6e-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d6e-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="62d6e-136">INPUTS</span></span>

### <span data-ttu-id="62d6e-137">System. String</span><span class="sxs-lookup"><span data-stu-id="62d6e-137">System.String</span></span>

### <span data-ttu-id="62d6e-138">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSHostGroup</span><span class="sxs-lookup"><span data-stu-id="62d6e-138">Microsoft.Azure.Commands.Compute.Automation.Models.PSHostGroup</span></span>

## <span data-ttu-id="62d6e-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="62d6e-139">OUTPUTS</span></span>

### <span data-ttu-id="62d6e-140">Microsoft. Azure. Commands. COMPUTE. Automation. Models. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="62d6e-140">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="62d6e-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="62d6e-141">NOTES</span></span>

## <span data-ttu-id="62d6e-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="62d6e-142">RELATED LINKS</span></span>
