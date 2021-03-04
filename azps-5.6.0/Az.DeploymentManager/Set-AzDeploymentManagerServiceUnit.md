---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 24c682faf725fd53e3b78e85c316318300ecbb62
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101886647"
---
# <span data-ttu-id="1c872-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="1c872-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="1c872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c872-102">SYNOPSIS</span></span>
<span data-ttu-id="1c872-103">Atualiza a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1c872-103">Updates the service unit.</span></span>

## <span data-ttu-id="1c872-104">SINTAXE</span><span class="sxs-lookup"><span data-stu-id="1c872-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c872-105">DESCRIPTION</span><span class="sxs-lookup"><span data-stu-id="1c872-105">DESCRIPTION</span></span>
<span data-ttu-id="1c872-106">O cmdlet **Set-AzDeploymentManagerServiceUnit** atualiza uma unidade de serviço com o objeto de unidade de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="1c872-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="1c872-107">O cmdlet retorna o objeto de unidade de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="1c872-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="1c872-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="1c872-108">EXAMPLES</span></span>

### <span data-ttu-id="1c872-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="1c872-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="1c872-110">Este comando atualiza uma unidade de serviço cujo nome, nome do serviço, nome da topologia de serviço e ResourceGroup corresponderão às propriedades Name, ServiceName, ServiceTopologyName e ResourceGroupName do $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="1c872-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="1c872-111">O comando retorna o objeto de unidade de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="1c872-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="1c872-112">PARÂMETROS</span><span class="sxs-lookup"><span data-stu-id="1c872-112">PARAMETERS</span></span>

### <span data-ttu-id="1c872-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c872-113">-DefaultProfile</span></span>
<span data-ttu-id="1c872-114">As credenciais, conta, locatário e assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="1c872-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c872-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c872-115">-InputObject</span></span>
<span data-ttu-id="1c872-116">O objeto da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="1c872-116">The service unit object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c872-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c872-117">-Confirm</span></span>
<span data-ttu-id="1c872-118">Solicita a confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c872-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c872-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c872-119">-WhatIf</span></span>
<span data-ttu-id="1c872-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="1c872-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c872-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="1c872-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c872-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c872-122">CommonParameters</span></span>
<span data-ttu-id="1c872-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c872-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c872-124">Para obter mais informações, [consulte about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c872-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c872-125">INPUTS</span><span class="sxs-lookup"><span data-stu-id="1c872-125">INPUTS</span></span>

### <span data-ttu-id="1c872-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="1c872-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="1c872-127">SAÍDAS</span><span class="sxs-lookup"><span data-stu-id="1c872-127">OUTPUTS</span></span>

### <span data-ttu-id="1c872-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="1c872-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="1c872-129">NOTES</span><span class="sxs-lookup"><span data-stu-id="1c872-129">NOTES</span></span>

## <span data-ttu-id="1c872-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="1c872-130">RELATED LINKS</span></span>
