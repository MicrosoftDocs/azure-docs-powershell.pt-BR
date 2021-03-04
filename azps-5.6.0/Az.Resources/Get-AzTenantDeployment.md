---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: 1755438dfc5bdb9b4eedf46ec364e851a2bca154
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101891268"
---
# <span data-ttu-id="77419-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="77419-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="77419-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77419-102">SYNOPSIS</span></span>
<span data-ttu-id="77419-103">Obter implantação no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="77419-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="77419-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="77419-104">SYNTAX</span></span>

### <span data-ttu-id="77419-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="77419-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="77419-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="77419-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77419-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="77419-107">DESCRIPTION</span></span>
<span data-ttu-id="77419-108">O cmdlet **Get-AzTenantDeployment** obtém as implantações no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="77419-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="77419-109">*Especifique o parâmetro Name* ou *Id* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="77419-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="77419-110">Por padrão, **Get-AzTenantDeployment** obtém todas as implantações no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="77419-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="77419-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="77419-111">EXAMPLES</span></span>

### <span data-ttu-id="77419-112">Exemplo 1: Obter todas as implantações no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="77419-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="77419-113">Esse comando obtém todas as implantações no escopo de locatário atual.</span><span class="sxs-lookup"><span data-stu-id="77419-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="77419-114">Exemplo 2: Obter uma implantação pelo nome</span><span class="sxs-lookup"><span data-stu-id="77419-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="77419-115">Este comando obtém a implantação "Deploy01" no escopo de locatário atual.</span><span class="sxs-lookup"><span data-stu-id="77419-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="77419-116">Você pode atribuir um nome a uma implantação ao criar usando os cmdlets **New-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="77419-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="77419-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="77419-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="77419-118">Exemplo 3: Obter uma implantação por ID</span><span class="sxs-lookup"><span data-stu-id="77419-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="77419-119">Este comando obtém a implantação "Deploy01" no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="77419-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="77419-120">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="77419-120">PARAMETERS</span></span>

### <span data-ttu-id="77419-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77419-121">-DefaultProfile</span></span>
<span data-ttu-id="77419-122">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="77419-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77419-123">-Id</span><span class="sxs-lookup"><span data-stu-id="77419-123">-Id</span></span>
<span data-ttu-id="77419-124">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="77419-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="77419-125">exemplo: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="77419-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="77419-126">-Name</span><span class="sxs-lookup"><span data-stu-id="77419-126">-Name</span></span>
<span data-ttu-id="77419-127">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="77419-127">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77419-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="77419-128">-Pre</span></span>
<span data-ttu-id="77419-129">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="77419-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="77419-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77419-130">CommonParameters</span></span>
<span data-ttu-id="77419-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77419-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77419-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77419-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77419-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="77419-133">INPUTS</span></span>

### <span data-ttu-id="77419-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="77419-134">None</span></span>

## <span data-ttu-id="77419-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="77419-135">OUTPUTS</span></span>

### <span data-ttu-id="77419-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="77419-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="77419-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="77419-137">NOTES</span></span>

## <span data-ttu-id="77419-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="77419-138">RELATED LINKS</span></span>
