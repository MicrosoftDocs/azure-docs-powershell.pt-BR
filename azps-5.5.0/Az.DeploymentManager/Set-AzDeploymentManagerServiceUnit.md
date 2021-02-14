---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 7d2a7916e73b20e4c4e7a3602dc23bc10a67c744
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100115839"
---
# <span data-ttu-id="a08f5-101">Set-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a08f5-101">Set-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a08f5-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="a08f5-102">SYNOPSIS</span></span>
<span data-ttu-id="a08f5-103">Atualiza a unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a08f5-103">Updates the service unit.</span></span>

## <span data-ttu-id="a08f5-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a08f5-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerServiceUnit [-InputObject] <PSServiceUnitResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a08f5-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="a08f5-105">DESCRIPTION</span></span>
<span data-ttu-id="a08f5-106">O cmdlet **Set-AzDeploymentManagerServiceUnit** atualiza uma unidade de serviço com o objeto de unidade de serviço especificada.</span><span class="sxs-lookup"><span data-stu-id="a08f5-106">The **Set-AzDeploymentManagerServiceUnit** cmdlet updates a service unit with the specified service unit object.</span></span>
<span data-ttu-id="a08f5-107">O cmdlet retorna o objeto da unidade de serviço atualizada.</span><span class="sxs-lookup"><span data-stu-id="a08f5-107">The cmdlet returns the updated service unit object.</span></span>

## <span data-ttu-id="a08f5-108">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a08f5-108">EXAMPLES</span></span>

### <span data-ttu-id="a08f5-109">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="a08f5-109">Example 1</span></span>
```powershell
PS C:\> Set-AzDeploymentManagerServiceUnit -InputObject $serviceUnitObject
```

<span data-ttu-id="a08f5-110">Este comando atualiza uma unidade de serviço cujo nome, nome do serviço, nome de topologia de serviço e Grupo de Recursos corresponderem às propriedades Nome, Nomedo ServiceTopology e NomeDoArqueamento do $serviceUnitObject, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a08f5-110">This command updates a service unit whose name, service name, service topology name and ResourceGroup match the Name, ServiceName, ServiceTopologyName and ResourceGroupName properties of the $serviceUnitObject, respectively.</span></span>
<span data-ttu-id="a08f5-111">O comando retorna o objeto da unidade de serviço atualizada.</span><span class="sxs-lookup"><span data-stu-id="a08f5-111">The command returns the updated service unit object.</span></span>

## <span data-ttu-id="a08f5-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a08f5-112">PARAMETERS</span></span>

### <span data-ttu-id="a08f5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a08f5-113">-DefaultProfile</span></span>
<span data-ttu-id="a08f5-114">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o Azure.</span><span class="sxs-lookup"><span data-stu-id="a08f5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a08f5-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a08f5-115">-InputObject</span></span>
<span data-ttu-id="a08f5-116">O objeto da unidade de serviço.</span><span class="sxs-lookup"><span data-stu-id="a08f5-116">The service unit object.</span></span>

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

### <span data-ttu-id="a08f5-117">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="a08f5-117">-Confirm</span></span>
<span data-ttu-id="a08f5-118">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a08f5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a08f5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a08f5-119">-WhatIf</span></span>
<span data-ttu-id="a08f5-120">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="a08f5-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a08f5-121">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="a08f5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a08f5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a08f5-122">CommonParameters</span></span>
<span data-ttu-id="a08f5-123">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a08f5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a08f5-124">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a08f5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a08f5-125">Entradas</span><span class="sxs-lookup"><span data-stu-id="a08f5-125">INPUTS</span></span>

### <span data-ttu-id="a08f5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceunitResource</span><span class="sxs-lookup"><span data-stu-id="a08f5-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a08f5-127">Saídas</span><span class="sxs-lookup"><span data-stu-id="a08f5-127">OUTPUTS</span></span>

### <span data-ttu-id="a08f5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceunitResource</span><span class="sxs-lookup"><span data-stu-id="a08f5-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a08f5-129">Notas</span><span class="sxs-lookup"><span data-stu-id="a08f5-129">NOTES</span></span>

## <span data-ttu-id="a08f5-130">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="a08f5-130">RELATED LINKS</span></span>
