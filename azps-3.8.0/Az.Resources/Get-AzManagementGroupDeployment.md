---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6a18c886ddddc30c82746ebe76d83d9477399755
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778114"
---
# <span data-ttu-id="ac8bf-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="ac8bf-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="ac8bf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ac8bf-102">SYNOPSIS</span></span>
<span data-ttu-id="ac8bf-103">Obter implantação em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ac8bf-103">Get deployment at a mangement group</span></span>

## <span data-ttu-id="ac8bf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac8bf-104">SYNTAX</span></span>

### <span data-ttu-id="ac8bf-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="ac8bf-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ac8bf-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="ac8bf-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac8bf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="ac8bf-107">DESCRIPTION</span></span>
<span data-ttu-id="ac8bf-108">O cmdlet **Get-AzManagementGroupDeployment** Obtém as implantações em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="ac8bf-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="ac8bf-110">Por padrão, **Get-AzManagementGroupDeployment** obtém todas as implantações no grupo Gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="ac8bf-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ac8bf-111">EXAMPLES</span></span>

### <span data-ttu-id="ac8bf-112">Exemplo 1: obter todas as implantações em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ac8bf-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="ac8bf-113">Esse comando obtém todas as implantações no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="ac8bf-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="ac8bf-114">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="ac8bf-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="ac8bf-115">Esse comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="ac8bf-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="ac8bf-116">Você pode atribuir um nome a uma implantação ao criá-lo usando cmdlets **New-AzManagementGroupDeployment** .</span><span class="sxs-lookup"><span data-stu-id="ac8bf-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="ac8bf-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="ac8bf-118">Exemplo 3: obter uma implantação por ID</span><span class="sxs-lookup"><span data-stu-id="ac8bf-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="ac8bf-119">Esse comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="ac8bf-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="ac8bf-120">OS</span><span class="sxs-lookup"><span data-stu-id="ac8bf-120">PARAMETERS</span></span>

### <span data-ttu-id="ac8bf-121">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="ac8bf-121">-ApiVersion</span></span>
<span data-ttu-id="ac8bf-122">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-122">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="ac8bf-123">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-123">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="ac8bf-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac8bf-124">-DefaultProfile</span></span>
<span data-ttu-id="ac8bf-125">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8bf-126">-ID</span><span class="sxs-lookup"><span data-stu-id="ac8bf-126">-Id</span></span>
<span data-ttu-id="ac8bf-127">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-127">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="ac8bf-128">exemplo:/providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="ac8bf-128">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8bf-129">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ac8bf-129">-ManagementGroupId</span></span>
<span data-ttu-id="ac8bf-130">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-130">The management group id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8bf-131">-Nome</span><span class="sxs-lookup"><span data-stu-id="ac8bf-131">-Name</span></span>
<span data-ttu-id="ac8bf-132">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-132">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ac8bf-133">-Pre</span><span class="sxs-lookup"><span data-stu-id="ac8bf-133">-Pre</span></span>
<span data-ttu-id="ac8bf-134">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-134">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ac8bf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac8bf-135">CommonParameters</span></span>
<span data-ttu-id="ac8bf-136">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac8bf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac8bf-137">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ac8bf-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac8bf-138">SENSORES</span><span class="sxs-lookup"><span data-stu-id="ac8bf-138">INPUTS</span></span>

### <span data-ttu-id="ac8bf-139">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="ac8bf-139">None</span></span>

## <span data-ttu-id="ac8bf-140">EXIBE</span><span class="sxs-lookup"><span data-stu-id="ac8bf-140">OUTPUTS</span></span>

### <span data-ttu-id="ac8bf-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="ac8bf-141">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ac8bf-142">INFORMA</span><span class="sxs-lookup"><span data-stu-id="ac8bf-142">NOTES</span></span>

## <span data-ttu-id="ac8bf-143">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ac8bf-143">RELATED LINKS</span></span>
