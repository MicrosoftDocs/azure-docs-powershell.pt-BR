---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: ED37B17D-C513-422A-89EA-A6AF1C9A5FEE
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerserviceagentpoolprofile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerServiceAgentPoolProfile.md
ms.openlocfilehash: b887110ecb0cd941af9c91417218ec2ca297be1c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100127088"
---
# <span data-ttu-id="822d7-101">Remove-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="822d7-101">Remove-AzContainerServiceAgentPoolProfile</span></span>

## <span data-ttu-id="822d7-102">Sinopse</span><span class="sxs-lookup"><span data-stu-id="822d7-102">SYNOPSIS</span></span>
<span data-ttu-id="822d7-103">Remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="822d7-103">Removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="822d7-104">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="822d7-104">SYNTAX</span></span>

```
Remove-AzContainerServiceAgentPoolProfile [-ContainerService] <PSContainerService> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="822d7-105">Descrição</span><span class="sxs-lookup"><span data-stu-id="822d7-105">DESCRIPTION</span></span>
<span data-ttu-id="822d7-106">O cmdlet **Remove-AzContainerServiceAgentPoolProfile** remove um perfil de pool de agente de um serviço de contêiner.</span><span class="sxs-lookup"><span data-stu-id="822d7-106">The **Remove-AzContainerServiceAgentPoolProfile** cmdlet removes an agent pool profile from a container service.</span></span>

## <span data-ttu-id="822d7-107">Exemplos</span><span class="sxs-lookup"><span data-stu-id="822d7-107">EXAMPLES</span></span>

### <span data-ttu-id="822d7-108">Exemplo 1: Remover um perfil de um serviço de contêineres</span><span class="sxs-lookup"><span data-stu-id="822d7-108">Example 1: Remove a profile from a container service</span></span>
```
PS C:\> $Container = Get-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17" 
PS C:\> Remove-AzContainerServiceAgentPoolProfile -ContainerService $Container -Name "AgentPool01"
```

<span data-ttu-id="822d7-109">O primeiro comando obtém um serviço de contêiner chamado CSResourceGroup17 usando o cmdlet Get-AzContainerService contêiner.</span><span class="sxs-lookup"><span data-stu-id="822d7-109">The first command gets a container service named CSResourceGroup17 by using the Get-AzContainerService cmdlet.</span></span>
<span data-ttu-id="822d7-110">O comando armazena o serviço na variável $Container dados.</span><span class="sxs-lookup"><span data-stu-id="822d7-110">The command stores the service in the $Container variable.</span></span>
<span data-ttu-id="822d7-111">O segundo comando remove o perfil chamado AgentPool01 do serviço de contêiner no $Container.</span><span class="sxs-lookup"><span data-stu-id="822d7-111">The second command removes the profile named AgentPool01 from the container service in $Container.</span></span>

## <span data-ttu-id="822d7-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="822d7-112">PARAMETERS</span></span>

### <span data-ttu-id="822d7-113">-ContainerService</span><span class="sxs-lookup"><span data-stu-id="822d7-113">-ContainerService</span></span>
<span data-ttu-id="822d7-114">Especifica o objeto de serviço de contêiner do qual este cmdlet remove um perfil de pool de agente.</span><span class="sxs-lookup"><span data-stu-id="822d7-114">Specifies the container service object from which this cmdlet removes an agent pool profile.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="822d7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="822d7-115">-DefaultProfile</span></span>
<span data-ttu-id="822d7-116">As credenciais, a conta, o locatário e a assinatura usadas para comunicação com o azure.</span><span class="sxs-lookup"><span data-stu-id="822d7-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="822d7-117">-Nome</span><span class="sxs-lookup"><span data-stu-id="822d7-117">-Name</span></span>
<span data-ttu-id="822d7-118">Especifica o nome do perfil de pool do agente que este cmdlet remove.</span><span class="sxs-lookup"><span data-stu-id="822d7-118">Specifies the name of the agent pool profile that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="822d7-119">-Confirmar</span><span class="sxs-lookup"><span data-stu-id="822d7-119">-Confirm</span></span>
<span data-ttu-id="822d7-120">Solicita confirmação antes de executar o cmdlet.</span><span class="sxs-lookup"><span data-stu-id="822d7-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="822d7-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="822d7-121">-WhatIf</span></span>
<span data-ttu-id="822d7-122">Mostra o que acontece se o cmdlet for executado.</span><span class="sxs-lookup"><span data-stu-id="822d7-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="822d7-123">O cmdlet não é executado.</span><span class="sxs-lookup"><span data-stu-id="822d7-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="822d7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="822d7-124">CommonParameters</span></span>
<span data-ttu-id="822d7-125">Este cmdlet dá suporte aos parâmetros comuns: -Depurar, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction e -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="822d7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="822d7-126">Para obter mais informações, [consulte about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="822d7-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="822d7-127">Entradas</span><span class="sxs-lookup"><span data-stu-id="822d7-127">INPUTS</span></span>

### <span data-ttu-id="822d7-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="822d7-128">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

### <span data-ttu-id="822d7-129">System.String</span><span class="sxs-lookup"><span data-stu-id="822d7-129">System.String</span></span>

## <span data-ttu-id="822d7-130">Saídas</span><span class="sxs-lookup"><span data-stu-id="822d7-130">OUTPUTS</span></span>

### <span data-ttu-id="822d7-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span><span class="sxs-lookup"><span data-stu-id="822d7-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSContainerService</span></span>

## <span data-ttu-id="822d7-132">Notas</span><span class="sxs-lookup"><span data-stu-id="822d7-132">NOTES</span></span>

## <span data-ttu-id="822d7-133">LINKS RELACIONADOS</span><span class="sxs-lookup"><span data-stu-id="822d7-133">RELATED LINKS</span></span>

[<span data-ttu-id="822d7-134">Add-AzContainerServiceAgentPoolProfile</span><span class="sxs-lookup"><span data-stu-id="822d7-134">Add-AzContainerServiceAgentPoolProfile</span></span>](./Add-AzContainerServiceAgentPoolProfile.md)

[<span data-ttu-id="822d7-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="822d7-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)


