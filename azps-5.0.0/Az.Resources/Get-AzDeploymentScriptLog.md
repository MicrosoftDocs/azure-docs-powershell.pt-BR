---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 608450112b7cd4f54ee0f08f0f29c3aa707fff9e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94115902"
---
# <span data-ttu-id="b1b40-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b1b40-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="b1b40-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="b1b40-102">SYNOPSIS</span></span>
<span data-ttu-id="b1b40-103">Obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1b40-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="b1b40-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b1b40-104">SYNTAX</span></span>

### <span data-ttu-id="b1b40-105">GetDeploymentScriptLogByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="b1b40-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1b40-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="b1b40-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b1b40-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="b1b40-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptObject] <PsDeploymentScript> [[-Tail] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b1b40-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="b1b40-108">DESCRIPTION</span></span>
<span data-ttu-id="b1b40-109">O cmdlet **Get-AzDeploymentScriptLog** Obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1b40-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="b1b40-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="b1b40-110">EXAMPLES</span></span>

### <span data-ttu-id="b1b40-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="b1b40-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="b1b40-112">Obtém o log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="b1b40-112">Gets the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="b1b40-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="b1b40-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg -Tail 3
```

<span data-ttu-id="b1b40-114">Obtém as três últimas linhas do log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="b1b40-114">Gets the last 3 lines of the log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="b1b40-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="b1b40-115">Example 3</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="b1b40-116">O primeiro comando obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="b1b40-116">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="b1b40-117">O segundo comando obtém o log do script de implantação fornecido.</span><span class="sxs-lookup"><span data-stu-id="b1b40-117">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="b1b40-118">OS</span><span class="sxs-lookup"><span data-stu-id="b1b40-118">PARAMETERS</span></span>

### <span data-ttu-id="b1b40-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1b40-119">-DefaultProfile</span></span>
<span data-ttu-id="b1b40-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="b1b40-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b1b40-121">-DeploymentScriptObject</span><span class="sxs-lookup"><span data-stu-id="b1b40-121">-DeploymentScriptObject</span></span>
<span data-ttu-id="b1b40-122">O objeto do PowerShell do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1b40-122">The deployment script PowerShell object.</span></span>

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

### <span data-ttu-id="b1b40-123">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="b1b40-123">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="b1b40-124">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1b40-124">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="b1b40-125">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="b1b40-125">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="b1b40-126">-Nome</span><span class="sxs-lookup"><span data-stu-id="b1b40-126">-Name</span></span>
<span data-ttu-id="b1b40-127">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="b1b40-127">The name of the deployment script.</span></span>

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

### <span data-ttu-id="b1b40-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b1b40-128">-ResourceGroupName</span></span>
<span data-ttu-id="b1b40-129">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="b1b40-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="b1b40-130">-Caudal</span><span class="sxs-lookup"><span data-stu-id="b1b40-130">-Tail</span></span>
<span data-ttu-id="b1b40-131">Limitar a saída às últimas n linhas</span><span class="sxs-lookup"><span data-stu-id="b1b40-131">Limit output to last n lines</span></span>

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

### <span data-ttu-id="b1b40-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1b40-132">CommonParameters</span></span>
<span data-ttu-id="b1b40-133">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1b40-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1b40-134">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b1b40-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1b40-135">SENSORES</span><span class="sxs-lookup"><span data-stu-id="b1b40-135">INPUTS</span></span>

### <span data-ttu-id="b1b40-136">System. String</span><span class="sxs-lookup"><span data-stu-id="b1b40-136">System.String</span></span>

### <span data-ttu-id="b1b40-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="b1b40-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="b1b40-138">EXIBE</span><span class="sxs-lookup"><span data-stu-id="b1b40-138">OUTPUTS</span></span>

### <span data-ttu-id="b1b40-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="b1b40-139">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="b1b40-140">INFORMA</span><span class="sxs-lookup"><span data-stu-id="b1b40-140">NOTES</span></span>

## <span data-ttu-id="b1b40-141">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="b1b40-141">RELATED LINKS</span></span>
