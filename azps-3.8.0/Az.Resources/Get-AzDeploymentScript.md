---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentScript.md
ms.openlocfilehash: 761969eea685c21bc513efdfde9ea79a9e1e4a70
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93942324"
---
# <span data-ttu-id="4ca59-101">Get-AzDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="4ca59-101">Get-AzDeploymentScript</span></span>

## <span data-ttu-id="4ca59-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4ca59-102">SYNOPSIS</span></span>
<span data-ttu-id="4ca59-103">Obtém ou lista os scripts de implantação.</span><span class="sxs-lookup"><span data-stu-id="4ca59-103">Gets or lists deployment scripts.</span></span>

## <span data-ttu-id="4ca59-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4ca59-104">SYNTAX</span></span>

### <span data-ttu-id="4ca59-105">ListDeploymentScript (padrão)</span><span class="sxs-lookup"><span data-stu-id="4ca59-105">ListDeploymentScript (Default)</span></span>
```
Get-AzDeploymentScript [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4ca59-106">GetDeploymentScriptByName</span><span class="sxs-lookup"><span data-stu-id="4ca59-106">GetDeploymentScriptByName</span></span>
```
Get-AzDeploymentScript [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4ca59-107">GetDeploymentScriptByResourceId</span><span class="sxs-lookup"><span data-stu-id="4ca59-107">GetDeploymentScriptByResourceId</span></span>
```
Get-AzDeploymentScript [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4ca59-108">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4ca59-108">DESCRIPTION</span></span>
<span data-ttu-id="4ca59-109">O cmdlet **Get-AzDeploymentScript** Obtém um único script de implantação ou uma lista de scripts de implantação.</span><span class="sxs-lookup"><span data-stu-id="4ca59-109">The **Get-AzDeploymentScript** cmdlet gets a single deployment script or a list of deployment scripts.</span></span>

## <span data-ttu-id="4ca59-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4ca59-110">EXAMPLES</span></span>

### <span data-ttu-id="4ca59-111">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="4ca59-111">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentScript
```

<span data-ttu-id="4ca59-112">Lista os scripts de implantação na assinatura do contexto do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="4ca59-112">Lists deployment scripts in the subscription in current user's context.</span></span>

### <span data-ttu-id="4ca59-113">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="4ca59-113">Example 2</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="4ca59-114">Lista scripts de implantação no grupo de recursos DS-TestRg.</span><span class="sxs-lookup"><span data-stu-id="4ca59-114">Lists deployment scripts in resource group DS-TestRg.</span></span>

### <span data-ttu-id="4ca59-115">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="4ca59-115">Example 3</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Name MyDeploymentScript -ResourceGroupName DS-TestRg
```

<span data-ttu-id="4ca59-116">Obtém um script de implantação com o nome MyDeploymentScript no grupo de recursos DS-TestRG.</span><span class="sxs-lookup"><span data-stu-id="4ca59-116">Gets a deployment script with the name MyDeploymentScript in resource group DS-TestRG.</span></span>

### <span data-ttu-id="4ca59-117">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="4ca59-117">Example 4</span></span>
```powershell
PS C:\> Get-AzDeploymentScript -Id "/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}"
```

<span data-ttu-id="4ca59-118">Obtém um script de implantação com a ID de recurso especificada.</span><span class="sxs-lookup"><span data-stu-id="4ca59-118">Gets a deployment script with the given resource Id.</span></span> 

## <span data-ttu-id="4ca59-119">OS</span><span class="sxs-lookup"><span data-stu-id="4ca59-119">PARAMETERS</span></span>

### <span data-ttu-id="4ca59-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ca59-120">-DefaultProfile</span></span>
<span data-ttu-id="4ca59-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4ca59-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ca59-122">-ID</span><span class="sxs-lookup"><span data-stu-id="4ca59-122">-Id</span></span>
<span data-ttu-id="4ca59-123">A ID de recurso totalmente qualificado do script de implantação.</span><span class="sxs-lookup"><span data-stu-id="4ca59-123">The fully qualified resource Id of the deployment script.</span></span>
<span data-ttu-id="4ca59-124">Exemplo:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span><span class="sxs-lookup"><span data-stu-id="4ca59-124">Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/deploymentScripts/{deploymentScriptName}</span></span>

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

### <span data-ttu-id="4ca59-125">-Nome</span><span class="sxs-lookup"><span data-stu-id="4ca59-125">-Name</span></span>
<span data-ttu-id="4ca59-126">O nome do script de implantação</span><span class="sxs-lookup"><span data-stu-id="4ca59-126">The name of the deployment script</span></span>

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

### <span data-ttu-id="4ca59-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ca59-127">-ResourceGroupName</span></span>
<span data-ttu-id="4ca59-128">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="4ca59-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4ca59-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ca59-129">CommonParameters</span></span>
<span data-ttu-id="4ca59-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ca59-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4ca59-131">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ca59-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ca59-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4ca59-132">INPUTS</span></span>

### <span data-ttu-id="4ca59-133">System. String</span><span class="sxs-lookup"><span data-stu-id="4ca59-133">System.String</span></span>

## <span data-ttu-id="4ca59-134">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4ca59-134">OUTPUTS</span></span>

### <span data-ttu-id="4ca59-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span><span class="sxs-lookup"><span data-stu-id="4ca59-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PsDeploymentScript</span></span>

## <span data-ttu-id="4ca59-136">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4ca59-136">NOTES</span></span>

## <span data-ttu-id="4ca59-137">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4ca59-137">RELATED LINKS</span></span>
