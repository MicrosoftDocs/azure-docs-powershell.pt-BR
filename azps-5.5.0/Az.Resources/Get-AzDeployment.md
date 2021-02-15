---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: 75ebbe0eedd9aad396500701d5e94efff76069f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111428"
---
# <span data-ttu-id="9a0f4-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="9a0f4-101">Get-AzDeployment</span></span>

## <span data-ttu-id="9a0f4-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="9a0f4-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0f4-103">Obter implantação</span><span class="sxs-lookup"><span data-stu-id="9a0f4-103">Get deployment</span></span>

## <span data-ttu-id="9a0f4-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a0f4-104">SYNTAX</span></span>

### <span data-ttu-id="9a0f4-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="9a0f4-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0f4-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="9a0f4-106">GetByDeploymentId</span></span>
```
Get-AzDeployment -Id <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0f4-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="9a0f4-107">DESCRIPTION</span></span>
<span data-ttu-id="9a0f4-108">O cmdlet **Get-AzDeployment** obtém as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="9a0f4-109">*Especifique o* parâmetro Nome ou *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="9a0f4-110">Por padrão, **o Get-AzDeployment** obtém todas as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="9a0f4-111">Exemplos</span><span class="sxs-lookup"><span data-stu-id="9a0f4-111">EXAMPLES</span></span>

### <span data-ttu-id="9a0f4-112">Exemplo 1: Obter todas as implantações no escopo da assinatura</span><span class="sxs-lookup"><span data-stu-id="9a0f4-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="9a0f4-113">Esse comando obtém todas as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="9a0f4-114">Exemplo 2: Obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="9a0f4-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="9a0f4-115">Esse comando obtém a implantação DeployRoles01 no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="9a0f4-116">Você pode atribuir um nome a uma implantação ao criar essa implantação usando os cmdlets **New-AzDeployment.**</span><span class="sxs-lookup"><span data-stu-id="9a0f4-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="9a0f4-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="9a0f4-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a0f4-118">PARAMETERS</span></span>

### <span data-ttu-id="9a0f4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0f4-119">-DefaultProfile</span></span>
<span data-ttu-id="9a0f4-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a0f4-121">-ID</span><span class="sxs-lookup"><span data-stu-id="9a0f4-121">-Id</span></span>
<span data-ttu-id="9a0f4-122">A ID de recurso totalmente qualificada da implantação.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-122">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="9a0f4-123">exemplo: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="9a0f4-123">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="9a0f4-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="9a0f4-124">-Name</span></span>
<span data-ttu-id="9a0f4-125">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-125">The name of deployment.</span></span>

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

### <span data-ttu-id="9a0f4-126">-Pré-</span><span class="sxs-lookup"><span data-stu-id="9a0f4-126">-Pre</span></span>
<span data-ttu-id="9a0f4-127">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="9a0f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0f4-128">CommonParameters</span></span>
<span data-ttu-id="9a0f4-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a0f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0f4-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a0f4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0f4-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="9a0f4-131">INPUTS</span></span>

### <span data-ttu-id="9a0f4-132">Nenhum</span><span class="sxs-lookup"><span data-stu-id="9a0f4-132">None</span></span>

## <span data-ttu-id="9a0f4-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="9a0f4-133">OUTPUTS</span></span>

### <span data-ttu-id="9a0f4-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="9a0f4-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="9a0f4-135">Notas</span><span class="sxs-lookup"><span data-stu-id="9a0f4-135">NOTES</span></span>

## <span data-ttu-id="9a0f4-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="9a0f4-136">RELATED LINKS</span></span>
