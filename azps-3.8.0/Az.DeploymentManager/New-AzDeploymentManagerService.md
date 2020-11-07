---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: aec721a3676a6b4510c7fe0eccf5badc4f9ccce2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944382"
---
# <span data-ttu-id="4930b-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="4930b-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="4930b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4930b-102">SYNOPSIS</span></span>
<span data-ttu-id="4930b-103">Cria um serviço na topologia de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="4930b-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="4930b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4930b-104">SYNTAX</span></span>

### <span data-ttu-id="4930b-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="4930b-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4930b-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="4930b-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4930b-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="4930b-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4930b-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4930b-108">DESCRIPTION</span></span>
<span data-ttu-id="4930b-109">O cmdlet **New-AzDeploymentManagerService** cria um serviço em uma topologia de serviço e retorna um objeto que representa esse serviço.</span><span class="sxs-lookup"><span data-stu-id="4930b-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="4930b-110">Especifique o serviço pelo nome, topologia de serviço em que ele se encontra e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4930b-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="4930b-111">O cmdlet retorna um objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="4930b-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="4930b-112">Você pode modificar esse objeto localmente e, em seguida, aplicar as alterações ao serviço usando o cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="4930b-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="4930b-113">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4930b-113">EXAMPLES</span></span>

### <span data-ttu-id="4930b-114">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4930b-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="4930b-115">Cria um novo serviço com o nome ContosoService1 em ContosoServiceTopology de topologia de serviço no grupo de recursos ContosoResourceGroup, no centro de localização dos EUA.</span><span class="sxs-lookup"><span data-stu-id="4930b-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="4930b-116">A propriedade TargetLocation indica que o serviço ContosoService1 deve ser implantado na região leste dos EUA na assinatura especificada.</span><span class="sxs-lookup"><span data-stu-id="4930b-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="4930b-117">OS</span><span class="sxs-lookup"><span data-stu-id="4930b-117">PARAMETERS</span></span>

### <span data-ttu-id="4930b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4930b-118">-DefaultProfile</span></span>
<span data-ttu-id="4930b-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4930b-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4930b-120">-Local</span><span class="sxs-lookup"><span data-stu-id="4930b-120">-Location</span></span>
<span data-ttu-id="4930b-121">O local do recurso de serviço.</span><span class="sxs-lookup"><span data-stu-id="4930b-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="4930b-122">-Nome</span><span class="sxs-lookup"><span data-stu-id="4930b-122">-Name</span></span>
<span data-ttu-id="4930b-123">O nome do serviço.</span><span class="sxs-lookup"><span data-stu-id="4930b-123">The name of the service.</span></span>

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

### <span data-ttu-id="4930b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4930b-124">-ResourceGroupName</span></span>
<span data-ttu-id="4930b-125">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4930b-125">The resource group.</span></span>

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

### <span data-ttu-id="4930b-126">-Imtopologyid</span><span class="sxs-lookup"><span data-stu-id="4930b-126">-ServiceTopologyId</span></span>
<span data-ttu-id="4930b-127">O identificador de recursos de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="4930b-127">The service topology resource identifier in which the service should be created.</span></span>

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

### <span data-ttu-id="4930b-128">-Imtopologyname</span><span class="sxs-lookup"><span data-stu-id="4930b-128">-ServiceTopologyName</span></span>
<span data-ttu-id="4930b-129">O nome da topologia de serviço a qual esse serviço pertence.</span><span class="sxs-lookup"><span data-stu-id="4930b-129">The name of the service topology this service belongs to.</span></span>

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

### <span data-ttu-id="4930b-130">-Imtopologyobject</span><span class="sxs-lookup"><span data-stu-id="4930b-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="4930b-131">O objeto de topologia de serviço no qual o serviço deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="4930b-131">The service topology object in which the service should be created.</span></span>

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

### <span data-ttu-id="4930b-132">-Marca</span><span class="sxs-lookup"><span data-stu-id="4930b-132">-Tag</span></span>
<span data-ttu-id="4930b-133">Uma tabela de hash que representa as marcas de recursos.</span><span class="sxs-lookup"><span data-stu-id="4930b-133">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="4930b-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="4930b-134">-TargetLocation</span></span>
<span data-ttu-id="4930b-135">Determina o local onde os recursos do serviço seriam implantados.</span><span class="sxs-lookup"><span data-stu-id="4930b-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="4930b-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4930b-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="4930b-137">Determina a assinatura na qual os recursos do serviço seriam implantados.</span><span class="sxs-lookup"><span data-stu-id="4930b-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="4930b-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4930b-138">-Confirm</span></span>
<span data-ttu-id="4930b-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4930b-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4930b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4930b-140">-WhatIf</span></span>
<span data-ttu-id="4930b-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4930b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4930b-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4930b-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4930b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4930b-143">CommonParameters</span></span>
<span data-ttu-id="4930b-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4930b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4930b-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4930b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4930b-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4930b-146">INPUTS</span></span>

### <span data-ttu-id="4930b-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="4930b-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4930b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4930b-148">OUTPUTS</span></span>

### <span data-ttu-id="4930b-149">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="4930b-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="4930b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4930b-150">NOTES</span></span>

## <span data-ttu-id="4930b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4930b-151">RELATED LINKS</span></span>
