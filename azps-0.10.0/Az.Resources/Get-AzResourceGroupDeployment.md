---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 20CB842B-F7A9-4052-85D9-0DF9586D5FEA
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeployment.md
ms.openlocfilehash: 2703a5f32142ddd8d5754c89924360564b45d0f9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776432"
---
# <span data-ttu-id="53ff1-101">Get-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53ff1-101">Get-AzResourceGroupDeployment</span></span>

## <span data-ttu-id="53ff1-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="53ff1-102">SYNOPSIS</span></span>
<span data-ttu-id="53ff1-103">Obtém as implantações em um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53ff1-103">Gets the deployments in a resource group.</span></span>

## <span data-ttu-id="53ff1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="53ff1-104">SYNTAX</span></span>

### <span data-ttu-id="53ff1-105">GetByResourceGroupDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="53ff1-105">GetByResourceGroupDeploymentName (Default)</span></span>
```
Get-AzResourceGroupDeployment [-ResourceGroupName] <String> [[-Name] <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53ff1-106">GetByResourceGroupDeploymentId</span><span class="sxs-lookup"><span data-stu-id="53ff1-106">GetByResourceGroupDeploymentId</span></span>
```
Get-AzResourceGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53ff1-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="53ff1-107">DESCRIPTION</span></span>
<span data-ttu-id="53ff1-108">O cmdlet **Get-AzResourceGroupDeployment** Obtém as implantações em um grupo de recursos do Azure.</span><span class="sxs-lookup"><span data-stu-id="53ff1-108">The **Get-AzResourceGroupDeployment** cmdlet gets the deployments in an Azure resource group.</span></span>
<span data-ttu-id="53ff1-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="53ff1-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="53ff1-110">Por padrão, **Get-AzResourceGroupDeployment** obtém todas as implantações para um grupo de recursos especificado.</span><span class="sxs-lookup"><span data-stu-id="53ff1-110">By default, **Get-AzResourceGroupDeployment** gets all deployments for a specified resource group.</span></span>
<span data-ttu-id="53ff1-111">Um recurso do Azure é uma entidade do Azure gerenciada pelo usuário, como um servidor de banco de dados, banco de dados ou site da Web.</span><span class="sxs-lookup"><span data-stu-id="53ff1-111">An Azure resource is a user-managed Azure entity, such as a database server, database, or web site.</span></span>
<span data-ttu-id="53ff1-112">Um grupo de recursos do Azure é uma coleção de recursos do Azure implantados como uma unidade.</span><span class="sxs-lookup"><span data-stu-id="53ff1-112">An Azure resource group is a collection of Azure resources that are deployed as a unit.</span></span>
<span data-ttu-id="53ff1-113">Uma implantação é a operação que torna os recursos do grupo de recursos disponíveis para uso.</span><span class="sxs-lookup"><span data-stu-id="53ff1-113">A deployment is the operation that makes the resources in the resource group available for use.</span></span>
<span data-ttu-id="53ff1-114">Para obter mais informações sobre os recursos do Azure e grupos de recursos do Azure, consulte o cmdlet New-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="53ff1-114">For more information about Azure resources and Azure resource groups, see the New-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="53ff1-115">Você pode usar esse cmdlet para acompanhamento.</span><span class="sxs-lookup"><span data-stu-id="53ff1-115">You can use this cmdlet for tracking.</span></span>
<span data-ttu-id="53ff1-116">Para a depuração, use esse cmdlet com o cmdlet Get-AzLog.</span><span class="sxs-lookup"><span data-stu-id="53ff1-116">For debugging, use this cmdlet with the Get-AzLog cmdlet.</span></span>

## <span data-ttu-id="53ff1-117">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="53ff1-117">EXAMPLES</span></span>

