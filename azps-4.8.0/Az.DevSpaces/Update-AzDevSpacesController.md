---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DevSpaces.dll-Help.xml
Module Name: Az.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/az.devspaces/update-azdevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DevSpaces/DevSpaces/help/Update-AzDevSpacesController.md
ms.openlocfilehash: 9de9f5e5870aed99a9ef7203bfea4797e78e5f8c
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94112791"
---
# <span data-ttu-id="1f057-101">Update-AzDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="1f057-101">Update-AzDevSpacesController</span></span>

## <span data-ttu-id="1f057-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="1f057-102">SYNOPSIS</span></span>
<span data-ttu-id="1f057-103">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="1f057-103">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="1f057-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1f057-104">SYNTAX</span></span>

### <span data-ttu-id="1f057-105">DevSpacesControllerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="1f057-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f057-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f057-106">ResourceIdParameterSet</span></span>
```
Update-AzDevSpacesController -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1f057-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1f057-107">InputObjectParameterSet</span></span>
```
Update-AzDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1f057-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="1f057-108">DESCRIPTION</span></span>
<span data-ttu-id="1f057-109">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="1f057-109">Update the DevSpaces controller to add tags.</span></span>

## <span data-ttu-id="1f057-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1f057-110">EXAMPLES</span></span>

### <span data-ttu-id="1f057-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1f057-111">Example 1</span></span>
```powershell
PS C:\> Update-AzDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="1f057-112">Marque um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1f057-112">Tag a DevSpaces controller.</span></span>

## <span data-ttu-id="1f057-113">OS</span><span class="sxs-lookup"><span data-stu-id="1f057-113">PARAMETERS</span></span>

### <span data-ttu-id="1f057-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1f057-114">-DefaultProfile</span></span>
<span data-ttu-id="1f057-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1f057-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1f057-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1f057-116">-InputObject</span></span>
<span data-ttu-id="1f057-117">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="1f057-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="1f057-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="1f057-118">-Name</span></span>
<span data-ttu-id="1f057-119">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="1f057-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="1f057-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1f057-120">-ResourceGroupName</span></span>
<span data-ttu-id="1f057-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1f057-121">Resource group name</span></span>

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

### <span data-ttu-id="1f057-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1f057-122">-ResourceId</span></span>
<span data-ttu-id="1f057-123">A ID do recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="1f057-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="1f057-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="1f057-124">-Tag</span></span>
<span data-ttu-id="1f057-125">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="1f057-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="1f057-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="1f057-126">-Confirm</span></span>
<span data-ttu-id="1f057-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1f057-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1f057-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1f057-128">-WhatIf</span></span>
<span data-ttu-id="1f057-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1f057-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1f057-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1f057-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1f057-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1f057-131">CommonParameters</span></span>
<span data-ttu-id="1f057-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1f057-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1f057-133">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1f057-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1f057-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="1f057-134">INPUTS</span></span>

### <span data-ttu-id="1f057-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1f057-135">System.String</span></span>

### <span data-ttu-id="1f057-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="1f057-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1f057-137">EXIBE</span><span class="sxs-lookup"><span data-stu-id="1f057-137">OUTPUTS</span></span>

### <span data-ttu-id="1f057-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="1f057-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="1f057-139">INFORMA</span><span class="sxs-lookup"><span data-stu-id="1f057-139">NOTES</span></span>

## <span data-ttu-id="1f057-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1f057-140">RELATED LINKS</span></span>
