---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: 01f2aa36a063caec233aa8c1600d4a01727a549b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94111403"
---
# <span data-ttu-id="4c80b-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c80b-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="4c80b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4c80b-102">SYNOPSIS</span></span>
<span data-ttu-id="4c80b-103">Cancela uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c80b-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="4c80b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4c80b-104">SYNTAX</span></span>

### <span data-ttu-id="4c80b-105">StopByResourceGroupDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4c80b-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c80b-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="4c80b-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c80b-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4c80b-107">DESCRIPTION</span></span>
<span data-ttu-id="4c80b-108">O cmdlet **Stop-AzResourceGroupDeployment** cancela uma implantação de grupo de recursos do Azure que foi iniciada, mas não foi completada.</span><span class="sxs-lookup"><span data-stu-id="4c80b-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="4c80b-109">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como provisionamento, e não um estado concluído, como provisionado ou com falha.</span><span class="sxs-lookup"><span data-stu-id="4c80b-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="4c80b-110">Um recurso do Azure é uma entidade gerenciada pelo usuário, como um site da Web, um banco de dados ou um servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="4c80b-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="4c80b-111">Um grupo de recursos é uma coleção de recursos implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="4c80b-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="4c80b-112">Para implantar um grupo de recursos, use o cmdlet New-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="4c80b-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="4c80b-113">O cmdlet New-AzResource cria um novo recurso, mas ele não aciona uma operação de implantação de grupo de recursos que esse cmdlet pode parar.</span><span class="sxs-lookup"><span data-stu-id="4c80b-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="4c80b-114">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="4c80b-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="4c80b-115">Use o parâmetro *Name* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="4c80b-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="4c80b-116">Se você omitir o parâmetro *Name* , **Stop-AzResourceGroupDeployment** procurará uma implantação em execução e a interromperá.</span><span class="sxs-lookup"><span data-stu-id="4c80b-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="4c80b-117">Se o cmdlet encontrar mais de uma implantação em execução, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="4c80b-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="4c80b-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4c80b-118">EXAMPLES</span></span>

### <span data-ttu-id="4c80b-119">Exemplo 1: Iniciando e interrompendo uma implantação de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="4c80b-119">Example 1: Starting and stopping a resource group deployment</span></span>

```powershell
PS C:\> New-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg -TemplateFile .\storage-account-create-azdeploy.json -TemplateParameterFile .\storage-account-create-azdeploy.parameters.json -AsJob

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Running       True            localhost            New-AzResourceGro...

PS C:\> Stop-AzResourceGroupDeployment -Name mynewstorageaccount -ResourceGroupName myrg
True

PS C:\> Get-Job 1

Id     Name            PSJobTypeName   State         HasMoreData     Location             Command
--     ----            -------------   -----         -----------     --------             -------
1      Long Running... AzureLongRun... Failed        True            localhost            New-AzResourceGro...
```

## <span data-ttu-id="4c80b-120">OS</span><span class="sxs-lookup"><span data-stu-id="4c80b-120">PARAMETERS</span></span>

### <span data-ttu-id="4c80b-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4c80b-121">-ApiVersion</span></span>
<span data-ttu-id="4c80b-122">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c80b-122">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="4c80b-123">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="4c80b-123">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="4c80b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c80b-124">-DefaultProfile</span></span>
<span data-ttu-id="4c80b-125">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="4c80b-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4c80b-126">-ID</span><span class="sxs-lookup"><span data-stu-id="4c80b-126">-Id</span></span>
<span data-ttu-id="4c80b-127">Especifica a ID da implantação do grupo de recursos a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="4c80b-127">Specifies the ID of the resource group deployment to stop.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c80b-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="4c80b-128">-Name</span></span>
<span data-ttu-id="4c80b-129">Especifica o nome da implantação do grupo de recursos a ser interrompida.</span><span class="sxs-lookup"><span data-stu-id="4c80b-129">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="4c80b-130">Se você não especificar esse parâmetro, esse cmdlet procurará uma implantação em execução no grupo de recursos e a interromperá.</span><span class="sxs-lookup"><span data-stu-id="4c80b-130">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="4c80b-131">Se ele encontrar mais de uma implantação em execução, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="4c80b-131">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="4c80b-132">Para obter o nome da implantação, use o cmdlet Get-AzResourceGroupDeployment.</span><span class="sxs-lookup"><span data-stu-id="4c80b-132">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases: DeploymentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c80b-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="4c80b-133">-Pre</span></span>
<span data-ttu-id="4c80b-134">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4c80b-134">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4c80b-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c80b-135">-ResourceGroupName</span></span>
<span data-ttu-id="4c80b-136">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4c80b-136">Specifies the name of the resource group.</span></span>
<span data-ttu-id="4c80b-137">Esse cmdlet interrompe a implantação do grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="4c80b-137">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: StopByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c80b-138">-Confirme</span><span class="sxs-lookup"><span data-stu-id="4c80b-138">-Confirm</span></span>
<span data-ttu-id="4c80b-139">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c80b-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c80b-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c80b-140">-WhatIf</span></span>
<span data-ttu-id="4c80b-141">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="4c80b-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c80b-142">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="4c80b-142">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c80b-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c80b-143">CommonParameters</span></span>
<span data-ttu-id="4c80b-144">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c80b-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c80b-145">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4c80b-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c80b-146">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4c80b-146">INPUTS</span></span>

### <span data-ttu-id="4c80b-147">System. String</span><span class="sxs-lookup"><span data-stu-id="4c80b-147">System.String</span></span>

## <span data-ttu-id="4c80b-148">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4c80b-148">OUTPUTS</span></span>

### <span data-ttu-id="4c80b-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c80b-149">System.Boolean</span></span>

## <span data-ttu-id="4c80b-150">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4c80b-150">NOTES</span></span>

## <span data-ttu-id="4c80b-151">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4c80b-151">RELATED LINKS</span></span>

[<span data-ttu-id="4c80b-152">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c80b-152">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="4c80b-153">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="4c80b-153">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="4c80b-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="4c80b-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="4c80b-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c80b-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="4c80b-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c80b-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="4c80b-157">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="4c80b-157">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


