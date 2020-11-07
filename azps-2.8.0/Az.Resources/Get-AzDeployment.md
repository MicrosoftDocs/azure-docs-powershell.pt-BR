---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzDeployment.md
ms.openlocfilehash: cde9c4f8827840047e7fa4a1c597ed6338ed8e54
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93772602"
---
# <span data-ttu-id="d268e-101">Get-AzDeployment</span><span class="sxs-lookup"><span data-stu-id="d268e-101">Get-AzDeployment</span></span>

## <span data-ttu-id="d268e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="d268e-102">SYNOPSIS</span></span>
<span data-ttu-id="d268e-103">Obter implantação</span><span class="sxs-lookup"><span data-stu-id="d268e-103">Get deployment</span></span>

## <span data-ttu-id="d268e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d268e-104">SYNTAX</span></span>

### <span data-ttu-id="d268e-105">GetByDeploymentName (padrão)</span><span class="sxs-lookup"><span data-stu-id="d268e-105">GetByDeploymentName (Default)</span></span>
```
Get-AzDeployment [[-Name] <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d268e-106">GetByDeploymentId</span><span class="sxs-lookup"><span data-stu-id="d268e-106">GetByDeploymentId</span></span>
```
Get-AzDeployment [-Id <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d268e-107">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="d268e-107">DESCRIPTION</span></span>
<span data-ttu-id="d268e-108">O cmdlet **Get-AzDeployment** Obtém as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d268e-108">The **Get-AzDeployment** cmdlet gets the deployments at the current subscription scope.</span></span>
<span data-ttu-id="d268e-109">Especifique o *nome* ou o parâmetro *ID* para filtrar os resultados.</span><span class="sxs-lookup"><span data-stu-id="d268e-109">Specify the *Name* or *Id* parameter to filter the results.</span></span>
<span data-ttu-id="d268e-110">Por padrão, **Get-AzDeployment** obtém todas as implantações no escopo de assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d268e-110">By default, **Get-AzDeployment** gets all deployments at the current subscription scope.</span></span>

## <span data-ttu-id="d268e-111">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="d268e-111">EXAMPLES</span></span>

### <span data-ttu-id="d268e-112">Exemplo 1: obter todas as implantações em escopo de assinatura</span><span class="sxs-lookup"><span data-stu-id="d268e-112">Example 1: Get all deployments at subscription scope</span></span>
```
PS C:\>Get-AzDeployment
```

<span data-ttu-id="d268e-113">Este comando obtém todas as implantações no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d268e-113">This command gets all deployments at the current subscription scope.</span></span>

### <span data-ttu-id="d268e-114">Exemplo 2: obter uma implantação por nome</span><span class="sxs-lookup"><span data-stu-id="d268e-114">Example 2: Get a deployment by name</span></span>
```
PS C:\>Get-AzDeployment -Name "DeployRoles01"
```

<span data-ttu-id="d268e-115">Este comando obtém a implantação do DeployRoles01 no escopo da assinatura atual.</span><span class="sxs-lookup"><span data-stu-id="d268e-115">This command gets the DeployRoles01 deployment at the current subscription scope.</span></span>
<span data-ttu-id="d268e-116">Você pode atribuir um nome a uma implantação ao criá-lo usando cmdlets **New-AzDeployment** .</span><span class="sxs-lookup"><span data-stu-id="d268e-116">You can assign a name to a deployment when you create it by using the **New-AzDeployment** cmdlets.</span></span>
<span data-ttu-id="d268e-117">Se você não atribuir um nome, os cmdlets fornecerão um nome padrão com base no modelo usado para criar a implantação.</span><span class="sxs-lookup"><span data-stu-id="d268e-117">If you do not assign a name, the cmdlets provide a default name based on the template that is used to create the deployment.</span></span>

## <span data-ttu-id="d268e-118">OS</span><span class="sxs-lookup"><span data-stu-id="d268e-118">PARAMETERS</span></span>

### <span data-ttu-id="d268e-119">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d268e-119">-ApiVersion</span></span>
<span data-ttu-id="d268e-120">Quando definido, indica a versão da API do provedor de recursos a ser usada.</span><span class="sxs-lookup"><span data-stu-id="d268e-120">When set, indicates the version of the resource provider API to use.</span></span>
<span data-ttu-id="d268e-121">Se não for especificado, a versão da API será automaticamente determinada como a mais recente disponível.</span><span class="sxs-lookup"><span data-stu-id="d268e-121">If not specified, the API version is automatically determined as the latest available.</span></span>

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

### <span data-ttu-id="d268e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d268e-122">-DefaultProfile</span></span>
<span data-ttu-id="d268e-123">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="d268e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d268e-124">-ID</span><span class="sxs-lookup"><span data-stu-id="d268e-124">-Id</span></span>
<span data-ttu-id="d268e-125">A ID de recurso totalmente qualificado da implantação.</span><span class="sxs-lookup"><span data-stu-id="d268e-125">The fully qualified resource Id of the deployment.</span></span>
<span data-ttu-id="d268e-126">exemplo:/subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span><span class="sxs-lookup"><span data-stu-id="d268e-126">example: /subscriptions/{subId}/providers/Microsoft.Resources/deployments/{deploymentName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentId
Aliases: DeploymentId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-127">-Nome</span><span class="sxs-lookup"><span data-stu-id="d268e-127">-Name</span></span>
<span data-ttu-id="d268e-128">O nome da implantação.</span><span class="sxs-lookup"><span data-stu-id="d268e-128">The name of deployment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByDeploymentName
Aliases: DeploymentName

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d268e-129">-Pre</span><span class="sxs-lookup"><span data-stu-id="d268e-129">-Pre</span></span>
<span data-ttu-id="d268e-130">Quando definido, indica que o cmdlet deve usar versões de API de pré-lançamento ao determinar automaticamente qual versão usar.</span><span class="sxs-lookup"><span data-stu-id="d268e-130">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>

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

### <span data-ttu-id="d268e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d268e-131">CommonParameters</span></span>
<span data-ttu-id="d268e-132">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d268e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d268e-133">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d268e-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d268e-134">SENSORES</span><span class="sxs-lookup"><span data-stu-id="d268e-134">INPUTS</span></span>

### <span data-ttu-id="d268e-135">Nenhuma</span><span class="sxs-lookup"><span data-stu-id="d268e-135">None</span></span>

## <span data-ttu-id="d268e-136">EXIBE</span><span class="sxs-lookup"><span data-stu-id="d268e-136">OUTPUTS</span></span>

### <span data-ttu-id="d268e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDEployment</span><span class="sxs-lookup"><span data-stu-id="d268e-137">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSDeployment</span></span>

## <span data-ttu-id="d268e-138">INFORMA</span><span class="sxs-lookup"><span data-stu-id="d268e-138">NOTES</span></span>

## <span data-ttu-id="d268e-139">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="d268e-139">RELATED LINKS</span></span>
