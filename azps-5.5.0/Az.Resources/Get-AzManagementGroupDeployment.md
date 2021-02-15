---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeployment.md
ms.openlocfilehash: 6c873dfda563c24104abc5e89b00569358084d96
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100118139"
---
# <span data-ttu-id="d637a-101">Get-AzManagementGroupDeployment</span><span class="sxs-lookup"><span data-stu-id="d637a-101">Get-AzManagementGroupDeployment</span></span>

## <span data-ttu-id="d637a-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d637a-102">SYNOPSIS</span></span>
<span data-ttu-id="d637a-103">Obter implantação em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d637a-103">Get deployment at a management group</span></span>

## <span data-ttu-id="d637a-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d637a-104">SYNTAX</span></span>

### <span data-ttu-id="d637a-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="d637a-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeployment [-ManagementGroupId] <String> [[-Name] <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d637a-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d637a-106">GetByDeploymentId</span></span>
```
Get-AzManagementGroupDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d637a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="d637a-107">DESCRIPTION</span></span>
<span data-ttu-id="d637a-108">O cmdlet **Get-AzManagementGroupDeployment** obtém as implantações em um grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d637a-108">The **Get-AzManagementGroupDeployment** cmdlet gets the deployments at the a management group.</span></span>
<span data-ttu-id="d637a-109">*Especifique o* parâmetro Nome ou *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="d637a-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d637a-110">Por padrão, **Get-AzManagementGroupDeployment** obtém todas as implantações no grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d637a-110">By default, **Get-AzManagementGroupDeployment** gets all deployments at the management group.</span></span>

## <span data-ttu-id="d637a-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="d637a-111">EXAMPLES</span></span>

### <span data-ttu-id="d637a-112">Exemplo 1: Obter todas as implantações em um grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="d637a-112">Example 1: Get all deployments at a management group</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId "myMG"
```

<span data-ttu-id="d637a-113">Esse comando obtém todas as implantações no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="d637a-113">This command gets all deployments at the management group "myMG".</span></span>

### <span data-ttu-id="d637a-114">Exemplo 2: Obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="d637a-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -ManagementGroupId "myMG" -Name "Deploy01"
```

<span data-ttu-id="d637a-115">Esse comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="d637a-115">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>
<span data-ttu-id="d637a-116">Você pode atribuir um nome a uma implantação quando a criar usando os cmdlets **New-AzManagementGroupDeployment.**</span><span class="sxs-lookup"><span data-stu-id="d637a-116">You can assign a name to a deployment when you create it by using the **New-AzManagementGroupDeployment** cmdlets.</span></span>
<span data-ttu-id="d637a-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="d637a-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="d637a-118">Exemplo 3: Obter uma implantação por ID</span><span class="sxs-lookup"><span data-stu-id="d637a-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Management/managementGroups/myMG/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="d637a-119">Esse comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="d637a-119">This command gets the "Deploy01" deployment at the management group "myMG".</span></span>

## <span data-ttu-id="d637a-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d637a-120">PARAMETERS</span></span>

### <span data-ttu-id="d637a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d637a-121">-DefaultProfile</span></span>
<span data-ttu-id="d637a-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d637a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d637a-123">-ID</span><span class="sxs-lookup"><span data-stu-id="d637a-123">-Id</span></span>
<span data-ttu-id="d637a-124">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="d637a-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d637a-125">exemplo: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d637a-125">example: /providers/Microsoft.Management/managementGroups/{managementGroupId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d637a-126">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="d637a-126">-ManagementGroupId</span></span>
<span data-ttu-id="d637a-127">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="d637a-127">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d637a-128">-Nome</span><span class="sxs-lookup"><span data-stu-id="d637a-128">-Name</span></span>
<span data-ttu-id="d637a-129">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="d637a-129">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d637a-130">-Pré-</span><span class="sxs-lookup"><span data-stu-id="d637a-130">-Pre</span></span>
<span data-ttu-id="d637a-131">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d637a-131">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d637a-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d637a-132">CommonParameters</span></span>
<span data-ttu-id="d637a-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d637a-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d637a-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d637a-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d637a-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="d637a-135">INPUTS</span></span>

### <span data-ttu-id="d637a-136">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d637a-136">None</span></span>

## <span data-ttu-id="d637a-137">Saídas</span><span class="sxs-lookup"><span data-stu-id="d637a-137">OUTPUTS</span></span>

### <span data-ttu-id="d637a-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="d637a-138">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d637a-139">Notas</span><span class="sxs-lookup"><span data-stu-id="d637a-139">NOTES</span></span>

## <span data-ttu-id="d637a-140">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d637a-140">RELATED LINKS</span></span>
