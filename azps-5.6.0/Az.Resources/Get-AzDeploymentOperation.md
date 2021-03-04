---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: 5507e180d5f56b75006f31f9cc6753f50d821a3b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888087"
---
# <span data-ttu-id="dfb83-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfb83-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="dfb83-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfb83-102">SYNOPSIS</span></span>
<span data-ttu-id="dfb83-103">Obter operação de implantação</span><span class="sxs-lookup"><span data-stu-id="dfb83-103">Get deployment operation</span></span>

## <span data-ttu-id="dfb83-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="dfb83-104">SYNTAX</span></span>

### <span data-ttu-id="dfb83-105">GetByDeploymentName (Padrão)</span><span class="sxs-lookup"><span data-stu-id="dfb83-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dfb83-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="dfb83-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfb83-107">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="dfb83-107">DESCRIPTION</span></span>
<span data-ttu-id="dfb83-108">O cmdlet **Get-AzDeploymentOperation** lista todas as operações que fazem parte de uma implantação para ajudá-lo a identificar e dar mais informações sobre as operações exatas que falharam em uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="dfb83-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="dfb83-109">Ele também pode mostrar a resposta e o conteúdo da solicitação para cada operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="dfb83-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="dfb83-110">Essas são as mesmas informações fornecidas nos detalhes de implantação no portal.</span><span class="sxs-lookup"><span data-stu-id="dfb83-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="dfb83-111">Para obter a solicitação e o conteúdo da resposta, habilita a configuração ao enviar uma implantação por meio do **New-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="dfb83-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="dfb83-112">Ele pode registrar e expor segredos como senhas usadas na propriedade de recursos ou operações **listKeys** que são retornadas quando você recupera as operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="dfb83-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="dfb83-113">Para saber mais sobre essa configuração e como habilita-la, consulte New-AzDeployment e Depuração ARM de modelo</span><span class="sxs-lookup"><span data-stu-id="dfb83-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="dfb83-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dfb83-114">EXAMPLES</span></span>

### <span data-ttu-id="dfb83-115">Exemplo 1: obter operações de implantação com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="dfb83-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="dfb83-116">Obtém a operação de implantação com o nome "test" no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="dfb83-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="dfb83-117">Exemplo 2: Obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="dfb83-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="dfb83-118">Esse comando obtém o "teste" de implantação no escopo de assinatura atual e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="dfb83-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="dfb83-119">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="dfb83-119">PARAMETERS</span></span>

### <span data-ttu-id="dfb83-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfb83-120">-DefaultProfile</span></span>
<span data-ttu-id="dfb83-121">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dfb83-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dfb83-122">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="dfb83-122">-DeploymentName</span></span>
<span data-ttu-id="dfb83-123">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="dfb83-123">The deployment name.</span></span>

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

### <span data-ttu-id="dfb83-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="dfb83-124">-DeploymentObject</span></span>
<span data-ttu-id="dfb83-125">O objeto deployment.</span><span class="sxs-lookup"><span data-stu-id="dfb83-125">The deployment object.</span></span>

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

### <span data-ttu-id="dfb83-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="dfb83-126">-OperationId</span></span>
<span data-ttu-id="dfb83-127">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="dfb83-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="dfb83-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="dfb83-128">-Pre</span></span>
<span data-ttu-id="dfb83-129">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="dfb83-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dfb83-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfb83-130">CommonParameters</span></span>
<span data-ttu-id="dfb83-131">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfb83-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfb83-132">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dfb83-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfb83-133">INPUTS</span><span class="sxs-lookup"><span data-stu-id="dfb83-133">INPUTS</span></span>

### <span data-ttu-id="dfb83-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span><span class="sxs-lookup"><span data-stu-id="dfb83-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dfb83-135">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="dfb83-135">OUTPUTS</span></span>

### <span data-ttu-id="dfb83-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="dfb83-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="dfb83-137">NOTES</span><span class="sxs-lookup"><span data-stu-id="dfb83-137">NOTES</span></span>

## <span data-ttu-id="dfb83-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dfb83-138">RELATED LINKS</span></span>
