---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermdeployment
schema: 2.0.0
ms.openlocfilehash: 1a86eb136fe976ba5e229ff36bd5d0e2a2cad340
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93785431"
---
# <span data-ttu-id="a639e-101">Get-AzureRmDeployment</span><span class="sxs-lookup"><span data-stu-id="a639e-101">Get-AzureRmDeployment</span></span>

## <span data-ttu-id="a639e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a639e-102">SYNOPSIS</span></span>
<span data-ttu-id="a639e-103">Obter implantação</span><span class="sxs-lookup"><span data-stu-id="a639e-103">Get deployment</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a639e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a639e-104">SYNTAX</span></span>

### <span data-ttu-id="a639e-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="a639e-105">GetByDeploymentName (Default)</span></span>
```
Get-AzureRmDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a639e-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="a639e-106">GetByDeploymentId</span></span>
```
Get-AzureRmDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a639e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="a639e-107">DESCRIPTION</span></span>
<span data-ttu-id="a639e-108">O cmdlet **Get-AzureRmDeployment** Obtém as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a639e-108">The **Get-AzureRmDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="a639e-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="a639e-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="a639e-110">Por padrão, **Get-AzureRmDeployment** obtém todas as implantações no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a639e-110">By default, **Get-AzureRmDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="a639e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="a639e-111">EXAMPLES</span></span>

### <span data-ttu-id="a639e-112">Exemplo 1: obter todas as implantações em escopo de assinatura</span><span class="sxs-lookup"><span data-stu-id="a639e-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzureRmDeployment
```

<span data-ttu-id="a639e-113">Este comando obtém todas as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a639e-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="a639e-114">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="a639e-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzureRmDeployment -Name "DeployRoles01"
```

<span data-ttu-id="a639e-115">Este comando obtém a implantação do DeployRoles01 no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="a639e-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="a639e-116">Você pode atribuir um nome a uma implantação ao criá-lo usando cmdlets **New-AzureRmDeployment** .</span><span class="sxs-lookup"><span data-stu-id="a639e-116">You can assign a name to a deployment when you create it by using the **New-AzureRmDeployment** cmdlets.</span></span>
<span data-ttu-id="a639e-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="a639e-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="a639e-118">OS</span><span class="sxs-lookup"><span data-stu-id="a639e-118">PARAMETERS</span></span>

### <span data-ttu-id="a639e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="a639e-119">-ApiVersion</span></span>
<span data-ttu-id="a639e-120">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="a639e-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="a639e-121">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="a639e-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="a639e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a639e-122">-DefaultProfile</span></span>
<span data-ttu-id="a639e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a639e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a639e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="a639e-124">-Id</span></span>
<span data-ttu-id="a639e-125">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="a639e-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="a639e-126">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="a639e-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

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

### <span data-ttu-id="a639e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="a639e-127">-Name</span></span>
<span data-ttu-id="a639e-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="a639e-128">The name of deployment.</span></span>

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

### <span data-ttu-id="a639e-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="a639e-129">-Pre</span></span>
<span data-ttu-id="a639e-130">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="a639e-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="a639e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a639e-131">CommonParameters</span></span>
<span data-ttu-id="a639e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a639e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a639e-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a639e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a639e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="a639e-134">INPUTS</span></span>

### <span data-ttu-id="a639e-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a639e-135">System.String</span></span>

## <span data-ttu-id="a639e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="a639e-136">OUTPUTS</span></span>

### <span data-ttu-id="a639e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="a639e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="a639e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="a639e-138">NOTES</span></span>

## <span data-ttu-id="a639e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a639e-139">RELATED LINKS</span></span>
