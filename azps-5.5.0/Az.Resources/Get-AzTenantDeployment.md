---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeployment.md
ms.openlocfilehash: a1cfbf131286a8bae7b8837f798c32b83d566b2d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114908"
---
# <span data-ttu-id="36e1b-101">Get-AzTenantDeployment</span><span class="sxs-lookup"><span data-stu-id="36e1b-101">Get-AzTenantDeployment</span></span>

## <span data-ttu-id="36e1b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="36e1b-102">SYNOPSIS</span></span>
<span data-ttu-id="36e1b-103">Obter implantação no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="36e1b-103">Get deployment at tenant scope</span></span>

## <span data-ttu-id="36e1b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36e1b-104">SYNTAX</span></span>

### <span data-ttu-id="36e1b-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="36e1b-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36e1b-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="36e1b-106">GetByDeploymentId</span></span>
```
Get-AzTenantDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36e1b-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="36e1b-107">DESCRIPTION</span></span>
<span data-ttu-id="36e1b-108">O cmdlet **Get-AzTenantDeployment** obtém as implantações no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="36e1b-108">The **Get-AzTenantDeployment** cmdlet gets the deployments at the tenant scope.</span></span>
<span data-ttu-id="36e1b-109">*Especifique o* parâmetro Nome ou *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="36e1b-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="36e1b-110">Por padrão, **Get-AzTenantDeployment** obtém todas as implantações no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="36e1b-110">By default, **Get-AzTenantDeployment** gets all deployments at the tenant scope.</span></span>

## <span data-ttu-id="36e1b-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="36e1b-111">EXAMPLES</span></span>

### <span data-ttu-id="36e1b-112">Exemplo 1: Obter todas as implantações no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="36e1b-112">Example 1: Get all deployments at the tenant scope</span></span>
```
PS C:\>Get-AzTenantDeployment
```

<span data-ttu-id="36e1b-113">Esse comando obtém todas as implantações no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="36e1b-113">This command gets all deployments at the current tenant scope.</span></span>

### <span data-ttu-id="36e1b-114">Exemplo 2: Obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="36e1b-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "Deploy01"
```

<span data-ttu-id="36e1b-115">Esse comando obtém a implantação "Implantar01" no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="36e1b-115">This command gets the "Deploy01" deployment at the current tenant scope.</span></span>
<span data-ttu-id="36e1b-116">Você pode atribuir um nome a uma implantação ao criar essa implantação usando os cmdlets **New-AzTenantDeployment.**</span><span class="sxs-lookup"><span data-stu-id="36e1b-116">You can assign a name to a deployment when you create it by using the **New-AzTenantDeployment** cmdlets.</span></span>
<span data-ttu-id="36e1b-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="36e1b-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

### <span data-ttu-id="36e1b-118">Exemplo 3: Obter uma implantação por ID</span><span class="sxs-lookup"><span data-stu-id="36e1b-118">Example 3: Get a deployment by ID</span></span>
```
PS C:\>Get-AzDeployment -Id "/providers/Microsoft.Resources/deployments/Deploy01"
```

<span data-ttu-id="36e1b-119">Esse comando obtém a implantação "Implantar01" no escopo do locatário.</span><span class="sxs-lookup"><span data-stu-id="36e1b-119">This command gets the "Deploy01" deployment at the tenant scope.</span></span>

## <span data-ttu-id="36e1b-120">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36e1b-120">PARAMETERS</span></span>

### <span data-ttu-id="36e1b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36e1b-121">-DefaultProfile</span></span>
<span data-ttu-id="36e1b-122">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="36e1b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36e1b-123">-ID</span><span class="sxs-lookup"><span data-stu-id="36e1b-123">-Id</span></span>
<span data-ttu-id="36e1b-124">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="36e1b-124">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="36e1b-125">exemplo: /providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="36e1b-125">example: /providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="36e1b-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="36e1b-126">-Name</span></span>
<span data-ttu-id="36e1b-127">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="36e1b-127">The name of deployment.</span></span>

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

### <span data-ttu-id="36e1b-128">-Pré-</span><span class="sxs-lookup"><span data-stu-id="36e1b-128">-Pre</span></span>
<span data-ttu-id="36e1b-129">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="36e1b-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="36e1b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36e1b-130">CommonParameters</span></span>
<span data-ttu-id="36e1b-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36e1b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36e1b-132">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="36e1b-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36e1b-133">Entradas</span><span class="sxs-lookup"><span data-stu-id="36e1b-133">INPUTS</span></span>

### <span data-ttu-id="36e1b-134">Nenhum</span><span class="sxs-lookup"><span data-stu-id="36e1b-134">None</span></span>

## <span data-ttu-id="36e1b-135">Saídas</span><span class="sxs-lookup"><span data-stu-id="36e1b-135">OUTPUTS</span></span>

### <span data-ttu-id="36e1b-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="36e1b-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="36e1b-137">Notas</span><span class="sxs-lookup"><span data-stu-id="36e1b-137">NOTES</span></span>

## <span data-ttu-id="36e1b-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="36e1b-138">RELATED LINKS</span></span>
