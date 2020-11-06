---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/remove-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Remove-AzDevSpacesController.md
ms.openlocfilehash: b6fb42ccafe5b70316ea29251a87b76ea65dda7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596622"
---
# <span data-ttu-id="ea5cf-101">Remove-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="ea5cf-101">Remove-AzDevSpacesController</span></span>

## <span data-ttu-id="ea5cf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ea5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ea5cf-103">Excluir um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-103">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="ea5cf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ea5cf-104">SYNTAX</span></span>

### <span data-ttu-id="ea5cf-105">DevSpacesControllerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="ea5cf-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5cf-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5cf-106">ResourceIdParameterSet</span></span>
```
Remove-AzDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea5cf-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ea5cf-107">InputObjectParameterSet</span></span>
```
Remove-AzDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ea5cf-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ea5cf-108">DESCRIPTION</span></span>
<span data-ttu-id="ea5cf-109">Excluir um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="ea5cf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ea5cf-110">EXAMPLES</span></span>

### <span data-ttu-id="ea5cf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ea5cf-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="ea5cf-112">Exclua um controlador de DevSpaces chamado devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="ea5cf-113">OS</span><span class="sxs-lookup"><span data-stu-id="ea5cf-113">PARAMETERS</span></span>

### <span data-ttu-id="ea5cf-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea5cf-114">-AsJob</span></span>
<span data-ttu-id="ea5cf-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="ea5cf-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ea5cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ea5cf-116">-DefaultProfile</span></span>
<span data-ttu-id="ea5cf-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ea5cf-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ea5cf-118">-InputObject</span></span>
<span data-ttu-id="ea5cf-119">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="ea5cf-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="ea5cf-120">-Name</span></span>
<span data-ttu-id="ea5cf-121">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="ea5cf-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ea5cf-122">-PassThru</span></span>
<span data-ttu-id="ea5cf-123">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="ea5cf-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="ea5cf-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea5cf-124">-ResourceGroupName</span></span>
<span data-ttu-id="ea5cf-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="ea5cf-125">Resource group name</span></span>

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

### <span data-ttu-id="ea5cf-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea5cf-126">-ResourceId</span></span>
<span data-ttu-id="ea5cf-127">A ID do recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="ea5cf-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="ea5cf-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="ea5cf-128">-Confirm</span></span>
<span data-ttu-id="ea5cf-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ea5cf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea5cf-130">-WhatIf</span></span>
<span data-ttu-id="ea5cf-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea5cf-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ea5cf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea5cf-133">CommonParameters</span></span>
<span data-ttu-id="ea5cf-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea5cf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea5cf-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea5cf-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea5cf-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ea5cf-136">INPUTS</span></span>

### <span data-ttu-id="ea5cf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ea5cf-137">System.String</span></span>

### <span data-ttu-id="ea5cf-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="ea5cf-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="ea5cf-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ea5cf-139">OUTPUTS</span></span>

### <span data-ttu-id="ea5cf-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="ea5cf-140">System.Boolean</span></span>

## <span data-ttu-id="ea5cf-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ea5cf-141">NOTES</span></span>

## <span data-ttu-id="ea5cf-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ea5cf-142">RELATED LINKS</span></span>
