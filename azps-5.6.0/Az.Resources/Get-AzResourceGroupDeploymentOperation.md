---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 06056bd8bf9060a7610b74b8332ff5ab2a4790f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101888077"
---
# <span data-ttu-id="1ae08-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1ae08-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="1ae08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ae08-102">SYNOPSIS</span></span>
<span data-ttu-id="1ae08-103">Obtém a operação de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="1ae08-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="1ae08-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1ae08-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1ae08-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1ae08-105">DESCRIPTION</span></span>
<span data-ttu-id="1ae08-106">O cmdlet **Get-AzResourceGroupDeploymentOperation** lista todas as operações que fazem parte de uma implantação para ajudá-lo a identificar e dar mais informações sobre as operações exatas que falharam em uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="1ae08-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="1ae08-107">Ele também pode mostrar a resposta e o conteúdo da solicitação para cada operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="1ae08-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="1ae08-108">Essas são as mesmas informações fornecidas nos detalhes de implantação no portal.</span><span class="sxs-lookup"><span data-stu-id="1ae08-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="1ae08-109">Para obter a solicitação e o conteúdo da resposta, habilita a configuração ao enviar uma implantação por meio de **New-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="1ae08-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="1ae08-110">Ele pode registrar e expor segredos como senhas usadas na propriedade de recursos ou operações **listKeys** que são retornadas quando você recupera as operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="1ae08-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="1ae08-111">Para saber mais sobre essa configuração e como habilita-la, consulte New-AzResourceGroupDeployment e Depuração ARM de modelo</span><span class="sxs-lookup"><span data-stu-id="1ae08-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="1ae08-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1ae08-112">EXAMPLES</span></span>

### <span data-ttu-id="1ae08-113">Exemplo 1: Get1</span><span class="sxs-lookup"><span data-stu-id="1ae08-113">Example 1: Get1</span></span>
```powershell
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="1ae08-114">Obtém a operação de implantação com o nome "test" no grupo de recursos "test"</span><span class="sxs-lookup"><span data-stu-id="1ae08-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="1ae08-115">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1ae08-115">PARAMETERS</span></span>

### <span data-ttu-id="1ae08-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ae08-116">-DefaultProfile</span></span>
<span data-ttu-id="1ae08-117">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1ae08-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ae08-118">-DeploymentName</span><span class="sxs-lookup"><span data-stu-id="1ae08-118">-DeploymentName</span></span>
<span data-ttu-id="1ae08-119">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="1ae08-119">The deployment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae08-120">-Pre</span><span class="sxs-lookup"><span data-stu-id="1ae08-120">-Pre</span></span>
<span data-ttu-id="1ae08-121">Quando definido, indica que o cmdlet deve usar versões da API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="1ae08-121">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="1ae08-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ae08-122">-ResourceGroupName</span></span>
<span data-ttu-id="1ae08-123">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="1ae08-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae08-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1ae08-124">-SubscriptionId</span></span>
<span data-ttu-id="1ae08-125">A assinatura a ser usada.</span><span class="sxs-lookup"><span data-stu-id="1ae08-125">The subscription to use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ae08-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ae08-126">CommonParameters</span></span>
<span data-ttu-id="1ae08-127">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1ae08-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ae08-128">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1ae08-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ae08-129">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1ae08-129">INPUTS</span></span>

### <span data-ttu-id="1ae08-130">System.String</span><span class="sxs-lookup"><span data-stu-id="1ae08-130">System.String</span></span>

### <span data-ttu-id="1ae08-131">System.Nullable'1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="1ae08-131">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="1ae08-132">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1ae08-132">OUTPUTS</span></span>

### <span data-ttu-id="1ae08-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="1ae08-133">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="1ae08-134">NOTES</span><span class="sxs-lookup"><span data-stu-id="1ae08-134">NOTES</span></span>

## <span data-ttu-id="1ae08-135">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1ae08-135">RELATED LINKS</span></span>
