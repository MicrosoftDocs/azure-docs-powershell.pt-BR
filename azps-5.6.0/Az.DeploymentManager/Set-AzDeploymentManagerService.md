---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: 4c33ba2bd87e1f6103454740529c5570ef04ea17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101887169"
---
# <span data-ttu-id="ebdbc-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="ebdbc-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="ebdbc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebdbc-102">SYNOPSIS</span></span>
<span data-ttu-id="ebdbc-103">Atualiza o serviço.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-103">Updates the service.</span></span>

## <span data-ttu-id="ebdbc-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="ebdbc-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ebdbc-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="ebdbc-105">DESCRIPTION</span></span>
<span data-ttu-id="ebdbc-106">O cmdlet **Set-AzDeploymentManagerService** atualiza um serviço com o objeto de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="ebdbc-107">O cmdlet retorna o objeto de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="ebdbc-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="ebdbc-108">EXAMPLES</span></span>

### <span data-ttu-id="ebdbc-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="ebdbc-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="ebdbc-110">Este comando atualiza um serviço cujo nome, nome da topologia de serviço e ResourceGroup corresponderem às propriedades Name, ServiceTopologyName e ResourceGroupName do $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="ebdbc-111">O serviço seria atualizado para as propriedades definidas no $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="ebdbc-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="ebdbc-112">PARAMETERS</span></span>

### <span data-ttu-id="ebdbc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebdbc-113">-DefaultProfile</span></span>
<span data-ttu-id="ebdbc-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebdbc-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ebdbc-115">-InputObject</span></span>
<span data-ttu-id="ebdbc-116">O objeto service.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-116">The service object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ebdbc-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ebdbc-117">-Confirm</span></span>
<span data-ttu-id="ebdbc-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdbc-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ebdbc-119">-WhatIf</span></span>
<span data-ttu-id="ebdbc-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ebdbc-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ebdbc-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebdbc-122">CommonParameters</span></span>
<span data-ttu-id="ebdbc-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebdbc-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebdbc-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ebdbc-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebdbc-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="ebdbc-125">INPUTS</span></span>

### <span data-ttu-id="ebdbc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="ebdbc-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ebdbc-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="ebdbc-127">OUTPUTS</span></span>

### <span data-ttu-id="ebdbc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="ebdbc-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="ebdbc-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="ebdbc-129">NOTES</span></span>

## <span data-ttu-id="ebdbc-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="ebdbc-130">RELATED LINKS</span></span>
