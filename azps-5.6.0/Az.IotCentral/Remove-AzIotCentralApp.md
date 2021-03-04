---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotCentral.dll-Help.xml
Module Name: Az.IotCentral
online version: https://docs.microsoft.com/powershell/module/az.iotcentral/remove-aziotcentralapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotCentral/IotCentral/help/Remove-AzIotCentralApp.md
ms.openlocfilehash: 29a53b49e579ab337c2345a15c86c4c27aaffe8e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891375"
---
# <span data-ttu-id="141c7-101">Remove-AzIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="141c7-101">Remove-AzIotCentralApp</span></span>

## <span data-ttu-id="141c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="141c7-102">SYNOPSIS</span></span>
<span data-ttu-id="141c7-103">Exclui um aplicativo central de IoT.</span><span class="sxs-lookup"><span data-stu-id="141c7-103">Deletes an IoT Central Application.</span></span>

## <span data-ttu-id="141c7-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="141c7-104">SYNTAX</span></span>

### <span data-ttu-id="141c7-105">ResourceIdParameterSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="141c7-105">ResourceIdParameterSet (Default)</span></span>
```
Remove-AzIotCentralApp [-PassThru] -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141c7-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="141c7-106">InputObjectParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] -InputObject <PSIotCentralApp> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="141c7-107">InteractiveIotCentralParameterSet</span><span class="sxs-lookup"><span data-stu-id="141c7-107">InteractiveIotCentralParameterSet</span></span>
```
Remove-AzIotCentralApp [-PassThru] [-AsJob] [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="141c7-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="141c7-108">DESCRIPTION</span></span>
<span data-ttu-id="141c7-109">Exclui um aplicativo central de IoT existente.</span><span class="sxs-lookup"><span data-stu-id="141c7-109">Deletes an existing IoT Central Application.</span></span>

## <span data-ttu-id="141c7-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="141c7-110">EXAMPLES</span></span>

### <span data-ttu-id="141c7-111">Exemplo 1 Excluir e IoT Aplicativo Central</span><span class="sxs-lookup"><span data-stu-id="141c7-111">Example 1 Delete and IoT Central Application</span></span>
```powershell
PS C:\> Remove-AzIotCentralApp -ResourceGroupName "MyResourceGroupName" -Name "MyAppResourceName"
```

<span data-ttu-id="141c7-112">Exclui o Aplicativo Central de IoT fornecido.</span><span class="sxs-lookup"><span data-stu-id="141c7-112">Deletes the provided IoT Central Application.</span></span>

## <span data-ttu-id="141c7-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="141c7-113">PARAMETERS</span></span>

### <span data-ttu-id="141c7-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="141c7-114">-AsJob</span></span>
<span data-ttu-id="141c7-115">Execute o cmdlet como um trabalho em segundo plano.</span><span class="sxs-lookup"><span data-stu-id="141c7-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="141c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="141c7-116">-DefaultProfile</span></span>
<span data-ttu-id="141c7-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="141c7-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="141c7-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="141c7-118">-InputObject</span></span>
<span data-ttu-id="141c7-119">Objeto de entrada de aplicativo central Iot.</span><span class="sxs-lookup"><span data-stu-id="141c7-119">Iot Central Application Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="141c7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="141c7-120">-Name</span></span>
<span data-ttu-id="141c7-121">Nome do Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="141c7-121">Name of the Iot Central Application Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141c7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="141c7-122">-PassThru</span></span>
<span data-ttu-id="141c7-123">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="141c7-123">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="141c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="141c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="141c7-125">Nome do Grupo de Recursos.</span><span class="sxs-lookup"><span data-stu-id="141c7-125">Name of the Resource Group.</span></span>

```yaml
Type: System.String
Parameter Sets: InteractiveIotCentralParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="141c7-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="141c7-126">-ResourceId</span></span>
<span data-ttu-id="141c7-127">Id de Recurso de Aplicativo Central de Iot.</span><span class="sxs-lookup"><span data-stu-id="141c7-127">Iot Central Application Resource Id.</span></span>

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

### <span data-ttu-id="141c7-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="141c7-128">-Confirm</span></span>
<span data-ttu-id="141c7-129">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="141c7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="141c7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="141c7-130">-WhatIf</span></span>
<span data-ttu-id="141c7-131">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="141c7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="141c7-132">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="141c7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="141c7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="141c7-133">CommonParameters</span></span>
<span data-ttu-id="141c7-134">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="141c7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="141c7-135">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="141c7-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="141c7-136">INPUTS</span><span class="sxs-lookup"><span data-stu-id="141c7-136">INPUTS</span></span>

### <span data-ttu-id="141c7-137">System.String</span><span class="sxs-lookup"><span data-stu-id="141c7-137">System.String</span></span>

### <span data-ttu-id="141c7-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span><span class="sxs-lookup"><span data-stu-id="141c7-138">Microsoft.Azure.Commands.IotCentral.Models.PSIotCentralApp</span></span>

## <span data-ttu-id="141c7-139">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="141c7-139">OUTPUTS</span></span>

### <span data-ttu-id="141c7-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="141c7-140">System.Boolean</span></span>

## <span data-ttu-id="141c7-141">NOTES</span><span class="sxs-lookup"><span data-stu-id="141c7-141">NOTES</span></span>

## <span data-ttu-id="141c7-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="141c7-142">RELATED LINKS</span></span>
