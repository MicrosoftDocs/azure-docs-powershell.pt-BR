---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: dc62e4766a83e1a2046b15fbdf6619e08c4b8e28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885965"
---
# <span data-ttu-id="5b1bc-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="5b1bc-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="5b1bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1bc-103">Obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="5b1bc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="5b1bc-104">SYNTAX</span></span>

### <span data-ttu-id="5b1bc-105">GetDeploymentScriptLogByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="5b1bc-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b1bc-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1bc-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5b1bc-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="5b1bc-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b1bc-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="5b1bc-108">DESCRIPTION</span></span>
<span data-ttu-id="5b1bc-109">O cmdlet **Get-AzDeploymentScriptLog** obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="5b1bc-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-110">EXAMPLES</span></span>

### <span data-ttu-id="5b1bc-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="5b1bc-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="5b1bc-112">Obtém o log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="5b1bc-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="5b1bc-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="5b1bc-114">Obtém as últimas 3 linhas do log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="5b1bc-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="5b1bc-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="5b1bc-116">O primeiro comando obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="5b1bc-117">O segundo comando obtém o log de determinado script de implantação.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="5b1bc-118">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-118">PARAMETERS</span></span>

### <span data-ttu-id="5b1bc-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1bc-119">-DefaultProfile</span></span>
<span data-ttu-id="5b1bc-120">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1bc-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="5b1bc-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="5b1bc-122">O objeto do PowerShell de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-122">The deployment script PowerShell object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases: DeploymentScriptInputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="5b1bc-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="5b1bc-124">A ID de recurso totalmente qualificada do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="5b1bc-125">Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="5b1bc-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5b1bc-126">-Name</span></span>
<span data-ttu-id="5b1bc-127">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-127">The name of the deployment script.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5b1bc-128">-ResourceGroupName</span></span>
<span data-ttu-id="5b1bc-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="5b1bc-130">-Tail</span></span>
<span data-ttu-id="5b1bc-131">Limitar a saída para as últimas linhas n</span><span class="sxs-lookup"><span data-stu-id="5b1bc-131">Limit output to last n lines</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5b1bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1bc-132">CommonParameters</span></span>
<span data-ttu-id="5b1bc-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b1bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1bc-134">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b1bc-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1bc-135">INPUTS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-135">INPUTS</span></span>

### <span data-ttu-id="5b1bc-136">System.String</span><span class="sxs-lookup"><span data-stu-id="5b1bc-136">System.String</span></span>

### <span data-ttu-id="5b1bc-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="5b1bc-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="5b1bc-138">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-138">OUTPUTS</span></span>

### <span data-ttu-id="5b1bc-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="5b1bc-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="5b1bc-140">NOTES</span><span class="sxs-lookup"><span data-stu-id="5b1bc-140">NOTES</span></span>

## <span data-ttu-id="5b1bc-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="5b1bc-141">RELATED LINKS</span></span>
