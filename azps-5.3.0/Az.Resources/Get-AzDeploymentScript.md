---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: b5c3ca86129e622a90a84d099961a8f8dd433eef
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427349"
---
# <span data-ttu-id="bcf1c-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="bcf1c-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="bcf1c-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="bcf1c-102">SYNOPSIS</span></span>
<span data-ttu-id="bcf1c-103">Obtém ou lista os scripts de implantação.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="bcf1c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bcf1c-104">SYNTAX</span></span>

### <span data-ttu-id="bcf1c-105">ListDeploymentScript (padrão)</span><span class="sxs-lookup"><span data-stu-id="bcf1c-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bcf1c-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="bcf1c-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bcf1c-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="bcf1c-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bcf1c-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="bcf1c-108">DESCRIPTION</span></span>
<span data-ttu-id="bcf1c-109">O cmdlet **Get-AzDeploymentScript** Obtém um único script de implantação ou uma lista de scripts de implantação.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="bcf1c-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="bcf1c-110">EXAMPLES</span></span>

### <span data-ttu-id="bcf1c-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bcf1c-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="bcf1c-112">Lista os scripts de implantação na assinatura do contexto do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="bcf1c-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bcf1c-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="bcf1c-114">Lista scripts de implantação no grupo de recursos DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="bcf1c-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bcf1c-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="bcf1c-116">Obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="bcf1c-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bcf1c-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="bcf1c-118">Obtém um script de implantação com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="bcf1c-119">OS</span><span class="sxs-lookup"><span data-stu-id="bcf1c-119">PARAMETERS</span></span>

### <span data-ttu-id="bcf1c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bcf1c-120">-DefaultProfile</span></span>
<span data-ttu-id="bcf1c-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bcf1c-122">-ID</span><span class="sxs-lookup"><span data-stu-id="bcf1c-122">-Id</span></span>
<span data-ttu-id="bcf1c-123">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="bcf1c-124">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="bcf1c-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="bcf1c-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="bcf1c-125">-Name</span></span>
<span data-ttu-id="bcf1c-126">O nome do script de implantação</span><span class="sxs-lookup"><span data-stu-id="bcf1c-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="bcf1c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bcf1c-127">-ResourceGroupName</span></span>
<span data-ttu-id="bcf1c-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="bcf1c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bcf1c-129">CommonParameters</span></span>
<span data-ttu-id="bcf1c-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bcf1c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bcf1c-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bcf1c-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bcf1c-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="bcf1c-132">INPUTS</span></span>

### <span data-ttu-id="bcf1c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="bcf1c-133">System.String</span></span>

## <span data-ttu-id="bcf1c-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="bcf1c-134">OUTPUTS</span></span>

### <span data-ttu-id="bcf1c-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="bcf1c-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="bcf1c-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="bcf1c-136">NOTES</span></span>

## <span data-ttu-id="bcf1c-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="bcf1c-137">RELATED LINKS</span></span>