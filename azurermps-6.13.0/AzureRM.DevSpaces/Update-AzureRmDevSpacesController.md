---
external help file: Microsoft.Azure.Commands.DevSpaces.dll-Help.xml
Module Name: AzureRM.DevSpaces
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.devspaces/update-azureevspacescontroller
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DevSpaces/Commands.DevSpaces/help/Update-AzureRmDevSpacesController.md
ms.openlocfilehash: b413311fea0d7e2235bc5e4ddb04e40db6d81162
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93610074"
---
# <span data-ttu-id="20950-101">Update-AzureRmDevSpacesController</span><span class="sxs-lookup"><span data-stu-id="20950-101">Update-AzureRmDevSpacesController</span></span>

## <span data-ttu-id="20950-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="20950-102">SYNOPSIS</span></span>
<span data-ttu-id="20950-103">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="20950-103">Update the DevSpaces controller to add tags.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20950-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="20950-104">SYNTAX</span></span>

### <span data-ttu-id="20950-105">DevSpacesControllerNameParameterSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="20950-105">DevSpacesControllerNameParameterSet (Default)</span></span>
```
Update-AzureRmDevSpacesController [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20950-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="20950-106">ResourceIdParameterSet</span></span>
```
Update-AzureRmDevSpacesController -ResourceId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20950-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="20950-107">InputObjectParameterSet</span></span>
```
Update-AzureRmDevSpacesController -InputObject <PSController> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="20950-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="20950-108">DESCRIPTION</span></span>
<span data-ttu-id="20950-109">Atualize o controlador DevSpaces para adicionar marcas.</span><span class="sxs-lookup"><span data-stu-id="20950-109">Update the DevSpaces controller to add tags.</span></span> 

## <span data-ttu-id="20950-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="20950-110">EXAMPLES</span></span>

### <span data-ttu-id="20950-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="20950-111">Example 1</span></span>
```powershell
PS C:\> Update-AzureRmDevSpacesController -ResourceGroupName devSpaceResourceGroup -Name devSpaceControllerName -Tag @{ tagKey="tagValue"}

Name        Resource Group  Location  Provisioning State
----------  --------------  --------  ------------------
devSpaceControllerName   devSpaceResourceGroup     eastus    Succeeded
```

<span data-ttu-id="20950-112">Marque um DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="20950-112">Tag a DevSpaces contoller.</span></span>

## <span data-ttu-id="20950-113">OS</span><span class="sxs-lookup"><span data-stu-id="20950-113">PARAMETERS</span></span>

### <span data-ttu-id="20950-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20950-114">-DefaultProfile</span></span>
<span data-ttu-id="20950-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="20950-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20950-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20950-116">-InputObject</span></span>
<span data-ttu-id="20950-117">Um objeto PSController, normalmente passado pelo pipeline.</span><span class="sxs-lookup"><span data-stu-id="20950-117">A PSController object, normally passed through the pipeline.</span></span>

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

### <span data-ttu-id="20950-118">-Nome</span><span class="sxs-lookup"><span data-stu-id="20950-118">-Name</span></span>
<span data-ttu-id="20950-119">Nome do controlador DevSpaces.</span><span class="sxs-lookup"><span data-stu-id="20950-119">DevSpaces controller name.</span></span>

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

### <span data-ttu-id="20950-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20950-120">-ResourceGroupName</span></span>
<span data-ttu-id="20950-121">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="20950-121">Resource group name</span></span>

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

### <span data-ttu-id="20950-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20950-122">-ResourceId</span></span>
<span data-ttu-id="20950-123">A ID do recurso DevSpaces</span><span class="sxs-lookup"><span data-stu-id="20950-123">The DevSpaces resource id</span></span>

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

### <span data-ttu-id="20950-124">-Marca</span><span class="sxs-lookup"><span data-stu-id="20950-124">-Tag</span></span>
<span data-ttu-id="20950-125">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="20950-125">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="20950-126">-Confirme</span><span class="sxs-lookup"><span data-stu-id="20950-126">-Confirm</span></span>
<span data-ttu-id="20950-127">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20950-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20950-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20950-128">-WhatIf</span></span>
<span data-ttu-id="20950-129">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="20950-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20950-130">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="20950-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20950-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20950-131">CommonParameters</span></span>
<span data-ttu-id="20950-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20950-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20950-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20950-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20950-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="20950-134">INPUTS</span></span>

### <span data-ttu-id="20950-135">System. String</span><span class="sxs-lookup"><span data-stu-id="20950-135">System.String</span></span>

### <span data-ttu-id="20950-136">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="20950-136">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>
<span data-ttu-id="20950-137">Parâmetros: inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="20950-137">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="20950-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="20950-138">OUTPUTS</span></span>

### <span data-ttu-id="20950-139">Microsoft. Azure. Commands. DevSpaces. Models. PSController</span><span class="sxs-lookup"><span data-stu-id="20950-139">Microsoft.Azure.Commands.DevSpaces.Models.PSController</span></span>

## <span data-ttu-id="20950-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="20950-140">NOTES</span></span>

## <span data-ttu-id="20950-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="20950-141">RELATED LINKS</span></span>
