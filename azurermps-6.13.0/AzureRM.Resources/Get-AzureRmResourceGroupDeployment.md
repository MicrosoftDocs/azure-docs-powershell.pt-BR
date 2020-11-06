---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: a125635ec9cce66cb74c9a9d7c5f56323fb9b53f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93429377"
---
# <span data-ttu-id="92e17-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92e17-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="92e17-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="92e17-102">SYNOPSIS</span></span>
<span data-ttu-id="92e17-103">Obtém as implantações em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e17-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92e17-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="92e17-104">SYNTAX</span></span>

### <span data-ttu-id="92e17-105">GetByResourceGroupDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="92e17-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="92e17-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="92e17-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="92e17-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="92e17-107">DESCRIPTION</span></span>
<span data-ttu-id="92e17-108">O cmdlet **Get-AzureRmResourceGroupDeployment** Obtém as implantações em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="92e17-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="92e17-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="92e17-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="92e17-110">Por padrão, **Get-AzureRmResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="92e17-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="92e17-111">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site da Web.</span><span class="sxs-lookup"><span data-stu-id="92e17-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="92e17-112">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="92e17-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="92e17-113">Uma implantação é a operação que torna os recursos do grupo de recursos disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="92e17-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="92e17-114">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="92e17-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="92e17-115">Você pode usar esse cmdlet para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="92e17-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="92e17-116">Para a depuração, use esse cmdlet com o cmdlet Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="92e17-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="92e17-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="92e17-117">EXAMPLES</span></span>

### <span data-ttu-id="92e17-118">Exemplo 1: obter todas as implantações para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="92e17-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="92e17-119">Esse comando obtém todas as implantações para o grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="92e17-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="92e17-120">A saída mostra uma implantação de um blog do WordPress que usava um modelo de galeria.</span><span class="sxs-lookup"><span data-stu-id="92e17-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="92e17-121">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="92e17-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="92e17-122">Esse comando obtém a implantação do DeployWebsite01 do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="92e17-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="92e17-123">Você pode atribuir um nome a uma implantação ao criá-lo usando os cmdlets **New-AzureRmResourceGroup** ou **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="92e17-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="92e17-124">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="92e17-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="92e17-125">Exemplo 3: obter as implantações de todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="92e17-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="92e17-126">Esse comando obtém todos os grupos de recursos na sua assinatura usando o cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="92e17-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="92e17-127">O comando passa os grupos de recursos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="92e17-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="92e17-128">O cmdlet atual obtém todas as implantações de todos os grupos de recursos na assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName** , **deploymentname** e **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="92e17-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="92e17-129">OS</span><span class="sxs-lookup"><span data-stu-id="92e17-129">PARAMETERS</span></span>

### <span data-ttu-id="92e17-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="92e17-130">-ApiVersion</span></span>
<span data-ttu-id="92e17-131">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e17-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="92e17-132">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="92e17-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="92e17-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92e17-133">-DefaultProfile</span></span>
<span data-ttu-id="92e17-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="92e17-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="92e17-135">-ID</span><span class="sxs-lookup"><span data-stu-id="92e17-135">-Id</span></span>
<span data-ttu-id="92e17-136">Especifica a ID da implantação do grupo de recursos a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="92e17-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="92e17-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="92e17-137">-Name</span></span>
<span data-ttu-id="92e17-138">Especifica o nome da implantação a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="92e17-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="92e17-139">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="92e17-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="92e17-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="92e17-140">-Pre</span></span>
<span data-ttu-id="92e17-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="92e17-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="92e17-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92e17-142">-ResourceGroupName</span></span>
<span data-ttu-id="92e17-143">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="92e17-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="92e17-144">O cmdlet obtém as implantações do grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="92e17-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="92e17-145">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="92e17-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="92e17-146">Esse parâmetro é obrigatório e você pode especificar apenas um grupo de recursos em cada comando.</span><span class="sxs-lookup"><span data-stu-id="92e17-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="92e17-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92e17-147">CommonParameters</span></span>
<span data-ttu-id="92e17-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92e17-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92e17-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92e17-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92e17-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="92e17-150">INPUTS</span></span>

### <span data-ttu-id="92e17-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="92e17-151">None</span></span>

## <span data-ttu-id="92e17-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="92e17-152">OUTPUTS</span></span>

### <span data-ttu-id="92e17-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="92e17-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="92e17-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92e17-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="92e17-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="92e17-155">NOTES</span></span>

## <span data-ttu-id="92e17-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="92e17-156">RELATED LINKS</span></span>

[<span data-ttu-id="92e17-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92e17-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="92e17-158">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="92e17-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="92e17-159">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92e17-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="92e17-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92e17-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="92e17-161">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92e17-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="92e17-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="92e17-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


