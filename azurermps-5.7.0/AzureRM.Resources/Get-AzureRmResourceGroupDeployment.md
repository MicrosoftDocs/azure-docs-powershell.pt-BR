---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmResourceGroupDeployment.md
ms.openlocfilehash: dd61700c5f064a7bc1db84286252a57c18a212db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93603232"
---
# <span data-ttu-id="2fdb5-101">Get-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fdb5-101">Get-AzureRmResourceGroupDeployment</span></span>

## <span data-ttu-id="2fdb5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="2fdb5-102">SYNOPSIS</span></span>
<span data-ttu-id="2fdb5-103">Obtém as implantações em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-103">Gets the deployments in a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fdb5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2fdb5-104">SYNTAX</span></span>

### <span data-ttu-id="2fdb5-105">GetByResourceGroupDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="2fdb5-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzureRmResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2fdb5-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="2fdb5-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzureRmResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fdb5-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="2fdb5-107">DESCRIPTION</span></span>
<span data-ttu-id="2fdb5-108">O cmdlet **Get-AzureRmResourceGroupDeployment** Obtém as implantações em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-108">The **Get-AzureRmResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="2fdb5-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="2fdb5-110">Por padrão, **Get-AzureRmResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-110">By default, **Get-AzureRmResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>

<span data-ttu-id="2fdb5-111">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site da Web.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="2fdb5-112">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>

<span data-ttu-id="2fdb5-113">Uma implantação é a operação que torna os recursos do grupo de recursos disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="2fdb5-114">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-114">For more information about Azure resources and Azure resource groups, see the New-AzureRmResourceGroup cmdlet.</span></span>

<span data-ttu-id="2fdb5-115">Você pode usar esse cmdlet para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="2fdb5-116">Para a depuração, use esse cmdlet com o cmdlet Get-AzureRmLog.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-116">For debugging, use this cmdlet with the Get-AzureRmLog cmdlet.</span></span>

## <span data-ttu-id="2fdb5-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="2fdb5-117">EXAMPLES</span></span>

### <span data-ttu-id="2fdb5-118">Exemplo 1: obter todas as implantações para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="2fdb5-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="2fdb5-119">Esse comando obtém todas as implantações para o grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="2fdb5-120">A saída mostra uma implantação de um blog do WordPress que usava um modelo de galeria.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="2fdb5-121">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="2fdb5-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="2fdb5-122">Esse comando obtém a implantação do DeployWebsite01 do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="2fdb5-123">Você pode atribuir um nome a uma implantação ao criá-lo usando os cmdlets **New-AzureRmResourceGroup** ou **New-AzureRmResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="2fdb5-123">You can assign a name to a deployment when you create it by using the **New-AzureRmResourceGroup** or **New-AzureRmResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="2fdb5-124">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="2fdb5-125">Exemplo 3: obter as implantações de todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="2fdb5-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzureRmResourceGroup | Get-AzureRmResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="2fdb5-126">Esse comando obtém todos os grupos de recursos na sua assinatura usando o cmdlet Get-AzureRmResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-126">This command gets all resource groups in your subscription by using the Get-AzureRmResourceGroup cmdlet.</span></span>
<span data-ttu-id="2fdb5-127">O comando passa os grupos de recursos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2fdb5-128">O cmdlet atual obtém todas as implantações de todos os grupos de recursos na assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName** , **deploymentname** e **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="2fdb5-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="2fdb5-129">OS</span><span class="sxs-lookup"><span data-stu-id="2fdb5-129">PARAMETERS</span></span>

### <span data-ttu-id="2fdb5-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="2fdb5-130">-ApiVersion</span></span>
<span data-ttu-id="2fdb5-131">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="2fdb5-132">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-132">You can specify a different version than the default version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb5-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fdb5-133">-DefaultProfile</span></span>
<span data-ttu-id="2fdb5-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="2fdb5-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb5-135">-ID</span><span class="sxs-lookup"><span data-stu-id="2fdb5-135">-Id</span></span>
<span data-ttu-id="2fdb5-136">Especifica a ID da implantação do grupo de recursos a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-136">Specifies the ID of the resource group deployment to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb5-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="2fdb5-137">-Name</span></span>
<span data-ttu-id="2fdb5-138">Especifica o nome da implantação a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="2fdb5-139">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-139">Wildcard characters are not permitted.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb5-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="2fdb5-140">-Pre</span></span>
<span data-ttu-id="2fdb5-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb5-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fdb5-142">-ResourceGroupName</span></span>
<span data-ttu-id="2fdb5-143">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="2fdb5-144">O cmdlet obtém as implantações do grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="2fdb5-145">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="2fdb5-146">Esse parâmetro é obrigatório e você pode especificar apenas um grupo de recursos em cada comando.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-146">This parameter is required and you can specify only one resource group in each command.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceGroupDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fdb5-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fdb5-147">CommonParameters</span></span>
<span data-ttu-id="2fdb5-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fdb5-149">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fdb5-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fdb5-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="2fdb5-150">INPUTS</span></span>

### <span data-ttu-id="2fdb5-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="2fdb5-151">None</span></span>

## <span data-ttu-id="2fdb5-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="2fdb5-152">OUTPUTS</span></span>

### <span data-ttu-id="2fdb5-153">Microsoft. Azure. Commands. ResourceManagement. Models. PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fdb5-153">Microsoft.Azure.Commands.ResourceManagement.Models.PSResourceGroupDeployment</span></span>
<span data-ttu-id="2fdb5-154">O cmdlet retorna implantações de grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="2fdb5-154">The cmdlet returns resource group deployments.</span></span>

## <span data-ttu-id="2fdb5-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="2fdb5-155">NOTES</span></span>

## <span data-ttu-id="2fdb5-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="2fdb5-156">RELATED LINKS</span></span>

[<span data-ttu-id="2fdb5-157">Get-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fdb5-157">Get-AzureRmResourceGroup</span></span>](./Get-AzureRmResourceGroup.md)

[<span data-ttu-id="2fdb5-158">New-AzureRmResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2fdb5-158">New-AzureRmResourceGroup</span></span>](./New-AzureRmResourceGroup.md)

[<span data-ttu-id="2fdb5-159">New-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fdb5-159">New-AzureRmResourceGroupDeployment</span></span>](./New-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2fdb5-160">Remove-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fdb5-160">Remove-AzureRmResourceGroupDeployment</span></span>](./Remove-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2fdb5-161">Parar-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fdb5-161">Stop-AzureRmResourceGroupDeployment</span></span>](./Stop-AzureRmResourceGroupDeployment.md)

[<span data-ttu-id="2fdb5-162">Test-AzureRmResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="2fdb5-162">Test-AzureRmResourceGroupDeployment</span></span>](./Test-AzureRmResourceGroupDeployment.md)


