---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmDeployment.md
ms.openlocfilehash: 6d25bcf98adb740ec695152eb5b27ec9402082c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93602584"
---
# <span data-ttu-id="dcf56-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="dcf56-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="dcf56-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="dcf56-102">SYNOPSIS</span></span>
<span data-ttu-id="dcf56-103">Obter implantação</span><span class="sxs-lookup"><span data-stu-id="dcf56-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dcf56-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dcf56-104">SYNTAX</span></span>

### <span data-ttu-id="dcf56-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="dcf56-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dcf56-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="dcf56-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dcf56-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="dcf56-107">DESCRIPTION</span></span>
<span data-ttu-id="dcf56-108">O cmdlet **Get-AzureRmDeployment** Obtém as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="dcf56-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="dcf56-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="dcf56-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="dcf56-110">Por padrão, **Get-AzureRmDeployment** obtém todas as implantações no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="dcf56-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="dcf56-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="dcf56-111">EXAMPLES</span></span>

### <span data-ttu-id="dcf56-112">Exemplo 1: obter todas as implantações em escopo de assinatura</span><span class="sxs-lookup"><span data-stu-id="dcf56-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="dcf56-113">Este comando obtém todas as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="dcf56-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="dcf56-114">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="dcf56-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="dcf56-115">Este comando obtém a implantação do DeployRoles01 no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="dcf56-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="dcf56-116">Você pode atribuir um nome a uma implantação ao criá-lo usando cmdlets **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="dcf56-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="dcf56-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="dcf56-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="dcf56-118">OS</span><span class="sxs-lookup"><span data-stu-id="dcf56-118">PARAMETERS</span></span>

### <span data-ttu-id="dcf56-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dcf56-119">-ApiVersion</span></span>
<span data-ttu-id="dcf56-120">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="dcf56-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="dcf56-121">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="dcf56-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="dcf56-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcf56-122">-DefaultProfile</span></span>
<span data-ttu-id="dcf56-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="dcf56-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcf56-124">-ID</span><span class="sxs-lookup"><span data-stu-id="dcf56-124">-Id</span></span>
<span data-ttu-id="dcf56-125">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="dcf56-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="dcf56-126">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="dcf56-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf56-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="dcf56-127">-Name</span></span>
<span data-ttu-id="dcf56-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="dcf56-128">The name of deployment.</span></span>

```yaml
Type: String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcf56-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="dcf56-129">-Pre</span></span>
<span data-ttu-id="dcf56-130">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="dcf56-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="dcf56-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcf56-131">CommonParameters</span></span>
<span data-ttu-id="dcf56-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dcf56-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcf56-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dcf56-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcf56-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="dcf56-134">INPUTS</span></span>

### <span data-ttu-id="dcf56-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dcf56-135">System.String</span></span>

## <span data-ttu-id="dcf56-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="dcf56-136">OUTPUTS</span></span>

### <span data-ttu-id="dcf56-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="dcf56-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="dcf56-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="dcf56-138">NOTES</span></span>

## <span data-ttu-id="dcf56-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="dcf56-139">RELATED LINKS</span></span>
