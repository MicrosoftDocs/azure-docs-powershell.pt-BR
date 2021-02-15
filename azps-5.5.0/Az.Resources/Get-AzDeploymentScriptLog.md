---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100111425"
---
# <span data-ttu-id="c36b3-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c36b3-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="c36b3-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="c36b3-102">SYNOPSIS</span></span>
<span data-ttu-id="c36b3-103">Obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="c36b3-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c36b3-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c36b3-104">SYNTAX</span></span>

### <span data-ttu-id="c36b3-105">GetDeploymentScriptLogByName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="c36b3-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36b3-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="c36b3-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c36b3-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="c36b3-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c36b3-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="c36b3-108">DESCRIPTION</span></span>
<span data-ttu-id="c36b3-109">O **cmdlet Get-AzDeploymentScriptLog** obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="c36b3-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="c36b3-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="c36b3-110">EXAMPLES</span></span>

### <span data-ttu-id="c36b3-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c36b3-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="c36b3-112">Obtém o log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c36b3-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c36b3-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c36b3-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="c36b3-114">Obtém as últimas 3 linhas do log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c36b3-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="c36b3-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c36b3-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="c36b3-116">O primeiro comando obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="c36b3-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="c36b3-117">O segundo comando obtém o log de determinado script de implantação.</span><span class="sxs-lookup"><span data-stu-id="c36b3-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="c36b3-118">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c36b3-118">PARAMETERS</span></span>

### <span data-ttu-id="c36b3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c36b3-119">-DefaultProfile</span></span>
<span data-ttu-id="c36b3-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="c36b3-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c36b3-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="c36b3-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="c36b3-122">O objeto do PowerShell de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="c36b3-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="c36b3-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="c36b3-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="c36b3-124">A ID de recurso totalmente qualificada do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="c36b3-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="c36b3-125">Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="c36b3-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="c36b3-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="c36b3-126">-Name</span></span>
<span data-ttu-id="c36b3-127">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="c36b3-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="c36b3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c36b3-128">-ResourceGroupName</span></span>
<span data-ttu-id="c36b3-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="c36b3-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="c36b3-130">-Tail</span><span class="sxs-lookup"><span data-stu-id="c36b3-130">-Tail</span></span>
<span data-ttu-id="c36b3-131">Limitar a saída para as últimas n linhas</span><span class="sxs-lookup"><span data-stu-id="c36b3-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="c36b3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c36b3-132">CommonParameters</span></span>
<span data-ttu-id="c36b3-133">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c36b3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c36b3-134">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c36b3-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c36b3-135">Entradas</span><span class="sxs-lookup"><span data-stu-id="c36b3-135">INPUTS</span></span>

### <span data-ttu-id="c36b3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="c36b3-136">System.String</span></span>

### <span data-ttu-id="c36b3-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="c36b3-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="c36b3-138">Saídas</span><span class="sxs-lookup"><span data-stu-id="c36b3-138">OUTPUTS</span></span>

### <span data-ttu-id="c36b3-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="c36b3-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="c36b3-140">Notas</span><span class="sxs-lookup"><span data-stu-id="c36b3-140">NOTES</span></span>

## <span data-ttu-id="c36b3-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="c36b3-141">RELATED LINKS</span></span>
