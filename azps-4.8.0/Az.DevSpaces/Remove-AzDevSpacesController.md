---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: ae183daeeb2e4bbc18f141c20a79be74118245c0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115000"
---
# <span data-ttu-id="5c6cc-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="5c6cc-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="5c6cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="5c6cc-102">SYNOPSIS</span></span>
<span data-ttu-id="5c6cc-103">Excluir um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="5c6cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5c6cc-104">SYNTAX</span></span>

### <span data-ttu-id="5c6cc-105">DevSpacesControllerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="5c6cc-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c6cc-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c6cc-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5c6cc-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5c6cc-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c6cc-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="5c6cc-108">DESCRIPTION</span></span>
<span data-ttu-id="5c6cc-109">Excluir um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="5c6cc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5c6cc-110">EXAMPLES</span></span>

### <span data-ttu-id="5c6cc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5c6cc-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="5c6cc-112">Exclua um controlador de DevSpaces chamado devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="5c6cc-113">OS</span><span class="sxs-lookup"><span data-stu-id="5c6cc-113">PARAMETERS</span></span>

### <span data-ttu-id="5c6cc-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5c6cc-114">-AsJob</span></span>
<span data-ttu-id="5c6cc-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="5c6cc-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5c6cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c6cc-116">-DefaultProfile</span></span>
<span data-ttu-id="5c6cc-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5c6cc-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5c6cc-118">-InputObject</span></span>
<span data-ttu-id="5c6cc-119">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="5c6cc-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="5c6cc-120">-Name</span></span>
<span data-ttu-id="5c6cc-121">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="5c6cc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5c6cc-122">-PassThru</span></span>
<span data-ttu-id="5c6cc-123">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="5c6cc-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="5c6cc-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c6cc-124">-ResourceGroupName</span></span>
<span data-ttu-id="5c6cc-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="5c6cc-125">Resource group name</span></span>

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

### <span data-ttu-id="5c6cc-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5c6cc-126">-ResourceId</span></span>
<span data-ttu-id="5c6cc-127">A ID do recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="5c6cc-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="5c6cc-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="5c6cc-128">-Confirm</span></span>
<span data-ttu-id="5c6cc-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c6cc-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c6cc-130">-WhatIf</span></span>
<span data-ttu-id="5c6cc-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c6cc-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c6cc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c6cc-133">CommonParameters</span></span>
<span data-ttu-id="5c6cc-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c6cc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c6cc-135">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c6cc-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c6cc-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="5c6cc-136">INPUTS</span></span>

### <span data-ttu-id="5c6cc-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5c6cc-137">System.String</span></span>

### <span data-ttu-id="5c6cc-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="5c6cc-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="5c6cc-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="5c6cc-139">OUTPUTS</span></span>

### <span data-ttu-id="5c6cc-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5c6cc-140">System.Boolean</span></span>

## <span data-ttu-id="5c6cc-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="5c6cc-141">NOTES</span></span>

## <span data-ttu-id="5c6cc-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5c6cc-142">RELATED LINKS</span></span>
