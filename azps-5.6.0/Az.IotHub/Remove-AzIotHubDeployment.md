---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: a125bd402a58bc138e1fa74ec2f68d659f2a1d1c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887734"
---
# <span data-ttu-id="050fb-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="050fb-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="050fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="050fb-102">SYNOPSIS</span></span>
<span data-ttu-id="050fb-103">Exclua uma implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="050fb-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="050fb-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="050fb-104">SYNTAX</span></span>

### <span data-ttu-id="050fb-105">ResourceSet (Padrão)</span><span class="sxs-lookup"><span data-stu-id="050fb-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="050fb-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="050fb-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="050fb-107">ResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="050fb-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="050fb-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="050fb-108">DESCRIPTION</span></span>
<span data-ttu-id="050fb-109">Confira https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring mais informações.</span><span class="sxs-lookup"><span data-stu-id="050fb-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="050fb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="050fb-110">EXAMPLES</span></span>

### <span data-ttu-id="050fb-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="050fb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="050fb-112">Exclua uma implantação de Borda de IoT.</span><span class="sxs-lookup"><span data-stu-id="050fb-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="050fb-113">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="050fb-113">PARAMETERS</span></span>

### <span data-ttu-id="050fb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="050fb-114">-DefaultProfile</span></span>
<span data-ttu-id="050fb-115">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="050fb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="050fb-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="050fb-116">-InputObject</span></span>
<span data-ttu-id="050fb-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="050fb-117">IotHub object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub
Parameter Sets: InputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="050fb-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="050fb-118">-IotHubName</span></span>
<span data-ttu-id="050fb-119">Nome do Hub de Iot</span><span class="sxs-lookup"><span data-stu-id="050fb-119">Name of the Iot Hub</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050fb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="050fb-120">-Name</span></span>
<span data-ttu-id="050fb-121">Identificador da implantação.</span><span class="sxs-lookup"><span data-stu-id="050fb-121">Identifier for the deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050fb-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="050fb-122">-PassThru</span></span>
<span data-ttu-id="050fb-123">Permite retornar o objeto booleano.</span><span class="sxs-lookup"><span data-stu-id="050fb-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="050fb-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="050fb-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="050fb-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="050fb-125">-ResourceGroupName</span></span>
<span data-ttu-id="050fb-126">Nome do Grupo de Recursos</span><span class="sxs-lookup"><span data-stu-id="050fb-126">Name of the Resource Group</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="050fb-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="050fb-127">-ResourceId</span></span>
<span data-ttu-id="050fb-128">Id de Recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="050fb-128">IotHub Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="050fb-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="050fb-129">-Confirm</span></span>
<span data-ttu-id="050fb-130">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="050fb-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="050fb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="050fb-131">-WhatIf</span></span>
<span data-ttu-id="050fb-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="050fb-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="050fb-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="050fb-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="050fb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="050fb-134">CommonParameters</span></span>
<span data-ttu-id="050fb-135">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="050fb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="050fb-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="050fb-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="050fb-137">INPUTS</span><span class="sxs-lookup"><span data-stu-id="050fb-137">INPUTS</span></span>

### <span data-ttu-id="050fb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span><span class="sxs-lookup"><span data-stu-id="050fb-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="050fb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="050fb-139">System.String</span></span>

## <span data-ttu-id="050fb-140">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="050fb-140">OUTPUTS</span></span>

### <span data-ttu-id="050fb-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="050fb-141">System.Boolean</span></span>

## <span data-ttu-id="050fb-142">NOTES</span><span class="sxs-lookup"><span data-stu-id="050fb-142">NOTES</span></span>

## <span data-ttu-id="050fb-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="050fb-143">RELATED LINKS</span></span>
