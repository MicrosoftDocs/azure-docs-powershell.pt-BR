---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: 4a9f785519710b7a6653b1ece27d7b526fceab31
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115842"
---
# <span data-ttu-id="fff9e-101">Set-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="fff9e-101">Set-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="fff9e-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="fff9e-102">SYNOPSIS</span></span>
<span data-ttu-id="fff9e-103">Atualiza a topologia do serviço.</span><span class="sxs-lookup"><span data-stu-id="fff9e-103">Updates the service topology.</span></span>

## <span data-ttu-id="fff9e-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fff9e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceTopology [-InputObject] <PSServiceTopologyResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fff9e-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="fff9e-105">DESCRIPTION</span></span>
<span data-ttu-id="fff9e-106">O cmdlet **Set-AzDeploymentManagerServiceTopology** atualiza uma topologia de serviço com o objeto de topologia de serviço especificado.</span><span class="sxs-lookup"><span data-stu-id="fff9e-106">The **Set-AzDeploymentManagerServiceTopology** cmdlet updates a service topology with the specified service topology object.</span></span>
<span data-ttu-id="fff9e-107">O cmdlet retorna o objeto de topologia de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="fff9e-107">The cmdlet returns the updated service topology object.</span></span>

## <span data-ttu-id="fff9e-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="fff9e-108">EXAMPLES</span></span>

### <span data-ttu-id="fff9e-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="fff9e-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerService -InputObject $serviceTopologyObject
```

<span data-ttu-id="fff9e-110">Esse comando atualiza uma topologia de serviço cujo nome e Grupo de Recursos corresponderem às propriedades Nome e NomeDoGrupo de Recursos da $serviceTopologyObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="fff9e-110">This command updates a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>
<span data-ttu-id="fff9e-111">O comando retorna o objeto de topologia de serviço atualizado.</span><span class="sxs-lookup"><span data-stu-id="fff9e-111">The command returns the updated service topology object.</span></span>

## <span data-ttu-id="fff9e-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fff9e-112">PARAMETERS</span></span>

### <span data-ttu-id="fff9e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fff9e-113">-DefaultProfile</span></span>
<span data-ttu-id="fff9e-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="fff9e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fff9e-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fff9e-115">-InputObject</span></span>
<span data-ttu-id="fff9e-116">O objeto de topologia de serviço.</span><span class="sxs-lookup"><span data-stu-id="fff9e-116">The service topology object.</span></span>

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

### <span data-ttu-id="fff9e-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="fff9e-117">-Confirm</span></span>
<span data-ttu-id="fff9e-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fff9e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fff9e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fff9e-119">-WhatIf</span></span>
<span data-ttu-id="fff9e-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="fff9e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fff9e-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="fff9e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fff9e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fff9e-122">CommonParameters</span></span>
<span data-ttu-id="fff9e-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fff9e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fff9e-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fff9e-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fff9e-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="fff9e-125">INPUTS</span></span>

### <span data-ttu-id="fff9e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fff9e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fff9e-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="fff9e-127">OUTPUTS</span></span>

### <span data-ttu-id="fff9e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="fff9e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="fff9e-129">Notas</span><span class="sxs-lookup"><span data-stu-id="fff9e-129">NOTES</span></span>

## <span data-ttu-id="fff9e-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="fff9e-130">RELATED LINKS</span></span>