### <span data-ttu-id="53ff1-118">Exemplo 1: obter todas as implantações para um grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="53ff1-118">Example 1: Get all deployments for a resource group</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG"
```

<span data-ttu-id="53ff1-119">Esse comando obtém todas as implantações para o grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="53ff1-119">This command gets all deployments for the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="53ff1-120">A saída mostra uma implantação de um blog do WordPress que usava um modelo de galeria.</span><span class="sxs-lookup"><span data-stu-id="53ff1-120">The output shows a deployment for a WordPress blog that used a gallery template.</span></span>

### <span data-ttu-id="53ff1-121">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="53ff1-121">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzResourceGroupDeployment -ResourceGroupName "ContosoLabsRG" -Name "DeployWebsite01"
```

<span data-ttu-id="53ff1-122">Esse comando obtém a implantação do DeployWebsite01 do grupo de recursos ContosoLabsRG.</span><span class="sxs-lookup"><span data-stu-id="53ff1-122">This command gets the DeployWebsite01 deployment of the ContosoLabsRG resource group.</span></span>
<span data-ttu-id="53ff1-123">Você pode atribuir um nome a uma implantação ao criá-lo usando os cmdlets **New-AzResourceGroup** ou **New-AzResourceGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="53ff1-123">You can assign a name to a deployment when you create it by using the **New-AzResourceGroup** or **New-AzResourceGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="53ff1-124">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="53ff1-124">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="53ff1-125">Exemplo 3: obter as implantações de todos os grupos de recursos</span><span class="sxs-lookup"><span data-stu-id="53ff1-125">Example 3: Get the deployments of all resource groups</span></span>
```
PS C:\>Get-AzResourceGroup | Get-AzResourceGroupDeployment | Format-Table ResourceGroupName, DeploymentName, ProvisioningState
```

<span data-ttu-id="53ff1-126">Esse comando obtém todos os grupos de recursos na sua assinatura usando o cmdlet Get-AzResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="53ff1-126">This command gets all resource groups in your subscription by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="53ff1-127">O comando passa os grupos de recursos para o cmdlet atual usando o operador pipeline.</span><span class="sxs-lookup"><span data-stu-id="53ff1-127">The command passes the resource groups to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="53ff1-128">O cmdlet atual obtém todas as implantações de todos os grupos de recursos na assinatura e passa os resultados para o cmdlet Format-Table para exibir seus valores de propriedade **ResourceGroupName** , **deploymentname** e **ProvisioningState** .</span><span class="sxs-lookup"><span data-stu-id="53ff1-128">The current cmdlet gets all deployments of all resource groups in the subscription, and passes the results to the Format-Table cmdlet to display their **ResourceGroupName** , **DeploymentName** , and **ProvisioningState** property values.</span></span>

## <span data-ttu-id="53ff1-129">OS</span><span class="sxs-lookup"><span data-stu-id="53ff1-129">PARAMETERS</span></span>

### <span data-ttu-id="53ff1-130">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="53ff1-130">-ApiVersion</span></span>
<span data-ttu-id="53ff1-131">Especifica a versão da API que é suportada pelo provedor de recursos.</span><span class="sxs-lookup"><span data-stu-id="53ff1-131">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="53ff1-132">Você pode especificar uma versão diferente da versão padrão.</span><span class="sxs-lookup"><span data-stu-id="53ff1-132">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="53ff1-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53ff1-133">-DefaultProfile</span></span>
<span data-ttu-id="53ff1-134">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="53ff1-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="53ff1-135">-ID</span><span class="sxs-lookup"><span data-stu-id="53ff1-135">-Id</span></span>
<span data-ttu-id="53ff1-136">Especifica a ID da implantação do grupo de recursos a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="53ff1-136">Specifies the ID of the resource group deployment to get.</span></span>

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

