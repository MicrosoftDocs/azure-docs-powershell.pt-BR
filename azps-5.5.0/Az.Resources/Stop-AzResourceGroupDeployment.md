---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 089954C3-7F3E-46C2-AA93-C0151EACDA2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/stop-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Stop-AzResourceGroupDeployment.md
ms.openlocfilehash: fa189637c9c2c1b63ab0e8dd0b00fab3f4505da0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111406"
---
# <span data-ttu-id="548cc-101">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="548cc-101">Stop-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="548cc-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="548cc-102">SYNOPSIS</span></span>
<span data-ttu-id="548cc-103">Cancela uma implantação de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="548cc-103">Cancels a resource group deployment.</span></span>

## <span data-ttu-id="548cc-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="548cc-104">SYNTAX</span></span>

### <span data-ttu-id="548cc-105">StopByResourceGroupDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="548cc-105">StopByResourceGroupDeploymentName (Default)</span></span>
```
Stop-AzResourceGroupDeployment [-ResourceGroupName] <String> [-Name] <String> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="548cc-106">StopByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="548cc-106">StopByResourceGroupDeploymentId</span></span>
```
Stop-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="548cc-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="548cc-107">DESCRIPTION</span></span>
<span data-ttu-id="548cc-108">O cmdlet **Stop-AzResourceGroupDeployment** cancela uma implantação de grupo de recursos do Azure iniciada, mas não concluída.</span><span class="sxs-lookup"><span data-stu-id="548cc-108">The **Stop-AzResourceGroupDeployment** cmdlet cancels an Azure resource group deployment that has started but not completed.</span></span>
<span data-ttu-id="548cc-109">Para interromper uma implantação, a implantação deve ter um estado de provisionamento incompleto, como Provisionamento, e não um estado concluído, como Provisionado ou Falha.</span><span class="sxs-lookup"><span data-stu-id="548cc-109">To stop a deployment, the deployment must have an incomplete provisioning state, such as Provisioning, and not a completed state, such as Provisioned or Failed.</span></span>
<span data-ttu-id="548cc-110">Um recurso do Azure é uma entidade gerenciada pelo usuário, como um site, um banco de dados ou um servidor de banco de dados.</span><span class="sxs-lookup"><span data-stu-id="548cc-110">An Azure resource is a user-managed entity, such as a website, database, or database server.</span></span>
<span data-ttu-id="548cc-111">Um grupo de recursos é um conjunto de recursos implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="548cc-111">A resource group is a collection of resources that are deployed as a unit.</span></span>
<span data-ttu-id="548cc-112">Para implantar um grupo de recursos, use o cmdlet New-AzResourceGroupDeployment dados.</span><span class="sxs-lookup"><span data-stu-id="548cc-112">To deploy a resource group, use the New-AzResourceGroupDeployment cmdlet.</span></span>
<span data-ttu-id="548cc-113">O New-AzResource cmdlet cria um novo recurso, mas não aciona uma operação de implantação de grupo de recursos que esse cmdlet pode parar.</span><span class="sxs-lookup"><span data-stu-id="548cc-113">The New-AzResource cmdlet creates a new resource, but it does not trigger a resource group deployment operation that this cmdlet can stop.</span></span>
<span data-ttu-id="548cc-114">Este cmdlet interrompe apenas uma implantação em execução.</span><span class="sxs-lookup"><span data-stu-id="548cc-114">This cmdlet stops only one running deployment.</span></span>
<span data-ttu-id="548cc-115">Use o *parâmetro Nome* para interromper uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="548cc-115">Use the *Name* parameter to stop a specific deployment.</span></span>
<span data-ttu-id="548cc-116">Se você omitir *o* parâmetro Nome, **Stop-AzResourceGroupDeployment** procurará uma implantação em execução e o interromperá.</span><span class="sxs-lookup"><span data-stu-id="548cc-116">If you omit the *Name* parameter, **Stop-AzResourceGroupDeployment** searches for a running deployment and stops it.</span></span>
<span data-ttu-id="548cc-117">Se o cmdlet encontrar mais de uma implantação em execução, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="548cc-117">If the cmdlet finds more than one running deployment, the command fails.</span></span>

## <span data-ttu-id="548cc-118">Exemplos</span><span class="sxs-lookup"><span data-stu-id="548cc-118">EXAMPLES</span></span>

