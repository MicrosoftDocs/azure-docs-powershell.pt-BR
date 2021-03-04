---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: eb79b6a46f2eaadfc6a42159706c37017cdac8d1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101890084"
---
# <span data-ttu-id="6e607-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e607-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="6e607-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e607-102">SYNOPSIS</span></span>
<span data-ttu-id="6e607-103">Obtém as implantações em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e607-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="6e607-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="6e607-104">SYNTAX</span></span>

### <span data-ttu-id="6e607-105">GetByResourceGroupDeploymentName (Default)</span><span class="sxs-lookup"><span data-stu-id="6e607-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6e607-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="6e607-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6e607-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="6e607-107">DESCRIPTION</span></span>
<span data-ttu-id="6e607-108">O cmdlet **Get-AzResourceGroupDeployment** obtém as implantações em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="6e607-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="6e607-109">*Especifique o parâmetro Name* ou *Id* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="6e607-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="6e607-110">Por padrão, **Get-AzResourceGroupDeployment** obtém todas as implantações de um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="6e607-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="6e607-111">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site.</span><span class="sxs-lookup"><span data-stu-id="6e607-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="6e607-112">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="6e607-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="6e607-113">Uma implantação é a operação que disponibiliza os recursos no grupo de recursos para uso.</span><span class="sxs-lookup"><span data-stu-id="6e607-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="6e607-114">Para obter mais informações sobre recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="6e607-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6e607-115">Você pode usar esse cmdlet para rastreamento.</span><span class="sxs-lookup"><span data-stu-id="6e607-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="6e607-116">Para depuração, use este cmdlet com Get-AzLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6e607-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="6e607-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6e607-117">EXAMPLES</span></span>

### <span data-ttu-id="6e607-118">Exemplo 1: Obter todas as implantações para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="6e607-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="6e607-119">Este comando obtém todas as implantações do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="6e607-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="6e607-120">A saída mostra uma implantação para um blog do WordPress que usou um modelo de galeria.</span><span class="sxs-lookup"><span data-stu-id="6e607-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="6e607-121">Exemplo 2: Obter uma implantação pelo nome</span><span class="sxs-lookup"><span data-stu-id="6e607-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="6e607-122">Este comando obtém a implantação DeployWebsite01 do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="6e607-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="6e607-123">Você pode atribuir um nome a uma implantação ao criar usando os cmdlets **New-AzResourceGroup** ou **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="6e607-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="6e607-124">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="6e607-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="6e607-125">Exemplo 3: Obter as implantações de todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="6e607-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="6e607-126">Esse comando obtém todos os grupos de recursos em sua assinatura usando o cmdlet Get-AzResourceGroup usuário.</span><span class="sxs-lookup"><span data-stu-id="6e607-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="6e607-127">O comando passa os grupos de recursos para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="6e607-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="6e607-128">O cmdlet atual obtém todas as implantações de todos os grupos de recursos na assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName,** **DeploymentName** e **ProvisioningState.**</span><span class="sxs-lookup"><span data-stu-id="6e607-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="6e607-129">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="6e607-129">PARAMETERS</span></span>

### <span data-ttu-id="6e607-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e607-130">-DefaultProfile</span></span>
<span data-ttu-id="6e607-131">As credenciais, conta, locatário e assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="6e607-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6e607-132">-Id</span><span class="sxs-lookup"><span data-stu-id="6e607-132">-Id</span></span>
<span data-ttu-id="6e607-133">Especifica a ID da implantação do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="6e607-133">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6e607-134">-Name</span><span class="sxs-lookup"><span data-stu-id="6e607-134">-Name</span></span>
<span data-ttu-id="6e607-135">Especifica o nome da implantação a ser obter.</span><span class="sxs-lookup"><span data-stu-id="6e607-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="6e607-136">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6e607-136">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e607-137">-Pre</span><span class="sxs-lookup"><span data-stu-id="6e607-137">-Pre</span></span>
<span data-ttu-id="6e607-138">Indica que esse cmdlet considera versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="6e607-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6e607-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e607-139">-ResourceGroupName</span></span>
<span data-ttu-id="6e607-140">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="6e607-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="6e607-141">O cmdlet obtém as implantações do grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6e607-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="6e607-142">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="6e607-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="6e607-143">Esse parâmetro é necessário e você pode especificar apenas um grupo de recursos em cada comando.</span><span class="sxs-lookup"><span data-stu-id="6e607-143">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6e607-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e607-144">CommonParameters</span></span>
<span data-ttu-id="6e607-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6e607-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e607-146">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6e607-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e607-147">INPUTS</span><span class="sxs-lookup"><span data-stu-id="6e607-147">INPUTS</span></span>

### <span data-ttu-id="6e607-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6e607-148">System.String</span></span>

## <span data-ttu-id="6e607-149">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="6e607-149">OUTPUTS</span></span>

### <span data-ttu-id="6e607-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e607-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="6e607-151">NOTES</span><span class="sxs-lookup"><span data-stu-id="6e607-151">NOTES</span></span>

## <span data-ttu-id="6e607-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6e607-152">RELATED LINKS</span></span>

[<span data-ttu-id="6e607-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e607-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="6e607-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6e607-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="6e607-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e607-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="6e607-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e607-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="6e607-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e607-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="6e607-158">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="6e607-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


