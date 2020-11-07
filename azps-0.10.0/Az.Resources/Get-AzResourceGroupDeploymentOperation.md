---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 9F29DFCB-A02B-45A5-99B9-C054BF4FCA6C
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azresourcegroupdeploymentoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzResourceGroupDeploymentOperation.md
ms.openlocfilehash: 22438110dd66fbbb89e992d79f37b1e8e2e325d9
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93776425"
---
# <span data-ttu-id="253f6-101">Get-AzResourceGroupDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="253f6-101">Get-AzResourceGroupDeploymentOperation</span></span>

## <span data-ttu-id="253f6-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="253f6-102">SYNOPSIS</span></span>
<span data-ttu-id="253f6-103">Obtém a operação de implantação do grupo de recursos</span><span class="sxs-lookup"><span data-stu-id="253f6-103">Gets the resource group deployment operation</span></span>

## <span data-ttu-id="253f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="253f6-104">SYNTAX</span></span>

```
Get-AzResourceGroupDeploymentOperation -DeploymentName <String> [-SubscriptionId <Guid>]
 -ResourceGroupName <String> [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="253f6-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="253f6-105">DESCRIPTION</span></span>
<span data-ttu-id="253f6-106">O cmdlet **Get-AzResourceGroupDeploymentOperation** lista todas as operações que fazem parte de uma implantação para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="253f6-106">The **Get-AzResourceGroupDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="253f6-107">Ele também pode mostrar a resposta e o conteúdo da solicitação para cada operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="253f6-107">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="253f6-108">Essas são as mesmas informações fornecidas nos detalhes da implantação no Portal.</span><span class="sxs-lookup"><span data-stu-id="253f6-108">This is the same information provided in the deployment details on the portal.</span></span>
<span data-ttu-id="253f6-109">Para obter a solicitação e o conteúdo da resposta, habilite a configuração ao enviar uma implantação por meio de **New-AzResourceGroupDeployment**.</span><span class="sxs-lookup"><span data-stu-id="253f6-109">To get the request and the response content, enable the setting when submitting a deployment through **New-AzResourceGroupDeployment**.</span></span>
<span data-ttu-id="253f6-110">Ele pode registrar e expor segredos como senhas usadas na propriedade de recurso ou **listKeys** operações que são retornadas quando você recupera as operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="253f6-110">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="253f6-111">Para saber mais sobre essa configuração e como habilitá-la, consulte implantações de modelo de New-AzResourceGroupDeployment e detentor de depuração</span><span class="sxs-lookup"><span data-stu-id="253f6-111">For more on this setting and how to enable it, see New-AzResourceGroupDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="253f6-112">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="253f6-112">EXAMPLES</span></span>

### <span data-ttu-id="253f6-113">Get1</span><span class="sxs-lookup"><span data-stu-id="253f6-113">Get1</span></span>
```
PS C:\>Get-AzResourceGroupDeploymentOperation -DeploymentName test -ResourceGroupName test
```

<span data-ttu-id="253f6-114">Obtém a operação de implantação com o nome "teste" no grupo de recursos "teste"</span><span class="sxs-lookup"><span data-stu-id="253f6-114">Gets deployment operation with name "test" under resource group "test"</span></span>

## <span data-ttu-id="253f6-115">OS</span><span class="sxs-lookup"><span data-stu-id="253f6-115">PARAMETERS</span></span>

### <span data-ttu-id="253f6-116">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="253f6-116">-ApiVersion</span></span>
<span data-ttu-id="253f6-117">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="253f6-117">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="253f6-118">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="253f6-118">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="253f6-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="253f6-119">-DefaultProfile</span></span>
<span data-ttu-id="253f6-120">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure</span><span class="sxs-lookup"><span data-stu-id="253f6-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253f6-121">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="253f6-121">-DeploymentName</span></span>
<span data-ttu-id="253f6-122">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="253f6-122">The deployment name.</span></span>

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

### <span data-ttu-id="253f6-123">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="253f6-123">-InformationAction</span></span>
<span data-ttu-id="253f6-124">Especifica como esse cmdlet responde a um evento de informações.</span><span class="sxs-lookup"><span data-stu-id="253f6-124">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="253f6-125">Os valores aceitáveis para esse parâmetro são:</span><span class="sxs-lookup"><span data-stu-id="253f6-125">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="253f6-126">Contínuo</span><span class="sxs-lookup"><span data-stu-id="253f6-126">Continue</span></span>
- <span data-ttu-id="253f6-127">Ignorar</span><span class="sxs-lookup"><span data-stu-id="253f6-127">Ignore</span></span>
- <span data-ttu-id="253f6-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="253f6-128">Inquire</span></span>
- <span data-ttu-id="253f6-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="253f6-129">SilentlyContinue</span></span>
- <span data-ttu-id="253f6-130">Finaliza</span><span class="sxs-lookup"><span data-stu-id="253f6-130">Stop</span></span>
- <span data-ttu-id="253f6-131">Suspensão</span><span class="sxs-lookup"><span data-stu-id="253f6-131">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253f6-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="253f6-132">-InformationVariable</span></span>
<span data-ttu-id="253f6-133">Especifica uma variável de informações.</span><span class="sxs-lookup"><span data-stu-id="253f6-133">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="253f6-134">-Pre</span><span class="sxs-lookup"><span data-stu-id="253f6-134">-Pre</span></span>
<span data-ttu-id="253f6-135">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="253f6-135">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="253f6-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="253f6-136">-ResourceGroupName</span></span>
<span data-ttu-id="253f6-137">O nome do grupo de recursos.</span><span class="sxs-lookup"><span data-stu-id="253f6-137">The resource group name.</span></span>

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

### <span data-ttu-id="253f6-138">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="253f6-138">-SubscriptionId</span></span>
<span data-ttu-id="253f6-139">A assinatura a ser usada.</span><span class="sxs-lookup"><span data-stu-id="253f6-139">The subscription to use.</span></span>

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

### <span data-ttu-id="253f6-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="253f6-140">CommonParameters</span></span>
<span data-ttu-id="253f6-141">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="253f6-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="253f6-142">Para obter mais informações, consulte about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="253f6-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="253f6-143">SENSORES</span><span class="sxs-lookup"><span data-stu-id="253f6-143">INPUTS</span></span>

## <span data-ttu-id="253f6-144">EXIBE</span><span class="sxs-lookup"><span data-stu-id="253f6-144">OUTPUTS</span></span>

## <span data-ttu-id="253f6-145">INFORMA</span><span class="sxs-lookup"><span data-stu-id="253f6-145">NOTES</span></span>

## <span data-ttu-id="253f6-146">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="253f6-146">RELATED LINKS</span></span>
