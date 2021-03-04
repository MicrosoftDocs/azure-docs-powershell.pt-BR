---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: b9922d84edfbf90e16db1f050ae7abaeef7442a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888976"
---
# <span data-ttu-id="aea11-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="aea11-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="aea11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aea11-102">SYNOPSIS</span></span>
<span data-ttu-id="aea11-103">Cria um serviço sob a topologia de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="aea11-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="aea11-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="aea11-104">SYNTAX</span></span>

### <span data-ttu-id="aea11-105">Interativo (Padrão)</span><span class="sxs-lookup"><span data-stu-id="aea11-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea11-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="aea11-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aea11-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="aea11-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aea11-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="aea11-108">DESCRIPTION</span></span>
<span data-ttu-id="aea11-109">O cmdlet **New-AzDeploymentManagerService** cria um serviço em uma topologia de serviço e retorna um objeto que representa esse serviço.</span><span class="sxs-lookup"><span data-stu-id="aea11-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="aea11-110">Especifique o serviço pelo nome, topologia de serviço em que ele está e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aea11-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="aea11-111">O cmdlet retorna um objeto Service.</span><span class="sxs-lookup"><span data-stu-id="aea11-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="aea11-112">Você pode modificar esse objeto localmente e aplicar alterações ao serviço usando o cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="aea11-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="aea11-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="aea11-113">EXAMPLES</span></span>

### <span data-ttu-id="aea11-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="aea11-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="aea11-115">Cria um novo serviço com o nome ContosoService1 em topologia de serviço ContosoServiceTopology no Grupo de Recursos ContosoResourceGroup, no local Central DOS EUA.</span><span class="sxs-lookup"><span data-stu-id="aea11-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="aea11-116">A propriedade TargetLocation indica que o serviço ContosoService1 deve ser implantado na região leste dos EUA na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="aea11-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="aea11-117">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="aea11-117">PARAMETERS</span></span>

### <span data-ttu-id="aea11-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aea11-118">-DefaultProfile</span></span>
<span data-ttu-id="aea11-119">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="aea11-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aea11-120">-Location</span><span class="sxs-lookup"><span data-stu-id="aea11-120">-Location</span></span>
<span data-ttu-id="aea11-121">O local do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="aea11-121">The location of the service resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-122">-Name</span><span class="sxs-lookup"><span data-stu-id="aea11-122">-Name</span></span>
<span data-ttu-id="aea11-123">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="aea11-123">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aea11-124">-ResourceGroupName</span></span>
<span data-ttu-id="aea11-125">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="aea11-125">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="aea11-126">-ServiceTopologyId</span></span>
<span data-ttu-id="aea11-127">O identificador de recurso de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="aea11-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="aea11-128">-ServiceTopologyName</span></span>
<span data-ttu-id="aea11-129">O nome da topologia de serviço a que esse serviço pertence.</span><span class="sxs-lookup"><span data-stu-id="aea11-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="aea11-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="aea11-131">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="aea11-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-132">-Tag</span><span class="sxs-lookup"><span data-stu-id="aea11-132">-Tag</span></span>
<span data-ttu-id="aea11-133">Uma tabela de hash que representa marcas de recurso.</span><span class="sxs-lookup"><span data-stu-id="aea11-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="aea11-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="aea11-134">-TargetLocation</span></span>
<span data-ttu-id="aea11-135">Determina o local para o qual os recursos sob o serviço seriam implantados.</span><span class="sxs-lookup"><span data-stu-id="aea11-135">Determines the location where resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aea11-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="aea11-137">Determina a assinatura para a qual recursos no serviço seriam implantados.</span><span class="sxs-lookup"><span data-stu-id="aea11-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="aea11-138">-Confirm</span><span class="sxs-lookup"><span data-stu-id="aea11-138">-Confirm</span></span>
<span data-ttu-id="aea11-139">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aea11-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aea11-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aea11-140">-WhatIf</span></span>
<span data-ttu-id="aea11-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="aea11-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aea11-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="aea11-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aea11-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aea11-143">CommonParameters</span></span>
<span data-ttu-id="aea11-144">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aea11-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aea11-145">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="aea11-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aea11-146">INPUTS</span><span class="sxs-lookup"><span data-stu-id="aea11-146">INPUTS</span></span>

### <span data-ttu-id="aea11-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="aea11-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="aea11-148">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="aea11-148">OUTPUTS</span></span>

### <span data-ttu-id="aea11-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="aea11-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="aea11-150">NOTES</span><span class="sxs-lookup"><span data-stu-id="aea11-150">NOTES</span></span>

## <span data-ttu-id="aea11-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="aea11-151">RELATED LINKS</span></span>