### <span data-ttu-id="548cc-119">Exemplo 1: Iniciar e interromper uma implantação de grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="548cc-119">Example 1: Starting and stopping a resource group deployment</span></span>

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

## <span data-ttu-id="548cc-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="548cc-120">PARAMETERS</span></span>

### <span data-ttu-id="548cc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="548cc-121">-DefaultProfile</span></span>
<span data-ttu-id="548cc-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="548cc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="548cc-123">-ID</span><span class="sxs-lookup"><span data-stu-id="548cc-123">-Id</span></span>
<span data-ttu-id="548cc-124">Especifica a ID da implantação do grupo de recursos a ser parada.</span><span class="sxs-lookup"><span data-stu-id="548cc-124">Specifies the ID of the resource group deployment to stop.</span></span>

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

### <span data-ttu-id="548cc-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="548cc-125">-Name</span></span>
<span data-ttu-id="548cc-126">Especifica o nome da implantação do grupo de recursos a ser parada.</span><span class="sxs-lookup"><span data-stu-id="548cc-126">Specifies the name of the resource group deployment to stop.</span></span>
<span data-ttu-id="548cc-127">Se você não especificar esse parâmetro, esse cmdlet procurará uma implantação em execução no grupo de recursos e o interrompe.</span><span class="sxs-lookup"><span data-stu-id="548cc-127">If you do not specify this parameter, this cmdlet searches for a running deployment in the resource group and stops it.</span></span>
<span data-ttu-id="548cc-128">Se ele encontrar mais de uma implantação em execução, o comando falhará.</span><span class="sxs-lookup"><span data-stu-id="548cc-128">If it finds more than one running deployment, the command fails.</span></span>
<span data-ttu-id="548cc-129">Para obter o nome da implantação, use Get-AzResourceGroupDeployment cmdlet.</span><span class="sxs-lookup"><span data-stu-id="548cc-129">To get the deployment name, use the Get-AzResourceGroupDeployment cmdlet.</span></span>

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

### <span data-ttu-id="548cc-130">-Pré-</span><span class="sxs-lookup"><span data-stu-id="548cc-130">-Pre</span></span>
<span data-ttu-id="548cc-131">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="548cc-131">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="548cc-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="548cc-132">-ResourceGroupName</span></span>
<span data-ttu-id="548cc-133">Especifica o nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="548cc-133">Specifies the name of the resource group.</span></span>
<span data-ttu-id="548cc-134">Esse cmdlet interrompe a implantação do grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="548cc-134">This cmdlet stops the deployment of the resource group that this parameter specifies.</span></span>

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

### <span data-ttu-id="548cc-135">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="548cc-135">-Confirm</span></span>
<span data-ttu-id="548cc-136">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="548cc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="548cc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="548cc-137">-WhatIf</span></span>
<span data-ttu-id="548cc-138">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="548cc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="548cc-139">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="548cc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="548cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="548cc-140">CommonParameters</span></span>
<span data-ttu-id="548cc-141">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="548cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="548cc-142">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="548cc-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="548cc-143">Entradas</span><span class="sxs-lookup"><span data-stu-id="548cc-143">INPUTS</span></span>

### <span data-ttu-id="548cc-144">System.String</span><span class="sxs-lookup"><span data-stu-id="548cc-144">System.String</span></span>

## <span data-ttu-id="548cc-145">Saídas</span><span class="sxs-lookup"><span data-stu-id="548cc-145">OUTPUTS</span></span>

### <span data-ttu-id="548cc-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="548cc-146">System.Boolean</span></span>

## <span data-ttu-id="548cc-147">Notas</span><span class="sxs-lookup"><span data-stu-id="548cc-147">NOTES</span></span>

## <span data-ttu-id="548cc-148">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="548cc-148">RELATED LINKS</span></span>

[<span data-ttu-id="548cc-149">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="548cc-149">Get-AzResourceGroupDeployment</span></span>](./Get-AzResourceGroupDeployment.md)

[<span data-ttu-id="548cc-150">New-AzResource</span><span class="sxs-lookup"><span data-stu-id="548cc-150">New-AzResource</span></span>](./New-AzResource.md)

[<span data-ttu-id="548cc-151">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="548cc-151">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="548cc-152">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="548cc-152">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="548cc-153">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="548cc-153">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="548cc-154">Teste-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="548cc-154">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


