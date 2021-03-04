---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 92a0aac5043be520f6a7ed7afc2066e0532b79ec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886401"
---
# <span data-ttu-id="38a0c-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="38a0c-101">Get-AzDeployment</span></span>

## <span data-ttu-id="38a0c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38a0c-102">SYNOPSIS</span></span>
<span data-ttu-id="38a0c-103">Obter implantação</span><span class="sxs-lookup"><span data-stu-id="38a0c-103">Get deployment</span></span>

## <span data-ttu-id="38a0c-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="38a0c-104">SYNTAX</span></span>

### <span data-ttu-id="38a0c-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="38a0c-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38a0c-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="38a0c-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38a0c-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="38a0c-107">DESCRIPTION</span></span>
<span data-ttu-id="38a0c-108">O cmdlet **Get-AzDeployment** obtém as implantações no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38a0c-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="38a0c-109">*Especifique o parâmetro Name* ou *Id* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="38a0c-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="38a0c-110">Por padrão, **Get-AzDeployment** obtém todas as implantações no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38a0c-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="38a0c-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="38a0c-111">EXAMPLES</span></span>

### <span data-ttu-id="38a0c-112">Exemplo 1: Obter todas as implantações no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="38a0c-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="38a0c-113">Esse comando obtém todas as implantações no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38a0c-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="38a0c-114">Exemplo 2: Obter uma implantação pelo nome</span><span class="sxs-lookup"><span data-stu-id="38a0c-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="38a0c-115">Este comando obtém a implantação DeployRoles01 no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="38a0c-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="38a0c-116">Você pode atribuir um nome a uma implantação ao criar usando os cmdlets **New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="38a0c-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="38a0c-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="38a0c-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="38a0c-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="38a0c-118">PARAMETERS</span></span>

### <span data-ttu-id="38a0c-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38a0c-119">-DefaultProfile</span></span>
<span data-ttu-id="38a0c-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="38a0c-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38a0c-121">-Id</span><span class="sxs-lookup"><span data-stu-id="38a0c-121">-Id</span></span>
<span data-ttu-id="38a0c-122">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="38a0c-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="38a0c-123">exemplo: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="38a0c-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="38a0c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="38a0c-124">-Name</span></span>
<span data-ttu-id="38a0c-125">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="38a0c-125">The name of deployment.</span></span>

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

### <span data-ttu-id="38a0c-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="38a0c-126">-Pre</span></span>
<span data-ttu-id="38a0c-127">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="38a0c-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="38a0c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38a0c-128">CommonParameters</span></span>
<span data-ttu-id="38a0c-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38a0c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38a0c-130">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="38a0c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38a0c-131">INPUTS</span><span class="sxs-lookup"><span data-stu-id="38a0c-131">INPUTS</span></span>

### <span data-ttu-id="38a0c-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="38a0c-132">None</span></span>

## <span data-ttu-id="38a0c-133">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="38a0c-133">OUTPUTS</span></span>

### <span data-ttu-id="38a0c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="38a0c-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="38a0c-135">NOTES</span><span class="sxs-lookup"><span data-stu-id="38a0c-135">NOTES</span></span>

## <span data-ttu-id="38a0c-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="38a0c-136">RELATED LINKS</span></span>
