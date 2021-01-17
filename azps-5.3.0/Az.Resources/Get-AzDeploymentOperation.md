---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeploymentOperation.md
ms.openlocfilehash: e1da6e54eac3e72217e83e498966bdfa80740762
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98427346"
---
# <span data-ttu-id="d84be-101">Get-AzDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d84be-101">Get-AzDeploymentOperation</span></span>

## <span data-ttu-id="d84be-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d84be-102">SYNOPSIS</span></span>
<span data-ttu-id="d84be-103">Obter operação de implantação</span><span class="sxs-lookup"><span data-stu-id="d84be-103">Get deployment operation</span></span>

## <span data-ttu-id="d84be-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d84be-104">SYNTAX</span></span>

### <span data-ttu-id="d84be-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d84be-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d84be-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d84be-106">GetByDeploymentObject</span></span>
```
Get-AzDeploymentOperation -DeploymentObject <PSDeployment> [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d84be-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d84be-107">DESCRIPTION</span></span>
<span data-ttu-id="d84be-108">O cmdlet **Get-AzDeploymentOperation** lista todas as operações que fazem parte de uma implantação para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="d84be-108">The **Get-AzDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="d84be-109">Ele também pode mostrar a resposta e o conteúdo da solicitação para cada operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="d84be-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="d84be-110">Essas são as mesmas informações fornecidas nos detalhes da implantação no Portal.</span><span class="sxs-lookup"><span data-stu-id="d84be-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="d84be-111">Para obter a solicitação e o conteúdo da resposta, habilite a configuração ao enviar uma implantação por meio de **New-AzDeployment**.</span><span class="sxs-lookup"><span data-stu-id="d84be-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzDeployment**.</span></span>
<span data-ttu-id="d84be-112">Ele pode registrar e expor segredos como senhas usadas na propriedade de recurso ou **listKeys** operações que são retornadas quando você recupera as operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="d84be-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="d84be-113">Para saber mais sobre essa configuração e como habilitá-la, consulte implantações de modelo de New-AzDeployment e detentor de depuração</span><span class="sxs-lookup"><span data-stu-id="d84be-113">For more on this setting and how to enable it, see New-AzDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="d84be-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d84be-114">EXAMPLES</span></span>

### <span data-ttu-id="d84be-115">Exemplo 1: obter operações de implantação de acordo com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="d84be-115">Example 1: Get deployment operations given a deployment name</span></span>
```powershell
PS C:\>Get-AzDeploymentOperation -DeploymentName test
```

<span data-ttu-id="d84be-116">Obtém a operação de implantação com o nome "Test" no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d84be-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="d84be-117">Exemplo 2: obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="d84be-117">Example 2: Get a deployment and get its deployment operations</span></span>
```powershell
PS C:\>Get-AzDeployment -Name "test" | Get-AzDeploymentOperation
```

<span data-ttu-id="d84be-118">Esse comando obtém a implantação "teste" no escopo da assinatura atual e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="d84be-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="d84be-119">OS</span><span class="sxs-lookup"><span data-stu-id="d84be-119">PARAMETERS</span></span>

### <span data-ttu-id="d84be-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d84be-120">-DefaultProfile</span></span>
<span data-ttu-id="d84be-121">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d84be-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d84be-122">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="d84be-122">-DeploymentName</span></span>
<span data-ttu-id="d84be-123">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="d84be-123">The deployment name.</span></span>

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

### <span data-ttu-id="d84be-124">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="d84be-124">-DeploymentObject</span></span>
<span data-ttu-id="d84be-125">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="d84be-125">The deployment object.</span></span>

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

### <span data-ttu-id="d84be-126">-OperationId</span><span class="sxs-lookup"><span data-stu-id="d84be-126">-OperationId</span></span>
<span data-ttu-id="d84be-127">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="d84be-127">The deployment operation Id.</span></span>

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

### <span data-ttu-id="d84be-128">-Pre</span><span class="sxs-lookup"><span data-stu-id="d84be-128">-Pre</span></span>
<span data-ttu-id="d84be-129">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d84be-129">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d84be-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d84be-130">CommonParameters</span></span>
<span data-ttu-id="d84be-131">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d84be-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d84be-132">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d84be-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d84be-133">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d84be-133">INPUTS</span></span>

### <span data-ttu-id="d84be-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="d84be-134">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d84be-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d84be-135">OUTPUTS</span></span>

### <span data-ttu-id="d84be-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="d84be-136">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="d84be-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d84be-137">NOTES</span></span>

## <span data-ttu-id="d84be-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d84be-138">RELATED LINKS</span></span>
