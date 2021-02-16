---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127004"
---
# <span data-ttu-id="20e0d-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="20e0d-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="20e0d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20e0d-102">SYNOPSIS</span></span>
<span data-ttu-id="20e0d-103">Exclua um controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="20e0d-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="20e0d-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="20e0d-104">SYNTAX</span></span>

### <span data-ttu-id="20e0d-105">DevSpacesControllerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="20e0d-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e0d-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e0d-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20e0d-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20e0d-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20e0d-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="20e0d-108">DESCRIPTION</span></span>
<span data-ttu-id="20e0d-109">Exclua um controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="20e0d-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="20e0d-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="20e0d-110">EXAMPLES</span></span>

### <span data-ttu-id="20e0d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20e0d-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="20e0d-112">Exclua um controlador de DevSpaces chamado devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="20e0d-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="20e0d-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="20e0d-113">PARAMETERS</span></span>

### <span data-ttu-id="20e0d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20e0d-114">-AsJob</span></span>
<span data-ttu-id="20e0d-115">Executar cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="20e0d-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="20e0d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20e0d-116">-DefaultProfile</span></span>
<span data-ttu-id="20e0d-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20e0d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20e0d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20e0d-118">-InputObject</span></span>
<span data-ttu-id="20e0d-119">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="20e0d-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="20e0d-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="20e0d-120">-Name</span></span>
<span data-ttu-id="20e0d-121">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="20e0d-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="20e0d-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20e0d-122">-PassThru</span></span>
<span data-ttu-id="20e0d-123">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="20e0d-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="20e0d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20e0d-124">-ResourceGroupName</span></span>
<span data-ttu-id="20e0d-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="20e0d-125">Resource group name</span></span>

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

### <span data-ttu-id="20e0d-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20e0d-126">-ResourceId</span></span>
<span data-ttu-id="20e0d-127">A ID de recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="20e0d-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="20e0d-128">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="20e0d-128">-Confirm</span></span>
<span data-ttu-id="20e0d-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20e0d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20e0d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20e0d-130">-WhatIf</span></span>
<span data-ttu-id="20e0d-131">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="20e0d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20e0d-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20e0d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20e0d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20e0d-133">CommonParameters</span></span>
<span data-ttu-id="20e0d-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20e0d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20e0d-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20e0d-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20e0d-136">Entradas</span><span class="sxs-lookup"><span data-stu-id="20e0d-136">INPUTS</span></span>

### <span data-ttu-id="20e0d-137">System.String</span><span class="sxs-lookup"><span data-stu-id="20e0d-137">System.String</span></span>

### <span data-ttu-id="20e0d-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="20e0d-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="20e0d-139">Saídas</span><span class="sxs-lookup"><span data-stu-id="20e0d-139">OUTPUTS</span></span>

### <span data-ttu-id="20e0d-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20e0d-140">System.Boolean</span></span>

## <span data-ttu-id="20e0d-141">Notas</span><span class="sxs-lookup"><span data-stu-id="20e0d-141">NOTES</span></span>

## <span data-ttu-id="20e0d-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20e0d-142">RELATED LINKS</span></span>
