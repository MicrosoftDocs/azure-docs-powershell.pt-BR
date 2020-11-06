---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93425722"
---
# <span data-ttu-id="b9119-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b9119-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="b9119-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b9119-102">SYNOPSIS</span></span>
<span data-ttu-id="b9119-103">Exclui uma topologia de serviço e todos os seus recursos.</span><span class="sxs-lookup"><span data-stu-id="b9119-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="b9119-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9119-104">SYNTAX</span></span>

### <span data-ttu-id="b9119-105">Interativo (padrão)</span><span class="sxs-lookup"><span data-stu-id="b9119-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9119-106">Identificação</span><span class="sxs-lookup"><span data-stu-id="b9119-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b9119-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b9119-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9119-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b9119-108">DESCRIPTION</span></span>
<span data-ttu-id="b9119-109">O cmdlet **Remove-AzureRmDeploymentManagerServiceTopology** exclui uma topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="b9119-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="b9119-110">Especifique a topologia do serviço de acordo com o nome e o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9119-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="b9119-111">Como alternativa, você pode fornecer o objeto imtopology ou o resourceId.</span><span class="sxs-lookup"><span data-stu-id="b9119-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="b9119-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b9119-112">EXAMPLES</span></span>

### <span data-ttu-id="b9119-113">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b9119-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="b9119-114">Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9119-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b9119-115">Exemplo 2: excluir uma topologia de serviço usando o identificador de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9119-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="b9119-116">Esse comando exclui uma topologia de serviço chamada ContosoServiceTopology no ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b9119-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="b9119-117">Exemplo 3: excluir uma topologia de serviço usando o objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="b9119-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="b9119-118">Esse comando exclui uma topologia de serviço cujo nome e o meu nome do contato correspondam às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="b9119-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="b9119-119">OS</span><span class="sxs-lookup"><span data-stu-id="b9119-119">PARAMETERS</span></span>

### <span data-ttu-id="b9119-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9119-120">-DefaultProfile</span></span>
<span data-ttu-id="b9119-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b9119-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9119-122">-Force</span><span class="sxs-lookup"><span data-stu-id="b9119-122">-Force</span></span>
<span data-ttu-id="b9119-123">Não peça confirmação.</span><span class="sxs-lookup"><span data-stu-id="b9119-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b9119-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="b9119-124">-Name</span></span>
<span data-ttu-id="b9119-125">O nome da topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="b9119-125">The name of the service topology.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9119-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b9119-126">-PassThru</span></span>
<span data-ttu-id="b9119-127">{{Descrição do PassThru de preenchimento}}</span><span class="sxs-lookup"><span data-stu-id="b9119-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="b9119-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9119-128">-ResourceGroupName</span></span>
<span data-ttu-id="b9119-129">O grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b9119-129">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9119-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9119-130">-ResourceId</span></span>
<span data-ttu-id="b9119-131">O identificador do recurso.</span><span class="sxs-lookup"><span data-stu-id="b9119-131">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b9119-132">-Outtopology</span><span class="sxs-lookup"><span data-stu-id="b9119-132">-ServiceTopology</span></span>
<span data-ttu-id="b9119-133">O recurso a ser removido.</span><span class="sxs-lookup"><span data-stu-id="b9119-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b9119-134">-Confirme</span><span class="sxs-lookup"><span data-stu-id="b9119-134">-Confirm</span></span>
<span data-ttu-id="b9119-135">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9119-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9119-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9119-136">-WhatIf</span></span>
<span data-ttu-id="b9119-137">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="b9119-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9119-138">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="b9119-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9119-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9119-139">CommonParameters</span></span>
<span data-ttu-id="b9119-140">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9119-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9119-141">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9119-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9119-142">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b9119-142">INPUTS</span></span>

### <span data-ttu-id="b9119-143">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="b9119-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="b9119-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b9119-144">OUTPUTS</span></span>

### <span data-ttu-id="b9119-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b9119-145">System.Boolean</span></span>

## <span data-ttu-id="b9119-146">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b9119-146">NOTES</span></span>

## <span data-ttu-id="b9119-147">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b9119-147">RELATED LINKS</span></span>

[<span data-ttu-id="b9119-148">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b9119-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="b9119-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b9119-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="b9119-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="b9119-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)