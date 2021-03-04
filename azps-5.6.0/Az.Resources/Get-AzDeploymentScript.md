---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 7b61444bb4f3a23e1611e90b79545e1c174b0437
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101885966"
---
# <span data-ttu-id="ae5cf-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ae5cf-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="ae5cf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae5cf-102">SYNOPSIS</span></span>
<span data-ttu-id="ae5cf-103">Obtém ou lista scripts de implantação.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="ae5cf-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ae5cf-104">SYNTAX</span></span>

### <span data-ttu-id="ae5cf-105">ListDeploymentScript (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ae5cf-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ae5cf-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="ae5cf-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ae5cf-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="ae5cf-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae5cf-108">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ae5cf-108">DESCRIPTION</span></span>
<span data-ttu-id="ae5cf-109">O cmdlet **Get-AzDeploymentScript** obtém um único script de implantação ou uma lista de scripts de implantação.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="ae5cf-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ae5cf-110">EXAMPLES</span></span>

### <span data-ttu-id="ae5cf-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ae5cf-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="ae5cf-112">Lista scripts de implantação na assinatura no contexto do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="ae5cf-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="ae5cf-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ae5cf-114">Lista scripts de implantação no grupo de recursos DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="ae5cf-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="ae5cf-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="ae5cf-116">Obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="ae5cf-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="ae5cf-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="ae5cf-118">Obtém um script de implantação com a ID de recurso determinada.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="ae5cf-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ae5cf-119">PARAMETERS</span></span>

### <span data-ttu-id="ae5cf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae5cf-120">-DefaultProfile</span></span>
<span data-ttu-id="ae5cf-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae5cf-122">-Id</span><span class="sxs-lookup"><span data-stu-id="ae5cf-122">-Id</span></span>
<span data-ttu-id="ae5cf-123">A ID de recurso totalmente qualificada do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="ae5cf-124">Exemplo: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="ae5cf-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByResourceId
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-125">-Name</span><span class="sxs-lookup"><span data-stu-id="ae5cf-125">-Name</span></span>
<span data-ttu-id="ae5cf-126">O nome do script de implantação</span><span class="sxs-lookup"><span data-stu-id="ae5cf-126">The name of the deployment script</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae5cf-127">-ResourceGroupName</span></span>
<span data-ttu-id="ae5cf-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-128">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: ListDeploymentScript
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetDeploymentScriptByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae5cf-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae5cf-129">CommonParameters</span></span>
<span data-ttu-id="ae5cf-130">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae5cf-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ae5cf-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae5cf-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae5cf-132">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ae5cf-132">INPUTS</span></span>

### <span data-ttu-id="ae5cf-133">System.String</span><span class="sxs-lookup"><span data-stu-id="ae5cf-133">System.String</span></span>

## <span data-ttu-id="ae5cf-134">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ae5cf-134">OUTPUTS</span></span>

### <span data-ttu-id="ae5cf-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="ae5cf-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="ae5cf-136">NOTES</span><span class="sxs-lookup"><span data-stu-id="ae5cf-136">NOTES</span></span>

## <span data-ttu-id="ae5cf-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ae5cf-137">RELATED LINKS</span></span>