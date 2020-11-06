---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: e64fdd0300f2ccad4c3904d472563bbc30374b67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93432578"
---
# <span data-ttu-id="8b623-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b623-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="8b623-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="8b623-102">SYNOPSIS</span></span>
<span data-ttu-id="8b623-103">Obtém as implantações em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b623-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8b623-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8b623-104">SYNTAX</span></span>

### <span data-ttu-id="8b623-105">O parâmetro de nome de implantação definido.</span><span class="sxs-lookup"><span data-stu-id="8b623-105">The deployment name parameter set.</span></span> <span data-ttu-id="8b623-106">Assume</span><span class="sxs-lookup"><span data-stu-id="8b623-106">(Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8b623-107">O conjunto de parâmetros de ID de implantação.</span><span class="sxs-lookup"><span data-stu-id="8b623-107">The deployment Id parameter set.</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8b623-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="8b623-108">DESCRIPTION</span></span>
<span data-ttu-id="8b623-109">O cmdlet **Get-AzureRmResourceGroupDeployment** Obtém as implantações em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="8b623-109">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="8b623-110">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="8b623-110">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="8b623-111">Por padrão, **Get-AzureRmResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="8b623-111">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="8b623-112">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site da Web.</span><span class="sxs-lookup"><span data-stu-id="8b623-112">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="8b623-113">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="8b623-113">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="8b623-114">Uma implantação é a operação que torna os recursos do grupo de recursos disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="8b623-114">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="8b623-115">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8b623-115">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="8b623-116">Você pode usar esse cmdlet para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="8b623-116">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="8b623-117">Para a depuração, use esse cmdlet com o cmdlet Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="8b623-117">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="8b623-118">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="8b623-118">EXAMPLES</span></span>

### <span data-ttu-id="8b623-119">Exemplo 1: obter todas as implantações para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="8b623-119">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="8b623-120">Esse comando obtém todas as implantações para o grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="8b623-120">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="8b623-121">A saída mostra uma implantação de um blog do WordPress que usava um modelo de galeria.</span><span class="sxs-lookup"><span data-stu-id="8b623-121">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="8b623-122">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="8b623-122">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="8b623-123">Esse comando obtém a implantação do DeployWebsite01 do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="8b623-123">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="8b623-124">Você pode atribuir um nome a uma implantação ao criá-lo usando os cmdlets **New-AzureRmResourceGroup** ou **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="8b623-124">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="8b623-125">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="8b623-125">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="8b623-126">Exemplo 3: obter as implantações de todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="8b623-126">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="8b623-127">Esse comando obtém todos os grupos de recursos na sua assinatura usando o cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="8b623-127">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="8b623-128">O comando passa os grupos de recursos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="8b623-128">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="8b623-129">O cmdlet atual obtém todas as implantações de todos os grupos de recursos na assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName** , **deploymentname** e **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="8b623-129">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="8b623-130">OS</span><span class="sxs-lookup"><span data-stu-id="8b623-130">PARAMETERS</span></span>

### <span data-ttu-id="8b623-131">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="8b623-131">-ApiVersion</span></span>
<span data-ttu-id="8b623-132">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b623-132">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="8b623-133">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="8b623-133">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="8b623-134">-ID</span><span class="sxs-lookup"><span data-stu-id="8b623-134">-Id</span></span>
<span data-ttu-id="8b623-135">Especifica a ID da implantação do grupo de recursos a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="8b623-135">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment Id parameter set.
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b623-136">-Nome</span><span class="sxs-lookup"><span data-stu-id="8b623-136">-Name</span></span>
<span data-ttu-id="8b623-137">Especifica o nome da implantação a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="8b623-137">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="8b623-138">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="8b623-138">Wildcard characters are not permitted.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b623-139">-Pre</span><span class="sxs-lookup"><span data-stu-id="8b623-139">-Pre</span></span>
<span data-ttu-id="8b623-140">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="8b623-140">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="8b623-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b623-141">-ResourceGroupName</span></span>
<span data-ttu-id="8b623-142">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b623-142">Specifies the name of a resource group.</span></span>
<span data-ttu-id="8b623-143">O cmdlet obtém as implantações do grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="8b623-143">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="8b623-144">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="8b623-144">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="8b623-145">Esse parâmetro é obrigatório e você pode especificar apenas um grupo de recursos em cada comando.</span><span class="sxs-lookup"><span data-stu-id="8b623-145">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: System.String
Parameter Sets: The deployment name parameter set.
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8b623-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b623-146">-DefaultProfile</span></span>
<span data-ttu-id="8b623-147">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="8b623-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b623-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b623-148">CommonParameters</span></span>
<span data-ttu-id="8b623-149">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b623-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b623-150">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b623-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b623-151">SENSORES</span><span class="sxs-lookup"><span data-stu-id="8b623-151">INPUTS</span></span>

### <span data-ttu-id="8b623-152">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="8b623-152">None</span></span>

## <span data-ttu-id="8b623-153">EXIBE</span><span class="sxs-lookup"><span data-stu-id="8b623-153">OUTPUTS</span></span>

### <span data-ttu-id="8b623-154">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b623-154">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="8b623-155">O cmdlet retorna implantações de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="8b623-155">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="8b623-156">INFORMA</span><span class="sxs-lookup"><span data-stu-id="8b623-156">NOTES</span></span>

## <span data-ttu-id="8b623-157">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="8b623-157">RELATED LINKS</span></span>

[<span data-ttu-id="8b623-158">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b623-158">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="8b623-159">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="8b623-159">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="8b623-160">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b623-160">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8b623-161">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b623-161">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8b623-162">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b623-162">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="8b623-163">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="8b623-163">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


