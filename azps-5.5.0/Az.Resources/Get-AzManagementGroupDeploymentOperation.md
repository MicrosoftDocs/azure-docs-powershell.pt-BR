---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroupDeploymentOperation.md
ms.openlocfilehash: 5054fe397c49e437b34755200b7f53c583e6e94f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100116216"
---
# <span data-ttu-id="ca6f5-101">Get-AzManagementGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ca6f5-101">Get-AzManagementGroupDeploymentOperation</span></span>

## <span data-ttu-id="ca6f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="ca6f5-102">SYNOPSIS</span></span>
<span data-ttu-id="ca6f5-103">Obter a operação de implantação para implantação de grupo de gerenciamento</span><span class="sxs-lookup"><span data-stu-id="ca6f5-103">Get deployment operation for management group deployment</span></span>

## <span data-ttu-id="ca6f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca6f5-104">SYNTAX</span></span>

### <span data-ttu-id="ca6f5-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="ca6f5-105">GetByDeploymentName (Default)</span></span>
```
Get-AzManagementGroupDeploymentOperation -ManagementGroupId <String> -DeploymentName <String>
 [-OperationId <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ca6f5-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ca6f5-106">GetByDeploymentObject</span></span>
```
Get-AzManagementGroupDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca6f5-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ca6f5-107">DESCRIPTION</span></span>
<span data-ttu-id="ca6f5-108">O cmdlet **Get-AzManagementGroupDeploymentOperation** lista todas as operações que fazem parte de uma implantação de grupo de gerenciamento para ajudá-lo a identificar e dar mais informações sobre as operações exatas que falharam em uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-108">The **Get-AzManagementGroupDeploymentOperation** cmdlet lists all the operations that were part of a management group deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="ca6f5-109">Essas são as mesmas informações fornecidas nos detalhes da implantação no portal.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-109">This is the same information provided in the deployment details on the portal.</span></span>

## <span data-ttu-id="ca6f5-110">Exemplos</span><span class="sxs-lookup"><span data-stu-id="ca6f5-110">EXAMPLES</span></span>

### <span data-ttu-id="ca6f5-111">Exemplo 1: obter operações de implantação com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="ca6f5-111">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzManagementGroupDeploymentOperation -ManagementGroupId myMG -DeploymentName Deploy01
```

<span data-ttu-id="ca6f5-112">Obtém operações de implantação com o nome "Deploy01" no grupo de gerenciamento "myMG".</span><span class="sxs-lookup"><span data-stu-id="ca6f5-112">Gets deployment operations with name "Deploy01" at the management group "myMG".</span></span>

### <span data-ttu-id="ca6f5-113">Exemplo 2: Obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="ca6f5-113">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzManagementGroupDeployment -ManagementGroupId myMG -Name Deploy01 | Get-AzManagementGroupDeploymentOperation
```

<span data-ttu-id="ca6f5-114">Esse comando obtém a implantação "Deploy01" no grupo de gerenciamento "myMG" e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-114">This command gets the deployment "Deploy01" at the management group "myMG" and get its deployment operations.</span></span>

## <span data-ttu-id="ca6f5-115">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca6f5-115">PARAMETERS</span></span>

### <span data-ttu-id="ca6f5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca6f5-116">-DefaultProfile</span></span>
<span data-ttu-id="ca6f5-117">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ca6f5-118">-Nomeda Implantação</span><span class="sxs-lookup"><span data-stu-id="ca6f5-118">-DeploymentName</span></span>
<span data-ttu-id="ca6f5-119">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-119">The deployment name.</span></span>

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

### <span data-ttu-id="ca6f5-120">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="ca6f5-120">-DeploymentObject</span></span>
<span data-ttu-id="ca6f5-121">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-121">The deployment object.</span></span>

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

### <span data-ttu-id="ca6f5-122">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="ca6f5-122">-ManagementGroupId</span></span>
<span data-ttu-id="ca6f5-123">A ID do grupo de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-123">The management group id.</span></span>

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

### <span data-ttu-id="ca6f5-124">-OperationId</span><span class="sxs-lookup"><span data-stu-id="ca6f5-124">-OperationId</span></span>
<span data-ttu-id="ca6f5-125">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-125">The deployment operation Id.</span></span>

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

### <span data-ttu-id="ca6f5-126">-Pré-</span><span class="sxs-lookup"><span data-stu-id="ca6f5-126">-Pre</span></span>
<span data-ttu-id="ca6f5-127">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-127">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="ca6f5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca6f5-128">CommonParameters</span></span>
<span data-ttu-id="ca6f5-129">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca6f5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca6f5-130">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ca6f5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca6f5-131">Entradas</span><span class="sxs-lookup"><span data-stu-id="ca6f5-131">INPUTS</span></span>

### <span data-ttu-id="ca6f5-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="ca6f5-132">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="ca6f5-133">Saídas</span><span class="sxs-lookup"><span data-stu-id="ca6f5-133">OUTPUTS</span></span>

### <span data-ttu-id="ca6f5-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="ca6f5-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="ca6f5-135">Notas</span><span class="sxs-lookup"><span data-stu-id="ca6f5-135">NOTES</span></span>

## <span data-ttu-id="ca6f5-136">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ca6f5-136">RELATED LINKS</span></span>
