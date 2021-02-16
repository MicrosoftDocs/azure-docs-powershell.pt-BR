---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100117686"
---
# <span data-ttu-id="b5204-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="b5204-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="b5204-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b5204-102">SYNOPSIS</span></span>
<span data-ttu-id="b5204-103">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="b5204-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="b5204-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5204-104">SYNTAX</span></span>

### <span data-ttu-id="b5204-105">DevSpacesControllerNameParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="b5204-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5204-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5204-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b5204-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b5204-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5204-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="b5204-108">DESCRIPTION</span></span>
<span data-ttu-id="b5204-109">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="b5204-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="b5204-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b5204-110">EXAMPLES</span></span>

### <span data-ttu-id="b5204-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b5204-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="b5204-112">Marcar um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="b5204-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="b5204-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5204-113">PARAMETERS</span></span>

### <span data-ttu-id="b5204-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5204-114">-DefaultProfile</span></span>
<span data-ttu-id="b5204-115">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b5204-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b5204-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b5204-116">-InputObject</span></span>
<span data-ttu-id="b5204-117">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="b5204-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="b5204-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="b5204-118">-Name</span></span>
<span data-ttu-id="b5204-119">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="b5204-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="b5204-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b5204-120">-ResourceGroupName</span></span>
<span data-ttu-id="b5204-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="b5204-121">Resource group name</span></span>

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

### <span data-ttu-id="b5204-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5204-122">-ResourceId</span></span>
<span data-ttu-id="b5204-123">A ID de recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="b5204-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="b5204-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="b5204-124">-Tag</span></span>
<span data-ttu-id="b5204-125">Uma tabela hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="b5204-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="b5204-126">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="b5204-126">-Confirm</span></span>
<span data-ttu-id="b5204-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5204-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b5204-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5204-128">-WhatIf</span></span>
<span data-ttu-id="b5204-129">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="b5204-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b5204-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b5204-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b5204-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5204-131">CommonParameters</span></span>
<span data-ttu-id="b5204-132">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5204-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5204-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5204-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5204-134">Entradas</span><span class="sxs-lookup"><span data-stu-id="b5204-134">INPUTS</span></span>

### <span data-ttu-id="b5204-135">System.String</span><span class="sxs-lookup"><span data-stu-id="b5204-135">System.String</span></span>

### <span data-ttu-id="b5204-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="b5204-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="b5204-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="b5204-137">OUTPUTS</span></span>

### <span data-ttu-id="b5204-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span><span class="sxs-lookup"><span data-stu-id="b5204-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="b5204-139">Notas</span><span class="sxs-lookup"><span data-stu-id="b5204-139">NOTES</span></span>

## <span data-ttu-id="b5204-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b5204-140">RELATED LINKS</span></span>
