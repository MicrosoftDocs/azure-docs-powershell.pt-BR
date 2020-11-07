---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeploymentoperation
schema: 2.0.0
ms.openlocfilehash: 2bb5c3823d974dad53045d9283099befd4d60855
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93786390"
---
# <span data-ttu-id="476cd-101">Get-AzureRmDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="476cd-101">Get-AzureRmDeploymentOperation</span></span>

## <span data-ttu-id="476cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="476cd-102">SYNOPSIS</span></span>
<span data-ttu-id="476cd-103">Obter operação de implantação</span><span class="sxs-lookup"><span data-stu-id="476cd-103">Get deployment operation</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="476cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="476cd-104">SYNTAX</span></span>

### <span data-ttu-id="476cd-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="476cd-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentName <String> [-OperationId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="476cd-106">GetByDeploymentObject</span><span class="sxs-lookup"><span data-stu-id="476cd-106">GetByDeploymentObject</span></span>
```
Get-AzureRmDeploymentOperation -DeploymentObject <PSDeployment> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="476cd-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="476cd-107">DESCRIPTION</span></span>
<span data-ttu-id="476cd-108">O cmdlet **Get-AzureRmDeploymentOperation** lista todas as operações que fazem parte de uma implantação para ajudá-lo a identificar e fornecer mais informações sobre as operações exatas que falharam para uma implantação específica.</span><span class="sxs-lookup"><span data-stu-id="476cd-108">The **Get-AzureRmDeploymentOperation** cmdlet lists all the operations that were part of a deployment to help you identify and give more information about the exact operations that failed for a particular deployment.</span></span>
<span data-ttu-id="476cd-109">Ele também pode mostrar a resposta e o conteúdo da solicitação para cada operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="476cd-109">It can also show the response and the request content for each deployment operation.</span></span>
<span data-ttu-id="476cd-110">Essas são as mesmas informações fornecidas nos detalhes da implantação no Portal.</span><span class="sxs-lookup"><span data-stu-id="476cd-110">This is the same information provided in the deployment details on the portal.</span></span>

<span data-ttu-id="476cd-111">Para obter a solicitação e o conteúdo da resposta, habilite a configuração ao enviar uma implantação por meio de **New-AzureRmDeployment**.</span><span class="sxs-lookup"><span data-stu-id="476cd-111">To get the request and the response content, enable the setting when submitting a deployment through **New-AzureRmDeployment**.</span></span>
<span data-ttu-id="476cd-112">Ele pode registrar e expor segredos como senhas usadas na propriedade de recurso ou **listKeys** operações que são retornadas quando você recupera as operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="476cd-112">It can potentially log and expose secrets like passwords used in the resource property or **listKeys** operations that are then returned when you retrieve the deployment operations.</span></span>
<span data-ttu-id="476cd-113">Para saber mais sobre essa configuração e como habilitá-la, consulte implantações de modelo de New-AzureRmDeployment e detentor de depuração</span><span class="sxs-lookup"><span data-stu-id="476cd-113">For more on this setting and how to enable it, see New-AzureRmDeployment and Debugging ARM template deployments</span></span>

## <span data-ttu-id="476cd-114">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="476cd-114">EXAMPLES</span></span>

### <span data-ttu-id="476cd-115">Obter operações de implantação de acordo com um nome de implantação</span><span class="sxs-lookup"><span data-stu-id="476cd-115">Get deployment operations given a deployment name</span></span>
```
PS C:\>Get-AzureRmDeploymentOperation -DeploymentName test
```

<span data-ttu-id="476cd-116">Obtém a operação de implantação com o nome "Test" no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="476cd-116">Gets deployment operation with name "test" at the current subscription scope.</span></span>

### <span data-ttu-id="476cd-117">Obter uma implantação e obter suas operações de implantação</span><span class="sxs-lookup"><span data-stu-id="476cd-117">Get a deployment and get its deployment operations</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "test" | Get-AzureRmDeploymentOperation
```

<span data-ttu-id="476cd-118">Esse comando obtém a implantação "teste" no escopo da assinatura atual e obtém suas operações de implantação.</span><span class="sxs-lookup"><span data-stu-id="476cd-118">This command gets the deployment "test" at the current subscription scope and get its deployment operations.</span></span>

## <span data-ttu-id="476cd-119">OS</span><span class="sxs-lookup"><span data-stu-id="476cd-119">PARAMETERS</span></span>

### <span data-ttu-id="476cd-120">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="476cd-120">-ApiVersion</span></span>
<span data-ttu-id="476cd-121">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="476cd-121">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="476cd-122">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="476cd-122">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="476cd-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="476cd-123">-DefaultProfile</span></span>
<span data-ttu-id="476cd-124">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="476cd-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="476cd-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="476cd-125">-DeploymentName</span></span>
<span data-ttu-id="476cd-126">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="476cd-126">The deployment name.</span></span>

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

### <span data-ttu-id="476cd-127">-DeploymentObject</span><span class="sxs-lookup"><span data-stu-id="476cd-127">-DeploymentObject</span></span>
<span data-ttu-id="476cd-128">O objeto de implantação.</span><span class="sxs-lookup"><span data-stu-id="476cd-128">The deployment object.</span></span>

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

### <span data-ttu-id="476cd-129">-OperationId</span><span class="sxs-lookup"><span data-stu-id="476cd-129">-OperationId</span></span>
<span data-ttu-id="476cd-130">A ID da operação de implantação.</span><span class="sxs-lookup"><span data-stu-id="476cd-130">The deployment operation Id.</span></span>

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

### <span data-ttu-id="476cd-131">-Pre</span><span class="sxs-lookup"><span data-stu-id="476cd-131">-Pre</span></span>
<span data-ttu-id="476cd-132">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="476cd-132">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="476cd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="476cd-133">CommonParameters</span></span>
<span data-ttu-id="476cd-134">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="476cd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="476cd-135">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="476cd-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="476cd-136">SENSORES</span><span class="sxs-lookup"><span data-stu-id="476cd-136">INPUTS</span></span>

### <span data-ttu-id="476cd-137">System. String</span><span class="sxs-lookup"><span data-stu-id="476cd-137">System.String</span></span>
<span data-ttu-id="476cd-138">System. Nullable ' 1 [[System. GUID, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="476cd-138">System.Nullable\`1[[System.Guid, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="476cd-139">EXIBE</span><span class="sxs-lookup"><span data-stu-id="476cd-139">OUTPUTS</span></span>

### <span data-ttu-id="476cd-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span><span class="sxs-lookup"><span data-stu-id="476cd-140">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeploymentOperation</span></span>

## <span data-ttu-id="476cd-141">INFORMA</span><span class="sxs-lookup"><span data-stu-id="476cd-141">NOTES</span></span>

## <span data-ttu-id="476cd-142">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="476cd-142">RELATED LINKS</span></span>
