---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/remove-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Remove-AzureRmDevSpacesController.md
ms.openlocfilehash: e242ba95330ac102fbfbcecf6f28326adb29a057
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610077"
---
# <span data-ttu-id="3c0c8-101">Remove-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="3c0c8-101">Remove-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="3c0c8-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="3c0c8-102">SYNOPSIS</span></span>
<span data-ttu-id="3c0c8-103">Excluir um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-103">Delete a DevSpaces controller.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3c0c8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3c0c8-104">SYNTAX</span></span>

### <span data-ttu-id="3c0c8-105">DevSpacesControllerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="3c0c8-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Remove-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0c8-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0c8-106">ResourceIdParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -ResourceId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3c0c8-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3c0c8-107">InputObjectParameterSet</span></span>
```
Remove-AzureRmDevSpacesController -InputObject <PSController> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3c0c8-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="3c0c8-108">DESCRIPTION</span></span>
<span data-ttu-id="3c0c8-109">Excluir um controlador de DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-109">Delete a DevSpaces controller.</span></span>

## <span data-ttu-id="3c0c8-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="3c0c8-110">EXAMPLES</span></span>

### <span data-ttu-id="3c0c8-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="3c0c8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName
```

<span data-ttu-id="3c0c8-112">Exclua um controlador de DevSpaces chamado devSpaceControllerName.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-112">Delete a DevSpaces controller named devSpaceControllerName.</span></span>

## <span data-ttu-id="3c0c8-113">OS</span><span class="sxs-lookup"><span data-stu-id="3c0c8-113">PARAMETERS</span></span>

### <span data-ttu-id="3c0c8-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3c0c8-114">-AsJob</span></span>
<span data-ttu-id="3c0c8-115">Executar o cmdlet em segundo plano</span><span class="sxs-lookup"><span data-stu-id="3c0c8-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3c0c8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3c0c8-116">-DefaultProfile</span></span>
<span data-ttu-id="3c0c8-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3c0c8-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3c0c8-118">-InputObject</span></span>
<span data-ttu-id="3c0c8-119">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-119">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="3c0c8-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="3c0c8-120">-Name</span></span>
<span data-ttu-id="3c0c8-121">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-121">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="3c0c8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3c0c8-122">-PassThru</span></span>
<span data-ttu-id="3c0c8-123">Retorna verdadeiro se a exclusão for bem-sucedida</span><span class="sxs-lookup"><span data-stu-id="3c0c8-123">Returns true if delete is successful</span></span>

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

### <span data-ttu-id="3c0c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3c0c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="3c0c8-125">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="3c0c8-125">Resource group name</span></span>

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

### <span data-ttu-id="3c0c8-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3c0c8-126">-ResourceId</span></span>
<span data-ttu-id="3c0c8-127">A ID do recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="3c0c8-127">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="3c0c8-128">-Confirme</span><span class="sxs-lookup"><span data-stu-id="3c0c8-128">-Confirm</span></span>
<span data-ttu-id="3c0c8-129">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3c0c8-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3c0c8-130">-WhatIf</span></span>
<span data-ttu-id="3c0c8-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3c0c8-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3c0c8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c0c8-133">CommonParameters</span></span>
<span data-ttu-id="3c0c8-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c0c8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c0c8-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c0c8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c0c8-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="3c0c8-136">INPUTS</span></span>

### <span data-ttu-id="3c0c8-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3c0c8-137">System.String</span></span>

### <span data-ttu-id="3c0c8-138">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="3c0c8-138">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="3c0c8-139">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3c0c8-139">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="3c0c8-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="3c0c8-140">OUTPUTS</span></span>

### <span data-ttu-id="3c0c8-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3c0c8-141">System.Boolean</span></span>

## <span data-ttu-id="3c0c8-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="3c0c8-142">NOTES</span></span>

## <span data-ttu-id="3c0c8-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="3c0c8-143">RELATED LINKS</span></span>
