---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: a531ffb8a4fae50b6d352fd1167af9c13cee409c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101893175"
---
# <span data-ttu-id="07b46-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="07b46-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="07b46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07b46-102">SYNOPSIS</span></span>
<span data-ttu-id="07b46-103">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="07b46-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="07b46-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="07b46-104">SYNTAX</span></span>

### <span data-ttu-id="07b46-105">DevSpacesControllerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="07b46-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b46-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="07b46-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07b46-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="07b46-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07b46-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="07b46-108">DESCRIPTION</span></span>
<span data-ttu-id="07b46-109">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="07b46-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="07b46-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="07b46-110">EXAMPLES</span></span>

### <span data-ttu-id="07b46-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="07b46-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="07b46-112">Marque um controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="07b46-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="07b46-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="07b46-113">PARAMETERS</span></span>

### <span data-ttu-id="07b46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07b46-114">-DefaultProfile</span></span>
<span data-ttu-id="07b46-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="07b46-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07b46-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07b46-116">-InputObject</span></span>
<span data-ttu-id="07b46-117">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="07b46-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="07b46-118">-Name</span><span class="sxs-lookup"><span data-stu-id="07b46-118">-Name</span></span>
<span data-ttu-id="07b46-119">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="07b46-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="07b46-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07b46-120">-ResourceGroupName</span></span>
<span data-ttu-id="07b46-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="07b46-121">Resource group name</span></span>

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

### <span data-ttu-id="07b46-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07b46-122">-ResourceId</span></span>
<span data-ttu-id="07b46-123">A ID de recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="07b46-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="07b46-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="07b46-124">-Tag</span></span>
<span data-ttu-id="07b46-125">Uma tabela de hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="07b46-125">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07b46-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="07b46-126">-Confirm</span></span>
<span data-ttu-id="07b46-127">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="07b46-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07b46-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07b46-128">-WhatIf</span></span>
<span data-ttu-id="07b46-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="07b46-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07b46-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="07b46-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07b46-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07b46-131">CommonParameters</span></span>
<span data-ttu-id="07b46-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07b46-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07b46-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07b46-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07b46-134">INPUTS</span><span class="sxs-lookup"><span data-stu-id="07b46-134">INPUTS</span></span>

### <span data-ttu-id="07b46-135">System.String</span><span class="sxs-lookup"><span data-stu-id="07b46-135">System.String</span></span>

### <span data-ttu-id="07b46-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="07b46-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="07b46-137">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="07b46-137">OUTPUTS</span></span>

### <span data-ttu-id="07b46-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="07b46-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="07b46-139">NOTES</span><span class="sxs-lookup"><span data-stu-id="07b46-139">NOTES</span></span>

## <span data-ttu-id="07b46-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="07b46-140">RELATED LINKS</span></span>
