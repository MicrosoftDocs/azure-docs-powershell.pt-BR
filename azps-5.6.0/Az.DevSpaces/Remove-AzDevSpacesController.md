---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: fa535876524961dc8e7a05ca3acc5fa007f759fc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887538"
---
# <span data-ttu-id="7e975-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="7e975-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="7e975-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e975-102">SYNOPSIS</span></span>
<span data-ttu-id="7e975-103">Exclua um controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7e975-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="7e975-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="7e975-104">SYNTAX</span></span>

### <span data-ttu-id="7e975-105">DevSpacesControllerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="7e975-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e975-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e975-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7e975-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7e975-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e975-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="7e975-108">DESCRIPTION</span></span>
<span data-ttu-id="7e975-109">Exclua um controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7e975-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="7e975-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="7e975-110">EXAMPLES</span></span>

### <span data-ttu-id="7e975-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="7e975-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="7e975-112">Exclua um controlador DevSpaces chamado devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="7e975-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="7e975-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="7e975-113">PARAMETERS</span></span>

### <span data-ttu-id="7e975-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7e975-114">-AsJob</span></span>
<span data-ttu-id="7e975-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="7e975-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7e975-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e975-116">-DefaultProfile</span></span>
<span data-ttu-id="7e975-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="7e975-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e975-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e975-118">-InputObject</span></span>
<span data-ttu-id="7e975-119">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="7e975-119">A PSController object, normally passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DevSpaces.Models.PSController
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e975-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7e975-120">-Name</span></span>
<span data-ttu-id="7e975-121">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="7e975-121">DevSpaces controller name.</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e975-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7e975-122">-PassThru</span></span>
<span data-ttu-id="7e975-123">Retorna true se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="7e975-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="7e975-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e975-124">-ResourceGroupName</span></span>
<span data-ttu-id="7e975-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="7e975-125">Resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: DevSpacesControllerNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e975-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7e975-126">-ResourceId</span></span>
<span data-ttu-id="7e975-127">A ID de recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="7e975-127">The DevSpaces resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e975-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7e975-128">-Confirm</span></span>
<span data-ttu-id="7e975-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e975-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e975-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e975-130">-WhatIf</span></span>
<span data-ttu-id="7e975-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="7e975-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e975-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="7e975-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e975-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e975-133">CommonParameters</span></span>
<span data-ttu-id="7e975-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e975-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e975-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e975-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e975-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="7e975-136">INPUTS</span></span>

### <span data-ttu-id="7e975-137">System.String</span><span class="sxs-lookup"><span data-stu-id="7e975-137">System.String</span></span>

### <span data-ttu-id="7e975-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="7e975-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="7e975-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="7e975-139">OUTPUTS</span></span>

### <span data-ttu-id="7e975-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7e975-140">System.Boolean</span></span>

## <span data-ttu-id="7e975-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="7e975-141">NOTES</span></span>

## <span data-ttu-id="7e975-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="7e975-142">RELATED LINKS</span></span>
