---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94280596"
---
# <span data-ttu-id="6829d-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="6829d-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="6829d-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6829d-102">SYNOPSIS</span></span>
<span data-ttu-id="6829d-103">Atualiza o serviço.</span><span class="sxs-lookup"><span data-stu-id="6829d-103">Updates the service.</span></span>

## <span data-ttu-id="6829d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6829d-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6829d-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="6829d-105">DESCRIPTION</span></span>
<span data-ttu-id="6829d-106">O cmdlet **set-AzDeploymentManagerService** atualiza um serviço com o objeto de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="6829d-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="6829d-107">O cmdlet retorna o objeto de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="6829d-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="6829d-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="6829d-108">EXAMPLES</span></span>

### <span data-ttu-id="6829d-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6829d-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="6829d-110">Esse comando atualiza um serviço cujo nome, nome da topologia de serviço e o nome do contato correspondem às propriedades Name, imtopologyname e ResourceGroupName da $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6829d-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="6829d-111">O serviço seria atualizado para as propriedades definidas no $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="6829d-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="6829d-112">OS</span><span class="sxs-lookup"><span data-stu-id="6829d-112">PARAMETERS</span></span>

### <span data-ttu-id="6829d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6829d-113">-DefaultProfile</span></span>
<span data-ttu-id="6829d-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6829d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6829d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6829d-115">-InputObject</span></span>
<span data-ttu-id="6829d-116">O objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="6829d-116">The service object.</span></span>

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

### <span data-ttu-id="6829d-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="6829d-117">-Confirm</span></span>
<span data-ttu-id="6829d-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6829d-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6829d-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6829d-119">-WhatIf</span></span>
<span data-ttu-id="6829d-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="6829d-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6829d-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6829d-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6829d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6829d-122">CommonParameters</span></span>
<span data-ttu-id="6829d-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6829d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6829d-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6829d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6829d-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="6829d-125">INPUTS</span></span>

### <span data-ttu-id="6829d-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6829d-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6829d-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="6829d-127">OUTPUTS</span></span>

### <span data-ttu-id="6829d-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6829d-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6829d-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="6829d-129">NOTES</span></span>

## <span data-ttu-id="6829d-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6829d-130">RELATED LINKS</span></span>
