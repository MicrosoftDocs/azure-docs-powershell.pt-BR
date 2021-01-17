---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427329"
---
# <span data-ttu-id="19161-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="19161-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="19161-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="19161-102">SYNOPSIS</span></span>
<span data-ttu-id="19161-103">Obter a operação de implantação para implantação de grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="19161-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="19161-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="19161-104">SYNTAX</span></span>

### <span data-ttu-id="19161-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="19161-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19161-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="19161-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19161-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="19161-107">DESCRIPTION</span></span>
<span data-ttu-id="19161-108">O cmdlet **Get-AzManagementGroupDeploymentOperation** lista todas as operações que fazem parte de uma implantação de grupo de gerenciamento para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="19161-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="19161-109">Essas são as mesmas informações fornecidas nos detalhes da implantação no Portal.</span><span class="sxs-lookup"><span data-stu-id="19161-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="19161-110">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="19161-110">EXAMPLES</span></span>

### <span data-ttu-id="19161-111">Exemplo 1: obter operações de implantação de acordo com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="19161-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="19161-112">Obtém operações de implantação com o nome "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="19161-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="19161-113">Exemplo 2: obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="19161-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="19161-114">Este comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG" e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="19161-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="19161-115">OS</span><span class="sxs-lookup"><span data-stu-id="19161-115">PARAMETERS</span></span>

### <span data-ttu-id="19161-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19161-116">-DefaultProfile</span></span>
<span data-ttu-id="19161-117">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="19161-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19161-118">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="19161-118">-DeploymentName</span></span>
<span data-ttu-id="19161-119">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="19161-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19161-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="19161-120">-DeploymentObject</span></span>
<span data-ttu-id="19161-121">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="19161-121">The deployment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment
Parameter Sets: GetByDeploymentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19161-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="19161-122">-ManagementGroupId</span></span>
<span data-ttu-id="19161-123">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="19161-123">The management group id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19161-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="19161-124">-OperationId</span></span>
<span data-ttu-id="19161-125">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="19161-125">The deployment operation Id.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19161-126">-Pre</span><span class="sxs-lookup"><span data-stu-id="19161-126">-Pre</span></span>
<span data-ttu-id="19161-127">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="19161-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="19161-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19161-128">CommonParameters</span></span>
<span data-ttu-id="19161-129">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19161-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19161-130">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="19161-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19161-131">SENSORES</span><span class="sxs-lookup"><span data-stu-id="19161-131">INPUTS</span></span>

### <span data-ttu-id="19161-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="19161-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="19161-133">EXIBE</span><span class="sxs-lookup"><span data-stu-id="19161-133">OUTPUTS</span></span>

### <span data-ttu-id="19161-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="19161-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="19161-135">INFORMA</span><span class="sxs-lookup"><span data-stu-id="19161-135">NOTES</span></span>

## <span data-ttu-id="19161-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="19161-136">RELATED LINKS</span></span>
