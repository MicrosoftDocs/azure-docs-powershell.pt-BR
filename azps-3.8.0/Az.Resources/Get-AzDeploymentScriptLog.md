---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscriptlog
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScriptLog.md
ms.openlocfilehash: 855127362fbcbf906755affde0bec6de5e7f2698
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93944319"
---
# <span data-ttu-id="eb28d-101">Get-AzDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="eb28d-101">Get-AzDeploymentScriptLog</span></span>

## <span data-ttu-id="eb28d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="eb28d-102">SYNOPSIS</span></span>
<span data-ttu-id="eb28d-103">Obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="eb28d-103">Gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="eb28d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="eb28d-104">SYNTAX</span></span>

### <span data-ttu-id="eb28d-105">GetDeploymentScriptLogByName (padrão)</span><span class="sxs-lookup"><span data-stu-id="eb28d-105">GetDeploymentScriptLogByName (Default)</span></span>
```
Get-AzDeploymentScriptLog [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="eb28d-106">GetDeploymentScriptLogByResourceId</span><span class="sxs-lookup"><span data-stu-id="eb28d-106">GetDeploymentScriptLogByResourceId</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="eb28d-107">GetDeploymentScriptLogByInputObject</span><span class="sxs-lookup"><span data-stu-id="eb28d-107">GetDeploymentScriptLogByInputObject</span></span>
```
Get-AzDeploymentScriptLog [-DeploymentScriptInputObject] <PsDeploymentScript>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="eb28d-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="eb28d-108">DESCRIPTION</span></span>
<span data-ttu-id="eb28d-109">O cmdlet **Get-AzDeploymentScriptLog** Obtém o log de uma execução de script de implantação.</span><span class="sxs-lookup"><span data-stu-id="eb28d-109">The **Get-AzDeploymentScriptLog** cmdlet gets the log of a deployment script execution.</span></span>

## <span data-ttu-id="eb28d-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="eb28d-110">EXAMPLES</span></span>

### <span data-ttu-id="eb28d-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="eb28d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScriptLog -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="eb28d-112">Obtém o log de um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="eb28d-112">Gets log of a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="eb28d-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="eb28d-113">Example 2</span></span>
```powershell
PS C:\> $ds = Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
PS C:\> Get-AzDeploymentScriptLog -DeploymentScriptInputObject $ds
```

<span data-ttu-id="eb28d-114">O primeiro comando obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="eb28d-114">The first command gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>
<span data-ttu-id="eb28d-115">O segundo comando obtém o log do script de implantação fornecido.</span><span class="sxs-lookup"><span data-stu-id="eb28d-115">The second command gets the log of given deployment script.</span></span>

## <span data-ttu-id="eb28d-116">OS</span><span class="sxs-lookup"><span data-stu-id="eb28d-116">PARAMETERS</span></span>

### <span data-ttu-id="eb28d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb28d-117">-DefaultProfile</span></span>
<span data-ttu-id="eb28d-118">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="eb28d-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="eb28d-119">-DeploymentScriptInputObject</span><span class="sxs-lookup"><span data-stu-id="eb28d-119">-DeploymentScriptInputObject</span></span>
<span data-ttu-id="eb28d-120">O objeto do PowerShell do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="eb28d-120">The deployment script PowerShell object.</span></span>

```yaml
Type: PsDeploymentScript
Parameter Sets: GetDeploymentScriptLogByInputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="eb28d-121">-DeploymentScriptResourceId</span><span class="sxs-lookup"><span data-stu-id="eb28d-121">-DeploymentScriptResourceId</span></span>
<span data-ttu-id="eb28d-122">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="eb28d-122">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="eb28d-123">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="eb28d-123">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb28d-124">-Nome</span><span class="sxs-lookup"><span data-stu-id="eb28d-124">-Name</span></span>
<span data-ttu-id="eb28d-125">O nome do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="eb28d-125">The name of the deployment script.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb28d-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb28d-126">-ResourceGroupName</span></span>
<span data-ttu-id="eb28d-127">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="eb28d-127">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: GetDeploymentScriptLogByName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="eb28d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb28d-128">CommonParameters</span></span>
<span data-ttu-id="eb28d-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb28d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="eb28d-130">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb28d-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb28d-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="eb28d-131">INPUTS</span></span>

### <span data-ttu-id="eb28d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="eb28d-132">System.String</span></span>

### <span data-ttu-id="eb28d-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="eb28d-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="eb28d-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="eb28d-134">OUTPUTS</span></span>

### <span data-ttu-id="eb28d-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span><span class="sxs-lookup"><span data-stu-id="eb28d-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScriptLog</span></span>

## <span data-ttu-id="eb28d-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="eb28d-136">NOTES</span></span>

## <span data-ttu-id="eb28d-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="eb28d-137">RELATED LINKS</span></span>
