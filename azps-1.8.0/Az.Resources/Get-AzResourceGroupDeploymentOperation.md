---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: a67bfb43aa4cafe4b9c7f20e6ff757989deee5d6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93599423"
---
# <span data-ttu-id="e122f-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="e122f-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="e122f-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="e122f-102">SYNOPSIS</span></span>
<span data-ttu-id="e122f-103">Obtém a operação de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="e122f-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="e122f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e122f-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e122f-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="e122f-105">DESCRIPTION</span></span>
<span data-ttu-id="e122f-106">O cmdlet **Get-AzResourceGroupDeploymentOperation** lista todas as operações que fazem parte de uma implantação para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="e122f-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="e122f-107">Ele também pode mostrar a resposta e o conteúdo da solicitação para cada operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="e122f-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="e122f-108">Essas são as mesmas informações fornecidas nos detalhes da implantação no Portal.</span><span class="sxs-lookup"><span data-stu-id="e122f-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="e122f-109">Para obter a solicitação e o conteúdo da resposta, habilite a configuração ao enviar uma implantação por meio de **New-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="e122f-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="e122f-110">Ele pode registrar e expor segredos como senhas usadas na propriedade de recurso ou **listKeys** operações que são retornadas quando você recupera as operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="e122f-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="e122f-111">Para saber mais sobre essa configuração e como habilitá-la, consulte implantações de modelo de New-AzResourceGroupDeployment e detentor de depuração</span><span class="sxs-lookup"><span data-stu-id="e122f-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="e122f-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="e122f-112">EXAMPLES</span></span>

### <span data-ttu-id="e122f-113">Get1</span><span class="sxs-lookup"><span data-stu-id="e122f-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="e122f-114">Obtém a operação de implantação com o nome "teste" no grupo de recursos "teste"</span><span class="sxs-lookup"><span data-stu-id="e122f-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="e122f-115">OS</span><span class="sxs-lookup"><span data-stu-id="e122f-115">PARAMETERS</span></span>

### <span data-ttu-id="e122f-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e122f-116">-ApiVersion</span></span>
<span data-ttu-id="e122f-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e122f-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="e122f-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="e122f-118">If not specified, the API version is automatically determined as the latest available.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e122f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e122f-119">-DefaultProfile</span></span>
<span data-ttu-id="e122f-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="e122f-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e122f-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="e122f-121">-DeploymentName</span></span>
<span data-ttu-id="e122f-122">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="e122f-122">The deployment name.</span></span>

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

### <span data-ttu-id="e122f-123">-Pre</span><span class="sxs-lookup"><span data-stu-id="e122f-123">-Pre</span></span>
<span data-ttu-id="e122f-124">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="e122f-124">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="e122f-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e122f-125">-ResourceGroupName</span></span>
<span data-ttu-id="e122f-126">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="e122f-126">The resource group name.</span></span>

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

### <span data-ttu-id="e122f-127">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e122f-127">-SubscriptionId</span></span>
<span data-ttu-id="e122f-128">A assinatura a ser usada.</span><span class="sxs-lookup"><span data-stu-id="e122f-128">The subscription to use.</span></span>

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

### <span data-ttu-id="e122f-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e122f-129">CommonParameters</span></span>
<span data-ttu-id="e122f-130">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e122f-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e122f-131">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e122f-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e122f-132">SENSORES</span><span class="sxs-lookup"><span data-stu-id="e122f-132">INPUTS</span></span>

### <span data-ttu-id="e122f-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e122f-133">System.String</span></span>

### <span data-ttu-id="e122f-134">System. Nullable ' 1 [[System. GUID, System. Private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e122f-134">System.Nullable\`1[[System.Guid, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e122f-135">EXIBE</span><span class="sxs-lookup"><span data-stu-id="e122f-135">OUTPUTS</span></span>

### <span data-ttu-id="e122f-136">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="e122f-136">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e122f-137">INFORMA</span><span class="sxs-lookup"><span data-stu-id="e122f-137">NOTES</span></span>

## <span data-ttu-id="e122f-138">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="e122f-138">RELATED LINKS</span></span>
