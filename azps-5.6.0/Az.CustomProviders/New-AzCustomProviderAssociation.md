---
external help file: ''
Module Name: Az.CustomProviders
online version: https://docs.microsoft.com/powershell/module/az.customproviders/new-azcustomproviderassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CustomProviders/help/New-AzCustomProviderAssociation.md
ms.openlocfilehash: af502cd4115ba9ef7467c15aa09b78e5e33c2337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891490"
---
# <span data-ttu-id="d8113-101">New-AzCustomProviderAssociation</span><span class="sxs-lookup"><span data-stu-id="d8113-101">New-AzCustomProviderAssociation</span></span>

## <span data-ttu-id="d8113-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8113-102">SYNOPSIS</span></span>
<span data-ttu-id="d8113-103">Criar ou atualizar uma associação.</span><span class="sxs-lookup"><span data-stu-id="d8113-103">Create or update an association.</span></span>

## <span data-ttu-id="d8113-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="d8113-104">SYNTAX</span></span>

```
New-AzCustomProviderAssociation -Name <String> -Scope <String> [-TargetResourceId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8113-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="d8113-105">DESCRIPTION</span></span>
<span data-ttu-id="d8113-106">Criar ou atualizar uma associação.</span><span class="sxs-lookup"><span data-stu-id="d8113-106">Create or update an association.</span></span>

## <span data-ttu-id="d8113-107">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d8113-107">EXAMPLES</span></span>

### <span data-ttu-id="d8113-108">Exemplo 1: Criar uma associação de provedor personalizada</span><span class="sxs-lookup"><span data-stu-id="d8113-108">Example 1: Create a custom provider association</span></span>
```powershell
PS C:\> $provider = Get-AzCustomProvider -ResourceGroupName myRg -Name Namespace.Type
PS C:\> New-AzCustomProviderAssociation -Scope $resourceId -Name MyAssoc -TargetResourceId $provider.Id

Location  Name     Type
--------  ----     ----
East US 2 MyAssoc  Microsoft.CustomProviders/associations
```

<span data-ttu-id="d8113-109">Criar uma associação de provedor personalizada, o provioder de destino associado deve ser configurado corretamente com uma rota para "associações"</span><span class="sxs-lookup"><span data-stu-id="d8113-109">Create a custom provider association, the associated target provioder must be properly configured with a route for "associations"</span></span>

## <span data-ttu-id="d8113-110">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="d8113-110">PARAMETERS</span></span>

### <span data-ttu-id="d8113-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8113-111">-AsJob</span></span>
<span data-ttu-id="d8113-112">Executar o comando como um trabalho</span><span class="sxs-lookup"><span data-stu-id="d8113-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d8113-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8113-113">-DefaultProfile</span></span>
<span data-ttu-id="d8113-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d8113-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8113-115">-Name</span><span class="sxs-lookup"><span data-stu-id="d8113-115">-Name</span></span>
<span data-ttu-id="d8113-116">O nome da associação.</span><span class="sxs-lookup"><span data-stu-id="d8113-116">The name of the association.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AssociationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8113-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d8113-117">-NoWait</span></span>
<span data-ttu-id="d8113-118">Executar o comando de forma assíncrona</span><span class="sxs-lookup"><span data-stu-id="d8113-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d8113-119">-Scope</span><span class="sxs-lookup"><span data-stu-id="d8113-119">-Scope</span></span>
<span data-ttu-id="d8113-120">O escopo da associação.</span><span class="sxs-lookup"><span data-stu-id="d8113-120">The scope of the association.</span></span>
<span data-ttu-id="d8113-121">O escopo pode ser qualquer instância de recurso REST válida.</span><span class="sxs-lookup"><span data-stu-id="d8113-121">The scope can be any valid REST resource instance.</span></span>
<span data-ttu-id="d8113-122">Por exemplo, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' para um recurso de máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="d8113-122">For example, use '/subscriptions/{subscription-id}/resourceGroups/{resource-group-name}/providers/Microsoft.Compute/virtualMachines/{vm-name}' for a virtual machine resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8113-123">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="d8113-123">-TargetResourceId</span></span>
<span data-ttu-id="d8113-124">A instância de recurso REST do recurso de destino para essa associação.</span><span class="sxs-lookup"><span data-stu-id="d8113-124">The REST resource instance of the target resource for this association.</span></span>

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

### <span data-ttu-id="d8113-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d8113-125">-Confirm</span></span>
<span data-ttu-id="d8113-126">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8113-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8113-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8113-127">-WhatIf</span></span>
<span data-ttu-id="d8113-128">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="d8113-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8113-129">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="d8113-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8113-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8113-130">CommonParameters</span></span>
<span data-ttu-id="d8113-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8113-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8113-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8113-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8113-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="d8113-133">INPUTS</span></span>

## <span data-ttu-id="d8113-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="d8113-134">OUTPUTS</span></span>

### <span data-ttu-id="d8113-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span><span class="sxs-lookup"><span data-stu-id="d8113-135">Microsoft.Azure.PowerShell.Cmdlets.CustomProviders.Models.Api20180901Preview.IAssociation</span></span>

## <span data-ttu-id="d8113-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="d8113-136">NOTES</span></span>

<span data-ttu-id="d8113-137">ALIASES</span><span class="sxs-lookup"><span data-stu-id="d8113-137">ALIASES</span></span>

## <span data-ttu-id="d8113-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d8113-138">RELATED LINKS</span></span>

