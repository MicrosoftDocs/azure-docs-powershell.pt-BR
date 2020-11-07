---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: 4505a64b25f0022763541e6cd5d700e7c6c05988
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93943777"
---
# <span data-ttu-id="e1baf-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e1baf-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="e1baf-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e1baf-102">SYNOPSIS</span></span>
<span data-ttu-id="e1baf-103">Obter a operação de implantação para implantação no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="e1baf-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="e1baf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e1baf-104">SYNTAX</span></span>

### <span data-ttu-id="e1baf-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="e1baf-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e1baf-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e1baf-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1baf-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e1baf-107">DESCRIPTION</span></span>
<span data-ttu-id="e1baf-108">O cmdlet **Get-AzTenantDeploymentOperation** lista todas as operações que fazem parte da implantação no escopo do locatário atual para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="e1baf-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="e1baf-109">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e1baf-109">EXAMPLES</span></span>

### <span data-ttu-id="e1baf-110">Exemplo 1: obter operações de implantação de acordo com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="e1baf-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="e1baf-111">Obtém operações de implantação com o nome "Deploy01" no escopo do locatário atual.</span><span class="sxs-lookup"><span data-stu-id="e1baf-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="e1baf-112">Exemplo 2: obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="e1baf-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="e1baf-113">Esse comando obtém a implantação "Deploy01" no escopo do locatário atual e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="e1baf-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="e1baf-114">OS</span><span class="sxs-lookup"><span data-stu-id="e1baf-114">PARAMETERS</span></span>

### <span data-ttu-id="e1baf-115">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e1baf-115">-ApiVersion</span></span>
<span data-ttu-id="e1baf-116">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e1baf-116">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e1baf-117">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e1baf-117">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="e1baf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1baf-118">-DefaultProfile</span></span>
<span data-ttu-id="e1baf-119">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="e1baf-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1baf-120">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="e1baf-120">-DeploymentName</span></span>
<span data-ttu-id="e1baf-121">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="e1baf-121">The deployment name.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1baf-122">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="e1baf-122">-DeploymentObject</span></span>
<span data-ttu-id="e1baf-123">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="e1baf-123">The deployment object.</span></span>

```yaml
Type: PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e1baf-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="e1baf-124">-OperationId</span></span>
<span data-ttu-id="e1baf-125">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e1baf-125">The deployment operation Id.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e1baf-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="e1baf-126">-Pre</span></span>
<span data-ttu-id="e1baf-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e1baf-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e1baf-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1baf-128">CommonParameters</span></span>
<span data-ttu-id="e1baf-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1baf-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1baf-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e1baf-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1baf-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e1baf-131">INPUTS</span></span>

### <span data-ttu-id="e1baf-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="e1baf-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="e1baf-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e1baf-133">OUTPUTS</span></span>

### <span data-ttu-id="e1baf-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e1baf-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="e1baf-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e1baf-135">NOTES</span></span>

## <span data-ttu-id="e1baf-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e1baf-136">RELATED LINKS</span></span>
