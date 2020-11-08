---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94115015"
---
# <span data-ttu-id="35662-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="35662-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="35662-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="35662-102">SYNOPSIS</span></span>
<span data-ttu-id="35662-103">Atualiza a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="35662-103">Updates the service unit.</span></span>

## <span data-ttu-id="35662-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35662-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35662-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="35662-105">DESCRIPTION</span></span>
<span data-ttu-id="35662-106">O cmdlet **set-AzDeploymentManagerServiceUnit** atualiza uma unidade de serviço com o objeto de unidade de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="35662-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="35662-107">O cmdlet retorna o objeto de unidade de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="35662-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="35662-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="35662-108">EXAMPLES</span></span>

### <span data-ttu-id="35662-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="35662-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="35662-110">Esse comando atualiza uma unidade de serviço cujo nome, nome do serviço, nome da topologia de serviço e o nome do contato correspondem às propriedades Name, ServiceName, Service Topologyname e ResourceGroupName da $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="35662-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="35662-111">O comando retorna o objeto de unidade de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="35662-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="35662-112">OS</span><span class="sxs-lookup"><span data-stu-id="35662-112">PARAMETERS</span></span>

### <span data-ttu-id="35662-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35662-113">-DefaultProfile</span></span>
<span data-ttu-id="35662-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="35662-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="35662-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="35662-115">-InputObject</span></span>
<span data-ttu-id="35662-116">O objeto de unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="35662-116">The service unit object.</span></span>

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

### <span data-ttu-id="35662-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="35662-117">-Confirm</span></span>
<span data-ttu-id="35662-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="35662-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35662-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35662-119">-WhatIf</span></span>
<span data-ttu-id="35662-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="35662-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35662-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="35662-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35662-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35662-122">CommonParameters</span></span>
<span data-ttu-id="35662-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35662-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35662-124">Para obter mais informações, consulte [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35662-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35662-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="35662-125">INPUTS</span></span>

### <span data-ttu-id="35662-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="35662-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="35662-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="35662-127">OUTPUTS</span></span>

### <span data-ttu-id="35662-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="35662-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="35662-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="35662-129">NOTES</span></span>

## <span data-ttu-id="35662-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="35662-130">RELATED LINKS</span></span>
