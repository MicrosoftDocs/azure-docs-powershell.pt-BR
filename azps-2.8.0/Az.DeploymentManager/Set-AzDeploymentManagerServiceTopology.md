---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: ff3cdb549835ceb4689ee5be8569b61ffa89538d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93596634"
---
# <span data-ttu-id="fc5cd-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fc5cd-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fc5cd-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fc5cd-102">SYNOPSIS</span></span>
<span data-ttu-id="fc5cd-103">Atualiza a topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-103">Updates the service topology.</span></span>

## <span data-ttu-id="fc5cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fc5cd-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc5cd-105">DESCRITIVO</span><span class="sxs-lookup"><span data-stu-id="fc5cd-105">DESCRIPTION</span></span>
<span data-ttu-id="fc5cd-106">O cmdlet **set-AzDeploymentManagerServiceTopology** atualiza uma topologia de serviço com o objeto de topologia de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="fc5cd-107">O cmdlet retorna o objeto de topologia do serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="fc5cd-108">EXEMPLOS</span><span class="sxs-lookup"><span data-stu-id="fc5cd-108">EXAMPLES</span></span>

### <span data-ttu-id="fc5cd-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fc5cd-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fc5cd-110">Esse comando atualiza uma topologia de serviço cujo nome e o meu nome de fonte correspondem às propriedades Name e ResourceGroupName do $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="fc5cd-111">O comando retorna o objeto de topologia do serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="fc5cd-112">OS</span><span class="sxs-lookup"><span data-stu-id="fc5cd-112">PARAMETERS</span></span>

### <span data-ttu-id="fc5cd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc5cd-113">-DefaultProfile</span></span>
<span data-ttu-id="fc5cd-114">As credenciais, a conta, o locatário e a assinatura usados para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc5cd-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fc5cd-115">-InputObject</span></span>
<span data-ttu-id="fc5cd-116">O objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-116">The service topology object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc5cd-117">-Confirme</span><span class="sxs-lookup"><span data-stu-id="fc5cd-117">-Confirm</span></span>
<span data-ttu-id="fc5cd-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc5cd-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc5cd-119">-WhatIf</span></span>
<span data-ttu-id="fc5cd-120">Mostra o que aconteceria se o cmdlet fosse executado.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc5cd-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc5cd-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc5cd-122">CommonParameters</span></span>
<span data-ttu-id="fc5cd-123">Esse cmdlet dá suporte a parâmetros comuns:-debug,-ErrorAction,-ErrorVariable,-Informationaction,-InformationVariable,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose-WarningAction e-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc5cd-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc5cd-124">Para obter mais informações, consulte about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc5cd-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc5cd-125">SENSORES</span><span class="sxs-lookup"><span data-stu-id="fc5cd-125">INPUTS</span></span>

### <span data-ttu-id="fc5cd-126">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fc5cd-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fc5cd-127">EXIBE</span><span class="sxs-lookup"><span data-stu-id="fc5cd-127">OUTPUTS</span></span>

### <span data-ttu-id="fc5cd-128">Microsoft. Azure. Commands. DeploymentManager. Models. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fc5cd-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fc5cd-129">INFORMA</span><span class="sxs-lookup"><span data-stu-id="fc5cd-129">NOTES</span></span>

## <span data-ttu-id="fc5cd-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fc5cd-130">RELATED LINKS</span></span>