### <span data-ttu-id="53ff1-137">-Nome</span><span class="sxs-lookup"><span data-stu-id="53ff1-137">-Name</span></span>
<span data-ttu-id="53ff1-138">Especifica o nome da implantação a ser obtida.</span><span class="sxs-lookup"><span data-stu-id="53ff1-138">Specifies the name of the deployment to get.</span></span>
<span data-ttu-id="53ff1-139">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="53ff1-139">Wildcard characters are not permitted.</span></span>

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

### <span data-ttu-id="53ff1-140">-Pre</span><span class="sxs-lookup"><span data-stu-id="53ff1-140">-Pre</span></span>
<span data-ttu-id="53ff1-141">Indica que esse cmdlet considera versões de API de pré-lançamento quando determina automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="53ff1-141">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="53ff1-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53ff1-142">-ResourceGroupName</span></span>
<span data-ttu-id="53ff1-143">Especifica o nome de um grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="53ff1-143">Specifies the name of a resource group.</span></span>
<span data-ttu-id="53ff1-144">O cmdlet obtém as implantações do grupo de recursos que esse parâmetro especifica.</span><span class="sxs-lookup"><span data-stu-id="53ff1-144">The cmdlet gets the deployments for the resource group that this parameter specifies.</span></span>
<span data-ttu-id="53ff1-145">Caracteres curinga não são permitidos.</span><span class="sxs-lookup"><span data-stu-id="53ff1-145">Wildcard characters are not permitted.</span></span>
<span data-ttu-id="53ff1-146">Esse parâmetro é obrigatório e você pode especificar apenas um grupo de recursos em cada comando.</span><span class="sxs-lookup"><span data-stu-id="53ff1-146">This parameter is required and you can specify only one resource group in each command.</span></span>

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

### <span data-ttu-id="53ff1-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53ff1-147">CommonParameters</span></span>
<span data-ttu-id="53ff1-148">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53ff1-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53ff1-149">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53ff1-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53ff1-150">SENSORES</span><span class="sxs-lookup"><span data-stu-id="53ff1-150">INPUTS</span></span>

### <span data-ttu-id="53ff1-151">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="53ff1-151">None</span></span>

## <span data-ttu-id="53ff1-152">EXIBE</span><span class="sxs-lookup"><span data-stu-id="53ff1-152">OUTPUTS</span></span>

### <span data-ttu-id="53ff1-153">Microsoft. Azure. Commands. ResourceManagement. Models.</span><span class="sxs-lookup"><span data-stu-id="53ff1-153">Microsoft.Azure.Commands.ResourceManagement.Models.</span></span> <span data-ttu-id="53ff1-154">PSResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53ff1-154">PSResourceGroupDeployment</span></span>

## <span data-ttu-id="53ff1-155">INFORMA</span><span class="sxs-lookup"><span data-stu-id="53ff1-155">NOTES</span></span>

## <span data-ttu-id="53ff1-156">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="53ff1-156">RELATED LINKS</span></span>

[<span data-ttu-id="53ff1-157">Get-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53ff1-157">Get-AzResourceGroup</span></span>](./Get-AzResourceGroup.md)

[<span data-ttu-id="53ff1-158">New-AzResourceGroup</span><span class="sxs-lookup"><span data-stu-id="53ff1-158">New-AzResourceGroup</span></span>](./New-AzResourceGroup.md)

[<span data-ttu-id="53ff1-159">New-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53ff1-159">New-AzResourceGroupDeployment</span></span>](./New-AzResourceGroupDeployment.md)

[<span data-ttu-id="53ff1-160">Remove-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53ff1-160">Remove-AzResourceGroupDeployment</span></span>](./Remove-AzResourceGroupDeployment.md)

[<span data-ttu-id="53ff1-161">Parar-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53ff1-161">Stop-AzResourceGroupDeployment</span></span>](./Stop-AzResourceGroupDeployment.md)

[<span data-ttu-id="53ff1-162">Test-AzResourceGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="53ff1-162">Test-AzResourceGroupDeployment</span></span>](./Test-AzResourceGroupDeployment.md)


