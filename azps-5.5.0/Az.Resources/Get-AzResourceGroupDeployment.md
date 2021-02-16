---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 82df573a658fda9af97778e59819e45359c226fd
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100113331"
---
# <span data-ttu-id="09fa2-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09fa2-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="09fa2-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="09fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="09fa2-103">Obtém as implantações em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09fa2-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="09fa2-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09fa2-104">SYNTAX</span></span>

### <span data-ttu-id="09fa2-105">GetByResourceGroupDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="09fa2-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09fa2-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="09fa2-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09fa2-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="09fa2-107">DESCRIPTION</span></span>
<span data-ttu-id="09fa2-108">O cmdlet **Get-AzResourceGroupDeployment** obtém as implantações em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="09fa2-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="09fa2-109">*Especifique o* parâmetro Nome ou *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="09fa2-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="09fa2-110">Por padrão, **Get-AzResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="09fa2-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="09fa2-111">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, um banco de dados ou um site da Web.</span><span class="sxs-lookup"><span data-stu-id="09fa2-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="09fa2-112">Um grupo de recursos do Azure é um conjunto de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="09fa2-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="09fa2-113">Uma implantação é a operação que disponibiliza os recursos no grupo de recursos para uso.</span><span class="sxs-lookup"><span data-stu-id="09fa2-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="09fa2-114">Para obter mais informações sobre recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="09fa2-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="09fa2-115">Você pode usar esse cmdlet para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="09fa2-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="09fa2-116">Para depuração, use este cmdlet com Get-AzLog cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09fa2-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="09fa2-117">Exemplos</span><span class="sxs-lookup"><span data-stu-id="09fa2-117">EXAMPLES</span></span>

### <span data-ttu-id="09fa2-118">Exemplo 1: Obter todas as implantações para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="09fa2-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="09fa2-119">Esse comando obtém todas as implantações do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="09fa2-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="09fa2-120">A saída mostra uma implantação para um blog do WordPress que usou um modelo de galeria.</span><span class="sxs-lookup"><span data-stu-id="09fa2-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="09fa2-121">Exemplo 2: Obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="09fa2-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="09fa2-122">Esse comando obtém a implantação DeployWebsite01 do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="09fa2-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="09fa2-123">Você pode atribuir um nome a uma implantação quando a criar usando os cmdlets **New-AzResourceGroup** ou **New-AzResourceGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="09fa2-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="09fa2-124">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="09fa2-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="09fa2-125">Exemplo 3: Obter as implantações de todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="09fa2-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="09fa2-126">Esse comando obtém todos os grupos de recursos em sua assinatura usando o cmdlet Get-AzResourceGroup dados.</span><span class="sxs-lookup"><span data-stu-id="09fa2-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="09fa2-127">O comando passa os grupos de recursos para o cmdlet atual usando o operador de pipeline.</span><span class="sxs-lookup"><span data-stu-id="09fa2-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="09fa2-128">O cmdlet atual obtém todas as implantações de todos os grupos de recursos da assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName,** **DeploymentName** e **ProvisioningState.**</span><span class="sxs-lookup"><span data-stu-id="09fa2-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName**, **DeploymentName**, and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="09fa2-129">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09fa2-129">PARAMETERS</span></span>

### <span data-ttu-id="09fa2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09fa2-130">-DefaultProfile</span></span>
<span data-ttu-id="09fa2-131">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure</span><span class="sxs-lookup"><span data-stu-id="09fa2-131">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09fa2-132">-ID</span><span class="sxs-lookup"><span data-stu-id="09fa2-132">-Id</span></span>
<span data-ttu-id="09fa2-133">Especifica a ID da implantação do grupo de recursos a ser obter.</span><span class="sxs-lookup"><span data-stu-id="09fa2-133">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="09fa2-134">-Nome</span><span class="sxs-lookup"><span data-stu-id="09fa2-134">-Name</span></span>
<span data-ttu-id="09fa2-135">Especifica o nome da implantação a ser obter.</span><span class="sxs-lookup"><span data-stu-id="09fa2-135">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="09fa2-136">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="09fa2-136">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="09fa2-137">-Pré-</span><span class="sxs-lookup"><span data-stu-id="09fa2-137">-Pre</span></span>
<span data-ttu-id="09fa2-138">Indica que esse cmdlet considera as versões da API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="09fa2-138">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="09fa2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09fa2-139">-ResourceGroupName</span></span>
<span data-ttu-id="09fa2-140">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="09fa2-140">Specifies the name of a resource group.</span></span>
<span data-ttu-id="09fa2-141">O cmdlet obtém as implantações do grupo de recursos especificado por esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="09fa2-141">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="09fa2-142">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="09fa2-142">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="09fa2-143">Esse parâmetro é necessário e você pode especificar apenas um grupo de recursos em cada comando.</span><span class="sxs-lookup"><span data-stu-id="09fa2-143">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="09fa2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09fa2-144">CommonParameters</span></span>
<span data-ttu-id="09fa2-145">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09fa2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09fa2-146">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="09fa2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09fa2-147">Entradas</span><span class="sxs-lookup"><span data-stu-id="09fa2-147">INPUTS</span></span>

### <span data-ttu-id="09fa2-148">System.String</span><span class="sxs-lookup"><span data-stu-id="09fa2-148">System.String</span></span>

## <span data-ttu-id="09fa2-149">Saídas</span><span class="sxs-lookup"><span data-stu-id="09fa2-149">OUTPUTS</span></span>

### <span data-ttu-id="09fa2-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09fa2-150">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroupDeployment</span></span>

## <span data-ttu-id="09fa2-151">Notas</span><span class="sxs-lookup"><span data-stu-id="09fa2-151">NOTES</span></span>

## <span data-ttu-id="09fa2-152">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="09fa2-152">RELATED LINKS</span></span>

[<span data-ttu-id="09fa2-153">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09fa2-153">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="09fa2-154">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="09fa2-154">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="09fa2-155">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09fa2-155">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="09fa2-156">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09fa2-156">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="09fa2-157">Stop-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09fa2-157">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="09fa2-158">Teste-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="09fa2-158">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


