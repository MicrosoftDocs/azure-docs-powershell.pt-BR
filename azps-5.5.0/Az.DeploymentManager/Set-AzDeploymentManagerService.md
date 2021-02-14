---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerService.md
ms.openlocfilehash: fb3f7ccab164370e1c55992a666ac7256b5a4a95
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115844"
---
# <span data-ttu-id="6dd3b-101">Set-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="6dd3b-101">Set-AzDeploymentManagerService</span></span>

## <span data-ttu-id="6dd3b-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="6dd3b-102">SYNOPSIS</span></span>
<span data-ttu-id="6dd3b-103">Atualiza o serviço.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-103">Updates the service.</span></span>

## <span data-ttu-id="6dd3b-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6dd3b-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerService [-InputObject] <PSServiceResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6dd3b-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="6dd3b-105">DESCRIPTION</span></span>
<span data-ttu-id="6dd3b-106">O cmdlet **Set-AzDeploymentManagerService** atualiza um serviço com o objeto de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-106">The **Set-AzDeploymentManagerService** cmdlet updates a service with the specified service object.</span></span>
<span data-ttu-id="6dd3b-107">O cmdlet retorna o objeto de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-107">The cmdlet returns the updated service object.</span></span>

## <span data-ttu-id="6dd3b-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6dd3b-108">EXAMPLES</span></span>

### <span data-ttu-id="6dd3b-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="6dd3b-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceObject
```

<span data-ttu-id="6dd3b-110">Esse comando atualiza um serviço cujo nome, nome de topologia de serviço e Grupo de Recursos corresponderem às propriedades Nome, ServiceTopologyName e ResourceGroupName do $serviceObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-110">This command updates a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>
<span data-ttu-id="6dd3b-111">O serviço seria atualizado para as propriedades definidas no $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-111">The service would be updated to the properties set in the $serviceObject.</span></span>

## <span data-ttu-id="6dd3b-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6dd3b-112">PARAMETERS</span></span>

### <span data-ttu-id="6dd3b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6dd3b-113">-DefaultProfile</span></span>
<span data-ttu-id="6dd3b-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6dd3b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6dd3b-115">-InputObject</span></span>
<span data-ttu-id="6dd3b-116">O objeto de serviço.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-116">The service object.</span></span>

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

### <span data-ttu-id="6dd3b-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="6dd3b-117">-Confirm</span></span>
<span data-ttu-id="6dd3b-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6dd3b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6dd3b-119">-WhatIf</span></span>
<span data-ttu-id="6dd3b-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6dd3b-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6dd3b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6dd3b-122">CommonParameters</span></span>
<span data-ttu-id="6dd3b-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6dd3b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6dd3b-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6dd3b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6dd3b-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="6dd3b-125">INPUTS</span></span>

### <span data-ttu-id="6dd3b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6dd3b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6dd3b-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="6dd3b-127">OUTPUTS</span></span>

### <span data-ttu-id="6dd3b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6dd3b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6dd3b-129">Notas</span><span class="sxs-lookup"><span data-stu-id="6dd3b-129">NOTES</span></span>

## <span data-ttu-id="6dd3b-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="6dd3b-130">RELATED LINKS</span></span>
