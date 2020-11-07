---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 4820a1aec02355a535ec7798eb7f8e3dba6458b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93778113"
---
# <span data-ttu-id="4b4eb-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4b4eb-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="4b4eb-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="4b4eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4b4eb-103">Obter a operação de implantação para implantação de grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="4b4eb-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="4b4eb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4b4eb-104">SYNTAX</span></span>

### <span data-ttu-id="4b4eb-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="4b4eb-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4b4eb-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4b4eb-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b4eb-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="4b4eb-107">DESCRIPTION</span></span>
<span data-ttu-id="4b4eb-108">O cmdlet **Get-AzManagementGroupDeploymentOperation** lista todas as operações que fazem parte de uma implantação de grupo de gerenciamento para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="4b4eb-109">Essas são as mesmas informações fornecidas nos detalhes da implantação no Portal.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="4b4eb-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="4b4eb-110">EXAMPLES</span></span>

### <span data-ttu-id="4b4eb-111">Exemplo 1: obter operações de implantação de acordo com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="4b4eb-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="4b4eb-112">Obtém operações de implantação com o nome "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="4b4eb-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="4b4eb-113">Exemplo 2: obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="4b4eb-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="4b4eb-114">Este comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG" e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="4b4eb-115">OS</span><span class="sxs-lookup"><span data-stu-id="4b4eb-115">PARAMETERS</span></span>

### <span data-ttu-id="4b4eb-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b4eb-116">-ApiVersion</span></span>
<span data-ttu-id="4b4eb-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="4b4eb-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="4b4eb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b4eb-119">-DefaultProfile</span></span>
<span data-ttu-id="4b4eb-120">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4b4eb-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="4b4eb-121">-DeploymentName</span></span>
<span data-ttu-id="4b4eb-122">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-122">The deployment name.</span></span>

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

### <span data-ttu-id="4b4eb-123">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="4b4eb-123">-DeploymentObject</span></span>
<span data-ttu-id="4b4eb-124">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-124">The deployment object.</span></span>

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

### <span data-ttu-id="4b4eb-125">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="4b4eb-125">-ManagementGroupId</span></span>
<span data-ttu-id="4b4eb-126">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-126">The management group id.</span></span>

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

### <span data-ttu-id="4b4eb-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="4b4eb-127">-OperationId</span></span>
<span data-ttu-id="4b4eb-128">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-128">The deployment operation Id.</span></span>

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

### <span data-ttu-id="4b4eb-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b4eb-129">-Pre</span></span>
<span data-ttu-id="4b4eb-130">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="4b4eb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b4eb-131">CommonParameters</span></span>
<span data-ttu-id="4b4eb-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4b4eb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b4eb-133">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4b4eb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b4eb-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="4b4eb-134">INPUTS</span></span>

### <span data-ttu-id="4b4eb-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="4b4eb-135">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="4b4eb-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="4b4eb-136">OUTPUTS</span></span>

### <span data-ttu-id="4b4eb-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="4b4eb-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="4b4eb-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="4b4eb-138">NOTES</span></span>

## <span data-ttu-id="4b4eb-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="4b4eb-139">RELATED LINKS</span></span>
