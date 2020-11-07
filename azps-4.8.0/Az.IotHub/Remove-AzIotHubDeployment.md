---
external help file: Microsoft.Azure.PowerShell.Cmdlets.IotHub.dll-Help.xml
Module Name: Az.IotHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.iothub/remove-aziothubdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/IotHub/IotHub/help/Remove-AzIotHubDeployment.md
ms.openlocfilehash: f5463015b93c209c6cf8952c566e9656da2fba18
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "93948239"
---
# <span data-ttu-id="c7c04-101">Remove-AzIotHubDeployment</span><span class="sxs-lookup"><span data-stu-id="c7c04-101">Remove-AzIotHubDeployment</span></span>

## <span data-ttu-id="c7c04-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c7c04-102">SYNOPSIS</span></span>
<span data-ttu-id="c7c04-103">Excluir uma implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="c7c04-103">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="c7c04-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7c04-104">SYNTAX</span></span>

### <span data-ttu-id="c7c04-105">ResourceSet (padrão)</span><span class="sxs-lookup"><span data-stu-id="c7c04-105">ResourceSet (Default)</span></span>
```
Remove-AzIotHubDeployment [-ResourceGroupName] <String> [-IotHubName] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c04-106">InputObjectSet</span><span class="sxs-lookup"><span data-stu-id="c7c04-106">InputObjectSet</span></span>
```
Remove-AzIotHubDeployment [-InputObject] <PSIotHub> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7c04-107">ResourceSet</span><span class="sxs-lookup"><span data-stu-id="c7c04-107">ResourceIdSet</span></span>
```
Remove-AzIotHubDeployment [-ResourceId] <String> [-Name <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c7c04-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="c7c04-108">DESCRIPTION</span></span>
<span data-ttu-id="c7c04-109">Consulte https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="c7c04-109">See https://docs.microsoft.com/azure/iot-edge/module-deployment-monitoring for more information.</span></span>

## <span data-ttu-id="c7c04-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="c7c04-110">EXAMPLES</span></span>

### <span data-ttu-id="c7c04-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c7c04-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzIotHubDeployment -ResourceGroupName "myresourcegroup" -IotHubName "myiothub" -Name "deploy1"
```

<span data-ttu-id="c7c04-112">Excluir uma implantação de borda IoT.</span><span class="sxs-lookup"><span data-stu-id="c7c04-112">Delete an IoT Edge deployment.</span></span>

## <span data-ttu-id="c7c04-113">OS</span><span class="sxs-lookup"><span data-stu-id="c7c04-113">PARAMETERS</span></span>

### <span data-ttu-id="c7c04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7c04-114">-DefaultProfile</span></span>
<span data-ttu-id="c7c04-115">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c7c04-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c7c04-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7c04-116">-InputObject</span></span>
<span data-ttu-id="c7c04-117">Objeto IotHub</span><span class="sxs-lookup"><span data-stu-id="c7c04-117">IotHub object</span></span>

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

### <span data-ttu-id="c7c04-118">-IotHubName</span><span class="sxs-lookup"><span data-stu-id="c7c04-118">-IotHubName</span></span>
<span data-ttu-id="c7c04-119">Nome do Hub IOT</span><span class="sxs-lookup"><span data-stu-id="c7c04-119">Name of the Iot Hub</span></span>

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

### <span data-ttu-id="c7c04-120">-Nome</span><span class="sxs-lookup"><span data-stu-id="c7c04-120">-Name</span></span>
<span data-ttu-id="c7c04-121">Identificador para a implantação.</span><span class="sxs-lookup"><span data-stu-id="c7c04-121">Identifier for the deployment.</span></span>

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

### <span data-ttu-id="c7c04-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c7c04-122">-PassThru</span></span>
<span data-ttu-id="c7c04-123">Permite retornar o objeto booliano.</span><span class="sxs-lookup"><span data-stu-id="c7c04-123">Allows to return the boolean object.</span></span>
<span data-ttu-id="c7c04-124">Por padrão, esse cmdlet não gera nenhuma saída.</span><span class="sxs-lookup"><span data-stu-id="c7c04-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="c7c04-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7c04-125">-ResourceGroupName</span></span>
<span data-ttu-id="c7c04-126">Nome do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="c7c04-126">Name of the Resource Group</span></span>

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

### <span data-ttu-id="c7c04-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7c04-127">-ResourceId</span></span>
<span data-ttu-id="c7c04-128">ID do recurso IotHub</span><span class="sxs-lookup"><span data-stu-id="c7c04-128">IotHub Resource Id</span></span>

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

### <span data-ttu-id="c7c04-129">-Confirme</span><span class="sxs-lookup"><span data-stu-id="c7c04-129">-Confirm</span></span>
<span data-ttu-id="c7c04-130">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7c04-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7c04-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7c04-131">-WhatIf</span></span>
<span data-ttu-id="c7c04-132">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="c7c04-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7c04-133">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="c7c04-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7c04-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7c04-134">CommonParameters</span></span>
<span data-ttu-id="c7c04-135">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7c04-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7c04-136">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7c04-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7c04-137">SENSORES</span><span class="sxs-lookup"><span data-stu-id="c7c04-137">INPUTS</span></span>

### <span data-ttu-id="c7c04-138">Microsoft. Azure. Commands. Management. IotHub. Models. PSIotHub</span><span class="sxs-lookup"><span data-stu-id="c7c04-138">Microsoft.Azure.Commands.Management.IotHub.Models.PSIotHub</span></span>

### <span data-ttu-id="c7c04-139">System. String</span><span class="sxs-lookup"><span data-stu-id="c7c04-139">System.String</span></span>

## <span data-ttu-id="c7c04-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="c7c04-140">OUTPUTS</span></span>

### <span data-ttu-id="c7c04-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="c7c04-141">System.Boolean</span></span>

## <span data-ttu-id="c7c04-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="c7c04-142">NOTES</span></span>

## <span data-ttu-id="c7c04-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c7c04-143">RELATED LINKS</span></span>
