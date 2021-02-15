---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztenantdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTenantDeploymentOperation.md
ms.openlocfilehash: d6afb06c05478066e4b76793625864a97e3b6758
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100114907"
---
# <span data-ttu-id="f6cff-101">Get-AzTenantDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f6cff-101">Get-AzTenantDeploymentOperation</span></span>

## <span data-ttu-id="f6cff-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="f6cff-102">SYNOPSIS</span></span>
<span data-ttu-id="f6cff-103">Obter a operação de implantação para implantação no escopo do locatário</span><span class="sxs-lookup"><span data-stu-id="f6cff-103">Get deployment operation for deployment at tenant scope</span></span>

## <span data-ttu-id="f6cff-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f6cff-104">SYNTAX</span></span>

### <span data-ttu-id="f6cff-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="f6cff-105">GetByDeploymentName (Default)</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f6cff-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f6cff-106">GetByDeploymentObject</span></span>
```
Get-AzTenantDeploymentOperation -DeploymentObject <PSDeployment> [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6cff-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6cff-107">DESCRIPTION</span></span>
<span data-ttu-id="f6cff-108">O cmdlet **Get-AzTenantDeploymentOperation** lista todas as operações que fazem parte da implantação no escopo atual do locatário para ajudá-lo a identificar e a dar mais informações sobre as operações exatas que falharam em uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="f6cff-108">The **Get-AzTenantDeploymentOperation** cmdlet lists all the operations that were part of deployment at the current tenant scope to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>

## <span data-ttu-id="f6cff-109">Exemplos</span><span class="sxs-lookup"><span data-stu-id="f6cff-109">EXAMPLES</span></span>

### <span data-ttu-id="f6cff-110">Exemplo 1: obter operações de implantação com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="f6cff-110">Example 1: Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzTenantDeploymentOperation -DeploymentName Deploy01
```

<span data-ttu-id="f6cff-111">Obtém operações de implantação com o nome "Deploy01" no escopo atual do locatário.</span><span class="sxs-lookup"><span data-stu-id="f6cff-111">Gets deployment operations with name "Deploy01" at the current tenant scope.</span></span>

### <span data-ttu-id="f6cff-112">Exemplo 2: Obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="f6cff-112">Example 2: Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzTenantDeployment -Name Deploy01 | Get-AzTenantDeploymentOperation
```

<span data-ttu-id="f6cff-113">Esse comando obtém a implantação "Deploy01" no escopo atual do locatário e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="f6cff-113">This command gets the deployment "Deploy01" at the current tenant scope and get its deployment operations.</span></span>

## <span data-ttu-id="f6cff-114">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f6cff-114">PARAMETERS</span></span>

### <span data-ttu-id="f6cff-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6cff-115">-DefaultProfile</span></span>
<span data-ttu-id="f6cff-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="f6cff-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6cff-117">-Nomeda Implantação</span><span class="sxs-lookup"><span data-stu-id="f6cff-117">-DeploymentName</span></span>
<span data-ttu-id="f6cff-118">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="f6cff-118">The deployment name.</span></span>

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

### <span data-ttu-id="f6cff-119">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="f6cff-119">-DeploymentObject</span></span>
<span data-ttu-id="f6cff-120">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="f6cff-120">The deployment object.</span></span>

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

### <span data-ttu-id="f6cff-121">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f6cff-121">-OperationId</span></span>
<span data-ttu-id="f6cff-122">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="f6cff-122">The deployment operation Id.</span></span>

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

### <span data-ttu-id="f6cff-123">-Pré-</span><span class="sxs-lookup"><span data-stu-id="f6cff-123">-Pre</span></span>
<span data-ttu-id="f6cff-124">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="f6cff-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="f6cff-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6cff-125">CommonParameters</span></span>
<span data-ttu-id="f6cff-126">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6cff-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6cff-127">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6cff-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6cff-128">Entradas</span><span class="sxs-lookup"><span data-stu-id="f6cff-128">INPUTS</span></span>

### <span data-ttu-id="f6cff-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="f6cff-129">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="f6cff-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="f6cff-130">OUTPUTS</span></span>

### <span data-ttu-id="f6cff-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="f6cff-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="f6cff-132">Notas</span><span class="sxs-lookup"><span data-stu-id="f6cff-132">NOTES</span></span>

## <span data-ttu-id="f6cff-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="f6cff-133">RELATED LINKS</span></span>
